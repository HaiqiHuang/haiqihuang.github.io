---
layout: default
title: Posts
permalink: /posts/
---

<div class="profile-card">
  <h2 class="card-title">ALL POSTS</h2>
  
  <div class="thinking-list">
    {% for post in site.posts %}
    <div class="thinking-item">
      <a href="{{ post.url | relative_url }}" class="thinking-title">{{ post.title }}</a>
      <div class="thinking-meta">{{ post.date | date: "%B %d, %Y" }}</div>
      <p class="thinking-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
    </div>
    {% endfor %}
  </div>
</div>