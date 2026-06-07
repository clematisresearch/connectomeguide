---
title: "LEMON Neuroimaging Dataset: Overview"
authors:
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
---

# Understanding the Dataset and Neuroimaging Workflow

## From Synapses to Brain Networks

In **Track 1 (Synapse-Level Connectomics)**, we explored the brain at the microscopic scale, focusing on individual neurons and synapses. In this track, we will take a very different perspective.

Rather than studying individual neurons, we will investigate the brain at the **macroscopic scale**. Here, we are interested in how entire brain regions interact with one another to form large-scale functional networks that support cognition, behavior, and mental health.

To study the brain at this scale, neuroscientists rely on a variety of neuroimaging techniques.

Some techniques are primarily used to study **brain structure**, such as structural magnetic resonance imaging (**structural MRI** or **sMRI**). These methods allow researchers to visualize brain anatomy and quantify properties such as cortical thickness, brain volume, and white matter organization.

Other techniques are used to study **brain function**, such as functional magnetic resonance imaging (**fMRI**). These methods allow researchers to investigate patterns of brain activity and communication between different brain regions.

For this competition, we will primarily focus on:

* **Structural MRI (sMRI)** — to study brain anatomy
* **Resting-State Functional MRI (rs-fMRI)** — to study functional brain networks

```{figure} ../static/smri_vs_fmri_placeholder.png
:width: 80%
:align: center

Placeholder: Structural MRI versus Functional MRI
```

---

## Task-Based versus Resting-State fMRI

Functional MRI can generally be divided into two major categories.

### Task-Based fMRI

In task-based fMRI, participants perform a specific task while inside the scanner.

Examples include:

* Looking at visual images
* Listening to sounds
* Performing memory tasks
* Solving problems
* Responding to emotional stimuli

Researchers then compare brain activity across different experimental conditions to identify regions involved in specific cognitive functions.

For example, a researcher interested in attention might compare brain activity while participants perform an attention-demanding task versus a control task.

### Resting-State fMRI

In resting-state fMRI (rs-fMRI), participants are not asked to perform any particular task.

Instead, they are typically instructed to:

* Keep their eyes open or closed
* Remain awake
* Relax and stay still

At first glance, this might seem uninteresting. However, even when a person is resting, the brain remains highly active.

Researchers have discovered that spontaneous fluctuations in brain activity are highly organized and reveal large-scale functional networks that consistently appear across individuals. These networks are thought to reflect the brain's intrinsic functional architecture.

Resting-state fMRI has become one of the most widely used tools in human connectomics because it allows researchers to investigate how different brain regions communicate with one another, how brain networks vary across individuals, and how these networks relate to cognition, behavior, physiology, and mental health.

**For this competition, we will primarily work with structural MRI and resting-state fMRI data.**

---

# Understanding the LEMON Dataset

The dataset used in this competition is the **Leipzig Mind-Brain-Body (LEMON) Dataset**.

Before we begin analyzing the data, it is useful to understand how neuroimaging studies are typically conducted and how researchers transform raw MRI scans into data that can be analyzed scientifically.

The LEMON dataset publication can be found here: https://www.nature.com/articles/sdata2018308

---

## Step 1: Collecting the Data

Every neuroimaging study begins with data acquisition.

If you were conducting your own experiment, participants would visit an MRI scanner where trained MRI technicians would collect structural and functional brain scans.

In the case of the LEMON dataset, the data have already been collected and shared publicly by the research team.

The paper's [Data Records/**MRI**](https://www.nature.com/articles/sdata2018308#Sec59) section describes several ways to access the dataset.

You may notice that there are multiple download options and repositories available. This is common for large neuroscience datasets because researchers often have different preferences for how they access and organize data.

The dataset includes multiple modalities, including:

* MRI
* EEG
* Behavioral assessments
* Physiological measurements
* Demographic information

For this competition, we will focus primarily on the MRI data and associated behavioral, psychological, psychiatric, and physiological measures.

---

## Step 2: Raw Data

If you visit the MRI download page:

[https://fcon_1000.projects.nitrc.org/indi/retro/MPI_LEMON/downloads/download_MRI.html](https://fcon_1000.projects.nitrc.org/indi/retro/MPI_LEMON/downloads/download_MRI.html)

you will notice that both **raw** and **preprocessed** data are available.

Raw MRI data are the closest representation of what was acquired directly from the scanner.

If you were conducting your own neuroimaging study, this is typically where your analysis would begin.

However, raw MRI data are not immediately ready for scientific analysis.

Before meaningful conclusions can be drawn, researchers must perform a series of preprocessing steps to improve data quality and place all participants into a common analytical framework.

---

## Step 3: What Is Preprocessing?

Preprocessing refers to the series of computational steps used to transform raw MRI scans into data that can be analyzed reliably.

Although different studies may use slightly different preprocessing pipelines, most workflows include many of the following steps.

```{note}
You do not need to understand all of these preprocessing steps right now. For the moment, it is sufficient to know that raw MRI data undergo extensive processing before they are suitable for analysis. Throughout this competition, we will work with data that have already been preprocessed.
```

### Structural MRI Preprocessing

For structural MRI data:

1. Correct image artifacts and scanner-related distortions
2. Remove non-brain tissue (e.g., skull, scalp, and surrounding tissue)
3. Segment the brain into different tissue classes:

   * Gray matter
   * White matter
   * Cerebrospinal fluid
4. Align each participant's brain to a common anatomical template (such as MNI space)

These steps make it easier to compare brain anatomy across individuals. For example, MRI scans include the skull and other non-brain tissues that are usually not relevant for analysis. In addition, no two brains are exactly the same size or shape. By removing non-brain tissue and aligning brains to a common template, researchers can compare corresponding brain regions across participants more accurately.


### Functional MRI Preprocessing

For resting-state fMRI data:

1. Correct for participant head motion
2. Correct timing differences between slices
3. Align functional images to the participant's structural scan
4. Transform images into a common template space
5. Reduce noise from motion, physiological processes, and scanner artifacts
6. Apply spatial smoothing (in some pipelines)

The goal is not to alter the underlying brain activity, but rather to reduce sources of noise and ensure that data can be meaningfully compared across participants.

---

## Step 4: From Preprocessed Data to Connectomics

Once preprocessing is complete, the real scientific analysis begins.

Researchers must still decide:

* How to define brain regions
* How to measure communication between regions
* How to construct functional networks
* How to quantify network properties
* How to relate these networks to cognition, behavior, physiology, and mental health

These are precisely the types of questions that form the foundation of human connectomics.

Importantly, **you will not need to perform the preprocessing steps described above (Step 3) yourself**. For this competition, we have already prepared the data so that you can focus on learning how to analyze and interpret brain networks rather than spending time processing hundreds of gigabytes of raw MRI data.

You will still perform many of the exciting downstream analyses that neuroscientists conduct after preprocessing. For example, you will learn how to construct and analyze functional brain networks, compute network measures, visualize patterns of connectivity, and investigate how these networks relate to cognition, behavior, physiology, and mental health.

The only major step that has already been completed for you is the preprocessing of the MRI data itself.

In the following sections, we will begin exploring how resting-state fMRI data can be transformed into functional brain networks and used to answer meaningful scientific questions about the human brain.

