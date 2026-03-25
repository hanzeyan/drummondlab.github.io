---
layout: default
title: News
permalink: /news/
---

<section class="page-hero page-hero--compact">
  <p class="eyebrow">News</p>
  <h1>Latest updates</h1>
</section>

<section class="section section--soft">
  <div class="post-list">
    {% for post in site.posts %}
      <article class="post-card">
        <p class="muted">{{ post.date | date: "%b %-d, %Y" }}</p>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt | strip_html | strip_newlines }}</p>
      </article>
    {% endfor %}
  </div>
</section>
