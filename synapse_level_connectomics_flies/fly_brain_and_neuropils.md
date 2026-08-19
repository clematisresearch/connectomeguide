---
title: "An Introduction to Fly Brain Anatomy and Neuropils"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

# An Introduction to Fly Brain Anatomy and Neuropils

Welcome to the world of fly connectomics! To explore and analyze real connectomic datasets effectively, it helps to understand how the fruit fly (*Drosophila melanogaster*) nervous system is organized.

Although a fruit fly's brain is roughly the size of a poppy seed, it contains over **140,000–160,000 neurons** and more than **50 million synaptic connections**. Within this compact nervous system lies an extraordinary computational capacity that allows the fly to dodge swatters, navigate toward odors, perform intricate courtship rituals, remember experiences, and control agile flight.

This guide provides a step-by-step introduction to the fundamental building blocks of the nervous system: from basic neuron anatomy and synapses to the concept of **neuropils**, the 3D organization of the fly brain, and how neurons are classified into cell types.

---

## 1. Basic Neuron Anatomy

Neurons are the fundamental building blocks of the brain and nervous system. They are specialized cells that receive, process, and transmit electrical and chemical signals.

```{figure} ../static/neuron_anatomy.png
:alt: Basic Neuron Anatomy
:width: 650px
:align: center

**Figure 1: Basic anatomy of a neuron.** A schematic highlighting the key structural components of a neuron: dendrites (inputs), cell body/soma (signal integration & nucleus), axon (conduction), and axon terminals (synaptic outputs). Adapted from Khan Academy.
```

While neurons vary considerably in shape and size, they typically have three main functional compartments:

1. **Dendrites (Inputs):**  
   Branch-like arborizations that receive signals from other neurons. Think of dendrites as the "input side" (postsynaptic side) of the neuron.
2. **Cell Body / Soma (Metabolic & Genetic Center):**  
   Contains the cell nucleus and metabolic machinery. It integrates incoming signals and maintains the cell.
3. **Axon (Conduction):**  
   The axon is a long, thin projection that carries electrical impulses away from the cell
body to other neurons, muscles, or glands. Some axons are wrapped in a fatty layer
called myelin, which helps speed up signal transmission.
4. **Axon Terminals (Outputs):**  
   The branched ends of the axon that form specialized contact points, called **synapses**, with the dendrites or cell bodies of other neurons.

At the end of the axon are axon terminals, which connect to the dendrites or cell bodies of
other neurons through tiny gaps called synapses. This is where communication between
two neurons happens.

* The neuron sending the signal is called the pre-synaptic neuron.
* The neuron receiving the signal is called the post-synaptic neuron.

---

## 2. Neurotransmitters & Neuromodulators

Signals across the synaptic cleft are transmitted by chemical messengers called **neurotransmitters**. When an action potential reaches the presynaptic terminal, neurotransmitters are released into the synaptic cleft and bind to **receptors** on the postsynaptic cell:

1. **Excitatory Neurotransmitters:**  
   Increase the likelihood that the postsynaptic neuron will fire an action potential.  
   * **Acetylcholine (Cholinergic):** The primary fast excitatory neurotransmitter in the insect central nervous system (in contrast to mammals, where glutamate is the primary excitatory transmitter).
2. **Inhibitory Neurotransmitters:**  
   Decrease the likelihood that the postsynaptic neuron will fire, stabilizing circuits and preventing runaway excitation.  
   * **GABA (GABAergic):** The major fast inhibitory neurotransmitter.  
   * **Glutamate (Glutamatergic):** In humans, glutamate is the primary excitatory transmitter. However, in the insect central brain, its polarity is **context-dependent and can be ambiguous**. It frequently acts as an **inhibitory** neurotransmitter, but can also act as an **excitatory** neurotransmitter.
3. **Neuromodulators:**  
   Chemicals that broadly modulate how circuits respond to inputs, regulating behavioral states, motivation, learning, and arousal:  
   * **Octopamine (Octopaminergic):** The insect analog of norepinephrine/adrenaline, promoting alertness, flight arousal, and reward signaling.  
   * **Dopamine (Dopaminergic):** Mediates reward and punishment signals during associative learning in the mushroom body.  
   * **Serotonin (Serotonergic):** Regulates sleep, feeding, aggression, and circadian rhythms.

