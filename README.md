# michaeldcruz.github.io

Personal site and blog. A minimal Jekyll site hosted free on GitHub Pages, live at
https://michaeldcruz.github.io

## How it works

- No external theme. All the HTML is here in `_layouts/` and the CSS in `style.css`, so it's fully yours to edit.
- GitHub Pages builds the Jekyll site automatically on every push to `main`. There is no build step to run yourself.

## Write a new post

Add a markdown file to `_posts/` named `YYYY-MM-DD-title.md` with front matter:

```
---
layout: post
title: "Your Title"
subtitle: "Optional one-line deck."
date: 2026-07-20
---

Your post, in markdown.
```

Commit and push. It appears on the homepage list and in the RSS feed within a minute or two.

## Pages

- `index.html` - homepage (intro + list of posts)
- `about.md` - about page at `/about/`
- `_layouts/default.html` - shared page shell (header, footer, styles)
- `_layouts/post.html` - post wrapper (title, date, back link)
- `style.css` - all styling

## Custom domain (optional, later)

Buy a domain, add a `CNAME` file containing just the domain (e.g. `mikecruz.com`),
point the DNS at GitHub Pages, and set the domain under Settings -> Pages.
