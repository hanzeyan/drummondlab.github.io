---
layout: default
title: Book Chapter & Review
permalink: /book-chapter-review/
---

<section class="page-hero page-hero--compact">
  <p class="eyebrow">Publications</p>
  <h1>Book Chapter &amp; Review</h1>
</section>

<section class="section section--soft">
  <div class="review-list">
    {% for item in site.data.reviews %}
      <article class="pub-item">
        <div class="pub-meta">{{ item.journal }} <span>•</span> {{ item.date }}</div>
        <div class="pub-title"><a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a></div>
        <div>{{ item.authors }}</div>
        {% if item.note %}<div class="note">{{ item.note }}</div>{% endif %}
      </article>
    {% endfor %}
  </div>
</section>
