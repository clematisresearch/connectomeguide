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

# Dataset and Tools

Now that you have some background on fly neuroanatomy, neurons, neuropils, and cell types, it is time to start exploring the connectome itself!

In this competition, we will learn how to explore the **connectome of the adult male *Drosophila* Central Nervous System (CNS)**.

A connectome of this scale contains an enormous amount of information: individual neurons, their shapes and locations, their cell types, their synapses, and the connections they form with thousands of other neurons.

To make sense of these data, scientists around the world have developed powerful tools for **searching, visualizing, and analysing connectomes**. Because many of these tools and datasets are openly available, the entire scientific community, including you, now has an unprecedented opportunity to work and explore interesting research questions about the brain with such an exciting dataset!

## Three Ways to Explore the Connectome

There are many tools available, but for this competition it is useful to think about them in three main categories:

### 1. Find Neurons and Cell Types — Cell Type Explorer

The [**Drosophila Male CNS Cell Type Explorer**](https://reiserlab.github.io/celltype-explorer-drosophila-male-cns/) provides a starting point for exploring the different **cell types** found in the male CNS connectome.

You can use it to search and browse cell types and begin investigating the neurons that belong to them.

### 2. See Neurons in 3D — Neuroglancer

Knowing that a neuron exists is one thing. Seeing its structure inside the nervous system is another!

**Neuroglancer** is an interactive 3D viewer that allows you to visualize reconstructed neurons and the anatomical regions through which they travel.

You will often encounter Neuroglancer **embedded within other connectome tools**, including the Cell Type Explorer and neuPrint, allowing you to move directly from information about a neuron to its 3D anatomy.

### 3. Explore Neural Connections — neuPrint

A connectome becomes especially powerful when we start asking **who connects to whom**.

**neuPrint** allows us to explore the connectivity between neurons. For example, we can investigate which neurons provide input to a particular neuron, which neurons receive its outputs, and where those connections occur.

Together, these tools allow us to move from:

**finding a cell type → seeing its neurons → investigating their connections**

## Another Useful Resource: Virtual Fly Brain

You may also encounter [**Virtual Fly Brain (VFB)**](https://www.virtualflybrain.org/docs/overview/).

Virtual Fly Brain is an online resource for exploring *Drosophila* neuroanatomy and neuroscience data. It brings together information from different datasets and resources, allowing researchers to search for neurons and brain regions, view anatomical data, and connect what they find to related biological information.

It can be particularly useful when you encounter an unfamiliar neuron or brain structure and want to learn more about it.

## GUI vs. API: Two Ways to Work with Connectome Data

There are two broad ways that we can interact with many of these tools.

A **Graphical User Interface (GUI)** lets you interact with data visually—for example, by clicking buttons, entering a neuron name into a search box, or selecting options from a menu.

An **Application Programming Interface (API)** allows us to interact with the data using **code**. Rather than manually searching for neurons one at a time, we can write programs that query and analyse large amounts of connectome data.

:::{important}

### Introductory vs. Advanced Level

For the **Introductory Level**, we will focus on using **GUIs**. No programming is required to begin exploring neurons, their anatomy, and their connections.

For the **Advanced Level**, we will learn how to use the **neuPrint API with Python**. This allows us to query the connectome programmatically and make fuller use of the complexity and scale of the connectomic data.
:::
