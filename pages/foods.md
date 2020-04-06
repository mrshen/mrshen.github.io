---
layout: page
title: Foods
description: 唯美食与爱不可辜负
comments: false
canvas: true
menu: 美食
permalink: /foods/
---

<div>
  {% assign sorted_categories = site.categories | sort %}
  {% for category in sorted_categories %}
    <h3 id="{{ category[0] }}" name="{{ category[0] }}">{{ category | first }}</h3>
    <ol class="posts-list">
      {% for post in category.last %}
        <li class="posts-list-item">
          <span class="posts-list-meta">{{ post.date | date:"%Y-%m-%d" }}</span>
          <a class="posts-list-name" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ol>
  {% endfor %}
</div>
