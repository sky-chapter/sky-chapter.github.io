---
layout: default
title: Yearly chapters | Sky Chapter
permalink: /yearly/
---
<h1>Yearly chapters</h1>
<p class="meta">«20XX for your sign» — long-range, very softly worded.</p>
{% assign items = site.yearly | sort: "date" | reverse %}
{% if items.size > 0 %}
<ul class="index-list">
  {% for y in items %}
  <li><a href="{{ y.url | relative_url }}">{{ y.title }}</a> <span class="meta">· {{ y.period }}</span></li>
  {% endfor %}
</ul>
{% else %}
<p>The yearly chapter is written at year's end, <strong>31 December 21:00 UTC</strong>.</p>
{% endif %}
