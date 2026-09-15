---
title: "Introduction to Git"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

# Git & GitHub Setup

Before starting the [synapse level connectomics flies track](synapse_level_connectomics_flies/6-neuprint-api-guide.md), you will need to set up Git and GitHub. We will use Git to keep track of changes to your code and GitHub to store your project.

Rather than creating a separate tutorial for Git, we recommend working through these three excellent lessons from **The Odin Project**:

1. **Introduction to Git**
   [The Odin Project — Introduction to Git](https://www.theodinproject.com/lessons/foundations-introduction-to-git)
   Learn what Git and GitHub are, how they differ, and why version control is useful.

2. **Setting Up Git**
   [The Odin Project — Setting Up Git](https://www.theodinproject.com/lessons/foundations-setting-up-git)
   Install Git, create your GitHub account, configure Git, and connect your computer to GitHub.

3. **Git Basics**
   [The Odin Project — Git Basics](https://www.theodinproject.com/lessons/foundations-git-basics)
   Work through the basic Git workflow: creating a repository, cloning it, tracking changes, committing, and pushing your work to GitHub.

# What you should be comfortable with afterwards

You do not need to become a Git expert. For this project, you should understand the basic workflow:

```text
Edit your code
     ↓
git status
     ↓
git add
     ↓
git commit
     ↓
git push
     ↓
GitHub
```
You should also know how to clone a repository from GitHub and understand the difference between your local project and the copy stored on GitHub.

# Git Ignore

Before we begin working with the neuPrint API, we need to set up a way to store our neuPrint connection details.

Throughout the tutorials, we will use information such as the neuPrint server, dataset, and your personal API token. Rather than entering these details in every notebook, we can store them in a local `.env` file and load them whenever we need them. A `.env` file is a simple text file used to store **environment variables**: pieces of information that your code may need, but that you do not necessarily want to write directly inside your notebook.

For example, our `.env` file might contain:

```text
NEUPRINT_SERVER=...
NEUPRINT_DATASET=...
NEUPRINT_TOKEN=...
```

Because your `.env` file contains your personal API token, we will tell Git to **ignore** this file. This means it will remain on your computer and will not be uploaded to GitHub.

This gives us two benefits:

* You only need to enter your neuPrint details once.
* Your API token stays private and is not included in the project repository.

We will set this up before starting the neuPrint API tutorials.

# 1. Create your `.env` file

First, open terminal and navigate to your project folder, where you will keep your notebooks and scripts.

Your project could look something like this:

```text
Connectome2026/
├── notebook.ipynb
└── data/
```

In the terminal, type:

```bash
touch .env
```

This creates an empty `.env` file. The . at the beginning means that .env is a hidden configuration file. It is a common convention for files that store settings or personal information.
Now open the file in VS Code.

# 2. Add your neuPrint details

Add the following to your `.env` file:

```env
NEUPRINT_SERVER=neuprint.janelia.org
NEUPRINT_DATASET=male-cns:v1.0
NEUPRINT_TOKEN=YOUR_TOKEN_HERE
```

Replace `YOUR_TOKEN_HERE` with your personal neuPrint API token.

# 3. Tell Git to ignore `.env`

We have now created a `.env` file containing information that our Python code will need. However, remember that your `.env` file will eventually contain your **personal neuPrint API token**. We want the file to stay on your computer and **not be uploaded to GitHub**.

Fortunately, Git gives us a way to tell it:

> "You can track the rest of my project, but please ignore this file."

We do this using a special file called **`.gitignore`**.

A `.gitignore` file contains a list of files and folders that you do **not** want Git to track.

For example, if `.gitignore` contains:

```text
.env
```
Git will ignore the .env file when tracking changes in your project.

## Create or open .gitignore

First, look in the main folder of your project for a file called: `.gitignore`. If it already exists, do not create another one. Simply open the existing file.
If it does not exist, create a new file:

```bash
touch .gitignore
```
Open the `.gitignore` file and add `.env` then save the file. 


Your project might now look something like this:
Connectome2026/
├── .env
├── .gitignore
├── notebook.ipynb
└── data/

Let's make sure everything worked. In your terminal, make sure you are inside your project folder and run:

```Bash
git status
```
You should see `.gitignore` listed. We **do want** Git to track `.gitignore` so that the rule itself becomes part of the project. However, you should **not** see `.env`.
Git now knows to leave your `.env` file on your computer instead of including it in future commits.


# 4. Install `python-dotenv`

Finally, install the `python-dotenv` package in the conda environment you are using for this project:

```bash
pip install python-dotenv
```

## What does `python-dotenv` do?

Python does not automatically read the variables stored in our `.env` file. The `python-dotenv` package gives us a simple way to **load those variables into Python**. Once they are loaded, we can retrieve them using `os.getenv()`.

For example, in our ipynb notebook we can write:

```python
import os
from dotenv import load_dotenv
load_dotenv()

c = Client(
    os.getenv("NEUPRINT_SERVER"),
    dataset=os.getenv("NEUPRINT_DATASET"),
    token=os.getenv("NEUPRINT_TOKEN")
)
```

Let's break this down:

- `import os` gives us access to `os.getenv()`, which retrieves environment variables.
- `from dotenv import load_dotenv` imports the function that reads our `.env` file.
- `load_dotenv()` loads the variables stored in `.env`.
- `os.getenv("NEUPRINT_SERVER")` retrieves the value we saved as `NEUPRINT_SERVER`. The same happens for our dataset and token.
- `Client(...)` uses these values to connect to neuPrint.

So instead of writing your personal API token directly inside every notebook, Python retrieves it from your `.env` file whenever you run the code.
