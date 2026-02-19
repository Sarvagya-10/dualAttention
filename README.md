# Meta-Cognition in Transformer Models (Experimental Framework)

This repository provides an **experimental implementation and controlled evaluation environment** for studying **context persistence, memory behavior, and internal state dynamics** in Transformer-based language models.

The code is intended to support **reproducible investigation of meta-cognitive properties** in autoregressive architectures such as GPT-2.

---

# Research Motivation

Modern Transformer language models exhibit behaviors that resemble:

* Context sensitivity
* History dependence
* Persistent internal representations
* Emergent memory-like dynamics

However, these properties are often **qualitatively observed rather than systematically tested**.

This project establishes a **minimal, controlled experimental setup** to:

* Isolate Transformer internal state behavior
* Evaluate repeatability vs. stochastic variation
* Examine whether prior context influences future outputs
* Prototype a **meta-memory augmentation mechanism**

---

# Experimental Design

The notebook performs four core evaluations:

### 1. Same Input, Repeated Execution

Tests whether identical inputs produce:

* Deterministic internal representations
* Stable hidden states across runs

This probes **repeatability and stochastic independence**.

---

### 2. Input Perturbation Sensitivity

Compares outputs from:

* Distinct random token sequences
* Identical architecture and weights

This measures **context-driven representational divergence**.

---

### 3. History Dependence

Evaluates whether:

* Sequential inputs alter later internal states
* Prior context persists beyond a single forward pass

This targets **temporal dependency within Transformer computation**.

---

### 4. Meta-Memory → Output Influence

Introduces a **meta-memory mechanism** and tests:

* Whether stored contextual traces affect inference
* How explicit memory interacts with Transformer hidden states

This explores **proto-meta-cognitive augmentation** in language models.

---

# Environment Control

To ensure reproducibility, the notebook:

* Pins **specific Transformers, Tokenizers, and Hub versions**
* Rebuilds the **exact GPT-2 implementation source**
* Eliminates dependency drift across runs

This avoids a common research failure mode:
**silent behavior changes due to library updates**.

---

# Repository Structure

```
meta-cognition-v1.ipynb   
```

This minimal structure is intentional to maintain:

* Transparency
* Reproducibility
* Ease of academic inspection

---

# Requirements

Tested with:

* Python 3.x
* PyTorch
* transformers == 4.28.1
* tokenizers == 0.13.3
* huggingface_hub == 0.14.1
* accelerate == 0.18.0
* safetensors

---

# Running the Experiments

Execute the notebook sequentially:

```bash
jupyter notebook meta-cognition-v1.ipynb
```

All experimental stages are **self-contained and reproducible** within the notebook.

---

# Research Scope

This repository is **not** a production model or benchmark system.

Instead, it serves as:

* A **controlled scientific probe** into Transformer cognition-like behavior
* A **prototype framework** for studying artificial meta-memory
* A **foundation for future formalization of meta-cognitive LLM architectures**

---

# Limitations

* Experiments are conducted on **small-scale GPT-2 configurations**
* Results are **exploratory, not conclusive**
* Meta-memory mechanism is **experimental and non-optimized**

This work should be interpreted as **hypothesis-generating research**, not final theory.

---


# License

MIT License

---

# Author

**Sarvagya Singh**
AI Research Student

---
