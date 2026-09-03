---
title: "Git: Coding Practices to keep in mind"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

## Git & GitHub Setup

Before starting the project, you will need to set up Git and GitHub. We will use Git to keep track of changes to your code and GitHub to store your project.

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

### What you should be comfortable with afterwards

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

### Git Ignore

Before we begin working with the neuPrint API, we need to set up a way to store our neuPrint connection details.

Throughout the tutorials, we will use information such as the neuPrint server, dataset, and your personal API token. Rather than entering these details in every notebook, we can store them in a local `.env` file and load them whenever we need them.

Because your `.env` file contains your personal API token, we will tell Git to **ignore** this file. This means it will remain on your computer and will not be uploaded to GitHub.

This gives us two benefits:

* You only need to enter your neuPrint details once.
* Your API token stays private and is not included in the project repository.

We will set this up before starting the neuPrint API tutorials.

#### 1. Create your `.env` file

First, open the terminal and navigate to your project folder, where you will keep your notebooks and scripts.

Your project could look something like this:

```text
Connectome2026/
├── .git/
├── .gitignore
├── notebook.ipynb
└── data/
```

In the terminal, type:

```bash
touch .env
```

This creates an empty `.env` file.

Now open the file in VS Code.

#### 2. Add your neuPrint details

Add the following to your `.env` file:

```env
NEUPRINT_SERVER=neuprint.janelia.org
NEUPRINT_DATASET=male-cns:v1.0
NEUPRINT_TOKEN=YOUR_TOKEN_HERE
```

Replace `YOUR_TOKEN_HERE` with your personal neuPrint API token.

#### 3. Tell Git to ignore `.env`

Open or create the `.gitignore` file in your project folder.

Add:

```text
.env
```

This tells Git not to track your `.env` file.

You can check that this worked by running:

```bash
git status
```

Your `.env` file should not appear as a file that Git is going to commit.

#### 4. Install `python-dotenv`

Finally, install the `python-dotenv` package in the conda environment you are using for this project:

```bash
pip install python-dotenv
```

We can now load our neuPrint details directly from `.env` in our notebooks, rather than entering them manually each time.
