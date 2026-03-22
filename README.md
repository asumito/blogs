# asumito's Blog

Personal blog built with **Jekyll** and hosted on **GitHub Pages** at:

→ https://asumito.github.io/blogs/

- **Theme**: Clean, modern, dark-mode supported
- **Accent color**: Red-ish (#e53e3e)
- **Hero**: Animated iridescent gradient background
- **Logo**: Cartoon character holding "BLOG" banner
- **Writing**: Pure Markdown files (no HTML needed for posts)
- **Features**: Dark mode toggle, recent posts grid, dropdown nav (Life / Tech subsections)

## Table of Contents

- [Live Site](#live-site)
- [Adding a New Blog Post](#adding-a-new-blog-post) ← **Most important section**
- [Post Front Matter Explained](#post-front-matter-explained)
- [Categories & Subsections](#categories--subsections)
- [Local Development (Optional)](#local-development-optional)
- [Folder Structure](#folder-structure)
- [Customization Ideas](#customization-ideas)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Live Site

https://asumito.github.io/blogs/

(If links look broken or 404s appear, make sure `_config.yml` has `baseurl: "/blogs"` exactly as shown.)

## Adding a New Blog Post

This is the main thing you'll do — it's super simple.

### Method 1: Directly on GitHub (easiest – no software needed)

1. Go to your repository: https://github.com/asumito/blogs
2. Click into the `_posts/` folder  
   (If it doesn't exist yet → create it by making a temporary file like `_posts/.gitkeep` then delete the .gitkeep later)
3. Click **Add file → Create new file**
4. Name the file using this **exact** pattern:

Examples:
- `2026-03-22-my-first-home-lab.md`
- `2026-04-01-proxmox-cluster-fail.md`
- `2026-05-15-learning-rust.md`

5. At the **very top** of the file, paste and edit this front matter block:

```yaml
---
layout: post
title:  "My First Home Lab Setup"           # This appears as the post title
date:   2026-03-22 16:30:00 +0600           # Optional – filename date used if missing
categories: [Tech, Server]                  # Pick from your sections
tags: [homelab, proxmox, networking]        # Optional – good for future filtering
---
Today I finally got my mini homelab running!

## Hardware used
- Old Dell OptiPlex
- 32 GB RAM scavenged
- 2× 4 TB HDD in ZFS mirror

## What broke first
- iGPU passthrough not enabled in BIOS 😅

Run this to check:
```bash
pveversion -v



blogs/
├── _config.yml               ← site settings (baseurl: "/blogs" is important!)
├── _posts/                   ← all your .md posts go here
│   └── 2026-03-22-hello.md
├── _layouts/
│   └── default.html          ← main layout (header, footer, dark mode)
├── assets/
│   └── img/
│       └── logo.jpg          ← your cartoon BLOG guy
├── index.html                ← homepage with hero + recent posts
└── README.md                 ← this file
