---
title: "Guiding Research Questions: Advanced (API) Track"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

# Guiding Research Questions: Advanced (API) Track

For the **Advanced Track**, you will use Python and the **neuPrint API** (`neuprint-python`) to query, manipulate, and analyze connectomic data programmatically from the Male CNS Connectome (`male-cns:v1.0`).

Rather than focusing on a single neuron, advanced projects typically investigate circuit-level, neuropil-wide, or whole-CNS connectivity patterns, testing hypotheses grounded in computational neuroscience, graph theory, or sensory-motor processing.

Below are several curated computational research directions to inspire your project. You are welcome to adapt these prompts or formulate your own independent research question.

---

## Direction 1: Network Graph Topology & Whole-Brain Information Flow

How is the fly nervous system organized to balance local, specialized processing with efficient global communication?

### Potential Analyses:
* Construct directed, weighted adjacency graphs of specific circuit modules or whole-brain networks using `networkx`.
* Compute network metrics: **degree distributions**, **clustering coefficients**, **characteristic path lengths**, **betweenness centrality**, and **small-worldness**.
* Perform **community detection (modularity optimization)** to identify functional subgraphs and compare whether topological clusters align with anatomical neuropil boundaries.
* Investigate "rich-club" organization: Do high-degree hub neurons connect predominantly to one another to form a core communication backbone?

### Guiding Questions:
* Which specific neuron types act as the primary communication hubs between the sensory periphery and central integration centers?
* How does the graph architecture of the insect brain compare with known topological properties of mammalian brain networks?

---

## Direction 2: Mapping Sensory-to-Motor Pathways & Transmission Latency

How do sensory signals from the visual or olfactory systems reach the motor circuits in the Ventral Nerve Cord (VNC)?

### Potential Analyses:
* Trace multi-hop pathways starting from primary sensory projection neurons (e.g., visual LC neurons or olfactory PNs) through central intermediate neuropils (e.g., SMP, LAL, CX) to **Descending Neurons (DNs)** that target the VNC.
* Compute **shortest path lengths** and **effective synaptic connection strengths** across multi-synaptic chains.
* Calculate the **effective number of synaptic hops** required for visual vs olfactory vs mechanosensory stimuli to engage descending motor commands.
* Quantify convergence (multiple sensory modalities feeding into shared premotor hubs) vs divergence (a single sensory feature engaging parallel motor behaviors).

### Guiding Questions:
* Are escape behaviors mediated by shorter synaptic pathways compared to exploratory navigation or courtship behaviors?
* Which central brain neuropils serve as the primary bottlenecks or convergence hubs for multimodal decision-making?

---

## Direction 3: Bilateral Symmetry, Hemispheric Specialization, & Stereotypy

In bilaterally symmetric animals, neural circuits in the left and right hemispheres perform complementary operations. How stereotyped (identical) is the synaptic wiring between the left and right hemispheres?

### Potential Analyses:
* Extract connectivity submatrices for homologous cell types in the left (`_L`) and right (`_R`) hemispheres (e.g., left vs right visual projection neurons or mushroom body output neurons).
* Calculate correlation coefficients (e.g., Pearson's $r$, cosine similarity) between left and right synaptic weight vectors.
* Identify cell types with high bilateral asymmetry: Which circuits exhibit significant left-right differences in synapse number or partner preference?
* Quantify contralateral (cross-hemisphere) vs ipsilateral (same-side) information flow across midline structures (e.g., Central Complex, Subesophageal Zone).

### Guiding Questions:
* What degree of developmental variability exists in synaptic connection counts between symmetric neuron pairs?
* Which circuit pathways rely on strong bilateral cross-inhibition or cross-excitation for spatial orientation and steering?

---

## Direction 4: Neurotransmitter Topography & Excitatory / Inhibitory Balance

Connectome datasets incorporate machine-learning predictions of neurotransmitter identities (e.g., cholinergic, GABAergic, glutamatergic, dopaminergic, octopaminergic).

### Potential Analyses:
* Map the spatial distribution and relative ratio of **excitatory (acetylcholine)** versus **inhibitory (GABA, glutamate)** synapses across different neuropils.
* Test whether sensory input neuropils (e.g., Medulla, Antennal Lobe) differ in their E/I balance compared to associative integration neuropils (e.g., Mushroom Body, Superior Protocerebrum) or motor execution circuits in the VNC.
* Analyze feedforward inhibition motifs: Identify circuits where an excitatory projection neuron simultaneously excites a target neuron and an inhibitory local interneuron that provides delayed inhibition.
* Map the target networks of modulatory neurotransmitters (dopamine and octopamine) to identify which circuits are most susceptible to behavioral state changes (e.g., hunger, arousal, circadian drive).

### Guiding Questions:
* How is balance maintained in recurrent feedback circuits (such as the central complex or mushroom body lobes) to prevent runaway excitation?

---

## Direction 5: Recurring Microcircuit Motifs across Functional Systems

Small subgraphs of 3–4 neurons (motifs) such as **feedforward loops**, **mutual inhibition**, **feedback loops**, and **cross-inhibition** serve as the fundamental building blocks of biological computation.

### Potential Analyses:
* Write graph-search algorithms in Python to enumerate 3-node and 4-node subgraph motifs in specific connectome subgraphs.
* Compare motif frequencies against randomized null-model networks (e.g., degree-preserving randomized graphs).
* Test whether specific computational tasks (e.g., persistent compass activity in the Central Complex vs sparse coding in the Mushroom Body vs directional motion detection in the Optic Lobe) utilize distinct microcircuit motifs.

---

## Recommended Computational Workflow

1. **Set Up Your Environment:** Follow the [Programming Guide](../programming_guide/index.md) and [Dataset and Tools](2-dataset_and_tools.md) to install Python, `neuprint-python`, `pandas`, `numpy`, `networkx`, and `plotly`.
2. **Authenticate:** Obtain your authentication token from the neuPrint web interface and initialize your `Client` object (see [neuPrint API Guide](3a-neuprint_api_guide.md)).
3. **Work Through the Tutorial Notebook:** Complete the [neuPrint API Tutorial Notebook](3b-neuprint_api_guide.ipynb) to master essential query functions (`fetch_neurons`, `fetch_adjacencies`, `fetch_synapse_connections`).
4. **Formulate & Test Hypotheses:** Write modular Python scripts to query, filter, and analyze the connectome data.
5. **Visualize Results:** Generate publication-quality figures using `plotly` or `matplotlib`.
6. **Write Your Manuscript:** Structure your 2,000–4,000 word paper following the [Expectations Guide](expectations_flies.md) and [Written Submission Guide](written_submission_guide.md).
