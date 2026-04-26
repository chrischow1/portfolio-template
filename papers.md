---
layout: page
title: Papers
subtitle: "Peer-reviewed publications, preprints, and selected talks."
permalink: /papers/
---

<div class="card-grid">
  {% for pub in site.data.publications %}
    <div class="card">
      <h3>{{ pub.title }}</h3>
      <p class="card-meta">{{ pub.authors }}</p>
      <p>{{ pub.venue }} ({{ pub.year }})</p>

      {% if pub.links %}
        <div class="tag-list" style="margin-top: 1rem;">
          {% if pub.links.pdf %}
            <a class="tag" href="{{ pub.links.pdf }}" target="_blank" rel="noopener">PDF</a>
          {% endif %}
          {% if pub.links.code %}
            <a class="tag" href="{{ pub.links.code }}" target="_blank" rel="noopener">Code</a>
          {% endif %}
          {% if pub.links.doi %}
            <a class="tag" href="{{ pub.links.doi }}" target="_blank" rel="noopener">DOI</a>
          {% endif %}
          {% if pub.links.project %}
            <a class="tag" href="{{ pub.links.project }}" target="_blank" rel="noopener">Project</a>
          {% endif %}
        </div>
      {% endif %}
    </div>
  {% endfor %}
</div>
