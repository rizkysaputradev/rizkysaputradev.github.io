---
title: Multithreaded Ambientor Real Time System
subtitle: "Cross-platform, multithreaded real-time ambient sound engine built with Rust, C++, Python bindings, and SIMD-accelerated DSP"
layout: page
slider_key: ambientor
repo_url: "https://github.com/rizkysaputradev/Ambientor-Real-Time-Engine"
---

<div class="project-layout">

  <!-- LEFT: structured writeup (rendered as real Markdown via markdownify) -->
  <div class="project-writeup">
    {% capture writeup %}

## Summary
**Ambientor** is a **real-time ambient music engine** designed as both a **creative instrument** and a **systems-level DSP playground**. This project in particular encapsulates the capacity of **multi-language stack** which combines:

- **Rust core DSP** (filters, envelopes, waveshaping, scenes)
- **C++ host** for low-level integration and embedding
- **Python bindings** for quick scripting and experimentation
- **Hand-tuned SIMD assembly** (AVX/SSE on x86, NEON on ARM64)
- **Realtime CLI player** using `cpal` on macOS (and portable to Linux)

This multithreaded Ambientor project is designed as a compact, transparent, and academically grounded exploration of how a real-time ambient sound engine can be constructed across multiple programming ecosystems. Instead of expanding into a large or opaque codebase, the system adopts a clean, layered architecture that spans **Rust, C++, Python, and low-level assembly**, providing a reproducible model for understanding real-time audio generation, systems programming, digital signal processing, and cross-language integration.

At its core, the project emphasizes **clarity, modularity, and cross-language interoperability**. It demonstrates how:

- Rust’s safety guarantees can coexist with external components via **C FFI**.  
- Rust modules can be embedded within **C++** applications without architectural friction.  
- High-level languages such as **Python** can interface with the same engine using `pyo3` and `maturin`.  
- **SIMD-optimized assembly** can be integrated in a controlled, testable, and portable manner.

Functionally, the engine provides **real-time stereo audio streaming** through the `cpal` backend while generating evolving ambient textures. These include amplitude envelopes, lightweight filtering, gradual modulation, and slowly dissipating low-frequency layers—behaviors aligned with foundational principles in sound synthesis and modern DSP. This makes the engine not only musically capable but also suitable for experimentation and academic analysis.

---

## Research Purpose
The primary goal of this particular project is to develop a **foundation** to a sound engine system with its robustness to perform several **low-level based** functionalities, likewise:
- Run **realtime ambient pads / drones / textures**.
- Demonstrate **SIMD acceleration** and **cross-language FFI**.
- Be used as a **reference project** for:
  - Writing DSP based program or code in **Rust**.
  - Calling it with other languages such as **C++** and **Python**.
  - Selectively dropping down to **assembly** for hot paths.

Ambientor is additionally structured around **benchmarkability and reproducibility**. Its design supports:

- Direct comparison between scalar and SIMD implementations  
- Measurement of CPU load, latency, and real-time performance  
- Rapid insertion of new waveforms, scenes, or modulation structures  
- Systematic evaluation of synthesis components under varying computational conditions  

In summary, Ambientor functions as a hybrid of **educational reference**, **real-time audio synthesizer**, and **performance-oriented research tool**, illustrating how a small but well-engineered system can bridge languages, abstractions, and low-level optimizations within a unified ambient audio engine.

---

## Future Roadmaps
- **Offline renderer**
- **More advanced scenes**
- **Modulation matrix with LFO routing**
- **Preset system integration**
- **GUI front-end setup**
- **Benchmark harness with scalar and SIMD comparison**

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
          <li><strong>Domain:</strong> Embedded System, Audio Processing, Hardware/Software Co-Design, Computer Architecture</li>
          <li><strong>Core:</strong> DSP, SIMD, CLI, FFI</li>
          <li><strong>Architecure:</strong> DSP, SIMD</li>
          <li><strong>Focus:</strong> Audio Classification, Multithreading, Parallelism</li>
        </ul>

        <div style="margin-top: 12px; display: flex; gap: 10px; flex-wrap: wrap;">
          <a class="btn" href="{{ page.repo_url }}" target="_blank" rel="noopener">View Repository</a>
          <a class="btn secondary" href="/projects/">All Projects</a>
        </div>
      </div>
    </div>

  </div>

</div>