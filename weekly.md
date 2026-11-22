---
layout: default
title: Weekly chapters | Sky Chapter
permalink: /weekly/
---
<h1>Weekly chapters</h1>
<p class="meta">Recap of the week behind + what the next week carries.</p>
{% assign items = site.weekly | sort: "date" | reverse %}
{% if items.size > 0 %}
<ul class="index-list">
  {% for w in items %}
  <li><a href="{{ w.url | relative_url }}">{{ w.title }}</a> <span class="meta">· week of {{ w.date | date: "%B %-d, %Y" }}</span></li>
  {% endfor %}
</ul>
{% else %}
<p>Next weekly chapter lands <strong>Sunday 18:00 UTC</strong>.</p>
{% endif %}
