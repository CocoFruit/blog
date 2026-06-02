# Parker Hance's Blog

A simple Jekyll blog for sharing thoughts, projects, and internship experiences.

## Local Development

1. Install Ruby and Bundler
2. Install dependencies:
   ```bash
   bundle install
   ```
3. Run the development server:
   ```bash
   bundle exec jekyll serve
   ```
4. Visit `http://localhost:4000`

## Structure

- `_config.yml` - Jekyll configuration
- `_layouts/` - Page templates
- `_includes/` - Reusable components (header, nav, footer)
- `_posts/` - Blog posts
- `_internship_2025/` - 2025 internship weekly updates
- `assets/` - CSS, images, and other static files

## Adding Content

### Blog Post
Create a file in `_posts/` with format `YYYY-MM-DD-title.md`:
```markdown
---
layout: post
title: "My Post Title"
date: 2026-06-02
---

Post content here...
```

### Internship Week
Create a file in `_internship_2025/` with format `weekN.md`:
```markdown
---
title: Week N
week: N
slug: weekN
photos:
  - /assets/images/weekN_1.jpg
---

Week content here...
```
