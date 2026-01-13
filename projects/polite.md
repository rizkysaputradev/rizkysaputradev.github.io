---
title: Classifier Guided Politeness Rewriting System
subtitle: "Politeness Rewriter is a hybrid NLP system that detects, classifies and rewrites user input into polite, respectful text using a combination of transformer-based classifiers and controlled text generation"
layout: page
slider_key: polite
repo_url: "https://github.com/rizkysaputradev/Politeness-Rewriters"
---

<div class="project-layout">

  <!-- LEFT: structured writeup (rendered as real Markdown via markdownify) -->
  <div class="project-writeup">
    {% capture writeup %}

## Summary
The **Politeness Rewriter** is a hybrid NLP system that **detects**, **classifies**, and **rewrites** user input into polite, respectful text using a combination of **transformer-based classifiers** and **controlled text generation**. It specifically combines:

- A **DistilRoBERTa politeness classifier** (trained on the *Stanford Politeness Corpus* from ConvoKit),
- A **T5-based paraphraser** conditioned for polite rewriting,
- A **modular rewrite pipeline** with scoring, reranking, and explainability,
- And an optional **Gradio demo app** for interactive rewriting.

The project demonstrates *classifier-guided text style transfer* — transforming the *tone* of a sentence without altering its *semantic meaning*. Additionally, this project was developed with the purpose for the project of **2025-2 Introduction to Natural Language Processing (001)** course. Contributors are credited below this page.

---

## Research Purpose
Politeness plays a critical role in communication, especially for social networking services within professional settings, AI chatbots, digital assistants, and automated email generation. This project aims to:

1. Build a lightweight yet robust **politeness classifier**.
2. Integrate it with a **T5-style paraphraser** to automatically rewrite impolite or neutral sentences into polite versions.
3. Provide a **human-interpretable pipeline** where users can trace:
   - Classification probability,
   - Semantic similarity,
   - Rewrite quality.

The ultimate goal is to construct a language-generation systems that is more **socially intelligent** with our own training set and evaluation results.

---

## Future Roadmaps
- **Context-Aware Rewriting**  
- **Multi-Style Transfer**  
- **Explainability**  
- **Better Reranker Architecture**  
- **Adversarial Evaluation**  
- **Multilingual Extension**  
- **User Controls in UI**  

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
- Instructor:
<a
      href="https://seungwonh.github.io"
      target="_blank"
      rel="noopener noreferrer"
      class="ref-link"
      >
      Prof. Hwang Seung-Won
      </a>
- Team Member 1:
<a
      href="https://github.com/buugiiman"
      target="_blank"
      rel="noopener noreferrer"
      class="ref-link"
      >
       Bat-Orshikh Butemj
       </a>
- Team Member 2:
 <a
      href="https://github.com/ahchowww"
      target="_blank"
      rel="noopener noreferrer"
      class="ref-link"
      >
      Shu Xian Chow
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
          <li><strong>Domain:</strong> Natural Language Processing, Deep Learning, Artificial Intelligence, Data Science</li>
          <li><strong>Core:</strong> T5, Distilbert, Convokit, Context Awareness</li>
          <li><strong>Architecture:</strong> T5, Distilbert</li>
          <li><strong>Focus:</strong> Smart Contextualization, Linguistic Analysis, NLP System Framework</li>
        </ul>

        <div style="margin-top: 12px; display: flex; gap: 10px; flex-wrap: wrap;">
          <a class="btn" href="{{ page.repo_url }}" target="_blank" rel="noopener">View Repository</a>
          <a class="btn secondary" href="/projects/">All Projects</a>
        </div>
      </div>
    </div>

  </div>

</div>
