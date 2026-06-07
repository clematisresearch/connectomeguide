---
title: "Neuroimaging Data Analysis"
authors:
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
---

# Overview

Now that we have introduced the basics of neuroimaging, resting-state fMRI, and the LEMON dataset, we are ready to begin working with the data itself.

This subsection **"Neuroimaging Data Analysis"** focuses on analyzing the **preprocessed resting-state fMRI data** from the LEMON dataset (i.e., the neuroimaging component of the dataset). Although we will use the LEMON dataset throughout the competition, many of the concepts, methods, and coding techniques you learn here are transferable to other fMRI datasets and neuroimaging studies.

Our goal is not only to teach you how to perform analyses, but also to help you understand the reasoning behind them. As a result, this section combines:

* **Conceptual explanations**, where we introduce the scientific ideas and principles behind each analysis step
* **Coding tutorials**, where we demonstrate how these analyses can be performed in Python

By the end of this subsection, you will understand how researchers transform preprocessed resting-state fMRI data into meaningful measures of brain connectivity.

The following subsections explain how to access the competition codebook, tutorials, and supporting materials. After that, we will begin working through the major steps involved in resting-state fMRI analysis!

<!-- * Brain parcellation
* Extracting regional time series
* Constructing resting-state functional connectivity (rsFC) matrices
* Visualizing and interpreting brain networks
* Applying graph-theoretical analyses
* Relating brain connectivity to cognition, behavior, physiology, and mental health
* Exploring predictive and machine learning approaches -->

These topics will provide many of the tools needed to explore your own research questions throughout the competition.

```{note}
If you are currently exploring the handbook and are simply curious about neuroimaging, you do not need to install anything yet. You are welcome to continue reading and learning about the dataset, neuroimaging, and connectomics before deciding whether you would like to perform the analyses yourself. You may also skip ahead to later sections and return to the coding tutorials when you are ready, including the materials below on accessing the dataset and codebook. When software installation becomes necessary, we will provide clear instructions and let you know exactly what needs to be installed and when.
```

# Accessing the Dataset and Codebook

The competition codebook, tutorials, analysis scripts, and supporting materials are available through the official Connectome2026 GitHub repository:

https://github.com/clematisresearch/competition

If you have never used Git, GitHub, or the command line before, do not worry. Please refer to our [Programming Guide](../programming_guide/index.md), where we provide a beginner-friendly introduction to these tools.

To download the repository onto your computer, open a command-line terminal and run:

```bash
git clone https://github.com/clematisresearch/competition.git
```

This command will create a local copy of the competition repository on your computer.

As the competition progresses, the organizers may update the repository with additional resources, code examples, bug fixes, clarifications, or new materials. To download the latest updates, navigate to the repository folder and run:

```bash
git pull
```

```{note} 
If you are currently exploring the handbook and are simply curious about neuroimaging, you do not need to install anything yet. You can continue reading and learning about the dataset, neuroimaging, and connectomics before deciding whether you would like to perform the analyses yourself. When software installation becomes necessary, we will provide clear instructions and let you know exactly what needs to be installed and when.
```

## Software Requirements

Throughout this track, we will be using **Python** for data analysis. 

In addition to downloading the competition repository, participants will eventually need to install several software tools and packages, including:

* **Python**
* **Conda** (recommended for managing Python environments)
* An integrated development environment (IDE), such as **Visual Studio Code (VS Code)**
* **Nilearn**, a popular Python library for neuroimaging analysis:
  https://nilearn.github.io/stable/quickstart.html
* **NetworkX**, a Python package for the creation, manipulation, and study of the structure, dynamics, and functions of complex networks: https://networkx.org/documentation/stable/index.html

```{note} 
If you are currently exploring the handbook and are simply curious about neuroimaging, you do not need to install anything yet. You can continue reading and learning about the dataset, neuroimaging, and connectomics before deciding whether you would like to perform the analyses yourself. When software installation becomes necessary, we will provide clear instructions and let you know exactly what needs to be installed and when.
```

