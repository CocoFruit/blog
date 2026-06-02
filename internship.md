---
layout: default
title: Internship
---

<div class="year-section">
  <h2>Summer Internships at Leidos Dynetics</h2>
  <p>Weekly reflections from my internships at Leidos Dynetics in Huntsville, AL</p>
  
  <ul class="internship-list">
    {% assign internship_posts = site.posts | where_exp: "post", "post.title contains 'Internship'" | sort: 'date' | reverse %}
    {% for post in internship_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-meta">{{ post.date | date: "%B %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
</div>
