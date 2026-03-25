---
layout: default
title: Home
---

<section class="hero hero-home">
  <div class="hero-copy">
    <p class="eyebrow">{{ site.data.site.lab_name }}</p>
    <h1>{{ site.data.site.intro }}</h1>
    <p class="hero-text">{{ site.data.site.tagline }}</p>
    <div class="cta-row">
      <a class="button" href="{{ '/research/' | relative_url }}">Explore Research</a>
      <a class="button secondary" href="{{ '/publications/' | relative_url }}">View Publications</a>
    </div>
  </div>
  <div class="hero-visual">
    <div align="center" style="margin: 20px 0;">
  <img src="{{ '/assets/images/d8287f_0e49b76980534dde9b8fa21eca252854~mv2.avif' | relative_url }}" alt="实验室首页图" style="max-width: 800px; width: 100%;">
</div>
    {% for item in site.data.home_research limit:4 %}
      <article class="visual-card">
        <img src="{{ item.image }}" alt="{{ item.title }}">
        <div class="visual-card__label">{{ item.title }}</div>
      </article>
    {% endfor %}
  </div>
</section>

<section class="section section--soft">
  <div class="section-head">
    <div>
      <p class="eyebrow">Research Area</p>
      <h2>Focus areas</h2>
    </div>
    <a class="text-link" href="{{ '/research/' | relative_url }}">Read More</a>
  </div>
  <div class="grid grid-2">
    {% for item in site.data.home_research %}
      <article class="card research-card">
        <img src="{{ item.image }}" alt="{{ item.title }}">
        <div class="card-body">
          <h3>{{ item.title }}</h3>
          <p>{{ item.description }}</p>
        </div>
      </article>
    {% endfor %}
  </div>
</section>

<section class="section two-col-section">
  <div>
    <div class="section-head">
      <div>
        <p class="eyebrow">News</p>
        <h2>Latest updates</h2>
      </div>
      <a class="text-link" href="{{ '/news/' | relative_url }}">All News</a>
    </div>
    <div class="post-list">
      {% for post in site.posts limit:3 %}
        <article class="post-card">
          <p class="muted">{{ post.date | date: "%b %-d, %Y" }}</p>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p>{{ post.excerpt | strip_html | strip_newlines }}</p>
        </article>
      {% endfor %}
    </div>
  </div>
  <div>
    <div class="section-head">
      <div>
        <p class="eyebrow">Publications</p>
        <h2>Selected papers</h2>
      </div>
      <a class="text-link" href="{{ '/publications/' | relative_url }}">All Publications</a>
    </div>
    <div class="compact-list">
      {% for item in site.data.publications limit:4 %}
        <article class="compact-item">
          <p class="compact-meta">{{ item.journal }} | {{ item.date }}</p>
          <h3>
            {% if item.url == '#' %}
              {{ item.title }}
            {% else %}
              <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>
            {% endif %}
          </h3>
          <p>{{ item.authors }}</p>
        </article>
      {% endfor %}
    </div>
  </div>
</section>
