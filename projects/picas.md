---
title: PICAS Memory Allocator
subtitle: "Policy-indexed contiguous allocation for deterministic real-time systems"
layout: page
slider_key: picas
repo_url: "https://github.com/rizkysaputradev/Policy-Indexed-Contiguous-Allocation-System"
---

<div class="project-layout">

  <!-- LEFT: structured writeup (rendered as real Markdown via markdownify) -->
  <div class="project-writeup">
    {% capture writeup %}

## Summary
**PICAS (Policy Indexed Contiguous Allocation System)** is a layered memory allocation framework designed to bridge the gap between traditional low-level allocators (such as `malloc`, `jemalloc`, and `tcmalloc`) and modern, context-sensitive memory management requirements found in real-time systems, adaptive runtimes, and data-intensive workloads. Conventional allocators predominantly rely on *local heuristics*—such as size classes, freelists, and arena partitioning—or *global statistical tuning* that reacts indirectly to workload behavior. While highly optimized for general-purpose use, these approaches lack an explicit representation of **execution phase**, **semantic intent**, or **future allocation trajectory**. As a result, they are often blind to higher-level structure in allocation patterns, leading to suboptimal memory placement, premature fragmentation, or uncontrolled cross-arena spillover. PICAS addresses this limitation by introducing a **policy-driven** yet **phase and context aware allocation model** in which allocation decisions are explicitly informed by *semantic execution context*. Memory is modeled not as a flat pool, but as a sequence of **logical layers**, each associated with both **data progression** and **memory capacity progression**. This allows allocation behavior to adapt dynamically as workloads evolve, rather than reacting only after memory pressure has already manifested.

At its core, PICAS implements a **dual-layer abstraction**:

- **Data Layers** represent the *conceptual phase* or progression stage of allocation requests (e.g., initialization, steady-state, streaming, finalization, or algorithmic epochs).
- **Memory Layers** represent *physically partitioned memory regions*, each with independent capacity limits, transitory checkpoints, and lifecycle constraints.

Allocation decisions are governed by a **policy engine** that continuously evaluates real-time signals, including:
- allocation counts and allocated bytes per data layer,
- memory layer transitory points (MEM-TP) and logical full conditions (MEM-LP),
- cross-layer stranding risk and fragmentation potential,
- bounded spill, probe, and backfill opportunities.

This design enables behaviors that are **non-expressible in traditional allocators**, such as:
- advancing data phases even when memory layers lag behind,
- safely backfilling into earlier memory layers to reduce stranded capacity,
- bounded cross-layer allocation with explicit penalty modeling,
- allocator-level reasoning about *future memory pressure*, not just current availability.

PICAS follows the same design principles as the **SyntraLine++ Compiler**: explicit structure, formal reasoning, observability, and extensibility—aiming where in this case is not merely to *allocate memory*, but simultaneously to **model, control, and reason about memory behavior over time**.

---

## Research Purpose
**PICAS is motivated by the idea that memory allocation should be:**
1. **Context-aware**, not purely size-driven  
2. **Policy-driven**, not hard-coded  
3. **Phase-aware**, not temporally blind  
4. **Observable**, not opaque  
5. **Safe**, even under pathological workloads  

Rather than replacing existing allocators with yet another heuristic, PICAS reframes memory allocation as a **controlled progression problem**, where both *data* and *memory* advance through structured layers under explicit rules.

---

## Future Roadmaps
- System stabilization
- Policy evaluation and extensibility
- Concurrency and scalability
- Integration of advanced memory management algorithms
- Formalization and verification
- Visualization and Run Time Integration

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
          <li><strong>Domain:</strong> Memory System, System Programming, Computer Architecture, Real-Time System</li>
          <li><strong>Core:</strong> Policy, Sanitizer, Cache, Virtual Memory</li>
          <li><strong>Neural Networks:</strong> Policy, Sanitizer</li>
          <li><strong>Focus:</strong> Memory Management, Advanced Algorithms, Smart Allocation System</li>
        </ul>

        <div style="margin-top: 12px; display: flex; gap: 10px; flex-wrap: wrap;">
          <a class="btn" href="{{ page.repo_url }}" target="_blank" rel="noopener">View Repository</a>
          <a class="btn secondary" href="/projects/">All Projects</a>
        </div>
      </div>
    </div>

  </div>

</div>