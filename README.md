# Kuan'Log

Source for my personal blog **Kuan'Log**, published at [https://KuanL1u.github.io/](https://KuanL1u.github.io/).

The site is a static blog built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, deployed to GitHub Pages.

## Tech Stack

- **Static site generator:** Hugo
- **Theme:** [PaperMod](https://github.com/adityatelange/hugo-PaperMod) (vendored as a git submodule under `themes/PaperMod`)
- **Hosting:** GitHub Pages (user site)
- **Search:** Fuse.js (configured in `hugo.yaml`)
- **Math rendering:** KaTeX (enabled per-post via `math: true`)

## Repository Layout

```
.
├── archetypes/        # Hugo content templates
├── content/
│   └── posts/         # Blog posts (Markdown)
├── layouts/           # Custom layout overrides
├── static/            # Static assets (favicon, images, etc.)
├── themes/PaperMod/   # PaperMod theme (git submodule)
├── public/            # Generated site output
├── hugo.yaml          # Site configuration
└── .github/           # GitHub workflows
```

## Getting Started

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended version recommended)
- Git

### Clone

This repo uses a git submodule for the theme, so clone with `--recurse-submodules`:

```bash
git clone --recurse-submodules https://github.com/KuanL1u/KuanL1u.github.io.git
cd KuanL1u.github.io
```

If you've already cloned without submodules:

```bash
git submodule update --init --recursive
```

### Run Locally

```bash
hugo server -D
```

The site will be available at [http://localhost:1313/](http://localhost:1313/). The `-D` flag includes draft posts.

### Build

```bash
hugo --minify
```

Output is written to the `public/` directory.

## Writing a New Post

Create a new Markdown file under `content/posts/`:

```bash
hugo new posts/my-new-post.md
```

A typical front matter looks like:

```yaml
---
title: "My New Post"
date: 2026-01-01
draft: false
tags: ["tag1", "tag2"]
categories: ["Category"]
summary: "Short summary shown on list pages."
ShowToc: true
TocOpen: false
math: false
---
```

Set `draft: false` to publish.

## Configuration

Site-wide settings live in [`hugo.yaml`](./hugo.yaml) — title, menus, social links, theme params, search options, and analytics tags.

## Deployment

The site is deployed to GitHub Pages at [https://KuanL1u.github.io/](https://KuanL1u.github.io/).

## License

Content is © Kuan Liu unless otherwise noted. The PaperMod theme is licensed separately under its own [MIT License](https://github.com/adityatelange/hugo-PaperMod/blob/master/LICENSE).
