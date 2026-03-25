---
layout: default
title: Team
permalink: /team/
---

<section class="page-hero page-hero--split">
  <div>
    <p class="eyebrow">Team</p>
    <h1>About Us</h1>
    <p>A collaborative team with expertise and research background in computational biology, single-cell and spatial multi-omics, immunology, neuroscience, microbiology, protein engineering and synthetic biology.</p>
  </div>
  <div class="hero-badge-list">
    <span>Computational Biology</span>
    <span>Single-cell &amp; Spatial Multi-omics</span>
    <span>Immunology</span>
    <span>Neuroscience</span>
    <span>Microbiology</span>
    <span>Protein Engineering</span>
    <span>Synthetic Biology</span>
  </div>
</section>

<section class="section section--soft">
  <div class="section-head">
    <div>
      <p class="eyebrow">Members</p>
      <h2>Current team</h2>
    </div>
  </div>
  <div class="team-grid">
    {% for member in site.data.team %}
      <article class="card member-card">
        <img src="{{ member.image }}" alt="{{ member.name }}">
        <div class="card-body">
          <h3>{{ member.name }}</h3>
          <p class="member-meta">{{ member.role }}</p>
          {% for line in member.lines %}<p>{{ line }}</p>{% endfor %}
          {% if member.link %}<p><a href="{{ member.link }}" target="_blank" rel="noopener noreferrer">{{ member.link }}</a></p>{% endif %}
        </div>
      </article>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section-head">
    <div>
      <p class="eyebrow">Affiliation</p>
      <h2>Institutional links</h2>
    </div>
  </div>
  <div class="logo-grid">
    {% for item in site.data.affiliations %}
      <div class="logo-card"><img src="{{ item.image }}" alt="{{ item.title }}"></div>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section-head">
    <div>
      <p class="eyebrow">Consortium</p>
      <h2>Collaborative network</h2>
    </div>
  </div>
  <div class="logo-grid">
    {% for item in site.data.consortium %}
      <div class="logo-card"><img src="{{ item.image }}" alt="{{ item.title }}"></div>
    {% endfor %}
  </div>
</section>
