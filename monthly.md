---
layout: default
title: Monthly chapters | Sky Chapter
permalink: /monthly/
---
<h1>Monthly chapters</h1>
<p class="meta">The month in one line: retrogrades, ingresses, Moon phases, and a line per sign.</p>
{% assign items = site.monthly | sort: "date" | reverse %}
{% if items.size > 0 %}
<ul class="index-list">
  {% for m in items %}
  <li><a href="{{ m.url | relative_url }}">{{ m.title }}</a> <span class="meta">· {{ m.period }}</span></li>
  {% endfor %}
</ul>
{% else %}
<p>The next monthly chapter is prepared on the last day of this month, <strong>20:00 UTC</strong>.</p>
{% endif %}
