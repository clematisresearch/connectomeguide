---
title: "Guiding Research Questions: Introductory (GUI) Track"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

# Guiding Research Questions: Introductory (GUI) Track

To help you get started on your Introductory Track project, we have curated a collection of guided research topics inspired by current questions in *Drosophila* neuroscience. 

For the Introductory Track, your goal is to:
1. **Choose a neuron or cell type of interest.**
2. **Visualize its 3D morphology and brain projections** using the [Male CNS Cell Type Explorer](male-cns-cell-type-explorer.md).
3. **Query its top upstream (inputs) and downstream (outputs) synaptic partners** using the [neuPrint Web GUI](4a-neuprint_gui_guide.md).
4. **Connect its wiring pattern to fly behavior** using published neuroscience literature.
5. **Write a 500–1,000 word research commentary** summarizing your findings (see [Expectations](expectations_flies.md)).

You are welcome to choose one of the topics below or formulate your own question!

---

## Topic 1: Visual Motion & Feature Detection in the Optic Lobe

Flies rely on rapid visual processing to dodge swatters, chase mates, and navigate complex environments. Over 60% of the fly brain is devoted to vision in the **Optic Lobes (Lamina, Medulla, Lobula, Lobula Plate)**.

### Example Neurons to Explore:
* **Lobula Columnar (LC) Neurons (e.g., `LC10a`, `LC4`, `LC11`, `LC17`):** Specialized projection neurons that detect visual features (such as small moving targets, looming shadows of predators, or looming obstacles) and send outputs to optic glomeruli in the central brain.
* **Lobula Plate Tangential Cells (LPTCs / HS and VS cells):** Wide-field neurons that detect horizontal and vertical optical flow during flight.
* **Transmedullary (Tm) and Medulla Intrinsic (Mi) Neurons (e.g., `Tm1`, `Tm3`, `Mi1`, `Mi9`):** Interneurons that process local light contrast and motion direction.

### Guiding Questions:
* Which specific layers of the medulla or lobula do this neuron's dendrites receive inputs from?
* Which central brain neuropils (e.g., Anterior Optic Tubercle `AOTU`, Optic Glomeruli `PVLP`) does its axon project to?
* Who are its top 3 upstream synaptic inputs in the visual system, and what sensory signals do they provide?
* Who are its top 3 downstream synaptic outputs? Does it connect to central brain interneurons or descending motor pathways?
* What behavioral response (e.g., escape jump, courtship pursuit, landing) is this neuron known or hypothesized to trigger?

---

## Topic 2: Navigation & Heading Compass in the Central Complex

The fly maintains an internal "compass" that tracks which way its body is facing relative to external landmarks. This navigation system is housed in the **Central Complex (EB, FB, PB, NO)**.

### Example Neurons to Explore:
* **EPG Ring Neurons (`EPG`):** The core "compass neurons" of the Ellipsoid Body (EB) that maintain a single bump of neural activity representing heading angle.
* **P-EN Neurons (`P-EN1`, `P-EN2`):** Neurons that update the heading bump when the fly turns left or right using angular velocity signals.
* **Delta7 Neurons (`Delta7`):** Inhibitory interneurons in the Protocerebral Bridge (PB) that sharpen the compass signal.
* **Fan-shaped Body Layer Neurons (e.g., `FB4r`, `FB6a`):** Neurons that integrate heading with goal orientation and flight speed.

### Guiding Questions:
* How is this neuron arranged in the 3D structure of the central complex (e.g., ring-shaped in the EB vs columnar in the FB/PB)?
* What upstream neurons feed self-motion (proprioceptive) or visual landmark information into this neuron?
* Does this neuron form reciprocal or recurrent feedback connections with other compass neurons?
* What downstream target neurons or motor steering hubs (e.g., Lateral Accessory Lobe `LAL`) does it connect to?

---

## Topic 3: Associative Learning & Memory in the Mushroom Body

How does a fly learn that a specific odor is paired with a sugary reward or an electric shock? This associative learning happens in the **Mushroom Body (MB)**.

