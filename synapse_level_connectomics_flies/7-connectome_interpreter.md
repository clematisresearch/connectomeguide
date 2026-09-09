---
title: "The Connectome Interpreter Toolkit Tutorial (Advanced Level)"
authors:
  - name: Aarushi Vardhan
    affiliations:
      - University of Toronto / University of Cambridge
  - name: Sapolnach Prompiengchai
    affiliations:
      - University of Oxford
---

# What is The Connectome Interpreter Toolkit?

The wealth of information contained in synapse-level connectomes, together with the release of several connectomes across sexes, developmental stages, and species, offers an exciting opportunity to understand how neuronal structure and circuit architecture give rise to function and behaviour. But, as you have probably noticed, there are **a lot of neurons and connections!** So how do we make sense of this complexity? 

A common approach in the field is to focus on the strongest connection partners of neurons. While this is useful for highlighting prominent interactions, choosing an appropriate threshold for what constitutes a “strong” connection can be challenging, given the continuous distribution of connection strengths. Applying such thresholds can also reduce the number of connections considered, potentially overlooking weaker or indirect interactions that may nevertheless contribute to circuit function. This complexity also reflects the fact that many neurons likely help process different types of sensory information and contribute to multiple behaviours. Yet, our understanding of the functional roles of neurons traditionally relies on experimentally manipulating and monitoring neurons under controlled conditions. Doing this for hundreds of thousands of neurons and the many more connections is not feasible. 

The [Connectome Interpreter Toolkit](https://www.biorxiv.org/content/10.1101/2025.09.29.679410v2.full) is a toolbox that helps researchers turn massive, complex connectome wiring diagrams into hypotheses about neural function and behaviour. 

Connectome Interpreter addresses this challenge by **combining structural connectome data with existing knowledge about neuronal function**. It provides computational tools to efficiently explore:

* **Direct and indirect (polysynaptic) connections**
* **How signals may propagate through circuits**
* **Which neurons or pathways may be functionally related**
* **What inputs might optimally activate a neuron**
* **How excitation and inhibition shape signal propagation**

So, conceptually:

**Known neuronal function + massive connectome → computational analysis → new hypotheses about circuit function and behaviour.**

To learn more about this work, please refer to and cite:
Yin, Y., Hoeller, J., Mathiasen, A., Tsang, J. M. F., Charrier, M. E., & Cardona, A. (2025). *The Connectome Interpreter Toolkit*. bioRxiv. [https://doi.org/10.1101/2025.09.29.679410](https://doi.org/10.1101/2025.09.29.679410)
**GitHub:** [https://github.com/YijieYin/connectome_interpreter](https://github.com/YijieYin/connectome_interpreter)
**Documentation:** [https://connectome-interpreter.readthedocs.io/en/latest/] (https://connectome-interpreter.readthedocs.io/en/latest/)
 