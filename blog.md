---
title: Blog
subtitle: "Notes, writeups, and system-level thinking"
layout: page
permalink: /blog/
---

<div class="blog-index">

  <div class="blog-intro">
    <p class="muted">
      A collection of technical notes, project writeups, and personal essays.
      Posts may include code, diagrams, and research-style reflections.
    </p>
  </div>

  <!-- BLOG SEARCH -->
  <div class="blog-search-wrap">
    <div class="blog-search">
      <span class="blog-search-icon" aria-hidden="true">⌕</span>
      <input
        id="blogSearch"
        class="blog-search-input"
        type="search"
        placeholder="Search posts by title, tags, or keywords (e.g., compiler, memory, notes)…"
        autocomplete="off"
      />
      <button id="blogSearchClear" class="blog-search-clear" type="button" aria-label="Clear search">
        ×
      </button>
    </div>
    <div id="blogSearchMeta" class="blog-search-meta"></div>
  </div>

  <hr class="blog-separator">

  <div class="blog-list">
    {% if paginator %}
      {% for post in paginator.posts %}
        {% include post_item.html post=post %}
      {% endfor %}
    {% else %}
      {% for post in site.posts %}
        {% include post_item.html post=post %}
      {% endfor %}
    {% endif %}
  </div>

  <div id="blogNoResults" class="blog-no-results" hidden>
    No posts match your search.
  </div>

  {% if paginator %}
    <div class="blog-pagination">
      {% if paginator.previous_page %}
        <a class="btn secondary" href="{{ paginator.previous_page_path }}">Newer</a>
      {% endif %}
      {% if paginator.next_page %}
        <a class="btn secondary" href="{{ paginator.next_page_path }}">Older</a>
      {% endif %}
    </div>
  {% endif %}

</div>

<script>
document.addEventListener("DOMContentLoaded", () => {
  const input = document.getElementById("blogSearch");
  const clearBtn = document.getElementById("blogSearchClear");
  const items = Array.from(document.querySelectorAll(".post-item"));
  const meta = document.getElementById("blogSearchMeta");
  const noRes = document.getElementById("blogNoResults");

  if (!input || items.length === 0) return;

  const normalize = (s) => (s || "").toString().toLowerCase().trim();

  function applyFilter() {
    const q = normalize(input.value);
    const terms = q.split(/\s+/).filter(Boolean);

    let shown = 0;

    for (const item of items) {
      const hay =
        normalize(item.dataset.title) + " " +
        normalize(item.dataset.tags) + " " +
        normalize(item.dataset.cats) + " " +
        normalize(item.dataset.excerpt);

      const ok = terms.length === 0 ? true : terms.every(t => hay.includes(t));

      item.style.display = ok ? "" : "none";
      if (ok) shown++;
    }

    if (meta) {
      meta.textContent = terms.length
        ? `${shown} / ${items.length} shown`
        : `${items.length} posts`;
    }

    if (noRes) noRes.hidden = shown !== 0;
    if (clearBtn) clearBtn.style.visibility = q ? "visible" : "hidden";
  }

  input.addEventListener("input", applyFilter);
  clearBtn?.addEventListener("click", () => {
    input.value = "";
    input.focus();
    applyFilter();
  });

  applyFilter();
});
</script>
