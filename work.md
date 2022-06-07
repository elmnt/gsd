---
layout: work
title: Work
intro: Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
weight: 3
---

{% include section-title.html label="Shizzle" %}

{% include button.html label="Shizzle" %}

{: .lh-copy .plex .f5 .f4-m .f4-l}
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

<figure>
  <img src="img/coffee.jpg" alt="Coffee">
  <figcaption class="plex gray">You're addicted to coffee</figcaption>
</figure>

{% for team_member in site.team_members %}
<ul class="plex lh-copy f5">
  <li>Name: {{ team_member.name }}</li>
  <li>Role: {{ team_member.role }}</li>
  <li>Start date: {{ team_member.start }}</li>
  <li>Role: {{ team_member.role }}</li>
</ul>
{% endfor %}

{: .plex .lh-copy .f5}
[Read a post](/2018/03/11/example-post/).
