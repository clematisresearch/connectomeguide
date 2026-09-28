---
title: "Tutorial 4: Git, GitHub, and the Command Line"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

# Tutorial 4: Git, GitHub, and the Command Line

If your project contains code, you will use **Git** to keep a history of your work and **GitHub** to share that work in a public repository. This guide assumes that you have never used either one.

You do not need to become a Git expert. By the end of this page, you should be able to:

* open a terminal and move to your project folder;
* install and configure Git;
* create a public GitHub repository;
* copy that repository to your computer;
* save a snapshot of your work with Git; and
* upload that snapshot to GitHub without exposing private information.

## Git and GitHub Are Different

**Git** is a program on your computer that records snapshots of a folder. These snapshots are called **commits**. They let you see what changed and return to an earlier version if something goes wrong.

**GitHub** is a website that stores an online copy of a Git project. It lets you back up and share your code.

We will use both copies:

```text
project folder on your computer         public repository on GitHub
           (local)          ──push──▶             (remote)
```

Saving a file in VS Code changes the local file. Making a Git commit records a snapshot. Pushing sends your commits to GitHub. These are three separate actions.

## What Is a Terminal?

A **terminal** is a program in which you control your computer by typing commands instead of clicking buttons. The **command line** is the place where you type. You have already encountered it when installing Python packages.

For this guide, use one of these:

* **Windows:** PowerShell, or the terminal built into VS Code.
* **macOS:** Terminal, or the terminal built into VS Code.

To open the VS Code terminal, select **Terminal → New Terminal**. A line of text ending in a symbol such as `>` or `%` is the **prompt**. Type commands after the prompt, but do not copy the prompt itself.

### Your Current Folder and `cd`

The terminal is always working inside one folder, called the **current working directory**. Git commands affect the repository in that folder, so it is important to know where you are.

| Goal | Windows PowerShell | macOS Terminal |
|---|---|---|
| Show the current folder | `Get-Location` | `pwd` |
| List its contents | `Get-ChildItem` | `ls` |
| Enter a folder | `cd folder-name` | `cd folder-name` |
| Go up one folder | `cd ..` | `cd ..` |
| Go to Documents | `cd "$HOME\Documents"` | `cd ~/Documents` |

`cd` means **change directory**; a directory is another name for a folder. A folder's location is called its **path**. Put quotation marks around a path containing spaces, for example:

```powershell
cd "$HOME\Documents\Science Projects"
```

```bash
cd ~/"Science Projects"
```

After using `cd`, list the folder contents and check that you can see the files you expected. This simple check prevents many beginner Git errors.

---

# Part 1: Install and Configure Git

## Windows

