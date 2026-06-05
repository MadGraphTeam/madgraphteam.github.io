---
layout: page
title: Publications
subtitle: Key papers published by the MadGraph collaboration members.
---

<div class="publications-list">
{% for pub in site.data.publications %}
<article class="publication-item">

  <div class="pub-header">
    <span class="pub-year">{{ pub.year }}</span>
    <h2 class="pub-title">{{ pub.title }}</h2>
  </div>

  <p class="pub-authors">{{ pub.authors }}</p>

  <div class="pub-meta">
    {% if pub.journal and pub.journal != '' %}
    <span class="pub-journal">{{ pub.journal }}</span>
    {% endif %}

    {% if pub.note and pub.note != '' %}
    <span class="pub-note">{{ pub.note }}</span>
    {% endif %}

    {% if pub.arxiv and pub.arxiv != '' %}
    <a href="https://arxiv.org/abs/{{ pub.arxiv }}" class="pub-link" target="_blank" rel="noopener noreferrer">
      <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
        <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/>
        <polyline points="15 3 21 3 21 9"/>
        <line x1="10" y1="14" x2="21" y2="3"/>
      </svg>
      arXiv:{{ pub.arxiv }}
    </a>
    {% endif %}

    {% if pub.doi and pub.doi != '' %}
    <a href="https://doi.org/{{ pub.doi }}" class="pub-link" target="_blank" rel="noopener noreferrer">
      <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
        <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/>
        <polyline points="15 3 21 3 21 9"/>
        <line x1="10" y1="14" x2="21" y2="3"/>
      </svg>
      DOI
    </a>
    {% endif %}
  </div>

</article>
{% endfor %}
</div>
