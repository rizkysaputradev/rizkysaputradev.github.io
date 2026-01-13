---
title: Contact
layout: page
permalink: /contact/
---

<div class="contact-grid">

  <!-- LEFT: Contact panel + form -->
  <div class="contact-panel">
    <div class="contact-header">
      <h2 class="contact-title">For professional inquiries and detailed information</h2>
      <p class="contact-subtitle muted">
        Reply is to be expected within 24–48 hours depending on the requests.
      </p>
    </div>

    <div class="contact-links">
      <a class="contact-link" href="mailto:flamablesrizky@gmail.com">
        <span class="contact-link-label">Email</span>
        <span class="contact-link-value">flamablesrizky@gmail.com</span>
      </a>

      <a class="contact-link" href="https://github.com/rizkysaputradev" target="_blank" rel="noopener noreferrer">
        <span class="contact-link-label">GitHub</span>
        <span class="contact-link-value">rizkysaputradev</span>
      </a>

      <a class="contact-link" href="https://www.linkedin.com/in/rizky-johan-saputra/" target="_blank" rel="noopener noreferrer">
        <span class="contact-link-label">LinkedIn</span>
        <span class="contact-link-value">rizky-johan-saputra</span>
      </a>
    </div>

    <div class="contact-form-card">
      <div class="contact-form-title">Send a message</div>

      <form id="contactForm" class="contact-form" autocomplete="on">
        <div class="contact-row">
          <div class="contact-field">
            <label for="cf_name">Name</label>
            <input id="cf_name" name="name" type="text" placeholder="Name / Recruiter / Institution / ..." required>
          </div>

          <div class="contact-field">
            <label for="cf_email">Email</label>
            <input id="cf_email" name="email" type="email" placeholder="you@example.com" required>
          </div>
        </div>

        <div class="contact-row">
          <div class="contact-field">
            <label for="cf_type">Inquiry</label>
            <select id="cf_type" name="type">
              <option value="Internship / Hiring">Internship / Work</option>
              <option value="Research / Lab">Research / Lab</option>
              <option value="Collaboration">Collaboration</option>
              <option value="Project Question">Project Question</option>
              <option value="Other">Other</option>
            </select>
          </div>

          <div class="contact-field">
            <label for="cf_subject">Subject</label>
            <input id="cf_subject" name="subject" type="text" placeholder="Work Related / Research Collaboration / ..." required>
          </div>
        </div>

        <div class="contact-field">
          <label for="cf_message">Message</label>
          <textarea id="cf_message" name="message" rows="6" placeholder="Write your message here…" required></textarea>
          <div class="contact-hint muted">
          </div>
        </div>

        <div class="contact-actions">
          <button class="btn" type="submit">Open Email</button>
          <a class="btn secondary" href="mailto:flamablesrizky@gmail.com">Email Directly</a>
        </div>
      </form>
    </div>
  </div>

<!-- RIGHT: Locations (Seoul + Jakarta) -->
<div class="contact-map-card">
  <div class="contact-map-head">
    <div class="contact-map-title">Locations</div>
    <div class="contact-map-note muted">OpenStreetMap · Leaflet</div>
  </div>

  <div class="contact-locations">
    <!-- SEOUL -->
    <div class="contact-location">
      <div class="contact-location-head">
        <div class="contact-location-title">Based in Seoul</div>
        <div class="contact-location-sub muted">South Korea · KST (UTC+9)</div>
      </div>
      <div id="mapSeoul" class="contact-map"></div>
    </div>

    <hr class="contact-location-sep">

    <!-- JAKARTA -->
    <div class="contact-location">
      <div class="contact-location-head">
        <div class="contact-location-title">Also based in Jakarta</div>
        <div class="contact-location-sub muted">Indonesia · WIB (UTC+7)</div>
      </div>
      <div id="mapJakarta" class="contact-map"></div>
    </div>
  </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", function () {
  // ---------------------------
  // 1) Leaflet maps (retina tiles)
  // ---------------------------
  if (window.L) {
    const tileUrl = "https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png";
    const tileOpts = {
      attribution: '© OpenStreetMap contributors © CARTO',
      maxZoom: 20,
      detectRetina: true
    };

    const makeMap = (id, center, zoom, label) => {
      const el = document.getElementById(id);
      if (!el) return null;

      const m = L.map(id, {
        zoomControl: true,
        scrollWheelZoom: false,
        preferCanvas: true
      }).setView(center, zoom);

      L.tileLayer(tileUrl, tileOpts).addTo(m);

      L.marker(center).addTo(m).bindPopup(label);

      // Fix “half-rendered / blurry / grey tiles” issues when maps are inside flex/cards
      setTimeout(() => m.invalidateSize(), 50);

      return m;
    };

    // Seoul
    makeMap(
      "mapSeoul",
      [37.5665, 126.9780],
      12,
      "Based in Seoul, South Korea"
    );

    // Jakarta
    makeMap(
      "mapJakarta",
      [-6.2088, 106.8456],
      11,
      "Also based in Jakarta, Indonesia"
    );
  }

  // ---------------------------
  // 2) Form -> mailto (no backend)
  // ---------------------------
  const form = document.getElementById("contactForm");
  if (!form) return;

  form.addEventListener("submit", function (e) {
    e.preventDefault();

    const name = document.getElementById("cf_name")?.value?.trim() || "";
    const email = document.getElementById("cf_email")?.value?.trim() || "";
    const type = document.getElementById("cf_type")?.value?.trim() || "Inquiry";
    const subjectRaw = document.getElementById("cf_subject")?.value?.trim() || "Hello";
    const message = document.getElementById("cf_message")?.value?.trim() || "";

    const subject = `[${type}] ${subjectRaw}`;
    const body =
`Name: ${name}
Email: ${email}
Inquiry: ${type}

Message:
${message}
`;

    const mailto = `mailto:flamablesrizky@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
    window.location.href = mailto;
  });
});
</script>
