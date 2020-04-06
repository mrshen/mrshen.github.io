---
layout: page
title: Journey
description:世界这么大，你该跟爱的人一起去看看 
menu: 旅行
repositories: false
share: false
comments: false
categories: true
calendar: true
canvas: true
permalink: /journey/
---

{% assign sorted_categories = site.journey | map: "categories" | sort | uniq %}
{% for category in sorted_categories %}
  <h3 name="{{ category }}" id="{{ category}}">{{ category }}</h3>
  <ol class="posts-list">
    {% for article in site.journey %}
      {% for article_category in article.categories %}
        {% if category == article_category %}
          <li class="posts-list-item"><a class="posts-list-name" href="{{ article.url }}">{{ article.title }}</a></li>
        {% endif %}
      {% endfor %}
    {% endfor %}
  </ol>
{% endfor %}
