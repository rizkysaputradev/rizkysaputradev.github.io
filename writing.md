---
title: Research Papers and Documentations
subtitle: "Research Paper, Thesis Dissertation, Technical Documentations, and Personal Notes"
---

<div class="list">
{% for pub in site.data.publications %}
  {% include publication_item.html pub=pub %}
{% endfor %}
</div>
