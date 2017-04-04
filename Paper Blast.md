---
layout: page
title: Paper Blast
---

<ul>
{% for post in site.paperposts %}
  <li>
    {{ post.date | date: "%Y-%m-%d"  }} &mdash; <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