---

## 3. What is a Neuropil?

You have learned that a neuron has different parts: a **cell body (soma)**, **dendrites**, and an **axon**. Neurons communicate with one another at **synapses**, where one neuron can pass a signal to another.

But where are all of these parts located in the brain?

In the insect brain, they are organized in a particularly interesting way. Most neuronal **cell bodies are located around the outside of the brain**, forming a layer called the **cell body rind** (or cortex).

Their branches extend inward into regions called **neuropils**.

A **neuropil** is a region packed with the branching processes of many neurons—especially their dendrites and axons—and the **synapses that connect them**. Unlike the outer cell body rind, neuropils contain very few or no neuronal cell bodies.

You can therefore think of the insect brain as having:

* an **outer region**, where most neuronal cell bodies are located; and
* an **inner region of neuropils**, where neurons extend their branches and form connections with other neurons.

Importantly, the inside of the brain is not just one large neuropil. It is divided into many **distinct neuropils**, each containing particular groups of neurons and connections. Different neuropils are associated with different kinds of information processing.

For example, some neuropils are involved in processing **visual information**, while others are involved in **smell, navigation, or movement**.

As we explore the connectome, neuropils will therefore give us a useful way to ask not only **which neurons connect to each other**, but also **where in the brain those connections occur**.


```{figure} ../static/cortex-neuropil-fly.jpeg
:alt: Fly Brain Overview
:width: 500px
:align: center

**Figure 2: Organization of the Drosophila Central Nervous System.** Schematic showing the organization of the fly central nervous system into **neuropil regions** (blue), surrounded by the **cortex or cell body rind** (gray), with **tract regions** (dark blue) connecting different parts of the nervous system. Adapted from https://doi.org/10.1002/glia.23115.
```

---

## 4. The Three Major Divisions of the Fly Central Nervous System (CNS)

The fly Central Nervous System is divided into three primary anatomical components (see Figure 2 above):

1. **The Optic Lobes (OL)**
2. **The Central Brain (CB)**
3. **The Ventral Nerve Cord (VNC)**

---

### A. The Optic Lobes (Vision)

Vision is the fly's largest sensory modality. **More than half of all neurons** in the fly brain reside in the optic lobes!

```{figure} ../static/optic_lobe_schematic.png
:alt: Optic Lobe Schematic
:width: 600px
:align: center

**Figure 3: Schematic of the Drosophila Optic Lobe.** Visual signals captured by photoreceptors in the retina pass sequentially through four neuropils: the Lamina, Medulla, Lobula, and Lobula Plate, before projecting to the central brain. The retina, lamina, and medulla process information sequentially, while information from the medulla splits into the lobula and lobula plate. Reproduced from https://doi.org/10.1016/j.ydbio.2013.04.007.
```

The fly views the world through two large **compound eyes**, each composed of approximately **800 individual optical units called ommatidia**. Each ommatidium functions like a single pixel, containing its own lens and 8 light-sensing **photoreceptor cells**:
* **R1–R6 (Outer Photoreceptors)** respond to a broad range of light
* **R7 & R8 (Inner Photoreceptors):** respond more specifically to UV and blue light.

Once light hits the photoreceptors, the visual signal is passed through four layers of the fly’s brain, called neuropils, in an organized way akin to passing a message down a line. 

The first neuropil is the lamina, where signals from R1–R6 connect to L1–L3 neurons. Each small part of the eye sends information to a matching column in the brain, keeping the visual "map" in order. This organization is called **retinotopy**, meaning the layout of what the fly sees is preserved throughout its brain. 

Next, the signal moves to the **medulla**, and then to the **lobula complex**, which includes the **lobula** and **lobula plate**. Finally, the information is sent to the central brain, where information can be further processed. 

What’s really cool about the optic lobe connectome we’ll be using is that this retinotopic map is computationally tracked across all layers, from the lamina to the deeper brain regions. Each column is given a **unique “address”** that represents its location in the fly’s visual space. This makes it much easier to tell different neurons apart and helps us explore the connectome data in a way that’s clear and user-friendly.

