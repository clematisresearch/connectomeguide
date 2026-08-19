---
title: "Putting It All Together: Your Connectomics Project (Introductory Track)"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---


You have now learned the foundations needed to begin exploring the **adult male *****Drosophila***** CNS connectome** independently.

Before moving on, let's briefly put together what you have learned.

# What Have We Learned?

## The Fly Nervous System

You began with the basic building blocks of the nervous system: **neurons, dendrites, axons, synapses, and neurotransmitters**.

From there, you explored how neurons are organized within the fly nervous system. You learned about **neuropils** and several major regions of the brain, including the:

* **optic lobes**, which process visual information;
* **antennal lobes**, which process olfactory information;
* **mushroom bodies**, which are important for learning and memory;
* **central complex**, which contributes to navigation and movement; and
* **gnathal ganglia and other neuropils** involved in sensory and motor processing.

You also learned an important distinction between an **individual neuron**, its **cell type**, and broader classifications such as **superclasses**.

## Exploring the Connectome

You then learned how several complementary tools allow us to investigate the same nervous system from different perspectives.

**Cell Type Explorer** helps you discover and browse cell types. You can search by properties such as brain region, examine how many neurons belong to a type, and investigate its anatomy and connectivity.

**Neuroglancer** lets you see neurons in **3D**. You can examine their morphology, determine which neuropils they enter, and visualize their presynaptic and postsynaptic sites.

**neuPrint** lets you investigate **neural connectivity**. You can ask which neurons provide input to your neuron, which neurons receive its outputs, and where those connections occur, and how your neuron fits into a larger circuit.

Finally, **Virtual Fly Brain** helps connect your observations to existing biological knowledge and published literature.

Together, these tools allow you to move from:

**finding a neuron → seeing its anatomy → exploring its connections → investigating what is already known → developing your own questions**

---

# What Can You Do for the Introductory Level Project?

You now have the tools to begin working like a connectomics researcher.

For the **Introductory Level (GUI Track)**, your goal is to choose a neuron or cell type from the **Male CNS Connectome**, investigate it using the tools you have learned, and use your observations together with scientific literature to develop a possible explanation of its role in the nervous system.

Your project might begin with something very simple:

**"This neuron looks interesting. What does it do?"**

From there, your investigation can grow.

# How to Approach Your Project

## 1. Choose a Neuron or Cell Type

Start by finding something that sparks your curiosity.

You might choose a neuron because of its:

* unusual **shape**;
* location in a particular **neuropil**;
* interesting **upstream or downstream connections**;
* association with a sensory system or behaviour you find interesting; or
* simply because **it looks cool!**

## 2. Explore Its Anatomy

Use **Neuroglancer** to examine the neuron in 3D.

Ask questions such as:

**Where does it branch? Which neuropils does it enter? Where are its inputs and outputs? Does it connect distant parts of the brain?**

Save useful visualizations that help communicate what you discover.

## 3. Explore Its Connectivity

Use the **Cell Type Explorer and neuPrint** to investigate its upstream and downstream partners.

Ask:

**Who sends information to this neuron?**

**Who receives information from it?**

**Where in the brain do these connections occur?**

Try to identify some meaningful insights or patterns rather than simply listing connections.

## 4. Investigate What Is Already Known

Use resources such as **Virtual Fly Brain**, scientific papers, and other reliable sources to investigate what researchers already know about your neuron.

Has it been studied before? What circuits is it associated with? Has it been linked to a particular sensory process or behaviour?

Your literature search gives you biological context for what you observed in the connectome.

## 5. Connect Structure, Connectivity, and Function

This is where your investigation becomes particularly interesting.

Bring together:

**Morphology + Connectivity + Scientific Literature**

and ask what they might tell you about the neuron's possible function.

For example, perhaps you notice that a neuron receives many inputs in one neuropil but sends most of its outputs somewhere else. What might that suggest about the flow of information through the circuit?

Your interpretation does not need to prove what the neuron does. Instead, develop a **well-reasoned hypothesis supported by evidence** from the connectome and scientific literature.

## 6. Communicate What You Found

You will bring your investigation together in a **500–1000 word research report**, supported by appropriate figures and references, and share highlights of your work and visualizations with the Clematis community on Discord.

Your project should tell a scientific story:

**What did you investigate? → What did you observe? → What is already known? → What do you think your observations might mean?**

:::{important}

## You Don't Need to Discover Something Completely New

Research begins by asking good questions and examining evidence carefully.

You may confirm something already described in the literature, find an interesting anatomical or connectivity pattern, compare neurons, or develop a hypothesis that could be tested in future work.

We hope, from whatever you find, you demonstrate curiosity and thoughtful exploration using the connectomic tools and data. 
:::

---

# Are You Ready?

Before beginning your project, return to [`Expectations: Intro vs Advanced Levels (Track 1)`](expectations_flies.md).

In particular, revisit:

**Stage 1: Fly Connectomics Foundations *(Essential for Everyone)***

and

**Introductory Level (GUI Track)**

Look through the expectations and ask yourself:

**Do I understand these concepts well enough to begin exploring independently?**

Remember, you can always return to these guides when you need them.

If you understand the major concepts and can navigate the tools, you are ready to start exploring.


---


# Where Do We Go Next?

For the **Introductory Track**, you already have the core tools you need.

But we have only scratched the surface of what this connectome contains.

So far, you have mostly explored neurons through **graphical user interfaces (GUIs)**, searching for neurons and examining the results provided by tools such as the Cell Type Explorer and neuPrint.

The next step is to learn how to interact with **neuPrint through its API using Python**.

Instead of examining neurons one at a time, we can use code to query, organize, compare, and analyse large amounts of connectome data. This opens the door to much more complex questions and forms the foundation of the **Advanced Level**.

And this is also worth keeping in perspective: the Male CNS Connectome contains **more than 160,000 neurons and hundreds of millions of synapses**. The examples in these tutorials represent only a tiny fraction of what can be investigated.

There are countless neurons to compare, circuits to trace, connectivity patterns to quantify, and hypotheses to test.

That is why datasets like this are so valuable to the scientific community. A connectome is a **research resource that can support new questions and discoveries for years to come**.

So, whether you continue to the Advanced Track or begin your Introductory project now:

**Pick something that makes you curious, and start exploring.**