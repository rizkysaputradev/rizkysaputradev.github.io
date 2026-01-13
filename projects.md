---
title: Projects
subtitle: "Computer Science and Engineering (CSE) projects ranging from low-level hardware machines to high-level AI optimization systems"
---

<div class="project-search-wrap">
  <div class="project-search">
    <span class="project-search-icon" aria-hidden="true">⌕</span>
    <input
      id="projectSearch"
      class="project-search-input"
      type="search"
      placeholder="Search projects by title or tags (e.g., allocator, compiler, pytorch)…"
      autocomplete="off"
    />
    <button id="projectSearchClear" class="project-search-clear" type="button" aria-label="Clear search">
      ×
    </button>
  </div>

  <div id="projectSearchMeta" class="project-search-meta"></div>
</div>

<div class="grid">
  {% for p in site.data.projects %}
    {% include project_card.html project=p %}
  {% endfor %}
</div>

<div id="projectNoResults" class="project-no-results" hidden>
  No projects match your search.
</div>

<script>
document.addEventListener("DOMContentLoaded", () => {
  const input = document.getElementById("projectSearch");
  const clearBtn = document.getElementById("projectSearchClear");
  const cards = Array.from(document.querySelectorAll(".project-card"));
  const meta = document.getElementById("projectSearchMeta");
  const noRes = document.getElementById("projectNoResults");

  if (!input || cards.length === 0) return;

  const normalize = (s) => (s || "").toString().toLowerCase().trim();

  function applyFilter() {
    const q = normalize(input.value);
    const terms = q.split(/\s+/).filter(Boolean);

    let shown = 0;

    for (const card of cards) {
      const hay =
        normalize(card.dataset.title) + " " +
        normalize(card.dataset.tags) + " " +
        normalize(card.dataset.desc);

      const ok = terms.length === 0 ? true : terms.every(t => hay.includes(t));

      card.style.display = ok ? "" : "none";
      if (ok) shown++;
    }

    if (meta) {
      meta.textContent = terms.length
        ? `${shown} / ${cards.length} shown`
        : `${cards.length} projects`;
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
