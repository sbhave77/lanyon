---
layout: default
title: ML Lectures
---

<ul>
{% for post in site.posts %}
  {% if post.category == "ml" %}
    <li>
      {{ post.date | date: "%Y-%m-%d"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
