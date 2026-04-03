# CheapBytes.dev

Personal blog built with Jekyll and hosted on GitHub Pages.

## Prerequisites

- Ruby (2.7+)
- Bundler (`gem install bundler`)

## Setup

```bash
bundle install --path vendor/bundle
```

## Local Development

Serve the site locally (binds to all interfaces so it's accessible over the network):

```bash
bundle exec jekyll serve --host 0.0.0.0
```

The site will be available at `http://localhost:4000`.

### Previewing from Windows via SSH

If you're developing on a remote Ubuntu machine and want to preview in Windows Chrome:

1. Open a terminal (PowerShell or CMD) on Windows
2. Connect with port forwarding:
   ```
   ssh -L 4000:localhost:4000 your-user@your-ubuntu-host
   ```
3. Start the Jekyll server on the Ubuntu machine:
   ```bash
   bundle exec jekyll serve --host 0.0.0.0
   ```
4. Open `http://localhost:4000` in Chrome on Windows

## Build

Generate the static site into `_site/`:

```bash
bundle exec jekyll build
```

## Deployment

The site is deployed automatically via GitHub Pages when pushing to the `main` branch. The repo must be named `<username>.github.io` for root domain hosting.

## Writing Posts

Add new posts to `_posts/` using the naming convention `YYYY-MM-DD-title-slug.md` with front matter:

```yaml
---
layout: post
title: "Post Title"
date: YYYY-MM-DD HH:MM:SS -0000
author: Nir Tarnopolski
tags: [tag1, tag2]
image: /assets/images/featured.jpg
---
```

Images go in `assets/images/`.
