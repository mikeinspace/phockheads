---
layout: home
title: Home
exclude: true
---

<ul class="assets">
{% for series in site.series %}
  <li>
  {% if series.image != '' %}
    <img src="{{ series.image }}">
  {% endif %}
    <a href="series/{{ series.name | downcase }}">
      <b>{{ series.name }}</b>
    </a>
    <p class="small">Artist: {{ series.author }}</p>
  </li>
{% endfor %}
</ul>