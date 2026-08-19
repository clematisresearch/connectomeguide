---
title: "Expectations: Intro vs Advanced Levels (Track 1)"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

This section outlines how the Track 1 resources are organised and what is expected for the **Introductory** and **Advanced** levels.

# The Learning Journey

The Track 1 materials are divided into **two stages**.

## Stage 1: Fly Connectomics Foundations *(Essential for Everyone)*

The first stage introduces the key concepts in synapse-level connectomics, fly brain organization, and web-based exploration tools. It does **not** require any programming experience. Regardless of whether you are completing the Introductory or Advanced pathway, we strongly recommend working through these materials first.

Topics include:

* The motivation behind mapping the fly nervous system at synapse resolution.
* An introduction to the fruit fly (*Drosophila melanogaster*) brain and central nervous system (CNS).
* The concept of **neuropils** (the specialized, synapse-dense brain compartments where neurons communicate).
* The 3D anatomical structure of the fly brain: the Optic Lobes, Central Brain, and Ventral Nerve Cord (VNC).
* Understanding neuron morphology, cell types, superclasses, and neurotransmitter predictions.
* Exploring 3D reconstructions and electron microscopy data using **Neuroglancer**.
* Querying neuron connectivity and synaptic partners using the **neuPrint Web GUI**.

The goal of this stage is to ensure that everyone understands **what connectome data represent** and **how neurons are structured and classified**.

## Stage 2: Advanced Track (API & Computational)

* Use **Python** and the **neuPrint API** to programmatically query the Male CNS connectome dataset, perform computational circuit or network analyses, and write a full scientific research manuscript.

---

# Introductory Level (GUI Track)

The introductory pathway is designed for students who are learning the fundamentals of synapse-level connectomics. The emphasis is on developing scientific curiosity, learning how to navigate real connectomic datasets using graphical interfaces, and interpreting circuit connectivity in light of fly behavior.

By the end of the introductory materials, you should be able to:

* Choose a neuron or cell type of interest from the Male CNS connectome.
* Visualize the neuron in 3D using Neuroglancer.
* Identify the brain regions and neuropils where the neuron branches, receives inputs, and sends outputs.
* Use the neuPrint Web GUI to identify top upstream (input) and downstream (output) synaptic partners.
* Extract quantitative connectivity data (e.g., synapse counts, connection weights, partner cell types).
* Interpret your observations using basic neuroscience concepts and connect them to published research on fly behavior (e.g., vision, navigation, odor learning, motor control).
* Produce clear figures (screenshots from Neuroglancer and connectivity summaries from neuPrint).

For example, you might investigate:

> **How does a visual projection neuron (such as LC10a) receive visual information in the optic lobe and relay signals to downstream target regions in the central brain?**

A suitable project would involve identifying the neuron's body ID, visualizing its 3D arborization across the lobula and central brain target regions in Neuroglancer, extracting its top 5 upstream and top 5 downstream synaptic partners via neuPrint, summarizing the circuit with clear figures, and discussing what role this circuit plays in fly vision or behavior based on the scientific literature.

## Written Report Structure (Introductory Level)

The accompanying report does **not** need to be overly long. The goal is to demonstrate that you can formulate a clear question about a neuron or circuit, navigate the tools correctly, extract and present accurate connectivity data, and interpret your findings thoughtfully.

We recommend a length of approximately **500–1,000 words** (excluding figures and references).

A suggested structure is:

1. **Neuron Overview & Motivation (50–150 words)**
   * Name/type of the neuron or cell type (e.g., `LC10a`, `EPG`, `KCa'b'-ap1`, `DNp01`) and its unique identifier (Body ID).
   * Brief motivation: Why did you choose this neuron? What general behavioral or sensory process is it involved in?

2. **Morphology & Anatomical Projections (150–300 words)**
   * Describe the 3D shape and structure of the neuron.
   * Identify the brain regions / neuropils where the neuron's dendrites receive inputs and where its axon branches project and form outputs.
   * Include at least one 3D visualization figure (screenshot from Neuroglancer) with clear labels.

3. **Synaptic Connectivity & Circuit Partners (200–350 words)**
   * Report the neuron's total input (post-synaptic) and output (pre-synaptic) synapse counts.
   * Identify its top upstream synaptic partners (neurons feeding into it) and top downstream synaptic partners (neurons it sends signals to).
   * Present these partners in a clean table or diagram showing partner cell types, Body IDs, and synapse counts / connection strengths.
   * Highlight any notable circuit motifs.

