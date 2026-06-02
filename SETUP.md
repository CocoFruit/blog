# Jekyll Blog Setup Guide

## Quick Start

### Option 1: Docker (No Ruby Installation Required)

1. **Install Docker Desktop** from https://www.docker.com/products/docker-desktop

2. **Run the development server**:
   ```bash
   docker-compose up
   # Or use the convenience script:
   ./serve-docker.sh
   ```

3. **View your site**:
   Open `http://localhost:4000` in your browser

### Option 2: GitHub Pages (No Local Setup)

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Update blog"
   git push
   ```

2. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Source: GitHub Actions
   - The site will auto-build and deploy

3. **View your site**:
   Visit `https://YOUR-USERNAME.github.io/blog`

### Option 3: Local Ruby (If Available)

1. **Install Jekyll**:
   ```bash
   gem install jekyll bundler
   ```

2. **Install dependencies**:
   ```bash
   bundle install
   ```

3. **Run the development server**:
   ```bash
   bundle exec jekyll serve
   # Or: ./serve.sh
   ```

4. **View your site**:
   Open `http://localhost:4000` in your browser

## Project Structure

```
blog/
├── _config.yml              # Jekyll configuration
├── _layouts/                # Page templates
│   ├── default.html         # Main layout
│   ├── post.html            # Blog post layout
│   └── internship_post.html # Internship week layout
├── _includes/               # Reusable components
│   ├── header.html
│   ├── nav.html
│   └── footer.html
├── _posts/                  # Blog posts (YYYY-MM-DD-title.md)
├── _internship_2025/        # 2025 internship weeks
├── _internship_2026/        # 2026 internship weeks (for this summer)
├── assets/
│   ├── css/
│   │   └── style.css        # Main stylesheet
│   └── images/              # All images go here
├── index.md                 # Home page
├── internship.md            # Internship listing page
└── about.md                 # About page
```

## Adding Content

### Blog Post
Create `_posts/YYYY-MM-DD-title.md`:
```markdown
---
layout: post
title: "My Post Title"
date: 2026-06-02
---

Your content here...
```

### Internship Week (2026)
Create `_internship_2026/weekN.md`:
```markdown
---
title: Week N
week: N
slug: weekN
photos:
  - /assets/images/2026_weekN_1.jpg
  - /assets/images/2026_weekN_2.jpg
---

Your week summary here...
```

## Deploying

### GitHub Pages
1. Push to GitHub
2. Enable GitHub Pages in repository settings
3. Set source to "main" branch

### Manual Build
```bash
bundle exec jekyll build
# Output will be in _site/
```

## Customization

- **Colors/Fonts**: Edit `assets/css/style.css`
- **Site title**: Edit `_config.yml`
- **Navigation**: Edit `_includes/nav.html`
- **Header/Footer**: Edit `_includes/header.html` and `_includes/footer.html`
