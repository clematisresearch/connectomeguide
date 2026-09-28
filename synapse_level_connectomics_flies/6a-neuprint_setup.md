---
title: "1a) Set Up neuPrint for Python"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

# 1a) Set Up neuPrint for Python

This page completes the setup for the advanced neuPrint tutorials. By the end, your project will contain the packages and connection information that Python needs, while your personal neuPrint token remains private.

:::{important}
Your neuPrint token is a **secret linked to your account**. Never paste it into a notebook, screenshot, report, Discord message, or GitHub repository.
:::

## Before You Begin

You should already have:

* Python, VS Code, and a Conda environment from the [Programming Guide](../programming_guide/index.md);
* a project folder opened in VS Code; and
* for an advanced competition project, a public repository created by following [Tutorial 4: Git, GitHub, and the Command Line](../programming_guide/7_introducing_git.md).

If you are not using Git yet, you can still complete the connection test below. You must set up the public repository before submitting a project that contains code.

## 1. Activate Your Environment and Install the Packages

In VS Code, select **Terminal → New Terminal**. Activate the Conda environment you created for this project. The Programming Guide used `neuroimaging` as its example name; replace it if you chose a different name:

```bash
conda activate neuroimaging
```

The environment name should appear near the beginning of the terminal prompt. Install the packages used across Tutorials 1b–1d:

```bash
python -m pip install neuprint-python python-dotenv pandas plotly scipy jupyter
```

`python -m pip` installs the packages for the active Python environment. In particular:

* `neuprint-python` communicates with neuPrint;
* `python-dotenv` reads the private settings in a `.env` file;
* `pandas` works with tables;
* `plotly` creates interactive figures; and
* `scipy` provides the clustering tools used later.

If you change environments later, you must install the packages in the new environment too.

## 2. Create a neuPrint Account and Copy Your Token

1. Open [neuPrint](https://neuprint.janelia.org/) in a browser and sign in with a Google account.
2. Select your account icon in the upper-right corner.
3. Open **Account** and copy the entire authentication token.

```{figure} ../static/token-screenshot.png
:alt: neuPrint account menu with the token location highlighted
:width: 500px
:align: center

**Finding your neuPrint token.** Open the account menu in the upper-right corner after signing in.
```

Python needs three values to create a neuPrint `Client`:

* **server** — where the neuPrint service is hosted;
* **dataset** — the connectome and version to query; and
* **token** — the private key that identifies your account.

This competition uses the server `neuprint.janelia.org` and dataset `male-cns:v1.0`.

## 3. Create the Private `.env` File

In the VS Code Explorer, select **New File** in the top level of your project folder and name the file exactly:

```text
.env
```

This method works on both Windows and macOS. Add the following lines:

```text
NEUPRINT_SERVER=neuprint.janelia.org
NEUPRINT_DATASET=male-cns:v1.0
NEUPRINT_TOKEN=PASTE_YOUR_TOKEN_HERE
```

Replace only `PASTE_YOUR_TOKEN_HERE`, then save the file. Do not add spaces around `=` and do not share the completed file.

A `.env` file is a plain text file containing **environment variables**: named settings that code can read. It is not the same as a Python or Conda environment. The similar names are unfortunate:

* a **Conda environment** keeps a project's Python and packages together;
* a **`.env` file** keeps small configuration values, including secrets, outside the notebook.

## 4. Make Git Ignore `.env`

In the same top-level project folder, open the existing `.gitignore` file. If it does not exist, create it in VS Code. Make sure it contains:

```text
.env
.ipynb_checkpoints/
__pycache__/
```

`.gitignore` tells Git not to track matching files. Save it, then check the rule in the terminal:

If this folder is not yet a Git repository, keep the rule and skip the next two Git commands until you have completed the Git/GitHub tutorial.

```bash
git check-ignore .env
```

The output should be `.env`. Now run:

```bash
git status
```

You may see `.gitignore`, but you should **not** see `.env` as a file to commit. If `.env` appears, stop and check that both files are in the repository's top-level folder and that the ignore line is exactly `.env`.

:::{warning}
Ignoring a file only prevents future tracking. If you already committed `.env`, do not push it. Run `git rm --cached .env` to stop tracking the local file, commit that removal, and ask an organizer for help. If the token has already appeared on GitHub, treat it as exposed and ask how to replace it.
:::

## 5. Add a Safe `.env.example`

Other people need to know which settings your code expects, but they do not need your values. Create a second file named `.env.example`:

```text
NEUPRINT_SERVER=neuprint.janelia.org
NEUPRINT_DATASET=male-cns:v1.0
NEUPRINT_TOKEN=paste-your-own-token-here
```

This example file contains no secret, so it **should** be committed to GitHub with `.gitignore`. Your folder may now look like this:

```text
connectome-2026-project/
├── .env                 # private; never commit
├── .env.example         # safe instructions; commit this
├── .gitignore           # tells Git to ignore .env
├── README.md
└── notebooks/
```

## 6. Test the Connection

Create a notebook in the project folder, select the kernel for your Conda environment, and run this cell:

```python
import os

from dotenv import load_dotenv
from neuprint import Client

load_dotenv()

settings = {
    "NEUPRINT_SERVER": os.getenv("NEUPRINT_SERVER"),
    "NEUPRINT_DATASET": os.getenv("NEUPRINT_DATASET"),
    "NEUPRINT_TOKEN": os.getenv("NEUPRINT_TOKEN"),
}

missing = [name for name, value in settings.items() if not value]
if missing:
    raise ValueError(f"Missing settings in .env: {', '.join(missing)}")

client = Client(
    settings["NEUPRINT_SERVER"],
    dataset=settings["NEUPRINT_DATASET"],
    token=settings["NEUPRINT_TOKEN"],
)

print("Connected to neuPrint version:", client.fetch_version())
```

The code loads the three values without displaying your token, checks that none is missing, creates the `Client`, and asks the server for its version. If a version prints, the setup is complete.

### If the Test Does Not Work

**`ModuleNotFoundError`:** the notebook is probably using a different Python environment. In VS Code, select the notebook's kernel in the upper-right corner and choose the environment in which you installed the packages.

**“Missing settings in `.env`”:** make sure the file is named exactly `.env`, is saved, and is in the project folder you opened. Check the spelling of all three variable names.

**Authentication or authorization error:** sign in to neuPrint again and copy the complete token. Check for accidental spaces. Do not post the token when asking for help.

**`git check-ignore .env` prints nothing:** check the names and locations of `.env` and `.gitignore`, then run the command from the repository's top-level folder.

For the underlying client requirements, see the official [`neuprint-python` Quickstart](https://connectome-neuprint.github.io/neuprint-python/docs/quickstart.html). Its examples place the token directly in code for brevity; keep using `.env` in your own project so the token cannot be committed accidentally.

## Setup Checklist

Before continuing, confirm that:

* the connection test prints a neuPrint version;
* `.env` contains your real token;
* `git check-ignore .env` prints `.env`;
* `git status` does not offer to commit `.env`; and
* `.env.example` contains only the placeholder token.

You are ready for **[1b) Querying Neuronal Connections with the neuPrint API](6b-neuprint_api_querying_connections.ipynb)**.
