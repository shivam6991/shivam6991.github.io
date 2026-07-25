# shivam6991.github.io

My personal website and tech blog, live at **https://shivam6991.github.io**.

Built with [Jekyll](https://jekyllrb.com/) using the
[al-folio](https://github.com/alshedivat/al-folio) theme, and deployed automatically by
GitHub Actions — every push to `main` rebuilds the site (no local setup required).

## One-time GitHub Pages setup

After the first Actions run finishes (green check in the **Actions** tab), a `gh-pages`
branch is created with the compiled site. Point Pages at it once:

> **Settings → Pages → Build and deployment → Source: _Deploy from a branch_ →
> Branch: `gh-pages` / `(root)` → Save.**

The site is live a minute or two later.

## Editing the site

| What | Where |
| --- | --- |
| Homepage bio & photo | `_pages/about.md`, `assets/img/prof_pic.jpg` |
| Social links (email, GitHub, …) | `_data/socials.yml` |
| Blog posts | `_posts/YYYY-MM-DD-title.md` |
| News / short updates | `_news/` |
| Projects | `_projects/` |
| Publications | `_bibliography/papers.bib` |
| CV | `assets/json/resume.json` |
| Site name, colours, options | `_config.yml` |

Commit and push your changes to `main`; the site redeploys on its own.

## Previewing locally (optional)

Local preview needs Ruby 3.x. It's entirely optional — pushing to `main` is enough.

```bash
bundle install
bundle exec jekyll serve
```

---

_Theme: [al-folio](https://github.com/alshedivat/al-folio) (MIT). See `LICENSE`._
