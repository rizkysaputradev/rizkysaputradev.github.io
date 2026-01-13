---
title: Research & Systems
subtitle: "Core directions: memory systems, compiler-style infrastructure, and multimodal pipelines"
---

<div class="about-grid">
  <!-- LEFT: content -->
  <div class="about-text">
    <p class="about-intro">
      My work focuses on building systems where behavior is <strong>predictable</strong>, constraints are <strong>explicit</strong>,
      and performance tradeoffs are <strong>measurable</strong>. I’m most interested in the intersection of
      <em>low-level runtimes</em>, <em>compiler-style tooling</em>, and <em>end-to-end ML pipelines</em>,
      especially when the system must hold under real-time or constraints.
    </p>
    <h3>Memory Systems & Allocation</h3>
    <p>
      I design allocation frameworks with deterministic behavior, explicit routing policies, and theory-informed
      models of fragmentation and runtime pressure. The goal is not only speed, but also <strong>control</strong>:
      predictable latency, clear failure modes, and debuggable policies.
    </p>
    <ul>
      <li><strong>Deterministic routing:</strong> hierarchical priority rules and policy-driven placement</li>
      <li><strong>Fragmentation modeling:</strong> tracking waste and stability under churn</li>
      <li><strong>Adaptive regimes:</strong> switching strategies based on runtime conditions</li>
      <li><strong>Real-time constraints:</strong> bounded behavior and predictable allocation paths</li>
    </ul>
    <p class="muted">
      Representative systems: DRMAT family, PICAS, and DIMCA-style low-level tracking allocators.
    </p>
    <h3>Multimodal AI Pipelines</h3>
    <p>
      I build end-to-end multimodal pipelines with emphasis on validation, longitudinal tracking, and
      interpretable metrics. I’m especially interested in systems that connect real-time signals to
      measurable outcomes (e.g., session metrics, trend analysis, and survey-backed validation).
    </p>
    <ul>
      <li><strong>Real-time inference:</strong> streaming pipelines with stable throughput and monitoring</li>
      <li><strong>Temporal modeling:</strong> LSTM / sequence modeling for state and trend estimation</li>
      <li><strong>Explainability:</strong> landmark-driven analysis and correlation-based interpretation</li>
      <li><strong>Validation:</strong> alignment against survey instruments and statistical evaluation</li>
    </ul>
    <h3>Compilers & Infrastructure</h3>
    <p>
      I approach complex systems with compiler-style structure: explicit intermediate representations,
      correctness constraints, and pass-based transformations. This helps keep systems scalable as features
      grow and backends diversify.
    </p>
    <ul>
      <li><strong>Pass-based architecture:</strong> semantic checking, validation, and transformation stages</li>
      <li><strong>Backend parity:</strong> consistent evaluation across PyTorch / JAX execution paths</li>
      <li><strong>Reproducibility:</strong> clear configs, measurable metrics, and traceable outputs</li>
    </ul>
  </div>
  <!-- RIGHT: media -->
  <div class="about-media">
    <!-- Slider (only one) -->
    <div class="about-slider-card">
      {% assign imgs = site.data.about_sliders["research_sliders"] %}
      {% include project_slider.html images=imgs title="Systems & Research" %}
    </div>
    <!-- Single card below slider -->
    <div class="about-side-card">
      <div class="about-side-title">Research priorities</div>
      <ul class="about-facts">
        <li><strong>Bias:</strong> Correctness and predictability before optimization</li>
        <li><strong>Metrics:</strong> Latency, Memory Footprint, Stability, Reproducibility</li>
        <li><strong>Style:</strong> Explicit Invariants, Documented Assumptions, Debuggable Policies</li>
        <li><strong>Open to:</strong> Internship/Working Roles, Research Collaboration, and Systems Discussions</li>
      </ul>
      <div class="about-side-actions">
        <a class="btn" href="/projects/">View Projects</a>
        <a class="btn secondary" href="/papers/">Papers</a>
        <a class="btn ghost" href="/contact/">Contact</a>
      </div>
      <p class="muted about-side-note">
        Click images to open full view.
      </p>
    </div>
  </div>
</div>
