---
layout: page
title: Publications
subtitle: Papers by and for the MadGraph collaboration.
---

<div class="pub-tabs">

  <nav class="pub-tab-nav" role="tablist" aria-label="Publication categories">
    <button class="pub-tab-btn active" role="tab" aria-selected="true"
            aria-controls="tab-main" data-tab="main">MadGraph releases</button>
    <button class="pub-tab-btn" role="tab" aria-selected="false"
            aria-controls="tab-contributing" data-tab="contributing">Contributing papers</button>
    <button class="pub-tab-btn" role="tab" aria-selected="false"
            aria-controls="tab-external" data-tab="external">External tools</button>
  </nav>

  <div class="pub-tab-panel active" id="tab-main" role="tabpanel">
    <div class="publications-list">
      {% assign pubs_main = site.data.publications.main | sort: 'year' | reverse %}
      {% for pub in pubs_main %}
      <article class="publication-item">
        <div class="pub-header">
          <span class="pub-year">{{ pub.year }}</span>
          <h2 class="pub-title">{{ pub.title }}</h2>
        </div>
        <p class="pub-authors">{{ pub.authors }}</p>
        <div class="pub-meta">
          {% if pub.journal and pub.journal != '' %}<span class="pub-journal">{{ pub.journal }}</span>{% endif %}
          {% if pub.note and pub.note != '' %}<span class="pub-note">{{ pub.note }}</span>{% endif %}
          {% if pub.arxiv and pub.arxiv != '' %}
          <a href="https://arxiv.org/abs/{{ pub.arxiv }}" class="pub-link" target="_blank" rel="noopener noreferrer">
            <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            arXiv:{{ pub.arxiv }}
          </a>
          {% endif %}
          {% if pub.doi and pub.doi != '' %}
          <a href="https://doi.org/{{ pub.doi }}" class="pub-link" target="_blank" rel="noopener noreferrer">
            <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            DOI
          </a>
          {% endif %}
        </div>
      </article>
      {% endfor %}
    </div>
  </div>

  <div class="pub-tab-panel" id="tab-contributing" role="tabpanel">
    <div class="publications-list">
      {% assign pubs_contributing = site.data.publications.contributing | sort: 'year' | reverse %}
      {% for pub in pubs_contributing %}
      <article class="publication-item">
        <div class="pub-header">
          <span class="pub-year">{{ pub.year }}</span>
          <h2 class="pub-title">{{ pub.title }}</h2>
        </div>
        <p class="pub-authors">{{ pub.authors }}</p>
        <div class="pub-meta">
          {% if pub.journal and pub.journal != '' %}<span class="pub-journal">{{ pub.journal }}</span>{% endif %}
          {% if pub.note and pub.note != '' %}<span class="pub-note">{{ pub.note }}</span>{% endif %}
          {% if pub.arxiv and pub.arxiv != '' %}
          <a href="https://arxiv.org/abs/{{ pub.arxiv }}" class="pub-link" target="_blank" rel="noopener noreferrer">
            <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            arXiv:{{ pub.arxiv }}
          </a>
          {% endif %}
          {% if pub.doi and pub.doi != '' %}
          <a href="https://doi.org/{{ pub.doi }}" class="pub-link" target="_blank" rel="noopener noreferrer">
            <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            DOI
          </a>
          {% endif %}
        </div>
      </article>
      {% endfor %}
    </div>
  </div>

  <div class="pub-tab-panel" id="tab-external" role="tabpanel">
    <div class="publications-list">
      {% assign pubs_external = site.data.publications.external | sort: 'year' | reverse %}
      {% for pub in pubs_external %}
      <article class="publication-item">
        <div class="pub-header">
          <span class="pub-year">{{ pub.year }}</span>
          <h2 class="pub-title">{{ pub.title }}</h2>
        </div>
        <p class="pub-authors">{{ pub.authors }}</p>
        <div class="pub-meta">
          {% if pub.journal and pub.journal != '' %}<span class="pub-journal">{{ pub.journal }}</span>{% endif %}
          {% if pub.note and pub.note != '' %}<span class="pub-note">{{ pub.note }}</span>{% endif %}
          {% if pub.arxiv and pub.arxiv != '' %}
          <a href="https://arxiv.org/abs/{{ pub.arxiv }}" class="pub-link" target="_blank" rel="noopener noreferrer">
            <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            arXiv:{{ pub.arxiv }}
          </a>
          {% endif %}
          {% if pub.doi and pub.doi != '' %}
          <a href="https://doi.org/{{ pub.doi }}" class="pub-link" target="_blank" rel="noopener noreferrer">
            <svg width="11" height="11" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
            DOI
          </a>
          {% endif %}
        </div>
      </article>
      {% endfor %}
    </div>
  </div>

</div>

<script>
(function() {
  var buttons = document.querySelectorAll('.pub-tab-btn');
  var panels  = document.querySelectorAll('.pub-tab-panel');

  function activate(tab) {
    buttons.forEach(function(b) {
      var match = b.dataset.tab === tab;
      b.classList.toggle('active', match);
      b.setAttribute('aria-selected', String(match));
    });
    panels.forEach(function(p) { p.classList.remove('active'); });
    var panel = document.getElementById('tab-' + tab);
    if (panel) panel.classList.add('active');
  }

  buttons.forEach(function(btn) {
    btn.addEventListener('click', function() {
      history.replaceState(null, '', '#' + btn.dataset.tab);
      activate(btn.dataset.tab);
    });
  });

  var hash = location.hash.replace('#', '');
  var valid = Array.from(buttons).some(function(b) { return b.dataset.tab === hash; });
  if (valid) activate(hash);
})();
</script>
