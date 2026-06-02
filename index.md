---
layout: default
title: Home
---

<div class="hero">
  <h2>Hey, I'm Parker Hance 👋</h2>
  <p>Student passionate about software engineering, AI, and machine learning. Currently interning at Leidos. I write about my projects, learnings, and experiences in tech.</p>
</div>

<div class="section-card">
  <h2>📝 Recent Posts</h2>
  {% if site.posts.size > 0 %}
  <ul class="post-list">
    {% for post in site.posts limit:5 %}
      <li>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
        {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
  {% else %}
  <p>No posts yet. Check back soon as I share my journey!</p>
  {% endif %}
</div>

<div class="section-card">
  <h2>💼 Internship @ Leidos</h2>
  <p>Follow my summer 2026 internship journey with weekly updates, photos, and reflections. <a href="{{ '/internship' | relative_url }}">View all weeks →</a></p>
  
  {% assign recent_weeks = site.internship_2026 | sort: 'week' | reverse %}
  {% if recent_weeks.size > 0 %}
  <ul class="post-list">
    {% for week in recent_weeks limit:3 %}
      <li>
        <h3><a href="{{ week.url | relative_url }}">{{ week.title }}</a></h3>
        <span class="post-meta">Week {{ week.week }}</span>
      </li>
    {% endfor %}
  </ul>
  {% endif %}
</div>

<div class="section-card">
  <h2>📸 Recent Photos</h2>
  <div class="photo-grid">
    <img src="{{ '/assets/images/week1_1.jpg' | relative_url }}" alt="Internship photo 1" loading="lazy">
    <img src="{{ '/assets/images/week1_2.jpg' | relative_url }}" alt="Internship photo 2" loading="lazy">
    <img src="{{ '/assets/images/week1_3.jpg' | relative_url }}" alt="Internship photo 3" loading="lazy">
    <img src="{{ '/assets/images/week1_4.jpg' | relative_url }}" alt="Internship photo 4" loading="lazy">
  </div>
</div>
