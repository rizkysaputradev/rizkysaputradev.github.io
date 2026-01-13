---
title: Vision Fusion Real Time (VFRT) System
subtitle: "Real-time retrieval multimodial AI system that allows a visual input into a CLIP-powered object recognizer with a small and self-growing memory"
layout: page
slider_key: vfrt
repo_url: "https://github.com/rizkysaputradev/Vision-Fusion-Real-Time"
---

<div class="project-layout">

  <!-- LEFT: structured writeup (rendered as real Markdown via markdownify) -->
  <div class="project-writeup">
    {% capture writeup %}

## Summary
**Vision Fusion Real Time (VFRT)** is a **real-time retrieval** multimodial AI based demo that allows a **visual input** such as a **webcam** into a **CLIP-powered** object recognizer with a small, yet sufficient **self-growing memory** and adjustable **text-prototype fusion**. This real-time system introduces the concept of **data retrieval** without strictly relying on a **pre-trained** or **fine-tuned** model. This project is inspired with the recurring innovations of **facial recognition systems**, which is simultaneously linked to the project that I am currently working on. Furthermore, this demo ensures **reproducibility** as well as both a **research and practical based modularity** with the following specifications:

- **Retrieve**: Encode frames → search FAISS memory → aggregate neighbor votes.
- **Fuse**: Interpolate image scores with **CLIP-Text prototypes** (e.g., prompts like “a photo of a `{label}`”).
- **Register on the fly**: Press `[r]` to capture a few recent frames and **add a new class**.
- **Open-set handling**: Temperature and threshold for the **unknown**.
- **Low-latency loop**: Threaded webcam which captures with a bounded queue and borders (e.g., “`latest-frame`” semantics).
- **Streamlit UI**: Start/Stop, sliders for fusion/EMA/temperature, live overlay preview.

---

## Research Purpose
Modern multimodal models such as CLIP establish a **joint latent embedding** space where **images** and **text** can be directly compared using **vector similarity**. However, these models are often **static**, **offline**, and **not incrementally adaptive**. Real-world robotics, sensing, and real-time perception systems **do not operate in offline curated datasets**, rather they are required to adapt **online** as new objects appear, disappear, change lighting, orientation, texture, deformation, etc. The system uses **CLIP image/text alignment** and **not a classifier**. Rather, the system run as a **semantic coordinate system**. Furthermore, the system includes the following implementations:

- a **dynamic incremental memory store** (FAISS vector store).
- an **online few-shot registration mechanism**.
- a **retrieval and fusion scoring based pipeline** (kNN, text priors and EMA smoothing).
- a **real-time control loop** with camera → embedding → retrieve → decide → UI.

---

## Future Roadmaps
- **IVF/PQ FAISS indices and on-disk persistence**.
- **On-screen label editor and per-label undo**.
- **Batch evaluation scripts and CSV metrics**.
- **Alternative backbones (e.g., SigLIP, EVA-CLIP)**.
- **WebRTC camera for remote browser demo**.

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
          <li><strong>Domain:</strong> Computer Vision, Deep Learning, Human-Computer Interactions, Real-Time System</li>
          <li><strong>Core:</strong> RAG, FAISS, CLIP, OpenCV</li>
          <li><strong>Architecure:</strong> RAG, FAISS</li>
          <li><strong>Focus:</strong> Clip Embeddings, Object Based Detection, Multimodal AI System</li>
        </ul>

        <div style="margin-top: 12px; display: flex; gap: 10px; flex-wrap: wrap;">
          <a class="btn" href="{{ page.repo_url }}" target="_blank" rel="noopener">View Repository</a>
          <a class="btn secondary" href="/projects/">All Projects</a>
        </div>
      </div>
    </div>

  </div>

</div>