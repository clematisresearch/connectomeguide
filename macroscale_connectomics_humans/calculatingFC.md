---
title: "Different Ways to Measure Functional Connectivity"
authors:
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
---

# Different Ways to Measure Functional Connectivity

So far, we have treated functional connectivity as the correlation between the time series of two brain regions.

In practice, however, researchers have developed many different ways of quantifying relationships between brain regions. Each method captures a slightly different aspect of brain organization and makes different assumptions about how brain regions interact.

In this competition, we will primarily focus on **correlation-based functional connectivity**, but it is useful to be aware of other approaches commonly used in the field.

---

## Pearson Correlation

The most common measure of functional connectivity is the **Pearson correlation coefficient**, which we have discussed before in the previous subsections. 

Suppose we have two regional time series:

```text
Region A: ↑ ↓ ↑ ↑ ↓ ...
Region B: ↑ ↓ ↑ ↑ ↓ ...
```

If the two signals fluctuate together over time, they will have a high positive correlation.

Mathematically, Pearson correlation measures how similarly two time series vary together.

```text
r = +1
Perfect positive correlation

r = 0
No linear relationship

r = -1
Perfect negative correlation
```

This approach forms the basis of most resting-state functional connectivity studies and is often the default choice in neuroimaging.

Feel free to watch this video to understand the mathematics behind correlation:

```{iframe} https://www.youtube.com/embed/uW0TapQ6UQU
:width: 100%
```

---

## Partial Correlation

One limitation of ordinary correlation is that two regions may appear connected simply because they are both influenced by a third region.

For example:

```text
Region A ← Region C → Region B
```

Even if A and B do not directly interact, they may still appear correlated.

**Partial correlation** attempts to address this issue by estimating the relationship between two regions after accounting for the influence of all other regions.

```text
Correlation
→ Total association

Partial Correlation
→ Direct association after controlling for others
```

Because of this property, partial correlation is often considered a useful estimate of more direct functional interactions.

---

## Precision Matrices

Closely related to partial correlation is the **precision matrix**, which is simply the inverse of the covariance matrix.

Although the mathematics can be challenging, the intuition is straightforward:

```text
Covariance Matrix
↓ invert
Precision Matrix
```

The precision matrix provides information about conditional relationships between brain regions and is often used when estimating sparse brain networks.

For now, it is sufficient to know that precision-based approaches are frequently used in modern connectomics and machine learning applications.

---

## Dynamic Functional Connectivity (dFC)

Everything we have discussed so far assumes that functional connectivity remains constant throughout the scan.

This is known as **static functional connectivity**.

However, the brain is continuously changing over time.

Dynamic functional connectivity asks:

> Does the connectivity between brain regions change during the scan?

Researchers often estimate connectivity within short sliding windows:

```text
Window 1 → FC Matrix 1
Window 2 → FC Matrix 2
Window 3 → FC Matrix 3
...
```

This produces a time-varying description of brain connectivity and can reveal transient brain states.

---

## Effective Connectivity

Functional connectivity tells us whether two regions are statistically related.

It does **not** tell us whether one region influences another.

Effective connectivity attempts to estimate:

```text
Region A
   ↓
Region B
```

In other words, it seeks to infer directional influences between brain regions.

This is substantially more difficult than estimating functional connectivity and often requires stronger modeling assumptions.

---

## Graph-Theoretical Connectivity Analysis

Rather than studying individual connections, researchers can also treat the entire functional connectivity matrix as a network.

In this framework:

```text
Brain Region = Node
Functional Connection = Edge
```

Viewing the brain as a network allows researchers to ask questions such as:

* Which brain regions are the most highly connected to the rest of the brain?
* Which regions act as important hubs for information transfer?
* How efficiently can information travel across the network?
* Do groups of brain regions naturally cluster together into communities?
* How does the overall organization of the brain network change across individuals or conditions?

These questions form the basis of graph-theoretical connectomics, which provides a powerful framework for studying the brain as an interconnected network rather than a collection of isolated connections.


---

## Functional Connectivity in Nilearn

The Nilearn package provides a convenient implementation of several commonly used connectivity estimators through the `ConnectivityMeasure` class.

Examples include:

```python
from nilearn.connectome import ConnectivityMeasure

correlation_measure = ConnectivityMeasure(
    kind="correlation"
)

partial_measure = ConnectivityMeasure(
    kind="partial correlation"
)

covariance_measure = ConnectivityMeasure(
    kind="covariance"
)

precision_measure = ConnectivityMeasure(
    kind="precision"
)
```

## Next Steps:

For Connectome 2026–2027, we will primarily begin with **correlation-based functional connectivity**, since it is intuitive, widely used, and forms the foundation for many subsequent analyses. The functional connectivity will then be used to for our graph theoretical analysis. We can then use FC and graph theoretical measures to link brain and behavior! 
