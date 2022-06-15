---
layout: default
title: Hello<span class="dark-red">.</span>
intro: Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
exclude: true
weight: 1
---

{% include section-title.html label="My work" %}

<div class="flex">

  <figure class="mr4" style="width:100%; min-width:200px; max-width:300px;">
    <img src="img/wgt-600.png" title="Walmart Global Tech" alt="Walmart Global Tech logo">
    <!-- <figcaption class="plex gray">Walmart Global Tech</figcaption> -->
  </figure>

  <div>
    <p class="mt0 pt0 lh-copy plex f5 f4-m f4-l">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor.
    </p>
    <p class="lh-copy plex f5 f4-m f4-l"><a href="">Read more</a></p>
  </div>

</div>

{% include section-title.html label="About me" %}

{: .mt0 .lh-copy .plex .f5 .f4-m .f4-l}
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

<!--
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
-->
