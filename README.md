# Matteo Aldovardi — Personal Website & Portfolio

Personal website and academic/ML portfolio built with [Quarto](https://quarto.org/) and published on GitHub Pages (`https://matteoaldovardi92.github.io`).

---

## Directory Structure

```
├── _quarto.yml          # Global site configuration, navbar, themes, and code options
├── index.qmd            # Homepage with hero banner and automatic recent posts grid
├── about.qmd            # Profile page (trestles layout) with bio, social links, and CV
├── portfolio.qmd        # Curated showcase of industrial, research, and coding projects
├── blog/
│   ├── index.qmd        # Dynamic blog listing with category filters and search
│   └── post_*.qmd       # Individual blog posts
├── assets/
│   └── cv/              # Local PDF CV files
├── images/              # Site banners, profile photo, and post figures
└── docs/                # Compiled static website output (published to GitHub Pages)
```

---

## How to Expand the Website

### 1. Adding a New Blog Post
To publish a new article, simply create a new `.qmd` file in `blog/` (e.g. `blog/my-new-post.qmd`) with the following frontmatter:

```yaml
---
title: "Title of Your Post"
description: "A short 1-2 sentence summary of what this post covers."
author: "Matteo Aldovardi"
date: "YYYY-MM-DD"
categories: ["Machine Learning", "Python"]
image: "../images/path-to-thumbnail.jpg"  # Optional: used for card previews
---

Your content in Markdown and executable Python/R code blocks...
```

> **Note:** The blog index and homepage will automatically detect, categorize, and sort your new post without any manual editing of `index.qmd`!

### 2. Adding a Project to Portfolio
Open `portfolio.qmd` and append a new callout block under the appropriate section:

```markdown
::: {.callout-tip appearance="simple" icon=false}
### Project Title
**Focus:** Key Area &bull; Topic  
**Tools:** PyTorch, Python, etc.  
- Project description and key achievements.  
[Read the Code or Paper &rarr;](link)
:::
```

### 4. Updating the CV
When you have a new version of your CV:
1. Replace `assets/cv/Matteo_Aldovardi_CV.pdf` with the updated PDF.
2. Re-render the site.

---

## Local Development & Publishing

### Live Preview
Preview the site with hot-reloading in your browser:
```bash
quarto preview
```

### Build for Production
Render all pages into the `docs/` folder:
```bash
quarto render
```

### Deploy to GitHub Pages
Commit the changes and push to GitHub:
```bash
git add .
git commit -m "Update website content"
git push origin main
```
