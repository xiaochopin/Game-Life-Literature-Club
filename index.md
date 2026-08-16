---
layout: default
title: 公告栏
---

# 公告栏

{% assign posts = site.pages | where: "post", true | sort: "date" | reverse %}
<ul class="board">
  {% for item in posts %}
  <li>
    <a class="notice-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
    <span class="notice-date">{{ item.date | date: "%Y-%m-%d" }}</span>
  </li>
  {% endfor %}
</ul>
