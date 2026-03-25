---
layout: default
title: Resources
permalink: /resources/
---

<section class="page-hero page-hero--compact">
  <p class="eyebrow">Resources</p>
  <h1>Lab Protocols</h1>
</section>

<section class="section section--soft">
  <div class="resource-grid">
    {% for block in site.data.resources %}
      <article class="resource-card">
        <h3>{{ block.category }}</h3>
        {% if block.items.size > 0 %}
        <ul>
          {% for item in block.items %}
            <li>{{ item }}</li>
          {% endfor %}
        </ul>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</section>
