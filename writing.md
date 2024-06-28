---
layout: default
title: Writing<span class="dark-red">.</span>
navlabel: Writing
intro: Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
exclude: true
weight: 4
---

{: .lh-copy .plex .f5 .f4-m .f4-l}
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

{% include section-title.html label="Articles" %}

<ul class="list ma0 pa0">
  {% for post in site.posts %}
  <li class="pb3 lh-copy mb4 blog-link">
    <span class="db plexb f5 silver lh-copy">{{ post.date | date: "%b %-d,  %Y" }}</span>
    <span class="db plex f5 f4-m f4-l lh-copy"><a class="link dim" href="{{ post.url }}">{{ post.title }}</a></span>
  </li>
  {% endfor %}
</ul>
