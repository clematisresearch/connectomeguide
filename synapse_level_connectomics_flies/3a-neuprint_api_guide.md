---
title: "neuPrint API Guide (Advanced Level)"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

# neuPrint API Guide (Advanced Level)

In the previous guides, we interacted with neuPrint and explored the connectome through the web interface. 

## But ... What *Really* is neuPrint? 

A connectome is a map of how neurons are connected to one another through synapses, much like a road map shows how different places are linked by roads. As advances in electron microscopy and artificial intelligence made it possible to reconstruct increasingly large connectomes, scientists needed an easy way to explore these vast datasets without downloading millions of connections or writing computer code. **neuPrint** was developed to meet this need. It is a free, web-based platform that allows researchers to search for neurons, view their shapes, identify their synaptic partners, and investigate how neural circuits are organized using only a web browser. Designed with biologists in mind, neuPrint makes complex connectome data accessible through an intuitive interface, enabling users to answer questions such as "Which neurons connect to this cell?" or "How strong are these connections?" in just a few clicks. 

While the neuPrint website is designed for interactive exploration through a web browser, it also provides Application Programming Interfaces (APIs) for users who wish to perform automated or large-scale analyses (which we will be using here!). An API allows a computer program to communicate directly with neuPrint, making it possible to retrieve data, run repeated queries, and integrate connectome information into custom analysis pipelines without manually using the website. The data within neuPrint is stored in a Neo4j graph database, which represents neurons as nodes and synaptic connections as relationships between them. This graph-based structure closely reflects the organization of neural circuits and allows complex connectivity queries to be performed efficiently, even for connectomes containing millions of synapses.

The neuPrint web browser interface is sufficient for many biological questions and exploratory analyses. However, some research questions require custom processing, large-scale analyses, or data manipulation that cannot easily be performed through the web interface alone. In these cases, programming provides greater flexibility and allows researchers to interact with the connectome in more advanced ways.

Both approaches serve different purposes. If a GUI is sufficient for your question, it is often the simplest approach. When greater flexibility, customization, or advanced analyses are required, programming becomes the more suitable option.

For more detailed information on neuPrint's features, feel free to read the [neuPrint User Guide](https://neuprint.janelia.org/public/neuprintuserguide.pdf).

---

## What Tools Do I Need to Begin?

If you are exploring the connectome programmatically, you will need to install several tools. If you are participating in the GUI track, feel free to refer to the [neuPrint GUI Guide](4a-neuprint_gui_guide.md) and [Male CNS Cell Type Explorer](male-cns-cell-type-explorer.md).

### 1. Install Python, a Code Editor, and Set Up Your Virtual Environment

You will need: **VS Code** (code editor), **Python**, and a **virtual environment**. See the [Programming Guide](../programming_guide/index.md) for more details. 

**Specifically,**

See [Installing Python and Exploring Basic Concepts](../programming_guide/2_python_install.md) for how to install Python and Visual Studio Code and for a Python crash course. 

See [Conda, Packages, and Jupyter Notebook](../programming_guide/3_python_conda.ipynb) for how to manage Python environments, install packages, and write code in Jupyter Notebooks (.ipynb), which are widely used in data science and neuroscience.

:::{tip}
### Programming Knowledge Needed
We will walk through the code step-by-step in the [neuPrint API Tutorial Notebook](3b-neuprint_api_guide.ipynb). However, it is very helpful to be comfortable with core Python fundamentals (variables, lists, dictionaries, loops, functions) and tabular data manipulation with **pandas**—all of which are covered in the [Programming Guide](../programming_guide/index.md).
:::

### 2. Install Python Packages into Your Virtual Environment via the Terminal

Python packages provide tools needed to interact with and analyse connectome data. Install these packages inside your virtual environment using the terminal:

**`neuprint-python`:**  
  The neuPrint Python package allows you to access and query connectome datasets directly from Python. Instead of manually searching through the neuPrint website, you can write Python code to retrieve neurons, synapses, connectivity, and metadata.

#### Step 1: Open a terminal
A terminal is a program where you can type commands:
* **Windows:** Open Command Prompt or PowerShell.
* **macOS:** Open the Terminal application (Applications → Utilities → Terminal).
* **Linux:** Open your preferred terminal.

#### Step 2: Install the package
Type the following command and press Enter:
```bash
pip install neuprint-python
```
Or, you can also use conda:
```bash
conda install -c flyem-forge neuprint-python
```
This command downloads and installs the neuPrint package along with any required dependencies.

