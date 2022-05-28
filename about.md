---
layout: default
title: About
intro: Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
weight: 2
---

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

{% for team_member in site.team_members %}
<ul>
  <li>Name: {{ team_member.name }}</li>
  <li>Role: {{ team_member.role }}</li>
  <li>Start date: {{ team_member.start }}</li>
  <li>Role: {{ team_member.role }}</li>
</ul>
{% endfor %}

<!--

For some reason, when formatted this way, with basic markup, 
the last list item is wrapping the content in a <p> tag

{% for team_member in site.team_members %}
- Name: {{ team_member.name }}
- Role: {{ team_member.role }}
- Start date: {{ team_member.start }}
- Role: {{ team_member.role }}
{% endfor %}
-->

This is the home page, which uses the default layout.
{: .code}

[Read a post](/2018/03/11/example-post/).
