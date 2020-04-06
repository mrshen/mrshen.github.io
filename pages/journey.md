---
layout: journey
title: Journey
description: 世界那么大，你应该跟爱的人一起去看看
keywords: 旅行, journey
comments: false
share: false
repositories: false
categories: true
canvas: true
menu: 旅行
permalink: /journey/
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