#### The Four Sequential Optic Neuropils

Once light reaches the photoreceptors, the visual signal does not travel directly to the central brain. Instead, it passes through a series of specialized **neuropils**, where the information is processed and transformed along the way.

In the fly's visual system, the pathway can be simplified as:

**Retina → Lamina → Medulla → Lobula and Lobula Plate → Central Brain**

You can think of this as passing a message through a series of processing stations. Each neuropil contains many neurons that receive information from the previous stage and pass processed information to the next.

The first neuropil is the **lamina (LA)**. It receives direct input from the outer photoreceptors (R1–R6). From the lamina, information is passed to the **medulla (ME)**, where it undergoes further processing.

From the medulla, the visual pathway splits into two neuropils that together form the **lobula complex**:

* **Lobula (LO)**
* **Lobula Plate (LOP)**

Information from these regions is then sent onward to the **central brain**, where visual information can be combined with other information and processed further.

You do not need to memorize every neuron or connection in this pathway yet. The important idea is that **visual information is processed progressively as it moves through a series of interconnected neuropils**.

#### Retinotopic Organization

There is another important feature of the fly's visual system: it preserves information about **where something appeared in the visual field**.

Each compound eye contains approximately **800 ommatidia**, which you can think of as many small sampling points across the fly's visual field. Information from neighbouring parts of the visual field is sent to neighbouring regions of the optic lobe.

This organization is called **retinotopy**. In simple terms, the spatial arrangement of the visual world is preserved as visual information moves through the optic lobe.

For example, two objects that appear next to each other in the fly's visual field will tend to be represented by nearby columns in the optic lobe. These corresponding regions can be followed across the lamina, medulla, and lobula complex.

This organization is particularly useful when exploring the fly connectome. Rather than treating the optic lobe as an unstructured collection of neurons, we can use the spatial organization of the visual system to understand where different neurons and connections are located.

In the optic lobe dataset used in this competition, these locations are represented using **columnar coordinates**, giving neurons and their branches a kind of spatial "address." This allows us to track how visual information is organized across different neuropils.

#### Types of Neurons in the Optic Lobe

So far, we have looked at the **regions** through which visual information travels. We can also classify the neurons themselves according to where they are located and how they connect these regions.

The neurons in the fly's optic lobe can be grouped into four main categories (Figure 4):

* **Optic Lobe Intrinsic Neurons** remain within a single optic lobe neuropil.
* **Optic Lobe Connecting Neurons** connect different neuropils within the optic lobe.
* **Visual Projection Neurons** carry visual information from the optic lobe to the **central brain**.
* **Visual Centrifugal Neurons** travel in the opposite direction, carrying signals from the **central brain back to the optic lobe**.

```{figure} ../static/optic_lobe_neuron_types.png
:alt: Visual Neuron Types
:width: 600px
:align: center

**Figure 4: Categories of neurons in the fly visual system.** Visual neurons are categorized into intrinsic neurons (within one neuropil), connecting neurons (linking visual neuropils), projection neurons (sending visual outputs to the central brain), and centrifugal neurons (providing signals from the central brain back to the optic lobe). Reproduced from FlyEM, Janelia Research Campus.
```

The scale and diversity of this system are remarkable. In total, the optic lobe contains:

* nearly **16,000 intrinsic neurons** across around **150 different types**;
* around **32,000 connecting neurons** from over **90 types**;
* about **4,500 projection neurons** belonging to over **350 types**; and
* more than **280 centrifugal neurons** spanning over **100 types**.

Together, these different neurons form the circuits that allow visual information to be processed within the optic lobe, transmitted to the central brain, and influenced by signals returning from the central brain.


---

### B. The Central Brain (Sensory Integration, Learning, & Navigation)

We have just seen that the **optic lobes** contain a series of neuropils specialized for processing visual information.

But visual information is only one part of what the fly's nervous system needs to process. A fly also smells and tastes its environment, learns from experience, keeps track of its direction, and uses all of this information to guide its behaviour.

Much of this processing takes place in the **central brain**, located between the two optic lobes.

