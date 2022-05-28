---
layout: default
title: Work
permalink: /work
weight: 3
---

{% for work in site.collections %}
  <h2>
    <a href="{{ work.url }}">
      {{ work.title }}
      </a>
  </h2>
  <p>{{ work.description }}</p>
{% endfor %}
