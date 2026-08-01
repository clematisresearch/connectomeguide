---
title: "Expectations: Intro vs Advanced Levels (Track 2)"
authors:
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
---

This section outlines how the Track 2 resources are organised and what is expected for the **Introductory** and **Advanced** levels.

# The Learning Journey

The Track 2 materials are divided into **two stages**.

## Stage 1: Neuroimaging Foundations *(Essential for Everyone)*

The first stage introduces the key concepts in human neuroimaging and does **not** require any programming experience. Regardless of whether you are completing the Introductory or Advanced pathway, we strongly recommend working through these materials before doing the tutorial codebook.

Topics include:

* The motivation behind studying the human brain at the macroscale.
* An introduction to human neuroimaging techniques, with a particular focus on resting-state fMRI.
* The neuroimaging analysis workflow, from data acquisition to statistical analysis.
* The LEMON dataset used for the competition.
* Brain parcellation, brain atlases, and resting-state networks.
* Brain timeseries and functional connectivity.

The goal of this stage is to ensure that everyone understands **what the data represent**, **how they were generated**, and **what the analyses mean**, before writing any code.

## Stage 2: Programming Tutorials

The second stage consists of hands-on programming tutorials, where you will analyse the LEMON dataset using Python.

This is where the expectations begin to differ between the **Introductory** and **Advanced** pathways. The analyses you perform, as well as the accompanying written report, should reflect the level that you are attempting.

The tutorial codebook will be clearly labeled as either `(Introductory)` or `(Advanced)`.

---

# Introductory Level

The introductory pathway is designed for students who are learning the fundamentals of neuroimaging data analysis. The emphasis is on understanding the complete workflow—from loading the data to interpreting the results—rather than performing sophisticated statistical analyses.

By the end of the introductory tutorials, you should be able to:

* Load and visualise resting-state fMRI data.
* Calculate functional connectivity (FC) matrices.
* Compute simple brain measures (e.g., mean functional connectivity within a network).
* Compare brain measures across groups or examine simple relationships with phenotypes.
* Produce appropriate figures (e.g., bar plots or scatter plots).
* Interpret your findings using appropriate neuroscience terminology.

For example, you might investigate the following question:

> **Do older adults exhibit different mean Default Mode Network (DMN) functional connectivity compared with younger adults?**

A suitable analysis could involve dividing participants into younger and older adults, calculating each participant's mean DMN connectivity, comparing the group averages, visualising the results with a bar plot, and discussing the findings.

## Written Report

The accompanying report does **not** need to be long. The goal is to demonstrate that you can formulate a research question, perform an appropriate analysis correctly, and interpret the results accurately. There is no strict word limit, although approximately **500–1,000 words** is likely to be sufficient.

A suggested structure is:

1. **Introduction (50–150 words)**
   Briefly explain what motivated the question. This may be inspired by previous literature or by your own scientific curiosity.

2. **Research Question and Hypothesis (50–150 words)**
   Clearly state the relationship you wish to investigate and, if appropriate, your hypothesis.

3. **Methods / Analysis Strategy (200–400 words)**
   Describe:

   * your independent and dependent variables,
   * how participants or groups were defined,
   * how the brain measure was calculated,
   * and any statistical analyses that were performed.

4. **Results (100–200 words)**
   Present your main findings and include appropriate figures where relevant.

5. **Discussion (100–200 words)**
   Discuss whether the findings matched your expectations, what they may imply, and any limitations.

The primary expectation is accuracy. We are looking for analyses that are appropriate for the research question, correctly implemented, and accurately interpreted. Likewise, neuroscience terminology should be used appropriately and be factually correct. For example, it would be incorrect to describe the Default Mode Network as being primarily involved in visual perception. An extensive literature review is **not** expected at this level.

---

# Advanced Level

The advanced pathway is intended for students who wish to undertake a more complete research project.

Here, you are expected to formulate a research question that is motivated by the scientific literature, design an appropriate analysis strategy, and interpret your findings within the broader context of existing research.

Depending on your research question, your analyses may include:

* comparative statistical analyses,
* correlation and regression,
* graph theoretical analyses,
* machine learning approaches,
* or other appropriate analytical methods.

Not every project needs to use every technique. Instead, the chosen analyses should be driven by the research question. A simpler analysis that is well-justified and correctly interpreted is preferable to a more sophisticated analysis that does not meaningfully address the question.

