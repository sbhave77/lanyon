---
layout: page
title: Explainer Pieces
---

<ul>
{% for post in site.posts %}
  {% if post.category == ep %}
    <li>
      {{ post.date | date: "%Y-%m-%d"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