### Example Neurons to Explore:
* **Kenyon Cells (e.g., `KCapbp-ap1`, `KCg-m`, `KCab`):** Intrinsic neurons of the mushroom body that encode sparse representations of odors and visual features.
* **Dopaminergic Neurons (DANs / PPL1 or PAM cluster, e.g., `DAN-PPL1-01`):** Modulatory neurons that convey punishment or reward signals to specific compartments of the mushroom body lobes.
* **Mushroom Body Output Neurons (MBONs, e.g., `MBON01`, `MBON11`):** Output neurons that read out the learned valence and drive approach or avoidance behaviors.

### Guiding Questions:
* Where do this neuron's dendrites receive synaptic inputs (e.g., Calyx vs specific lobe compartments)?
* What upstream projection neurons or modulatory dopaminergic neurons connect to it?
* What downstream premotor or central brain targets receive output from this cell?
* How does the neurotransmitter of this neuron (e.g., cholinergic excitation vs GABAergic inhibition) shape learning or memory recall?

---

## Topic 4: Descending Motor Control from Brain to Body

All behavioral decisions made in the brain must eventually be transmitted to the **Ventral Nerve Cord (VNC)** to execute physical movement through the legs, wings, and abdomen.

### Example Neurons to Explore:
* **Descending Neurons (DNs, e.g., `DNp01`, `DNa01`, `DNb01`, `MDN`):** Giant command fibers that extend from the central brain through the neck connective into the thoracic neuromeres of the VNC.
* **Moonwalker Descending Neuron (`MDN`):** A famous descending neuron that causes the fly to walk backward when activated.
* **Giant Fiber Neuron (`GF`):** A massive escaping-triggering descending neuron that mediates rapid jump-and-flight responses.

### Guiding Questions:
* Which central brain neuropils (e.g., Lateral Accessory Lobe `LAL`, Superior Protocerebrum `SMP`, Subesophageal Zone `SEZ`) provide synaptic input to this descending neuron?
* Which segments of the VNC (T1 front legs, T2 wings/middle legs, T3 hind legs, or ANm abdomen) do its axon terminals reach?
* Who are its top downstream motor or premotor partners in the VNC?
* How does this connectivity allow the brain to switch, initiate, or steer movement?

---

## Topic 5: Innate Olfactory & Gustatory Processing

Some smells and tastes trigger automatic, hardwired behaviors (e.g., fleeing from carbon dioxide, feeding on sucrose, or avoiding bitter toxins) without requiring prior learning.

### Example Neurons to Explore:
* **Lateral Horn Neurons (LHNs, e.g., `LHAD1b1`, `LHMB1`):** Neurons in the Lateral Horn that receive direct odor input from projection neurons.
* **Antennal Lobe Local Interneurons (`LN`):** Inhibitory interneurons that mediate cross-talk between olfactory glomeruli.
* **Subesophageal Zone Gustatory Interneurons:** Neurons in the SEZ that process sweet, bitter, or pheromonal tastants.

### Guiding Questions:
* Which specific glomeruli or projection neuron cell types provide synaptic input to this cell?
* Does this neuron receive input from multiple sensory modalities (e.g., combining odor and visual cues)?
* Where does it send its outputs, and what innate behavioral action does it mediate?

---

## How to Structure Your Investigation

1. **Pick one topic and choose 1–2 specific neurons.**
2. **Look up the Body ID** in [neuPrint](https://neuprint.janelia.org) (`male-cns:v1.0`).
3. **Open the 3D view** in the [Male CNS Cell Type Explorer](male-cns-cell-type-explorer.md) and take clean screenshots.
4. **Extract the top 5 upstream and top 5 downstream partner tables** from neuPrint.
5. **Search Google Scholar or PubMed** for papers discussing your neuron/circuit (e.g., search `"LC10a Drosophila"` or `"EPG neurons fly navigation"`).
6. **Write your 500–1,000 word commentary** following the structure outlined in the [Expectations Guide](expectations_flies.md).
