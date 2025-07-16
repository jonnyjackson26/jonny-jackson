---
title: "Draft"
date: 2024-01-16T10:00:00Z
draft: true
summary: "A deep dive into how I built my personal website from scratch using Hugo and PaperMod."
tags: ["portfolio", "hugo", "webdev", "PaperMod"]
categories: ["Projects", "Web Development"]
author: "Your Name"

cover:
  image: "/images/portfolio-cover.jpg"
  alt: "Screenshot of my portfolio homepage"
  caption: "A clean and minimal homepage built with Hugo and PaperMod."
  relative: true

showToc: true
tocOpen: true
showReadingTime: true
showBreadcrumbs: true
showPostNavLinks: true
showCodeCopyButtons: true
---

Welcome! 👋

This post documents how I built my personal developer portfolio using **Hugo**, a blazing fast static site generator, and the awesome **PaperMod** theme. Inspired by [jonny-jackson.com](https://jonny-jackson.com), I wanted a site that was minimalist, fast, and easy to maintain.

---

## 🚀 Goals

- ✅ Showcase my projects in a clean layout
- ✅ Optimize for SEO and performance
- ✅ Include a blog section for thoughts & tutorials
- ✅ Use dark mode and responsive design
- ✅ Deploy for free (spoiler: I used GitHub Pages)

---

## 🛠 Tech Stack

- [Hugo](https://gohugo.io/)
- [PaperMod Theme](https://github.com/adityatelange/hugo-PaperMod)
- Markdown for writing content
- Git + GitHub for version control and deployment

---

## 💡 Features

- Cover images on posts
- Automatic Table of Contents
- Code block highlighting with copy buttons
- Social links and share buttons
- Fast load times with minified assets

---

## 🖼 Sample Project Section

I created a `content/projects` section and used custom archetypes to add metadata for each project.

```toml
title = "PlayBoard"
description = "A stats tracker and league management app for basketball players."
repo = "https://github.com/yourname/playboard"
tags = ["react", "firebase", "typescript"]
```
