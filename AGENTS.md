# AGENTS.md

Shared instructions for any coding agent (Codex, Claude, etc.) working in this repo.

## What this repo is
- A personal website + blog built with the **al-folio Jekyll theme**, published to
  GitHub Pages (`https://shivam6991.github.io`). Deploys automatically on push to `main`.

## Quick reference (how to add a blog post)
- Posts live in `_posts/` as `YYYY-MM-DD-title.md` with YAML front matter.
- Front matter required fields: `layout: post`, `title`, `date` (format
  `YYYY-MM-DD HH:MM:SS+0530`), `description`, `tags`. Optional: `categories`,
  `giscus_comments`, `related_posts`, `featured`, `thumbnail`.
- Post body is Markdown. Raw HTML is also fine inside a post if the source is HTML.
- Blog index is `_pages/blog.md` (paginated, 5 per page, reverse-chronological).
- `_config.yml` → Blog section sets `blog_name`, `permalink: /blog/:year/:title/`,
  and `display_tags`.

## Repo layout
- `_posts/` – blog posts (the main thing people add here)
- `_pages/` – static pages (about, blog, cv, news, projects, publications)
- `_data/` – YAML data (cv.yml, socials.yml, repositories.yml, citations.yml, etc.)
- `_news/` – homepage news/announcement snippets
- `_projects/` – project showcase pages
- `_bibliography/` – publications list

## Build / test locally
- Jekyll site. Use `bundle install`, then `bundle exec jekyll serve` (or `bundle exec jekyll build`).

## Shared agent notes (IMPORTANT)
- This file is the single source of truth for repo conventions.
- `CLAUDE.md` (if present) just points here — do not duplicate content there.
- If other agents create durable notes, put them under `_agent-notes/` and reference
  them here so every agent (Codex and Claude) picks them up automatically.
