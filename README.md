# 🖥️ **GitHub Personal Website (rizkysaputradev.github.io)**

Personal academic and engineering work related website for **Rizky Johan Saputra**. This site serves as a central hub:

- Research and systems work (memory allocation, compilers, multimodal AI)
- Project documentation and write-ups
- Blog posts and technical reflections
- Contact and academic materials (papers, slides, CV)

The site is built with **Jekyll** and hosted via **GitHub Pages**.

## 🎄 **Project Structure**
```graphql
.(root)
├── _config.yml            # Jekyll configuration
├── _layouts/              # Page, post, and default layouts
├── _includes/             # Reusable components (nav, footer, sliders, etc.)
├── _posts/                # Blog posts (Markdown)
├── projects/              # Project pages
├── Papers/                # Research papers and writeups
├── assets/
│   ├── css/               # Styles (SCSS/CSS)
│   ├── img/               # Images (blog covers, sliders, etc.)
│   ├── js/                # Client-side scripts
│    └── ...
├── about.md               # About page
├── research.md            # Research & systems overview
├── blog/                  # Blog index and pagination
├── contact.md             # Contact page
├── index.md               # Homepage
└── README.md
```

## 🦺 **Local Development**
### 📚 **Prerequisites**
- Ruby (`>= 2.7` recommended)
- Bundler
- Jekyll

---

### 🔩 **Install dependencies**
```bash
bundle install
```

---

### 👟 **Local Run**
``` bash
bundle exec jekyll serve
```

The site will be available at the following URL via local run:
```bash
http://localhost:4000
```

## ⚙️ **Deployment**
The site is automatically deployed via GitHub Pages from the main branch with a repo name of:
```bash
rizkysaputradev.github.io
```
Notes
- Dark mode is the default theme, with a manual light/dark toggle.
- Content is written in Markdown with HTML and some JavaScript used selectively for layout control.
- Research artifacts (papers, slides) are hosted directly in the repository.

## 👤 **Author and Credentials**
This project is fully established and contributed by the following author and co-authors:
- **Name:** Rizky Johan Saputra
- **Role:** Website Developer, Manager and Author 
- **Project Scope:** Web Development, Front-End Systems, Computer Networks

## 📜 **License**
This repository is distributed under a Personal License tailored by the author. See LICENSE for the full terms. For further inquiries and requests, please contact via GitHub or Email only.
> If you intend to reuse significant portions for research and academia purposes, please open and inquire an issue to discuss attribution and terms.