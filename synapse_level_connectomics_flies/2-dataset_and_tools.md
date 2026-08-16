---
title: Dataset and Tools
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
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

<div style="text-align: center;">

:::{figure} ../static/malecns.jpg
:alt: A Drosophila CNS Connectome
:width: 500px

**Figure 1: A male CNS connectome of *Drosophila melanogaster*.** This connectome contains 166,691 neurons that have been annotated into cell types.
:::

</div>

(cell-types)=
## What are cell types?

Imagine trying to understand a dataset containing over 160,000 individual neurons. It would be extremely challenging to determine the role and organization of every neuron individually. To make sense of this complexity, anatomists group neurons into **cell types** based on shared characteristics, including morphology (physical structure) and connectivity patterns (the types of neurons they connect to).

For example, if a group of neurons has similar structures and consistently connects to similar partners, these neurons may be classified as belonging to the same cell type. This classification allows researchers to study large connectomes at a more manageable level of organization.

To better understand cell types, consider the examples below: **LC10a** and **LC10b**.



<div style="text-align: center;">

:::{figure} ../static/LC10a_celltypes.png
:width: 500px

**Figure 2: Comparison of LC10a and LC10b cell types.** When a connectome is constructed without annotations, these two neuron types may appear very similar. However, closer examination of their morphology and connectivity patterns reveals subtle differences that justify classifying them as distinct cell types.
:::

</div>

Cataloguing cell types based on connectivity is one way to group neurons into meaningful categories. However, defining what exactly makes a **cell type** has been a long-standing challenge. Neurons can differ in many ways, including their **molecular profiles, morphology, electrical properties, and functional responses**. Understanding how these different features can be used to define cell types is an entire field of research.

If you are interested in learning more, we highly recommend this [review](https://www.cell.com/cell/fulltext/S0092-8674%2822%2900783-8).

To get a good introduction to the topic, we recommend reading:

* **Summary**
* **Introduction**
* **Approaches to characterise cell types**
* **Figure 1: Approaches to characterize cell types**

These sections will help you understand what cell types are, how researchers identify them, and how connectomics contributes to the broader goal of understanding the brain.

# How do I access the connectome?

There are two primary ways to access and explore the connectome:

1. **Graphical User Interface (GUI):** A web-browser-based interface that allows users to explore neurons and connections without writing code. See the [neuPrint GUI guide](link).

2. **Application Programming Interface (API):** A programming interface that allows users to query, manipulate, and analyse connectome data. See the [neuPrint API guide](link).

The neuPrint web browser interface is sufficient for many biological questions and exploratory analyses. However, some research questions require custom processing, large-scale analyses, or data manipulation that cannot easily be performed through the web interface alone. In these cases, programming provides greater flexibility and allows researchers to interact with the connectome in more advanced ways.

Both approaches serve different purposes. If a GUI is sufficient for your question, it is often the simplest approach. When greater flexibility, customization, or advanced analyses are required, programming becomes the more suitable option.

# What tools do I need to begin?

If you are exploring the connectome programmatically, you will need to install several tools. If you are participating in the GUI track, feel free to skip this section and refer to the [neuPrint GUI Guide](../synapse_level_connectomics_flies/4a-neuprint_gui_guide.md).


## 1. Install Python, a code editor, and set-up you virtual environment

You will need:  VS Code (code editor), Python, and a virtual environment. See [Programming Guide](../programming_guide/index.md) for more details.

## 2. Install Python packages into your virtual environment via the terminal 

Python packages provide tools needed to interact with and analyse connectome data. Install these packages inside your virtual environment using the terminal:

- **neuPrint:** 
The neuPrint Python package allows you to access and query connectome datasets directly from Python. Instead of manually searching through the neuPrint website, you can write Python code to retrieve neurons, synapses, connectivity, and metadata.

### Step 1: Open a terminal

A terminal is a program where you can type commands.

Windows: Open Command Prompt or PowerShell.

macOS: Open the Terminal application (Applications → Utilities → Terminal).

Linux: Open your preferred terminal.
### Step 2: Install the package

Type the following command and press Enter:

```bash
pip install neuprint-python
```

Or, you can also use conda 

```bash
conda install -c flyem-forge neuprint-python
```

This command downloads and installs the neuPrint package along with any required dependencies.

For more details, please refer to the [neuPrint documentation](https://connectome-neuprint.github.io/neuprint-python/docs/quickstart.html).

- **Plotly:** 
Plotly is a Python library used to create **interactive visualizations**. Plotly graphs allow you to:

- zoom into specific regions of a plot
- hover over points to see additional information
- select and explore subsets of data
- interactively examine patterns and relationships

These features make Plotly especially useful during the **initial exploration of connectome data**, where datasets can contain thousands of neurons, connections, and cell types. Interactive plots can help you identify trends, outliers, clusters, and interesting biological patterns before performing more detailed analyses.

For example, Plotly can be used to create:

- scatter plots showing relationships between neuronal properties
- heatmaps showing connectivity patterns between cell types
- bar charts comparing groups of neurons
- network visualizations showing connections between brain regions

### Installing Plotly

Before using Plotly, install the package using `pip`.

Open your terminal and run:
```bash
pip install plotly
```

Or, if using Conda:
```bash
conda install -c conda-forge plotly
```

Documentation: https://pypi.org/project/plotly-express/

## Rendering Plotly Figures in a Browser

For interactive Plotly figures, especially large or data-heavy plots, rendering directly in a web browser is faster than rendering the figure inside a Jupyter notebook.

You can set the default Plotly renderer to your browser with:
```bash
import plotly.io as pio
pio.renderers.default = "browser"
```

This causes Plotly figures to open in your default web browser rather than being rendered directly inside the notebook.The browser renderer is therefore a useful option when working with large Plotly visualizations, although the standard notebook renderer is still convenient for smaller and simpler figures.

## New to Programming?

If you are new to programming or this seems overwhelming at first, that is completely normal!

Please refer to the [Programming Guide](../programming_guide/index.md) for guidance. It is highly encouraged to complete all sections if you are considering participating in the API/computational track.

Take your time, and feel free to ask questions through the Clematis Discord or during office hours! 🪰