4. **Functional Interpretation & Literature Context (100–250 words)**
   * Discuss what is known from the neuroscience literature about this neuron or its circuit.
   * Connect your structural findings to the relevant fly behavior (e.g., how the connections support motion detection, spatial navigation, memory formation, or motor execution).
   * Note the predicted neurotransmitter type if known (e.g., cholinergic, GABAergic, glutamatergic).
   * Mention any open questions or hypotheses for future investigation.

5. **Declaration of Generative AI and AI-Assisted Technologies in the Writing Process**
   * Required section heading disclosing any use of GenAI tools (see [Generative AI Policy](../handbook/generative_ai.md)).

6. **References & Citations**
   * Cite the dataset ([Berg et al., 2025](https://www.biorxiv.org/content/10.1101/2025.10.09.680999v2)), tools used (neuPrint, Neuroglancer), and relevant scientific papers cited in your text.

The primary expectation is **accuracy** and biological insight. An exhaustive literature review is not required; rather, we want to see that you can explore a real biological circuit and describe it accurately using appropriate neuroscience concepts.

---

# Advanced Level (Computational / API Track)

The advanced pathway is intended for students who wish to undertake a more complete and independent research project.

Here, you will formulate a research question motivated by the scientific literature, design a computational analysis strategy using the `neuprint-python` API, and interpret your findings within the broader context of current neuroscience research.

Your computational analyses should be driven by a clear biological question. A focused, well-justified, and accurately interpreted analysis is preferable to a complex computational methodology that does not meaningfully address the biological question.

## Written Report Structure (Advanced Level)

For general advice on writing a scientific paper, please refer to the [Writing Guide](../handbook/writing_guide.md).

Below are specific guidelines for **Track 1 (Advanced Level)**.

The advanced report should resemble a concise scientific research manuscript. We recommend a total length of approximately **2,000–4,000 words** (excluding references), although there is no strict word limit.

A suggested structure is:

1. **Abstract (150–250 words)**
   * Concise summary of the research question, computational methods, principal findings, and main biological conclusions.

2. **Introduction (200–800 words)**
   * Introduce the biological background and motivate the research question using relevant literature.
   * State the knowledge gap your project addresses and formulate your specific hypotheses.

3. **Materials and Methods (600–1,200 words)**
   * Describe your study in sufficient detail that another researcher could reproduce your analyses.
   * **Dataset & Server:** Describe the Male CNS connectome dataset (`male-cns:v1.0`) hosted on neuPrint.
   * **Selection Criteria & Filtering / Preprocessing:** State how neurons, cell types, or brain regions of interest were selected and filtered (e.g., synapse count thresholds).
   * **Data Analyses:** Describe any calculations made.

4. **Results (400–800 words)**
   * Present your quantitative findings systematically using clear figures, tables, connectivity heatmaps, and network graphs.
   * Report the key findings clearly before interpreting them in the discussion.

5. **Discussion (400–800 words)**
   * Interpret your findings in relation to your research question and existing neuroscience literature.
   * Discuss how the identified connectivity patterns support biological computations or behavior.
   * Evaluate the limitations of your analysis.
   * Propose future directions or testable experimental hypotheses.

6. **Acknowledgements**
   * Acknowledge any individuals or mentors who provided guidance.

7. **Declaration of Generative AI and AI-Assisted Technologies in the Writing Process**
   * Required section disclosing any GenAI tools used.

8. **References**
   * Full citations for datasets, software, and referenced literature using a consistent style (e.g., APA).

## A Note on Manuscript Structure

The section order above follows the conventional structure:

> **Abstract → Introduction → Materials and Methods → Results → Discussion**

You may also choose the alternative format common in many biology journals:

> **Abstract → Introduction → Results → Discussion → Materials and Methods**

Placing the **Materials and Methods** at the end of the manuscript is common in many scientific journals, particularly in neuroscience and the life sciences. This allows readers to focus on the motivation and findings first, while the methodological details are presented later.

You are welcome to adopt either structure for your report. If this is your first research manuscript, however, we recommend keeping the Materials and Methods before the Results, as it often makes the report easier to read and assess. Regardless of the order you choose, ensure that all methodological details are described clearly enough for another researcher to reproduce your analysis.