---
layout: page
title: Team
subtitle: An international collaboration of particle physicists advancing Monte Carlo simulation.
---

{% for institution in site.data.team.institutions %}
<div class="institution-block">

  <div class="institution-header">
    <div class="institution-icon" aria-hidden="true">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>
        <polyline points="9 22 9 12 15 12 15 22"/>
      </svg>
    </div>
    <div>
      <div class="institution-name">{{ institution.name }}</div>
      <div class="institution-location">{{ institution.location }}</div>
    </div>
    {% if institution.url %}
    <a href="{{ institution.url }}" class="institution-link" target="_blank" rel="noopener noreferrer">
      Visit website ↗
    </a>
    {% endif %}
  </div>

  <div class="members-grid">
    {% for member in institution.members %}
    <div class="member-card">
      <div class="member-photo-wrap">
        {% if member.photo %}
        <img src="{{ member.photo | relative_url }}" alt="{{ member.name }}">
        {% else %}
        <div class="photo-placeholder" aria-hidden="true">
          <svg width="48" height="48" viewBox="0 0 100 100" fill="none">
            <circle cx="50" cy="36" r="18" fill="#8998b0"/>
            <ellipse cx="50" cy="86" rx="32" ry="24" fill="#8998b0"/>
          </svg>
        </div>
        {% endif %}
      </div>
      <div class="member-info">
        <div class="member-name">{{ member.name }}</div>
        <div class="member-role">{{ member.role }}</div>
      </div>
    </div>
    {% endfor %}
  </div>

</div>
{% endfor %}
