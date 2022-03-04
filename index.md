---
title: Thoughts
layout: default
indexed: false
---

<ul>
  {% for page in site.pages %}
    {% if page.indexed %}
      <li><a href="{{ page.url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
