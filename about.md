---
title: About
subtitle: "Systems-first engineer with research-style rigor"
---

<div class="about-grid">
  <div class="about-text">
    <p class="about-intro">
      Hello, I am Rizky Johan Saputra. I am an aspire to be a AI/CS engineer with a strong focus primarily on the fields of
      <a
      href="https://en.wikipedia.org/wiki/Artificial_intelligence"
      target="_blank"
      rel="noopener noreferrer"
      >
      artificial intelligence 
      </a>
      . However, I am also interested in working on hardware/software co-design and real-time systems due to its applicability alongside AI. In particular, my interest revolves around <strong>machine learning, memory systems, computer vision, system programming and deep learning</strong>. My work sits at the integration of <em>theory-driven design</em> and
      <em>production-grade implementation</em>.
    </p>
    <p>
      I recently completed my B.S. in Computer Science and Engineering at
      <a href="https://www.snu.ac.kr" target="_blank" rel="noopener noreferrer">Seoul National University</a>, where my work spanned low-level systems, vision-based systems, compiler-style pipelines, and applied multimodal AI. I did my undergraduate thesis on <a href="/Papers/fer.md" target="_blank" rel="noopener noreferrer">The Application of Facial Emotion Recognition (FER) in the Detection and Measurement of Burnout and Prolonged Stress Levels</a>. My ultimate goal is to create a tech based startup firm related to either machine learning, computer vision or robotics systems into various fields such as AI, medicine or farming.
    </p>
    <h3>Core Research and Engineering Focus</h3>
    <ul>
      <li>
        <strong>Memory Allocation and Runtime Systems</strong><br>
        Design of deterministic, policy-driven, and hierarchical memory allocators (PICAS, DIMCA, DRMAT).
      </li>
      <li>
        <strong>Real-Time Systems and Constraints</strong><br>
        Explicit handling of predictability, fragmentation, priority routing and performance bounds.
      </li>
      <li>
        <strong>Compiler-Style Architectures</strong><br>
        Pass-based pipelines, semantic validation, intermediate representations,
        and backend parity (e.g., SyntraLine++).
      </li>
      <li>
        <strong>Applied Multimodal AI and Vision Based Systems</strong><br>
        End-to-end pipelines combining computer vision, temporal modeling,
        validation metrics, and explainability (FER-based burnout detection).
      </li>
    </ul>
    <h3>My Interpretation About Computer Systems</h3>
    <ul>
      <li>Explicit invariants and clearly defined failure modes</li>
      <li>Mathematical or algorithmic justification before optimization</li>
      <li>Predictability over heuristics in system-critical paths</li>
      <li>Strong documentation and reproducibility as first-class concerns</li>
    </ul>
    <h3>Technical Toolkit</h3>
    <p>
      I work across the full stack of system building from low-level memory and runtime design to applied machine learning pipelines and deployment. Recently, I have also been developing high-level systems and focus on front-end systems by doing web development and learning AWS APIs to comprehend the functionality of modern systems. Below is a practical summary of the tools and environments that I utilized.
    </p>
    <ul>
      <li>
        <strong>Programming Languages:</strong><br>
        Python, C/C++, Rust, Java, C#, SQL, Assembly, Verilog, Javascript, TypeScript, HTML, CSS, Ruby, OCaml and Shell/Bash.
      </li>
      <li>
        <strong>Machine Learning & Vision:</strong><br>
        PyTorch and TensorFlow/Keras for training and experimentation, Hugging Face Transformersvfor NLP workflows, OpenCV for computer vision pipelines, and scikit-learn for classical ML. Whereas for analysis and reporting, NumPy, Pandas, Matplotlib (and occasional Seaborn) are utilized.
      </li>
      <li>
        <strong>Systems, Backend and Deployment:</strong><br>
        Linux/macOS development, Git-based workflows, Docker for reproducible environments, FastAPI/Flask for lightweight services and APIs, Nginx/Apache basics for hosting, and CI with GitHub Actions. Comfortable working remotely over SSH and in terminal-first setups (tmux, Vim).
      </li>
      <li>
        <strong>Hardware and Embedded Exposure:</strong><br>
        Familiar with FPGA/HDL workflows (Verilog/VHDL/SystemVerilog) and prototyping with Arduino / Raspberry Pi for hardware-adjacent experimentation.
      </li>
      <li>
        <strong>Workflow:</strong><br>
        VSCode, Jupyter/Colab, GitHub, Makefiles, LaTeX/Overleaf for technical writing and structured documentation.
      </li>
    </ul>
    <h3>Multilinguality</h3>
    Aside from programming, I am also multilingual in various languages. Below shows all the languages I am capable of speaking, with english as my preferred daily language.
    <ul>
      <li><strong>English</strong> — Native/Fluent</li>
      <li><strong>Indonesian</strong> — Native/Fluent</li>
      <li><strong>Korean</strong> — Advanced/Intermediate </li>
      <li><strong>Japanese</strong> — Fluent/Advanced</li>
      <li><strong>Chinese</strong> — Intermediate/Basic</li>
      <li><strong>German</strong> — Basic</li>
    </ul>
  </div>
  <div class="about-media">

  <!-- Slider 1: Portraits -->
  <div class="about-slider-card">
    {% assign imgs = site.data.about_sliders["about_me"] %}
    {% include project_slider.html images=imgs title="Portraits" %}
  </div>

  <!-- Card 1: Quick facts -->
  <div class="about-side-card">
    <div class="about-side-title">Quick facts</div>
    <ul class="about-facts">
      <li><strong>Base:</strong> Seoul and Jakarta</li>
      <li><strong>Focus:</strong> Memory Systems, Computer Vision, Machine Learning, Real-Time Systems</li>
      <li><strong>Work style:</strong> Applicability, Discussion Based, Research Grade, Detailed Analysis, Debugging</li>
      <li><strong>Open to:</strong> Internship/Work Opportunities, Collaboration, Research Discussion, Team Project</li>
    </ul>
    <div class="about-side-actions">
      <a class="btn" href="/projects/">View Projects</a>
      <a class="btn secondary" href="/contact/">Contact</a>
      <a class="btn ghost" href="https://github.com/rizkysaputradev" target="_blank">GitHub</a>
    </div>
    <p class="muted about-side-note">
      Photos open in full view when clicked.
    </p>
  </div>

  <!-- Slider 2: Work / Systems -->
  <div class="about-slider-card">
    {% assign imgs = site.data.about_sliders["about_work"] %}
    {% include project_slider.html images=imgs title="Work & Systems" %}
  </div>

  <!-- Card 2: Currently -->
  <div class="about-side-card about-now">
    <div class="about-side-title">Currently</div>
    <ul class="about-facts">
      <li><strong>Building:</strong> Customized Memory Allocators (DRMAT/PICAS/DIMCA) and Multimodal Scent Based AI System</li>
      <li><strong>Exploring:</strong> Advanced AI systems, Vision Based Analysis, and Hardware/Software Co-Design</li>
      <li><strong>Interested in:</strong> Internships / Works, Research Discussions and Collaborations</li>
    </ul>
    <div class="about-chips">
      <span class="about-chip">C/C++</span>
      <span class="about-chip">Python</span>
      <span class="about-chip">Rust</span>
      <span class="about-chip">HuggingFace</span>
      <span class="about-chip">OpenCV</span>
      <span class="about-chip">VLLM</span>
      <span class="about-chip">AWS</span>
      <span class="about-chip">Linux</span>
      <span class="about-chip">MacOS</span>
      <span class="about-chip">GitHub</span>
    </div>
    <hr class="about-mini-sep" />
    <p class="muted about-side-note" style="margin-top: 0;">
      Prefer work that’s measurable: correctness, latency, memory, and reproducibility.
    </p>
  </div>
</div>
</div>
