---
title: Installing Python and Exploring Basic Concepts
authors:
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
---

# Installing Python

Before we can begin programming, we first need to install Python on our computer.

Although the installation process is usually straightforward, it can vary slightly depending on your operating system and your computer's settings. Don't worry if your screen doesn't look exactly like the examples in the tutorials—we'll point you towards reliable resources, and a quick Google search or ChatGPT can usually help explain any differences you encounter.

> [!TIP]
> We know installation guides aren't the most exciting part of learning Python, but taking a few minutes to read the instructions carefully can save you from spending much longer troubleshooting avoidable setup issues later. A little patience now can save a lot of frustration down the road.

---

## macOS

Many Macs already come with a version of Python pre-installed. However, this version is intended for the operating system itself and may not be the version you want for scientific programming.

For this reason, **we recommend installing the latest version of Python yourself**, even if Python is already installed on your Mac.

### Step 1: Install Python

If you've never installed Python before, follow the official installation guide from Real Python:

**Installing Python on macOS (Official Installer)**

https://realpython.com/installing-python/#macos-how-to-install-python-using-the-official-installer

The second step mentions "Press Customize in the Installation Type window if you want to customize the installation." When you reach the Installation Type window, you do not need to click Customize. The default installation settings are suitable for this guide, so simply click Install to continue.

During the installation, one of the final steps mentions:

> *"When the installer is finished, a Finder window will be opened and you'll see the installation artifacts there."*

At this stage, **you do not need to understand what these installation artifacts are** (for example, Python Launcher, IDLE, documentation, or other files that were installed). Simply completing the installation is enough for now. We'll introduce the tools you'll actually use later in this guide.

### Step 2: Check That Python Was Installed

After installation, it's good practice to confirm that Python was installed successfully and to check which version you have.

Follow the instructions here:

https://realpython.com/installing-python/#macos-how-to-check-or-get-python

This introduces a program called **Terminal**, which allows you to interact with your computer by typing commands instead of clicking buttons. Every Macbook should have a Terminal as one of their apps. While it may look unfamiliar at first, don't worry!

### Video Tutorial

If you'd prefer to follow a video, this tutorial covers both installation and checking your Python version:

https://www.youtube.com/watch?v=nhv82tvFfkM

* Watch **0:00–2:17** to install Python.
* Continue until approximately **4:00** to learn how to check your Python version.

---

## Windows

There are now several ways to install Python on Windows.

We recommend using the **Python Install Manager** from https://www.python.org/, as it provides a simple and reliable way to install and manage Python versions.

### Step 1: Install Python

Follow the written guide below:

https://code-campus.at/python/installation/

The page also contains a short video walkthrough if you prefer to follow along visually.

Alternatively, you can watch the installation video directly here:

https://www.youtube.com/watch?v=jnNJr-U2LhM

### Command Prompt and PowerShell

During the installation process, you'll encounter either **Command Prompt** or **PowerShell**.

These are command-line programs that allow you to communicate with your computer by typing commands instead of using a graphical interface. They are Windows' equivalent of the macOS Terminal. As you continue learning Python, you'll occasionally use these tools to install packages, create environments, and run simple commands.

Don't worry if you've never used them before. We'll introduce the commands you need gradually throughout this guide.

### Installation Questions

We hope the instructions above were sufficient to help you install Python using the Python Install Manager. However, depending on your version of Windows or your system configuration, you may encounter slight variations during the installation process, particularly in the Command Prompt or PowerShell. For example, you may be asked questions such as:

* **Update settings now?**
* **Add commands directory to your PATH now?**
* **Install CPython now?**

For the purposes of this guide, you can generally answer **Yes** to these prompts.

### If Your Installation Looks Different

Depending on your version of Windows or your laptop's configuration, the installation process may look slightly different from the tutorials above.

If your screen doesn't exactly match the instructions:

1. Compare both the written guide and the accompanying video.
2. Search online (or ask ChatGPT) if you're unsure what a particular option means.
3. If you're still stuck, don't hesitate to reach out to us for help.


# Visual Studio Code and Python Crash Course

Now that Python is installed, it's time to install an **Integrated Development Environment (IDE)**.

An IDE is a program that helps you write, organise, and run your code. Think of it as your programming workspace—it provides useful features such as syntax highlighting, code completion, debugging tools, and an integrated terminal.

For this guide, we'll use **Visual Studio Code (VS Code)**, one of the most popular and beginner-friendly code editors used by students, researchers, and professional software developers.

---

## Step 1: Install Visual Studio Code

Visit the official Visual Studio Code website:

https://code.visualstudio.com/

Click the large **Download** button for your operating system and install Visual Studio Code.

During the installation, the default settings are suitable for this guide, so you can simply proceed through the installer using the default options.

---

## Step 2: Learn the Basics

We recommend the following beginner-friendly video:

**Python Tutorial for Beginners - Learn the basics in 20 Min**

https://www.youtube.com/watch?v=Js05B8Z1ivE&t=953s

> [!IMPORTANT]
> **Skip the Python installation section (00:21–01:03).**
>
> In the video, Python is installed using the standalone installer which is gradually being phased out. Since you've already installed Python (using the Python Install Manager on Windows or the official installer on macOS), you can safely skip this part and continue watching from **01:03**.

The remainder of the video provides an excellent introduction to both Visual Studio Code and the fundamentals of Python programming.

In particular, it demonstrates:

* setting up Visual Studio Code as your IDE,
* installing the Python extension for Visual Studio Code,
* creating and running your first Python program,
* variables,
* strings,
* f-strings,
* user input,
* lists,
* conditional statements (`if`),
* `for` loops,
* functions.

If you are completely new to programming, don't feel that you need to memorise everything in these videos. The goal at this stage is simply to become familiar with the basic terminology. We encourage you to watch the videos, follow along by running each piece of code at least once, and gain a general understanding of what the different Python concepts do. Many of these ideas will be revisited and reinforced throughout Tutorial 1 of the Programming Guide and the subsequent tutorials, so there is no expectation that you will remember everything after a single pass.

As you watch the videos, try to follow along in your own Python file using Visual Studio Code. Pause the video occasionally, type the code yourself, and run it to see what happens. Once it works, experiment by changing a few things—for example, modify a variable's value, change the text being printed, or rename a function or variable. Small experiments like these are one of the best ways to build intuition and confidence.

If you come across a concept that doesn't quite make sense—such as variables, functions, or for loops—you may ask ChatGPT (or another AI assistant) to explain the intuition behind it or walk through an example step by step. AI can be an excellent tutor for answering questions and clarifying concepts. However, try to write and run the code yourself rather than simply copying the answers. Programming is a practical skill, and the more you experiment with the code on your own, especially at this stage, the faster you'll learn.
