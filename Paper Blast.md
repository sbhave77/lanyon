---
layout: page
title: Paper Blast
---

<ul>
{% for post in site.posts %}
  {% if post.id == pb %}
    <li>
      {{ post.date | date: "%Y-%m-%d"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
