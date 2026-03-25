---
layout: default
title: Home
---

<style>
  .hero-home {
    display: block !important;
  }

  .hero-home .hero-visual {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-bottom: 28px;
  }

  .hero-home .hero-visual img {
    width: 100%;
    max-width: 1250px;
    height: auto;
    display: block;
    margin: 0 auto;
    border-radius: 18px;
    object-fit: cover;
  }

  .hero-home .hero-copy {
    max-width: 1000px;
    margin: 0 auto;
    text-align: left;
  }

  .hero-home .hero-copy .eyebrow {
    margin-bottom: 8px;
    font-size: 0.78rem;
  }

  .hero-home .hero-copy h1 {
    font-size: clamp(1.45rem, 2vw, 1.9rem);
    line-height: 1.35;
    font-weight: 650;
    margin-bottom: 14px;
    letter-spacing: -0.01em;
    max-width: 900px;
  }

  .hero-home .hero-text {
    font-size: 0.9rem;
    line-height: 1.6;
    color: #5f6b7a;
    margin-bottom: 18px;
  }

  .hero-home .cta-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  @media (max-width: 768px) {
    .hero-home .hero-visual {
      margin-bottom: 20px;
    }

    .hero-home .hero-visual img {
      max-width: 100%;
    }

    .hero-home .hero-copy h1 {
      font-size: clamp(1.2rem, 4.8vw, 1.6rem);
      line-height: 1.32;
    }

    .hero-home .hero-text {
      font-size: 0.88rem;
    }
  }
</style>

<section class="hero hero-home">
  <div class="hero-visual">
    <img src="{{ '/assets/images/d8287f_0e49b76980534dde9b8fa21eca252854~mv2.avif' | relative_url }}" alt="实验室首页图">
  </div>

  <div class="hero-copy">
    <p class="eyebrow">{{ site.data.site.lab_name }}</p>
    <h1>{{ site.data.site.intro }}</h1>
    <p class="hero-text">{{ site.data.site.tagline }}</p>
    <div class="cta-row">
      <a class="button" href="{{ '/research/' | relative_url }}">Explore Research</a>
      <a class="button secondary" href="{{ '/publications/' | relative_url }}">View Publications</a>
    </div>
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
