---
layout: page
title: Paper Rev
---

<ul>
{% for post in site.posts %}
  {% if post.category == "pb" %}
    <li>
      {{ post.date | date: "%Y-%m-%d"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
