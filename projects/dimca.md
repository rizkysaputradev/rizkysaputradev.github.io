---
title: DIMCA Memory Allocator
subtitle: "Customized algorithm designed to enhance memory allocation performance by optimizing how data capsules are distributed across multi-level memory pools"
layout: page
slider_key: dimca
repo_url: "https://github.com/rizkysaputradev/Dynamic-Integrated-Memory-Cross-Allocation"
---

<div class="project-layout">

  <!-- LEFT: structured writeup (rendered as real Markdown via markdownify) -->
  <div class="project-writeup">
    {% capture writeup %}

## Summary
**DIMCA (Dynamic Integrated Memory Cross Allocation)** is a custom algorithm designed to enhance memory allocation performance by optimizing how data capsules are distributed across multi-level memory pools. The goal is to minimize allocation time penalties due to mismatches between data and memory levels, simulating scenarios found in hierarchical memory systems (e.g., CPU cache levels, RAM tiers, or storage stacks).

---

## Research Purpose
Modern computing systems operate with tiered memory hierarchies:

- **Level 1 (L1)**: Fastest but smallest (e.g., CPU cache)
- **Level 2 (L2)**: Larger but slower (e.g., main memory)
- **Level 3 (L3)**: Largest but slowest (e.g., disk or virtual memory)

Traditional allocation models often place data indiscriminately, causing performance drops due to:

- **Time penalties** when accessing deeper memory levels
- **Lack of alignment** between data's urgency or criticality and memory proximity

DIMCA seeks to fix this by introducing an adaptive and dynamic placement model that:

- Matches **data capsule priority levels** to **memory level tiers**
- Penalizes mismatches in levels with a cost function
- Supports **concurrent allocation** across multiple threads

---

## Future Roadmaps
- LRU-based eviction for full memory levels
- Real-time simulation interface / GUI
- Workload-aware capsule ranking
- Allocation visualization via heatmaps or memory charts

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
          <li><strong>Core:</strong> Multilevel Memory Pooling, Concurrent Allocation, Cache, Virtual Memory</li>
          <li><strong>Neural Networks:</strong> Multilevel Memory Pooling, Concurrent Allocation</li>
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