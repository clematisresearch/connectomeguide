---
title: Dataset and Tools
authors:
  - name:
      given: Aarushi
      family: Vardhan
---

Welcome to exploring the fly connectome!

Regardless of your background, this guide is designed to help you learn how to access and analyse the connectome programmatically, allowing you to investigate research questions that interest you. This guide assumes some basic programming knowledge. If you are new to programming, check out our introductory programming resources first: [Programming Guide](../programming_guide/index.md).

This guide outlines the essential steps needed to get started, including the tools and resources required to access and analyse the connectome. We welcome your feedback and suggestions on how this guide can be improved and developed as an evolving resource for students.

Enjoy exploring the fly brain!

# The maleCNS Dataset

We will be using the [maleCNS Connectome](https://www.janelia.org/project-team/flyem/male-cns-connectome). This is a male *Drosophila* connectome of the entire central nervous system (hence, maleCNS). This connectome consists of three major regions:

- **Optic Lobe:** The visual processing system of the fly.
- **Ventral Nerve Cord:** Similar to the spinal cord in vertebrates, this region processes and relays information throughout the body.
- **Central Brain:** The main processing center of the fly brain.

:::{image} ../static/malecns.jpg
:alt: A Drosophila CNS Connectome
:width: 500px
:::

This connectome contains **166,691 neurons** that have been annotated into cell types.

## What are cell types?

Imagine trying to understand a dataset containing over 160,000 individual neurons. It would be extremely challenging to determine the role and organization of every neuron individually. To make sense of this complexity, anatomists have grouped neurons into **cell types** based on shared characteristics, including morphology (physical structure) and connectivity patterns.

For example, if a group of neurons has similar structures and consistently connects to similar partners, these neurons may be classified as belonging to the same cell type. This classification allows researchers to study large connectomes at a more manageable level of organization.

To better understand cell types, consider the examples below: **LC10a** and **LC10b**.

When a connectome is constructed without annotations, these two neuron types may appear very similar. However, closer examination of their morphology and connectivity patterns reveals subtle differences that justify classifying them as distinct cell types.

:::{image} ../static/LC10a_celltypes.png
:alt: Comparison of LC10a and LC10b cell types
:width: 500px
:::

# How do I access the connectome?

There are two primary ways to access and explore the connectome:

1. **Graphical User Interface (GUI):** A web-browser-based interface that allows users to explore neurons and connections without writing code. See the [neuPrint GUI guide](link).

2. **Application Programming Interface (API):** A programming interface that allows users to query, manipulate, and analyse connectome data. See the [neuPrint API guide](link).

The neuPrint web browser interface is sufficient for many biological questions and exploratory analyses. However, some research questions require custom processing, large-scale analyses, or data manipulation that cannot easily be performed through the web interface alone. In these cases, programming provides greater flexibility and allows researchers to interact with the connectome in more advanced ways.

Both approaches serve different purposes. If a GUI is sufficient for your question, it is often the simplest approach. When greater flexibility, customization, or advanced analyses are required, programming becomes the more suitable option.

# What tools do I need to begin?

Before exploring the connectome programmatically, you will need to install several tools.

## 1. Install Python, a code editor, and set-up you virtual environment

You will need:

- A code editor (we recommend [Visual Studio Code](https://code.visualstudio.com/)).
- Python, the programming language used for analysis.

For background on code editors, see:
[IDE vs Code Editor](https://www.geeksforgeeks.org/blogs/ide-vs-code-editor/)

For a tutorial on installing VS Code, Python, and setting up a virtual environment:
[VS Code, Python, Virtual Environment setup tutorial](https://www.youtube.com/watch?v=D2cwvpJSBX4)

## 2. Install Python packages into your virtual environment via the terminal 

Python packages provide tools needed to ineract with and analyse connectome data. Install these packages inside your virtual environment using the terminal:

- **neuPrint:** 
The neuPrint Python package allows you to access and query connectome data

Open terminal and run the following command: 
```bash
pip install neuprint-python
```
Documentation: https://connectome-neuprint.github.io/neuprint-python/docs/quickstart.html

- **Plotly:** 
Plotly is used for creating interactive visualizations.

Run the following command on terminal: 

```bash
pip install plotly_express==0.4.0
```
Documentation: https://pypi.org/project/plotly-express/

- **Pandas:** 
Pandas is used for organizing and analysing data.

```bash
pip install pandas
```
Documentation: https://pypi.org/project/pandas/

## 3. Create a neuPrint Account and Client 

You will need to have a Google account. You can find the client... 

## New to Programming?

If you are new to programming or this seems overwhelming at first, that is completely normal!

Here is a resource that we personally found very helpful for building programming foundations:

https://www.theodinproject.com/paths

You will need to create an account (you can use your Google account).

We recommend completing the following sections:

Foundations → Introduction
Introduction to Web Development
Motivation and Mindset
Foundations → Prerequisites
How Does the Web Work?
Installations
Text Editors
Command Line Basics

Take your time, and feel free to ask questions through Discord or during office hours! 