1. Download **Git for Windows** from the [official Git website](https://git-scm.com/download/win).
2. Run the installer. The default choices are suitable for this guide.
3. Close and reopen VS Code after installation.
4. Open a new terminal and run:

```powershell
git --version
```

You should see a version number. If PowerShell says that `git` is not recognized, restart your computer and try once more. If it still fails, reinstall Git and make sure the installer is allowed to add Git to your command line.

## macOS

Use the [official Git installation choices for macOS](https://git-scm.com/download/mac) to install git.

Once you install, open Terminal and run:

```bash
git --version
```

If macOS asks to install the Command Line Developer Tools, select **Install**, wait for it to finish, and run `git --version` again.

## Tell Git Who You Are

Git records a name and email with each commit. Replace the example values below with your own. Keep the quotation marks around your name.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
```

Use an email connected to your GitHub account. If you do not want your personal email recorded in public commits, GitHub provides a private `noreply` address under **GitHub → Settings → Emails**. Copy that address into the second command instead.

Check your configuration:

```bash
git config --get user.name
git config --get user.email
```

These configuration commands work in both PowerShell and macOS Terminal.

---

# Part 2: Create a Public GitHub Repository

1. Create an account at [GitHub](https://github.com/) if you do not already have one. Verify your email address.
2. In the upper-right corner of GitHub, select **+ → New repository**.
3. Give the repository a clear name, such as `connectome-2026-project`.
4. Add a short description of your research project.
5. Select **Private** for now under "Choose Visibility" so your work is only visible to you. However, when you submit your competition entry, change the visibility to Public. Judges must be able to open the repository.
6. Select **Add a README file**. A README explains what the project contains.
7. Under **Add `.gitignore`**, select the **Python** template.
8. Select **Create repository**.

GitHub's [repository creation guide](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository) shows the same process with screenshots if the page looks unfamiliar.

:::{important}
A public repository can be seen by anyone. Never place passwords, personal access tokens, neuPrint tokens, or private participant data in it. The [neuPrint setup tutorial](../synapse_level_connectomics_flies/6a-neuprint_setup.md) shows how to keep a token in an ignored `.env` file.
:::

## Copy the Repository to Your Computer

On your new GitHub repository page:

1. Select the green **Code** button.
2. Select **HTTPS** and copy the URL. It will look like `https://github.com/USERNAME/connectome-2026-project.git`.
3. Open a terminal and use `cd` to move to the folder in which you want to keep the project. For example:

```powershell
cd "$HOME\Documents"
```

```bash
cd ~/Documents
```

4. Run `git clone`, replacing the example URL with the one you copied:

```bash
git clone https://github.com/USERNAME/connectome-2026-project.git
```

**Clone** means “make a local copy of this repository.” Git creates a new folder with the repository's name. Enter it:

```bash
cd connectome-2026-project
```

Then open that folder in VS Code with **File → Open Folder**. From now on, keep your notebooks, scripts, `.gitignore`, and README inside this repository folder.

---

# Part 3: Make Your First Commit

Open `README.md` in VS Code and add one sentence describing your research question. Save the file, then return to the terminal.

## 1. Inspect Your Changes

```bash
git status
```

`git status` does not change anything. It shows files that are new, modified, staged, or ignored. You should see `README.md` under “Changes not staged for commit.”

## 2. Stage the File

```bash
git add README.md
```

**Staging** means choosing which changes will go into the next snapshot. Run `git status` again and check that only the files you intend to share are staged.

## 3. Commit the Change

```bash
git commit -m "Describe research question"
```

A **commit** is a named snapshot. Write a short message that describes what changed. “Add connectivity analysis” is more useful than “update.”

## 4. Push the Commit to GitHub

```bash
git push
```

**Push** means upload your local commits to the remote repository on GitHub. The first push may open a browser and ask you to sign in to GitHub.

If the terminal asks for a GitHub *password*, do not enter your normal account password—GitHub does not accept it for Git operations. The simplest beginner option is to open VS Code's **Source Control** panel, select **Sync Changes**, and follow the browser sign-in prompt. GitHub also documents [HTTPS and SSH authentication options](https://docs.github.com/en/get-started/git-basics/set-up-git#authenticating-with-github-from-git).

Refresh the repository page in your browser. Your new README text should now appear online.

---

# Your Regular Git Workflow

Repeat this cycle whenever you complete a small, meaningful piece of work:

```text
Edit and save files
        ↓
git status
        ↓
git add specific-file.ipynb
        ↓
git commit -m "Describe the change"
        ↓
git push
```

For example:

```bash
git status
git add notebooks/query_connections.ipynb README.md
git commit -m "Add Kenyon cell connection query"
git push
```

Prefer naming the files you want to stage. `git add .` stages every non-ignored change in the current folder, which makes it easier to include an unwanted file accidentally. Always inspect `git status` before committing.

If you edit the repository from more than one computer, run `git pull` before starting work. **Pull** downloads commits from GitHub into your local copy.

## What Your Public Project Repository Should Contain

For a coding project, upload:

* every notebook or script needed to reproduce your analysis;
* a `README.md` stating your question, dataset, setup instructions, and the order in which to run files;
* small supporting files that are permitted to be shared; and
* an `.env.example` file showing required variable names but containing no real token.

Do **not** upload your `.env` file, authentication tokens, passwords, private data, or unnecessary large outputs. Before submission, open the public GitHub URL in a private/incognito browser window. If you can see the repository without signing in and can follow the README, it is ready to share.

## Protect Secrets with `.gitignore`

A `.gitignore` file tells Git which local files it should not track. For example:

```text
.env
.ipynb_checkpoints/
__pycache__/
```

The leading dot makes `.env` a hidden configuration file on many systems; it does **not** make the file secure. The protection comes from listing it in `.gitignore` **before the first commit**.

Check that Git is ignoring it:

```bash
git check-ignore .env
git status
```

The first command should print `.env`, and `.env` should not appear as a file to commit. If a secret ever appears on GitHub, removing the file later is not enough because it may remain in Git history. Stop using the exposed credential and ask an organizer or the service provider how to replace it.

---

# Optional Practice: The Odin Project

This guide contains everything required for the competition. If you would like more practice, The Odin Project offers clear explanations:

* [Introduction to Git](https://www.theodinproject.com/lessons/foundations-introduction-to-git): reinforces why version control is more useful than files named `final-v2-really-final`.
* [Git Basics](https://www.theodinproject.com/lessons/foundations-git-basics): gives extra practice with repositories, `status`, `add`, `commit`, and `push`.
* [Setting Up Git](https://www.theodinproject.com/lessons/foundations-setting-up-git): useful if you want to learn the SSH-key method.

The Odin setup lesson currently does not provide a direct Windows installation path and uses SSH rather than the HTTPS workflow above. Windows students should follow this page for setup; everyone can still use Odin's conceptual and practice sections.

# Common Problems

**“`git` is not recognized” or “command not found.”** Close and reopen VS Code after installing Git. If needed, restart the computer and check `git --version` again.

**“Not a git repository.”** The terminal is in the wrong folder. Show your current location, list its contents, and use `cd` to enter the folder you cloned. You should see `README.md` and `.gitignore` there.

**Git does not show my latest edit.** Save the file in VS Code, then run `git status` again.

**A push is rejected.** Do not force the push. Run `git pull`, read the message carefully, and ask for help if Git reports a conflict.

**My `.env` appears in `git status`.** Do not commit it. Confirm that `.gitignore` and `.env` are in the repository's top-level folder and that `.gitignore` contains a line that is exactly `.env`.

Getting an error here does not mean that you are bad at programming. Git is a new vocabulary and workflow; check one step at a time, starting with your current folder and `git status`.
