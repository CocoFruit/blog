---
layout: default
title: Home
---

<div class="hero">
  <h2>Hey, I'm Parker Hance</h2>
  <p>I'm a student passionate about technology in its truest sense—not just software and hardware, but the application of knowledge to solve problems. I write about my projects, what I learn, and my experiences along the way.</p>
</div>

<div class="section-card">
  <h2>Recent Posts</h2>
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
  <h2>Internship @ Leidos</h2>
  <p>Follow my summer internship journey with weekly updates and reflections. <a href="{{ '/internship' | relative_url }}">View all →</a></p>
  
  {% assign internship_posts = site.posts | where_exp: "post", "post.title contains 'Internship'" | sort: 'date' | reverse %}
  {% if internship_posts.size > 0 %}
  <ul class="post-list">
    {% for post in internship_posts %}
      <li>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <span class="post-meta">{{ post.date | date: "%B %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
  {% endif %}
</div>

<div class="section-card">
  <h2>Recent Photos</h2>
  <div class="photo-grid">
    <img src="{{ '/assets/images/week1_1.jpg' | relative_url }}" alt="Internship photo 1" loading="lazy">
    <img src="{{ '/assets/images/week1_2.jpg' | relative_url }}" alt="Internship photo 2" loading="lazy">
    <img src="{{ '/assets/images/week1_3.jpg' | relative_url }}" alt="Internship photo 3" loading="lazy">
    <img src="{{ '/assets/images/week1_4.jpg' | relative_url }}" alt="Internship photo 4" loading="lazy">
  </div>
</div>
