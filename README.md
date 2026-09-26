# Personal site

Static site built with [Quarto](https://quarto.org): profile/CV, Projects &
Articles, an occasional Blog, and Links.

## Structure

```
index.qmd        → Profile / CV (home page)
projects.qmd      → listing page, pulls everything in projects/
projects/*.qmd    → one file per project or in-depth article
blog.qmd          → listing page, pulls everything in posts/
posts/*.qmd       → occasional short notes (kept deliberately low-key)
links.qmd         → static list of external links
images/           → avatar, favicon, project banner illustrations
files/cv.pdf      → put your real CV PDF here (linked from the home page)
styles.scss       → colors/fonts (Bootstrap variables)
styles.css        → extra styling (card hover effects, etc.)
_quarto.yml       → site config: nav, theme, site title
```

## Test / run locally

```bash
quarto preview
```

Opens the site at http://localhost:4200-ish with live reload — edit any
`.qmd` file and the browser refreshes automatically. Stop with Ctrl+C.

To just build the static files without a live server:

```bash
quarto render
```

Output goes to `_site/` (gitignored — this is the build artifact, not
source).

## Publish

Simplest path — one command, no CI needed for an infrequently-updated
personal site:

```bash
quarto publish gh-pages
```

First run will ask to create/link a GitHub repo and a `gh-pages` branch.
After that, running the same command again re-publishes your latest
changes. (Requires `git` and `gh`/GitHub auth already set up.)

## Adding a new project or blog post

1. Copy an existing `.qmd` in `projects/` or `posts/` as a starting point.
2. Update the YAML frontmatter (`title`, `date`, `image` for projects,
   `categories`).
3. Write the content in Markdown (LaTeX math works: `$x^2$` inline,
   `$$...$$` display).
4. `quarto preview` to check it renders, then `quarto publish gh-pages`.

The listing pages (`projects.qmd`, `blog.qmd`) update automatically —
nothing to edit there.

## Turning a private note into a public post

Keep your working notes wherever you already keep them. When one is ready
to share:

- Ask Claude to distill it into a new file under `projects/` (or `posts/`
  for something lighter) — condensed, with one clear figure, linking out
  to the full PDF/paper at the end if there is one.
- The original note stays untouched wherever it lives; only the public
  distillation lives in this repo.
