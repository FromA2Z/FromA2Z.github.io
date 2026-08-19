---
layout: page
title: 项目
permalink: /works/
---

<div class="works">
  {% for work in site.data.works %}
  <a class="work-card" href="{{ work.link }}" target="_blank" rel="noopener">
    <div class="work-cover">
      <img src="{{ work.image }}" alt="{{ work.title }}" loading="lazy">
    </div>
    <div class="work-body">
      <h2 class="work-title">{{ work.title }}</h2>
      <span class="work-venue">{{ work.venue }}</span>
      <p class="work-desc">{{ work.description }}</p>
      <div class="work-links">
        {% for l in work.links %}
        <span class="work-link">{{ l.label }}</span>
        {% endfor %}
      </div>
    </div>
  </a>
  {% endfor %}
</div>
