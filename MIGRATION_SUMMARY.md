# Blog Migration to Jekyll - Summary

## What Changed

Your blog has been converted from plain HTML to Jekyll, a static site generator. The structure is now more maintainable while keeping the same low-tech, clean aesthetic.

## Key Improvements

1. **Modular Design**: Layouts and includes make it easy to update the header, nav, or footer in one place
2. **Markdown Content**: Write posts and internship updates in simple Markdown instead of HTML
3. **Collections**: Internship weeks are organized by year (`_internship_2025/`, `_internship_2026/`)
4. **Automatic Listings**: The internship page automatically shows all weeks from each collection
5. **Clean URLs**: Jekyll generates clean URLs like `/internship/2025/week1/`
6. **Easy to Extend**: Adding new years or post types is straightforward

## File Structure

```
blog/
├── _config.yml                    # Jekyll configuration
├── _layouts/                      # HTML templates
│   ├── default.html               # Main page template
│   ├── post.html                  # Blog post template
│   └── internship_post.html       # Internship week template
├── _includes/                     # Reusable components
│   ├── header.html                # Site header
│   ├── nav.html                   # Navigation menu
│   └── footer.html                # Site footer
├── _posts/                        # Blog posts
│   └── 2026-06-02-welcome-to-jekyll.md
├── _internship_2025/              # 2025 Leidos Dynetics internship
│   ├── week1.md
│   ├── week2.md
│   ├── week3.md
│   ├── week4.md
│   ├── week5.md
│   └── week6.md
├── _internship_2026/              # 2026 summer internship (empty, ready for use)
│   └── README.md
├── assets/
│   ├── css/
│   │   └── style.css              # Your existing styles (preserved)
│   └── images/
│       └── week1_*.jpg            # Your photos
├── index.md                       # Home page
├── internship.md                  # Internship listings by year
├── about.md                       # About page
├── Gemfile                        # Ruby dependencies
├── serve.sh                       # Quick serve script
├── README.md                      # Project documentation
└── SETUP.md                       # Setup instructions
```

## Preserved Elements

- **Same look and feel**: All your original CSS is preserved in `assets/css/style.css`
- **Same content**: All 6 weeks of 2025 internship updates are converted to Markdown
- **Same images**: Week 1 photos are in `assets/images/`
- **Same font**: Inter font from Google Fonts
- **Same colors**: Dark header (#1f2937), darker nav (#111827), etc.

## New Features

### 2026 Internship Section
The internship page now has a dedicated section for this year's internship. To add weeks:

1. Create `_internship_2026/week1.md`:
   ```markdown
   ---
   title: Week 1
   week: 1
   slug: week1
   photos:
     - /assets/images/2026_week1_1.jpg
   ---

   Your content here...
   ```

2. Add photos to `assets/images/` with the naming pattern `2026_weekN_X.jpg`

3. The internship page will automatically list all weeks

### Blog Posts
Create posts in `_posts/` with the format `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "My Post Title"
date: 2026-06-02
---

Your content...
```

## How to Use

### Local Development
```bash
# Install dependencies (first time only)
bundle install

# Start the development server
bundle exec jekyll serve

# Or use the convenience script
./serve.sh

# Visit http://localhost:4000
```

### Adding Content

**Blog Post**: Create `_posts/2026-06-15-my-post.md`

**2026 Internship Week**: Create `_internship_2026/week1.md`

**Add Images**: Place in `assets/images/`

### Customization

- **Site title/description**: Edit `_config.yml`
- **Styles**: Edit `assets/css/style.css`
- **Navigation links**: Edit `_includes/nav.html`
- **Header/footer**: Edit `_includes/header.html` or `_includes/footer.html`

## Deployment

### GitHub Pages (Recommended)
1. Push to GitHub
2. Settings → Pages → Source: "main" branch
3. Your site will be live at `username.github.io/blog`

### Manual Deploy
```bash
bundle exec jekyll build
# Upload contents of _site/ to your web server
```

## Old Files

- `index.html.old` - Your original home page (backup)
- `internship.html.old` - Your original internship page (backup)

These can be deleted once you verify everything works.

## What's Low-Tech About This?

Despite using Jekyll, this remains low-tech:

- **Static HTML**: No server-side processing, no database
- **Simple Markdown**: No complex CMS
- **Plain CSS**: No fancy frameworks
- **Minimal dependencies**: Just Jekyll and a couple plugins
- **Git-based**: Version control for everything
- **Fast**: Static files load instantly

## Next Steps

1. Install Ruby and Jekyll (see SETUP.md)
2. Run `bundle install`
3. Run `bundle exec jekyll serve`
4. Visit `http://localhost:4000`
5. Start adding 2026 internship weeks as they happen!

## Questions?

Check out:
- `README.md` - Project overview
- `SETUP.md` - Detailed setup instructions
- `_internship_2026/README.md` - Guide for adding 2026 weeks
- [Jekyll Documentation](https://jekyllrb.com/docs/)
