---
layout: default
title: Startseite
---

# Scratch Aufgaben

{% for page in site.pages %}
  {% if page.path contains 'package/' and page.path ends_with '.html' %}
    - [{{ page.name }}]({{ page.url }})
  {% endif %}
{% endfor %}