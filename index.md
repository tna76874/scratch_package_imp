---
layout: default
title: Scratch IMP Kontaktstudium 2023/2024
---

# Scratch IMP Kontaktstudium 2023/2024

{% for file in site.static_files %}
  {% if file.path contains 'packages/' and file.extname == '.html' %}
    {% assign file_parts = file.name | split: '_' %}
    {% if file_parts.size == 2 %}
        {% assign index = file_parts[1] | remove: '.html' | plus: 0 %}
        {% assign filename_without_extension = file.name | remove: '.html' %}
[{{ filename_without_extension }}](packages/{{ file.name }})
    {% endif %}
  {% endif %}
{% endfor %}