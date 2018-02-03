---
layout: page
title: Opinion
---

<ul>
{% for post in site.posts %}
  {% if post.category == "op" %}
    <li>
      {{ post.date | date: "%Y-%m-%d"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
