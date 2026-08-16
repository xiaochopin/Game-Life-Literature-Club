---
layout: default
title: 公告栏
---

# 公告栏

{% assign posts = site.pages | where: "post", true | sort: "name" | reverse %}
<ul class="board">
  {% for item in posts %}
  {% assign name_parts = item.name | split: "-" %}
  {% assign post_date = name_parts[0] | append: "-" | append: name_parts[1] | append: "-" | append: name_parts[2] %}
  <li>
    <a class="notice-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
    <span class="notice-date">{{ post_date }}</span>
  </li>
  {% endfor %}
</ul>
