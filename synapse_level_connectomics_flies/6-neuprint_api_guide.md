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

In the previous guides, we explored neurons and their connections through graphical web tools. The advanced track adds Python so that we can repeat queries, analyze many neurons at once, and adapt an analysis to a biological question.

## What *Really* Is neuPrint?

A connectome is a map of how neurons are connected through synapses, much like a road map shows how places are connected by roads. Modern connectomes contain millions of connections, so scientists need a practical way to search them without downloading the entire database.

**neuPrint** is a platform for searching, visualizing, and analyzing connectome data. Its web interface lets you explore interactively. Its **Application Programming Interface (API)** lets a Python program request the same kinds of information automatically—for example, “find these neurons,” “return their upstream partners,” or “compare connection strengths across cell types.”

The data are stored as a graph: neurons are represented as nodes and synaptic connections as relationships between them. This structure makes questions about networks and paths efficient to query.

The GUI and API are complementary:

* Use the **GUI** to inspect neurons, learn the dataset's terminology, and explore a small number of examples.
* Use the **API** when you need repeatable queries, many neurons, custom processing, or analyses that are difficult to perform by clicking.

If the GUI answers your question, it may be the simplest tool. Programming becomes useful when your question requires more scale or flexibility.

For a broader reference, see the [neuPrint User Guide](https://neuprint.janelia.org/public/neuprintuserguide.pdf).

## Before Starting the API Tutorials

The tutorials explain the connectomics code step by step, but they assume that you have completed these foundations:

1. Work through the Track 1 introductory materials, especially the [neuPrint GUI Guide](5a-neuprint_gui_guide.md) and [Male CNS Cell Type Explorer](5b-male-cns-cell-type-explorer.md). Knowing what a neuron, cell type, body ID, synapse, upstream partner, and downstream partner represent will make the code meaningful.
2. Complete the relevant parts of the [Programming Guide](../programming_guide/index.md): install Python and VS Code, learn the Python basics, create a Conda environment, and practise with pandas.
3. If you do not yet have a project repository, complete [Tutorial 4: Git, GitHub, and the Command Line](../programming_guide/7_introducing_git.md). Advanced projects must place their code in a public GitHub repository, but private credentials must stay off GitHub.

You do not need to memorize every Python command before beginning. You should be able to run a notebook cell, recognize variables and functions, and ask for help when an error appears.

## The Advanced neuPrint Sequence

Complete these pages in order:

1. **[1a) Set Up neuPrint for Python](6a-neuprint_setup.md)** — install the packages, obtain a neuPrint token, protect it in a `.env` file, and test the connection.
2. **[1b) Query Neuronal Connections](6b-neuprint_api_querying_connections.ipynb)** — select Kenyon cells and retrieve their input and output partners.
3. **[1c) Turn a Biological Question into Code](6c-neuprint_api_biology_to_code.ipynb)** — reshape and filter the connection data while explaining each analytical decision.
4. **[1d) Visualize and Interpret the Data](6d-neuprint_plotting.ipynb)** — compare connectivity patterns and connect those patterns back to biology.

The mushroom body and Kenyon cells provide a worked example. The larger goal is to learn a process that you can adapt:

```text
biological question
        ↓
choose neurons and connection data
        ↓
query and check the results
        ↓
process and visualize
        ↓
interpret with biological evidence
```

## New to Programming?

Feeling overwhelmed at first is normal. Run one cell at a time, read the output, and change only one thing before running it again. If an error occurs, start by checking that you completed Tutorial 1a, selected the correct Conda environment and notebook kernel, and opened the project folder that contains your `.env` file.

Now continue to **[1a) Set Up neuPrint for Python](6a-neuprint_setup.md)**. Do not skip it: the later notebooks deliberately assume that the setup and token-safety checks have already passed.
