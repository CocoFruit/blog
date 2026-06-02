# Quick Start Guide

## First Time Setup

```bash
# 1. Install dependencies
bundle install

# 2. Start the server
bundle exec jekyll serve

# 3. Open browser
# Visit: http://localhost:4000
```

## Adding 2026 Internship Week

**Step 1**: Create the file `_internship_2026/weekN.md`

```markdown
---
title: Week N
week: N
slug: weekN
---

Your week summary here...
```

**Step 2**: (Optional) Add photos to `assets/images/` and reference them:

```markdown
---
title: Week N
week: N
slug: weekN
photos:
  - /assets/images/2026_weekN_1.jpg
  - /assets/images/2026_weekN_2.jpg
---
```

**Step 3**: Save and refresh your browser - Jekyll will rebuild automatically!

## Adding a Blog Post

**Step 1**: Create `_posts/2026-MM-DD-title.md`

```markdown
---
layout: post
title: "My Post Title"
date: 2026-06-15
---

Your content here...
```

**Step 2**: Save and it appears on the home page automatically!

## Common Commands

```bash
# Start server
bundle exec jekyll serve

# Start with live reload
bundle exec jekyll serve --livereload

# Build site only (output to _site/)
bundle exec jekyll build

# Clean build artifacts
bundle exec jekyll clean
```

## File Locations

- **2026 internship weeks**: `_internship_2026/weekN.md`
- **Blog posts**: `_posts/YYYY-MM-DD-title.md`
- **Images**: `assets/images/`
- **Styles**: `assets/css/style.css`

That's it! Keep it simple.
