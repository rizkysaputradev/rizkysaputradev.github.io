---
title: FER Burnout Detection System
subtitle: "Real Time Stress and Burnout Predictor Through Facial Emotion Recognition System (FER) and Hybrid Deep Learning CNN/LSTM Models"
layout: page
slider_key: fer
repo_url: "https://github.com/rizkysaputradev/FER-Burnout-Detection-System"
---

<div class="project-layout">

  <!-- LEFT: structured writeup (rendered as real Markdown via markdownify) -->
  <div class="project-writeup">
    {% capture writeup %}

## Summary
Burnout and prolonged stress have become increasingly prevalent in academic and professional environments, negatively affecting cognitive performance, emotional well-being, and productivity. Conventional burnout assessment methods—most notably survey-based instruments such as the Maslach Burnout Inventory (MBI)—are widely validated but inherently limited by subjectivity, recall bias, and their inability to capture real-time emotional dynamics.

This project was developed in accordance with my undergraduate thesis dissertation for my B.S. in computer science and engineering (CSE) at Seoul National University, where the system specifically presents a **real-time, non-invasive burnout detector** based on **Facial Emotion Recognition (FER)** and **temporal deep learning models**. The system integrates a convolutional neural network (CNN) for per-frame facial emotion classification with a Long Short-Term Memory (LSTM) network to model emotional persistence and variability across time. Emotion probabilities are transformed into an interpretable burnout score using a weighted emotional valence formulation combined with temporal volatility. The system implements an end-to-end pipeline that estimates a **burnout/stress proxy score** from real-time webcam streams by combining the listed modules:

- **Face detection + landmarks** (MTCNN-based localization + keypoints)
- **Facial emotion recognition (CNN)** producing an emotion probability vector
- **Geometric fatigue cues** from facial landmarks (lightweight features)
- **Temporal modeling (LSTM)** to capture gradual stress accumulation
- **Burnout scoring** via weighted emotion/landmark signals over time
- **Survey validation integration** (MBI / PSS-style alignment)
- **Explainability** using Grad-CAM and saliency visualizations
- **Session logging + longitudinal analysis** for multi-session trends

In order to validate the system, FER-derived burnout scores are statistically compared with standardized survey-based burnout scores (MBI/PSS) using Pearson’s correlation analysis. Experimental results demonstrate a **strong positive correlation (r ≈ 0.904)** between system-generated burnout scores and survey measurements, supporting the system’s reliability as a complementary, continuous burnout monitoring framework. Consequently, this project is specifically designed to be **computer-science oriented** (architecture + implementation + reproducibility), while still acknowledging the psychological grounding of burnout through its validation logic and longitudinal interpretation.

---

## Future Roadmaps
Despite the robustness and cosistency of the FER based system in detection the burnout in real-time, there are several considerations in which this specific roadmap reflects such potential features to either increase the practical robustness or extend its theoretical and experimental applicability. In addition, this section outlines intentional future directions to enhance the project, such as:
- Optimize for higher FPS (GPU inference / batching / faster detectors)
- Improve any landmark features or utilize face mesh models
- Include diverse datastes (Race, Culture, Age, Gender)
- Strengthen temporal modeling (Transformer, TCN)
- Integrate personalized calibration per user
- Improve survey protocol and longitudinal validation design

---

## Credits
- Institution:
<a
      href="https://en.snu.ac.kr/index.html"
      target="_blank"
      rel="noopener noreferrer"
      class="ref-link"
      >
      Seoul National University
      </a>
- Thesis Advisor:
<a
      href="https://rubis.snu.ac.kr"
      target="_blank"
      rel="noopener noreferrer"
      class="ref-link"
      >
      Prof. Chang-Gun Lee
      </a>

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
          <li><strong>Domain:</strong> Computer Vision, Machine Learning, Deep Learning, Real-Time System</li>
          <li><strong>Core:</strong> FER, CNN, LSTM, MBI</li>
          <li><strong>Neural Networks:</strong> CNN, LSTM</li>
          <li><strong>Focus:</strong> Emotion Classification, Facial Detection, Deep Learning Framework</li>
        </ul>

        <div style="margin-top: 12px; display: flex; gap: 10px; flex-wrap: wrap;">
          <a class="btn" href="{{ page.repo_url }}" target="_blank" rel="noopener">View Repository</a>
          <a class="btn secondary" href="/projects/">All Projects</a>
        </div>
      </div>
    </div>

  </div>

</div>