Just like the optic lobes, the central brain is not one uniform structure. It is divided into many **neuropils**, containing different groups of neurons and connections. Some of these neuropils are particularly well studied and have been associated with functions such as **olfaction, learning and memory, navigation, and movement**.

```{figure} ../static/neuropils-guide-flywire.jpg
:alt: Guide to neuropils of the adult Drosophila brain
:width: 750px
:align: center

**Figure 5: Neuropils of the Adult Drosophila Brain.** Neuropils are shown grouped into major anatomical regions, including the optic lobe, central complex, mushroom body, antennal lobe, lateral horn, and several regions of the protocerebrum. Figure from the [FlyWire Codex Neuropil Guide](https://codex.flywire.ai/app/neuropils?dataset=fafb), based on the Female Adult Fly Brain (FAFB) connectome.
```

Figure 5 may look complicated at first—and that is okay! You do **not** need to memorize all of these neuropils or their abbreviations.

Instead, we will focus on a few important examples to understand how different parts of the central brain contribute to different functions.

:::{tip} Want to learn more?
For a more detailed overview of the anatomy and functions of the *Drosophila* brain, see the **“Major brain structures”** section of [this review](https://www.sciencedirect.com/science/article/pii/S2666515825000083#sec0003).
:::

The review covers many of the structures introduced below and is a useful starting point if you want to explore a particular brain region in more depth.

#### 1. Antennal Lobes (AL): Processing Smell

Let's begin with another sensory system.

Odor molecules are detected by **olfactory receptor neurons** associated with the fly's antennae. These neurons carry information into a pair of structures in the central brain called the **antennal lobes (AL)**.

The antennal lobes are the fly's **primary olfactory processing centers**.

Within each antennal lobe are many small compartments called **glomeruli**. Olfactory receptor neurons detecting particular kinds of odors converge onto these glomeruli, where they connect with other neurons.

From the antennal lobe, **projection neurons (PNs)** carry olfactory information deeper into the brain, including to two important regions:

* the **mushroom body**, which is strongly involved in learning and memory; and
* the **lateral horn**, which is particularly important for innate responses to odors.

So, in simplified form:

**Odor → Olfactory receptor neurons → Antennal lobe → Mushroom body and Lateral horn**

#### 2. Mushroom Bodies (MB): Learning & Memory

The **mushroom bodies (MB)** are among the most extensively studied structures in the fly brain and play important roles in **learning and memory**.

Each mushroom body contains approximately **2,000–2,500 intrinsic neurons called Kenyon cells (KCs)**.

The mushroom body itself contains several anatomically distinct regions. The **calyx (CA)** is an important input region, where Kenyon cells receive sensory information. Their axons then travel through the **pedunculus (PED)** and form the characteristic mushroom body **lobes**.

```{figure} ../static/mushroom-body-janelia.jpg
:alt: Mushroom Body Anatomy
:width: 750px
:align: center

**Figure 6: Anatomy of the Drosophila mushroom bodies.** 3D reconstruction showing the bilateral mushroom bodies within the fly brain. Each mushroom body includes the **calyx**, where Kenyon cells receive sensory inputs, and the **α, α′, β, β′, and γ lobes**, formed by the projections of Kenyon cell axons. The **dorsal and ventral accessory calyces**, additional input regions of the mushroom body, are also shown. Reproduced from the [Rubin Lab, HHMI Janelia](https://www.janelia.org/lab/rubin-lab/our-research/anatomical-and-behavioral-analyses-brain-areas/learning-and-memory).
```

Within these circuits, experience can change how sensory information influences behaviour. For example, a fly can learn that a particular odor predicts something rewarding or unpleasant and subsequently change its response to that odor.

Two other neuron classes you may encounter when exploring mushroom body circuits are:

* **Dopaminergic neurons (DANs)**, which provide signals important for learning and reinforcement; and
* **Mushroom body output neurons (MBONs)**, which carry information out of mushroom body compartments and help influence behaviour.

For now, the main idea is:

**The mushroom body helps the fly use previous experience to change how it responds to sensory information.**

#### 3. Lateral Horn (LH): Innate Responses to Odors

Remember that olfactory projection neurons can carry information from the antennal lobe to both the **mushroom body** and the **lateral horn (LH)**.

These two pathways illustrate an important distinction.

The mushroom body is strongly associated with **learned associations**. The lateral horn, in contrast, is particularly associated with **innate or unlearned responses to odors**.

For example, some odors may naturally signal attractive or potentially dangerous things in the environment without the fly first having to learn their significance.

This gives us a useful simplified comparison:

**Mushroom body → learned associations**

**Lateral horn → innate odor-related responses**

The real circuits are more complicated than this distinction, but it provides a useful starting point for understanding the two regions.

#### 4. Central Complex (CX): Navigation & Movement

Another major system within the central brain is the **central complex (CX)**.

Unlike the optic lobe or antennal lobe, which are strongly associated with processing particular sensory modalities, the central complex brings together different kinds of information to help the fly **orient itself, navigate through its environment, and control movement**.

The central complex is composed of four major neuropils:

* **Protocerebral Bridge (PB)**
* **Ellipsoid Body (EB)**
* **Fan-shaped Body (FB)**
* **Noduli (NO)**

```{figure} ../static/cx-janelia-depiction.jpg
:alt: Anatomy and neurons of the Drosophila central complex
:width: 750px
:align: center

**Figure 7: The Drosophila Central Complex.** The central complex consists of four interconnected neuropils: the **protocerebral bridge (PB)**, **ellipsoid body (EB)**, **fan-shaped body (FB)**, and paired **noduli (NO)**. The schematic on the left shows their relative anatomical positions, while the image on the right shows examples of neurons innervating the central complex. Reproduced from the [Rubin Lab, HHMI Janelia Research Campus](https://www.janelia.org/lab/rubin-lab/research/anatomical-and-behavioral-analyses-of-brain-areas/sensory-integration-the).
```

Together, circuits within these structures allow the fly to combine sensory information with information about its own movement and orientation. The central complex has been implicated in functions including **motor control and planning, orientation, and spatial navigation**.

One particularly fascinating example is the fly's sense of **direction**.

Within the **ellipsoid body**, a population of neurons called **EPG neurons** helps represent the direction in which the fly is facing. Rather than a single EPG neuron acting as a compass, the activity of the population forms a localized **"bump" of neural activity** around the ellipsoid body.

As the fly turns, this activity bump moves around the ellipsoid body with it. In this way, the position of the bump can represent the fly's current **heading direction**.

You can think of this as part of an **internal compass**: the fly's nervous system maintains an internal representation of which direction it is facing as it moves through the world.

:::{tip} See the Fly's Internal Compass in Action
The following video provides a useful visualization of how activity in the fly's central complex can represent its heading direction:

```{iframe} https://www.youtube.com/embed/nu0b_tjCGxQ
:width: 100%
```
:::



#### 5. Other Central Brain Neuropils

The antennal lobes, mushroom bodies, lateral horn, and central complex are useful examples, but Figure 5 shows that they represent only part of the central brain.

Many other neuropils contribute to sensory integration and behaviour.

For example, the **lateral accessory lobes (LAL)** receive and integrate information from systems including the central complex and mushroom body and are involved in coordinating movement.

The **posterior slope (PS)** contains circuits associated with motor control, including flight-related behaviours.

Near the base of the brain are the **periesophageal neuropils (PENP)**, which integrate several forms of sensory information. These include the **antennal mechanosensory and motor centre (AMMC)**, which processes mechanosensory information from the antennae.

The **gnathal ganglia (GNG)** are particularly important for processing **taste (gustatory) information and feeding-related behaviours**. The GNG, together with parts of the periesophageal neuropils, forms part of a broader region called the **subesophageal zone (SEZ)**.

The SEZ also provides an important interface between the brain and the **ventral nerve cord**, which we will explore next.

#### Putting It Together

The central brain therefore contains many interconnected neuropils rather than a single general-purpose processing center.

A useful starting point is to remember a few examples:

* **Antennal lobes → smell**
* **Mushroom bodies → learning and memory**
* **Lateral horn → innate odor-related responses**
* **Central complex → navigation and movement**
* **GNG / SEZ → taste, feeding, and sensorimotor processing**

These labels are useful landmarks when exploring a connectome. If you find that a neuron sends branches or forms synapses within one of these neuropils, you immediately gain a clue about the kinds of circuits in which that neuron might participate.

As you explore the connectome, however, remember that **a neuron's function cannot be determined from its location alone**. Many neurons span multiple neuropils, allowing information to move between different parts of the brain.

##### How Much of the Fly Brain Can You Recognize Now?

Let's finish by taking a step back and looking at the nervous system as a whole.

```{figure} ../static/drosophila-complete-overview.jpg
:alt: Cellular and circuitry overview of the adult Drosophila central nervous system
:width: 750px
:align: center

**Figure 8: Cellular and Circuitry Overview of the Adult Drosophila Central Nervous System.** This overview brings together several levels of organization in the fly nervous system, from major brain neuropils and the ventral nerve cord to neurons, glia, synapses, and sensory-to-motor circuits. It also highlights several additional topics, including neuropeptide circuits and sexually dimorphic *fruitless*-expressing neurons. Figure reproduced from [Akin et al. (2025)](https://www.sciencedirect.com/science/article/pii/S2666515825000083).
```

At first glance, Figure 8 might look complicated. But after working through this guide, you should already recognize many of its major features.

For example, see if you can find:

* the **optic lobes** and their major neuropils: lamina, medulla, lobula, and lobula plate;
* the **mushroom bodies** and **central complex**;
* the distinction between **neuronal cell bodies (somata)** and the **neuropil**;
* a **synapse**, including its presynaptic and postsynaptic sides;
* pathways carrying **visual and olfactory information** through the brain; and
* the **ventral nerve cord (VNC)** extending from the brain into the body.

If you can recognize these features and understand broadly what they represent, you have already built a useful anatomical framework for exploring the fly connectome.

There are also several things in the figure that we have **not** covered, such as the different classes of **glia**, **neuropeptide circuits**, and ***fruitless*-expressing neurons**. Don't worry about these for now. The goal is not to memorize every structure, cell type, or abbreviation in the fly nervous system.

Instead, the important thing is to have a mental map: **neurons connect at synapses, synapses are concentrated within neuropils, different neuropils form specialized brain regions, and neurons connecting these regions together form the circuits underlying sensation, learning, navigation, and behaviour.**

With that foundation, we are ready to move beyond individual brain regions and start thinking about how the **connectome** captures these neurons and connections as a whole.


---

### C. The Ventral Nerve Cord (VNC — Motor Control)

The competition focuses primarily on the **brain**, rather than the VNC, but it is useful to understand where the VNC fits into the fly's nervous system.

The **Ventral Nerve Cord (VNC)** is roughly analogous to the vertebrate spinal cord and contains circuits that control much of the fly's movement and process sensory information from the body.

* **Cervical Connective (Neck):** Connects the brain and VNC. **Descending neurons (DNs)** carry signals from the brain toward the VNC, while **ascending neurons (ANs)** carry information from the VNC toward the brain.
* **Prothoracic Neuromere (T1):** Primarily associated with the **front legs**.
* **Mesothoracic Neuromere (T2):** Primarily associated with the **middle legs and wings**.
* **Metathoracic Neuromere (T3):** Primarily associated with the **hind legs and halteres**, which contribute to balance during flight.
* **Abdominal Neuromeres:** Contain circuits controlling the **abdomen and reproductive organs**.

Together, the brain and VNC allow sensory information, internal goals, and motor commands to be transformed into coordinated behaviour.


---

## 5. From Individual Neurons to Cell Types

So far, we have talked about neurons as individual cells. But a whole-brain connectome contains **more than 160,000 neurons**!

If every neuron were treated as completely unique, understanding such a large dataset would quickly become overwhelming. Fortunately, many neurons share similar anatomical and connectivity patterns. Connectomics therefore organizes neurons into **cell types** and broader groups.

### A. Individual Neurons

Let's start with a single neuron.

In a connectome dataset, every reconstructed neuron needs a way to be uniquely identified. It is therefore assigned a unique identifier, often called a **Body ID**.

For example:

`Body ID: 10378`

Think of a Body ID like an **ID number for one particular neuron**. Two individual neurons may look very similar, but they will still have different Body IDs.

### B. What is a Cell Type?

Now imagine that we find several neurons with very similar shapes, locations, and patterns of connectivity.

Rather than treating each as an entirely unrelated neuron, researchers can classify them as belonging to the same **cell type**.

Examples of cell-type names you may encounter include:

* `L2`
* `LC10a`
* `EPG`
* `KCapbp-ap1`

A **cell type is therefore a group of neurons that share important biological characteristics**, such as their anatomy and connectivity.

Importantly, a cell type does **not** necessarily refer to just one neuron. There can be many individual neurons belonging to the same cell type.

For example, **L2** is a cell type in the fly visual system. There are hundreds of individual L2 neurons arranged across the optic lobe. Each is a separate neuron, but because they share characteristic anatomical and connectivity features, they are all classified as the same **L2 cell type**.

```{figure} ../static/L2-693neurons.png
:alt: 693 L2 neurons in the Drosophila optic lobe
:width: 750px
:align: center

**Figure 9: 693 L2 columnar neurons from the fly optic lobe.** Each colored structure is an **individual neuron**, but all 693 neurons belong to the same **L2 cell type**. The neurons are repeated across the columns of the optic lobe, allowing the same type of neuron to process information from different locations in the fly's visual field. Reproduced from https://www.youtube.com/watch?v=fWW0gQlut9U 
```

This is particularly common in the visual system. Remember the **retinotopic organization** we discussed earlier: the optic lobe contains many repeated columns representing different locations in visual space. A particular cell type can therefore have many individual neurons distributed across these columns.

Cataloguing cell types based on connectivity is one way to group neurons into meaningful categories. However, defining what exactly makes a **cell type** has been a long-standing challenge. Neurons can differ in many ways, including their **molecular profiles, morphology, electrical properties, and functional responses**. Understanding how these different features can be used to define cell types is an entire field of research.

:::{important}

### Individual Neuron ≠ Cell Type

A **Body ID** identifies **one individual neuron**.

A **cell type** is a category that can contain **multiple individual neurons**.

For example, each of the 693 L2 neurons shown in Figure 9 is a different individual neuron with its own identity, but they all belong to the same `L2` cell type.

This distinction will become very important when you start exploring connectome data. Sometimes you will want to investigate **one particular neuron**, while at other times you may want to investigate **all neurons belonging to a particular cell type**.
:::

### C. Superclasses: Broader Groups of Neurons

Individual neurons can be grouped into **cell types**, but we can also organize neurons into even broader categories.

In the connectome datasets and tools you will use, you may see the term **superclass**. A superclass groups together many neurons and cell types that share broad anatomical or functional characteristics.

For example, neurons can belong to broad groups such as:

* **Sensory Neurons:** Carry information from sensory organs, such as the eyes or antennae, into the nervous system.
* **Local / Intrinsic Neurons:** Primarily connect neurons within a particular brain region or neuropil.
* **Projection Neurons:** Carry information between different brain regions.
* **Descending Neurons (DNs):** Carry information from the brain down toward the **ventral nerve cord (VNC)**.
* **Ascending Neurons (ANs):** Carry information from the VNC upward toward the brain.
* **Motor Neurons (MNs):** Send signals from the nervous system to muscles.

You have actually encountered several examples already. **Kenyon cells** are intrinsic neurons of the mushroom body, **olfactory projection neurons** carry information away from the antennal lobe, and **descending neurons** provide one route through which activity in the brain can influence circuits in the VNC.

So, as a simple way to think about the different levels:

**Individual neuron (Body ID) → Cell type → Superclass**

For example, many individual neurons can belong to the same cell type, and multiple related cell types can fall within a broader superclass.

You do not need to memorize the different superclasses. The important thing is to recognize the term when you encounter it in **Neuroglancer or other connectome tools** and understand that it provides a broader way of grouping neurons.

## Next Steps

You now have the basic anatomical vocabulary needed to start exploring the fly connectome yourself.

Next, you can:

* Learn how to explore cell types and 3D neurons in the [Male CNS Cell Type Explorer](male-cns-cell-type-explorer.md).
* Learn how to search for neurons and their synaptic partners in the [neuPrint GUI Guide](4a-neuprint_gui_guide.md).