For more details, please refer to the [neuPrint documentation](https://connectome-neuprint.github.io/neuprint-python/docs/quickstart.html).


**`plotly`:**  
  Plotly is a Python library used to create **interactive visualizations**. Plotly graphs allow you to:
  * zoom into specific regions of a plot
  * hover over points to see additional information
  * select and explore subsets of data
  * interactively examine patterns and relationships

These features make Plotly especially useful during the **initial exploration of connectome data**, where datasets can contain thousands of neurons, connections, and cell types. Interactive plots can help you identify trends, outliers, clusters, and interesting biological patterns before performing more detailed analyses.

For example, Plotly can be used to create:
* scatter plots showing relationships between neuronal properties
* heatmaps showing connectivity patterns between cell types
* bar charts comparing groups of neurons
* network visualizations showing connections between brain regions

#### Installing Plotly
Before using Plotly, install the package using `pip`. Open your terminal and run:
```bash
pip install plotly
```
Or, if using Conda:
```bash
conda install -c conda-forge plotly
```
Documentation: https://pypi.org/project/plotly-express/

### Rendering Plotly Figures in a Browser

For interactive Plotly figures, especially large or data-heavy plots, rendering directly in a web browser is faster than rendering the figure inside a Jupyter notebook.

You can set the default Plotly renderer to your browser with:
```python
import plotly.io as pio
pio.renderers.default = "browser"
```

This causes Plotly figures to open in your default web browser rather than being rendered directly inside the notebook. The browser renderer is therefore a useful option when working with large Plotly visualizations, although the standard notebook renderer is still convenient for smaller and simpler figures.

---

## Create a neuPrint Account

Installing `neuprint-python` is the first step, but before Python can retrieve data from neuPrint, you need a neuPrint account, an authentication token, the URL of the neuPrint server, and the name of the dataset you want to query.

You will need to have a Google account. Using your Google Account, go ahead and log in to [neuPrint](https://neuprint.janelia.org).

---

## Connecting to a neuPrint Server

The next step is to connect to a neuPrint server.

Before Python can retrieve any data from neuPrint, it needs to know **where** the data is located and **whether you have permission** to access it.

This is done by creating a **Client** object.

### What is a Client?

A **Client** acts as the connection between your Python program and the neuPrint server. Every time you ask for information such as a neuron, cell type, or synaptic connection, the Client sends your request to the server and returns the results.

Without a Client, Python has no way of knowing:
- which neuPrint server to connect to
- which connectome dataset to use
- whether you are authorized to access the data

### Information Required to Create a Client

To create a Client, you need three pieces of information:

#### 1. neuPrint server address
The **server address** tells Python where the connectome database is hosted:
```text
https://neuprint.janelia.org
```
This is the website that stores several publicly available connectome datasets.

#### 2. Dataset
A neuPrint server can contain multiple connectome datasets. The **dataset name** tells Python which connectome you want to query:
```text
male-cns:v1.0
```
Think of a dataset as a specific version of a connectome. Different datasets may represent different brain regions, species, or releases. The dataset we are using is the **male CNS connectome**, and **v1.0** is the version used in this competition. It is good practice to check whether a newer dataset version is available before starting your analysis, so that you are working with the most up-to-date version.

#### 3. Authentication token
An **authentication token** is a unique string of characters linked to your neuPrint account.

When Python connects to the server, it sends this token to prove your identity. This allows the server to verify that you have permission to access the requested data.

You can think of the token as a **digital key** that unlocks access to the neuPrint server. Instead of entering your username and password every time you run your code, Python uses the token automatically.

:::{important}
**Keep your authentication token private.** Anyone with your token may be able to access neuPrint using your account. You get the token by going to the neuPrint web browser. Click on the upper right corner (see image below) where your account is located. There you will find your unique neuPrint token.
:::

```{figure} ../static/token-screenshot.png
:alt: neuPrint Token
:width: 500px
:align: center

**Figure 1: Finding your neuPrint token.** Click on the account icon in the upper right corner (circled in red). There you will find your unique token.
```

Once you have these three pieces of information, you are ready to create your first `Client` object and begin querying connectome data!

For more details, check out the [neuPrint documentation](https://connectome-neuprint.github.io/neuprint-python/docs/quickstart.html).

---

## New to Programming?

If you are new to programming or this seems overwhelming at first, that is completely normal!

Please refer to the [Programming Guide](../programming_guide/index.md) for guidance. It is highly encouraged to complete all sections if you are considering participating in the API/computational track.

Take your time, and feel free to ask questions through the Clematis Discord or during office hours! 🪰

---

## Next Steps

Now head over to the [neuPrint API Tutorial Notebook](3b-neuprint_api_guide.ipynb) to get started with querying the connectome in Python!