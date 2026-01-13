---
title: SyntraLine++ Compiler
subtitle: "Customized DSL-based compiler for machine learning and synthesized training pipelines with C++ and Python integration"
layout: page
slider_key: syntra
repo_url: "https://github.com/rizkysaputradev/Syntralinepp-Compiler"
---

<div class="project-layout">

  <!-- LEFT: structured writeup (rendered as real Markdown via markdownify) -->
  <div class="project-writeup">
    {% capture writeup %}

## Summary

**SyntraLine++** is a compiler-oriented DSL and execution pipeline that turns machine learning experiments into **structured, statically validated programs** whilst bridging the clarity of DSLs, the safety of compiler passes, and the flexibility of modern ML frameworks. In this project, the compiler is developed with the following properties:

- **Parses `.syntra` programs** and constructs a strongly typed Abstract Syntax Tree (AST).
- **Lowers programs into an Intermediate Representation (IR)** consisting of datasets, models, and experiment pipelines.
- **Performs semantic validation & normalization**, including architecture collapsing, dataset–model consistency checks, hyperparameter inference, and experiment correctness.
- **Emits runnable execution code** in either **PyTorch** or **JAX**, matching the user’s backend selection.
- **Supports experimentation constructs** such as automatic version comparison, hypergrid search, evaluation suites, and real-data CSV integration.
- **Produces reproducible experiment outputs** with structured dictionaries for downstream logging, visualization, and benchmarking.

---

## Research Purpose
The majority of machine learning codebases encode experiments as ad-hoc scripts. SyntraLine++ pushes the workflow into a **declarative program** that can be:

- validated before it runs,
- normalized into canonical forms (so experiments are comparable),
- compiled into backend-specific runners (PyTorch/JAX),
- and logged with consistent artifacts.

---

## Architecture Overview

1. **Frontend**: DSL parsing + AST construction  
2. **Lowering**: AST → IR (datasets/models/pipelines)  
3. **Passes**: semantic checks, normalization, inference, consistency validation  
4. **Backend emission**: generate runnable pipelines for PyTorch / JAX  
5. **Artifacts**: structured outputs for eval, tracking, and reproducibility

---

## Future Roadmaps

- Semantic checking and validation passes  
- Precision / Recall / F1 metrics for evalsuite in PyTorch and JAX  
- JAX backend parity with PyTorch pipeline examples  
- Distributed-training hints (gradient accumulation + config propagation)  
- Channel-aware and shape-aware dataset handling in both backends  

    {% endcapture %}

    {{ writeup | markdownify }}
  </div>

  <!-- RIGHT: slider first, then quick facts -->
  <div class="project-media">

    {% assign slider_images = site.data.project_sliders[page.slider_key] %}
    {% include project_slider.html images=slider_images %}

    <div class="mini-card" style="margin-top: 12px;">
      <div class="mini-title">Detailed Specifications</div>
      <div class="mini-body">
        <ul style="margin: 10px 0 0; padding-left: 18px;">
          <li><strong>Domain:</strong> DSL Compiler Design, Operating System, Real-Time System, Machine Learning</li>
          <li><strong>Core:</strong> AST, IR, Passes, Backend</li>
          <li><strong>Backends:</strong> PyTorch, JAX</li>
          <li><strong>Focus:</strong> Validation, Operationalization, Reproducibility</li>
        </ul>

        <div style="margin-top: 12px; display: flex; gap: 10px; flex-wrap: wrap;">
          <a class="btn" href="{{ page.repo_url }}" target="_blank" rel="noopener">View Repository</a>
          <a class="btn secondary" href="/projects/">All Projects</a>
        </div>
      </div>
    </div>

  </div>

</div>
