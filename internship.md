---
layout: default
title: Internship
---

<div class="year-section">
  <h2>2025 - Leidos Dynetics</h2>
  <p>Weekly reflections from my role at Leidos Dynetics in Huntsville, AL</p>
  
  <ul class="internship-list">
    {% assign sorted_posts = site.internship_2025 | sort: 'week' %}
    {% for post in sorted_posts reversed %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
</div>

<div class="year-section">
  <h2>2026 - Current Internship</h2>
  <p>Updates from this year's summer internship experience.</p>
  
  {% if site.internship_2026.size > 0 %}
  <ul class="internship-list">
    {% assign sorted_2026 = site.internship_2026 | sort: 'week' %}
    {% for post in sorted_2026 reversed %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
  {% else %}
  <p><em>Coming soon...</em></p>
  {% endif %}
</div>
