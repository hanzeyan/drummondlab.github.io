---
layout: default
title: Research
permalink: /research/
---

<section class="page-hero page-hero--feature">
  <div class="hero-copy">
    <p class="eyebrow">Research</p>
    <h1>Spatiotemporal dynamics of inflammation</h1>
    <p class="muted"><strong>Click on the grey icons for more details.</strong></p>
  </div>
  <div class="feature-image-wrap">
    <img src="https://static.wixstatic.com/media/d8287f_4b92be91e3f8469394b3ca53be2bbe09~mv2.png/v1/fill/w_652%2Ch_687%2Cal_c%2Cq_90%2Cusm_0.66_1.00_0.01%2Cenc_avif%2Cquality_auto/Untitled%20%284%29.png" alt="Spatiotemporal dynamics of inflammation" class="feature-image">
  </div>
</section>

<section class="section section--soft">
  <div class="section-head">
    <div>
      <p class="eyebrow">Highlights</p>
      <h2>Research directions</h2>
    </div>
  </div>
  <div class="stack-list">
    {% for item in site.data.research %}
      <article class="stack-card">
        <h3>{{ item.title }}</h3>
        <p>{{ item.summary }}</p>
        <ul>
          {% for bullet in item.bullets %}
            <li>{{ bullet }}</li>
          {% endfor %}
        </ul>
      </article>
    {% endfor %}
  </div>
</section>
