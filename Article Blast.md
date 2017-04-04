---
layout: page
title: Article Blast
---

<ul>
{% for post in site.posts %}
  {% if post.category == "ab" %}
    <li>
      {{ post.date | date: "%Y-%m-%d"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
