---
layout: default
title: Home
---

<article>
  <h2>Welcome to My Blog</h2>
  <p>This is my personal space to share thoughts, projects, and anything I'm currently exploring. Feel free to browse my posts or check out my dedicated internship page for weekly updates from my current at Leidos.</p>
</article>

<article>
  <h2>Recent Posts</h2>
  {% if site.posts.size > 0 %}
  <ul>
    {% for post in site.posts limit:5 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
  {% else %}
  <p>No posts yet. Check back soon!</p>
  {% endif %}
</article>

<article>
  <h2>Internship Updates</h2>
  <p>Curious about my internship experience? Head over to the <a href="{{ '/internship' | relative_url }}">Internship page</a> for week-by-week updates and photos!</p>
</article>
