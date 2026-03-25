---
layout: default
title: Publications
permalink: /publications/
---

<section class="page-hero page-hero--compact">
  <p class="eyebrow">Publications</p>
  <h1>Publications &amp; Preprints</h1>
  <p># denotes co-first authors; * denotes corresponding authors</p>
</section>

<section class="section section--soft">
  <div class="pub-list">
    {% for item in site.data.publications %}
      <article class="pub-item">
        <div class="pub-meta">{{ item.journal }} <span>•</span> {{ item.date }}</div>
        <div class="pub-title">{% if item.url == '#' %}{{ item.title }}{% else %}<a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>{% endif %}</div>
        <div>{{ item.authors }}</div>
        {% if item.note %}<div class="note">{{ item.note }}</div>{% endif %}
      </article>
    {% endfor %}
  </div>
</section>
