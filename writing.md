---
layout: default
title: Writing<span class="hilight">.</span>
navlabel: Writing
intro: Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
exclude: false
weight: 2
---

{% include section-title.html label="Articles" %}

<ul class="list mt4 mr0 mb0 ml0 pa0">
  {% for post in site.posts %}
  <li class="pb3 lh-copy mb4 blog-link">
    <span class="db plexb f5 silver lh-copy">{{ post.date | date: "%b %-d,  %Y" }}</span>
    <span class="db plex f5 f4-m f4-l lh-copy"><a class="link dim" href="{{ post.url }}">{{ post.title }}</a></span>
  </li>
  {% endfor %}
</ul>
