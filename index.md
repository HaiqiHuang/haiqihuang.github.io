---
layout: default
title: My Personal Blog
---

<h1>Latest Thinking</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <span>{{ post.date | date: "%Y-%m-%d" }}</span> &raquo; 
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>