Compared with the introductory pathway, we expect the advanced report to provide a stronger motivation from the literature, employ more rigorous statistical analyses where appropriate, critically evaluate the findings, and discuss the results in relation to previous neuroscience research.

## Written Report

For general guidance on writing a scientific manuscript, including the purpose of each section and general writing advice, please refer to the [Writing Guide](../handbook/writing_guide.md).

Below are some more detailed guidelines that are specific to **Track 2 (Advanced Level)**.

Unlike the introductory pathway, the advanced report should resemble a concise scientific research paper. We recommend a total length of approximately **2,000–4,000 words** (excluding references), although there is no strict word limit. The emphasis is on conducting a well-motivated and rigorous analysis. 

A suggested structure is:

1. **Abstract (150–250 words)**
   Provide a concise summary of the study, including the research question, methods, principal findings, and main conclusions.

2. **Introduction (200–800 words)**
   Introduce the scientific background and motivate the research question using relevant literature. Clearly identify the knowledge gap your project aims to address and state your research question and, where appropriate, your hypotheses.

3. **Materials and Methods (600–1,200 words)**
   Describe your study in sufficient detail that another researcher could reproduce your analysis. Depending on your project, the following subheadings may be useful. Furthermore, readig other neuroimaging paper to see how they write their methods may help you make sense of the suggested subheadings. 

   **Participants**

   * Describe the dataset used (e.g., the LEMON dataset).
   * Report the number of participants included in your analysis, their age range (and any other relevant demographic characteristics).
   * State any inclusion or exclusion criteria applied. If using the LEMON dataset, these can be based on the original data descriptor paper.
   * Briefly mention the ethical approval for the dataset and informed consent procedures (refer to the original LEMON publication).

   **Behavioural / Physiological Data**

   * Describe the behavioural, physiological demographic, or questionnaire data used in your study.
   * Explain how the phenotype(s) of interest were defined or derived (e.g., personality questionnaire scores, cognitive test scores, age groups, sex, or education level).

   **Neuroimaging Data**

   * Describe the neuroimaging modality used (e.g., resting-state fMRI).
   * Briefly summarise the preprocessing pipeline, citing the original LEMON paper where appropriate.
   * Explain how brain timeseries were extracted (e.g., using a brain parcellation atlas such as the Yeo 7- or 17-network atlas).
   * Describe how functional connectivity was calculated and define any additional brain measures used (e.g., within-network connectivity, between-network connectivity, graph theoretical measures, or other derived metrics).

   **Statistical Analysis**

   * Describe the statistical or computational methods used to answer your research question.
   * Clearly define the independent and dependent variables.
   * Explain any statistical tests, regression models, graph theoretical analyses, or machine learning methods that were performed.
   * If applicable, describe any assumption checks, multiple comparison correction, bootstrapping, permutation testing, cross-validation, or other validation procedures.
   * List the main software and Python packages used for the analysis.

4. **Results (400–800 words)**
   Present your findings clearly using appropriate figures and tables. Report the key quantitative results without interpreting them in detail.

5. **Discussion (400–800 words)**
   Interpret your findings in relation to your research question and the existing literature. Discuss whether the results support your hypotheses, consider alternative explanations and limitations, and suggest possible directions for future work.

6. **Acknowledgements**
   Acknowledge any individuals or organisations who contributed to the project but do not meet the criteria for authorship.

7. **Declaration of Generative AI and AI-assisted Technologies in the Writing Process**
   You are required to have “Declaration of Generative AI and AI-assisted technologies in the writing process” section heading in your report, even if you have not used generative AI. Note that participants will not be penalized for the responsible and transparent use of generative AI tools.
   
8. **References**
   Cite all relevant sources using a consistent referencing style.

## A Note on Manuscript Structure

The section order above follows a conventional manuscript structure:

> **Abstract → Introduction → Materials and Methods → Results → Discussion**

However, you may notice that many published neuroscience papers use a different format:

> **Abstract → Introduction → Results → Discussion → Materials and Methods**

Placing the **Materials and Methods** at the end of the manuscript is common in many scientific journals, particularly in neuroscience and the life sciences. This allows readers to focus on the motivation and findings first, while the methodological details are presented later.

You are welcome to adopt either structure for your report. If this is your first research manuscript, however, we recommend keeping the **Materials and Methods** before the **Results**, as it often makes the report easier to read and assess. Regardless of the order you choose, ensure that all methodological details are described clearly enough for another researcher to reproduce your analysis.
