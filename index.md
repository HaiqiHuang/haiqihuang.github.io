---
layout: default
title: Haiqi Huang
---

<!-- Education 卡片模块 -->
<div class="profile-card">
  <h2 class="card-title">EDUCATION</h2>
  
  <ul class="education-list">
    {% for edu in site.data.education %}
    <li>
      <div class="degree-name">{{ edu.degree }}</div>
      <div class="degree-meta">{{ edu.school }} &bull; {{ edu.year }}</div>
      
      {% if edu.details %}
        <ul class="degree-details-list">
          {% for detail in edu.details %}
            <li>{{ detail }}</li>
          {% endfor %}
        </ul>
      {% endif %}

    </li>
    {% endfor %}
  </ul>
</div>

<!-- Latest Thinking 卡片模块 -->
<div class="profile-card">
  <h2 class="card-title">LATEST THINKING</h2>
  
  <div class="thinking-list">
    <!-- 循环读取最近的 3 篇文章 -->
    {% for post in site.posts limit:3 %}
    <div class="thinking-item">
      <!-- 文章标题和链接 -->
      <a href="{{ post.url | relative_url }}" class="thinking-title">{{ post.title }}</a>
      
      <!-- 文章日期 -->
      <div class="thinking-meta">{{ post.date | date: "%B %d, %Y" }}</div>
      
      <!-- 文章摘要 (自动截取前 20 个词) -->
      <p class="thinking-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
    </div>
    {% endfor %}
  </div>
</div>