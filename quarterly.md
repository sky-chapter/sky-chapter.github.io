---
layout: default
title: Quarterly chapters | Sky Chapter
permalink: /quarterly/
---
<h1>Quarterly chapters</h1>
<p class="meta">The season: retrograde cycles, eclipse seasons, major ingresses — soft themes, not promises.</p>
{% assign items = site.quarterly | sort: "date" | reverse %}
{% if items.size > 0 %}
<ul class="index-list">
  {% for q in items %}
  <li><a href="{{ q.url | relative_url }}">{{ q.title }}</a> <span class="meta">· {{ q.period }}</span></li>
  {% endfor %}
</ul>
{% else %}
<p>The first quarterly chapter lands at the <strong>December solstice</strong>.</p>
{% endif %}
