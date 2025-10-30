---
layout: home
title: SIGPhil repository
nav_order: 1
---

Welcome to the SIGPhil repository. Below is a list of available pages and directories.

<ul>
{% for page in site.pages %}
  {% unless page.name == "index.md" %}
    <li><a href="{{ page.url | relative_url }}">{{ page.title | default: page.path }}</a></li>
  {% endunless %}
{% endfor %}
</ul>
