---
layout: default
title: Home
---

<style>
  .hero-home {
    display: block !important;
    padding-top: 8px;
  }

  .hero-home .hero-visual {
    width: 100%;
    display: flex;
    justify-content: center;
    margin: 0 0 32px 0;
  }

  .hero-home .hero-visual img {
    width: 100%;
    max-width: 1180px;
    height: auto;
    display: block;
    margin: 0 auto;
    border-radius: 18px;
    object-fit: cover;
    box-shadow: 0 10px 28px rgba(15, 23, 42, 0.08);
  }

  .hero-home .hero-copy {
    max-width: 980px;
    margin: 0 auto;
    text-align: left;
  }

  .hero-home .hero-copy .eyebrow {
    margin-bottom: 10px;
    font-size: 0.78rem;
    letter-spacing: 0.08em;
  }

  .hero-home .hero-copy h1 {
    font-size: clamp(1.28rem, 1.85vw, 1.72rem);
    line-height: 1.55;
    font-weight: 600;
    margin: 0 0 16px 0;
    letter-spacing: 0;
    max-width: 920px;
    text-align: justify;
    text-justify: inter-word;
    text-align-last: left;
    hyphens: auto;
  }

  .hero-home .hero-text {
    font-size: 0.92rem;
    line-height: 1.7;
    color: #5f6b7a;
    margin: 0 0 22px 0;
    text-align: justify;
    text-justify: inter-word;
    text-align-last: left;
  }

  .hero-home .cta-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 4px;
  }

  .hero-home .button,
  .hero-home .button.secondary {
    min-width: 160px;
    justify-content: center;
  }

  @media (max-width: 900px) {
    .hero-home .hero-visual img {
      max-width: 100%;
    }

    .hero-home .hero-copy {
      max-width: 100%;
    }

    .hero-home .hero-copy h1 {
      font-size: clamp(1.16rem, 3.6vw, 1.42rem);
      line-height: 1.48;
      text-align: left;
      text-align-last: auto;
      hyphens: none;
    }

    .hero-home .hero-text {
      text-align: left;
      text-align-last: auto;
    }
  }

  @media (max-width: 768px) {
    .hero-home {
      padding-top: 0;
    }

    .hero-home .hero-visual {
      margin-bottom: 22px;
    }

    .hero-home .hero-copy .eyebrow {
      margin-bottom: 8px;
      font-size: 0.74rem;
    }

    .hero-home .hero-copy h1 {
      font-size: clamp(1.08rem, 4.8vw, 1.28rem);
      line-height: 1.45;
      margin-bottom: 12px;
    }

    .hero-home .hero-text {
      font-size: 0.88rem;
      line-height: 1.65;
      margin-bottom: 18px;
    }

    .hero-home .cta-row {
      gap: 10px;
    }

    .hero-home .button,
    .hero-home .button.secondary {
      min-width: 0;
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
