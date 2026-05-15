# aarongood.com

Personal site for Aaron Good (LPC, Portland OR). Deployed to GitHub Pages with a custom domain.

## Deployment

- **Repo**: github.com/MonsieurBon-65000/aarongood.github.io
- **Live URL**: https://aarongood.com
- **Hosting**: GitHub Pages (main branch, root folder)
- **Domain registrar**: Google Domains (now Squarespace Domains)
- **DNS**: Four A records pointing `@` to GitHub's IPs; `www` CNAME → `monsieurbon-65000.github.io`

Push to main deploys automatically. No build step.

## Structure

```
index.html                  # Homepage — bio + Tools for Counselors card grid
CHANGELOG.md
CNAME                       # Created by GitHub; do not delete
tools/
  liability-insurance.html
  superbills.html
  progress-notes.html
  accepting-new-clients.html
  files/
    SuperbillTemplate.docx
    ProgressNotes.docx
    ProgressNotes-2020.docx
```

## Design system

All CSS is inlined per file — no external stylesheet. Copy the `<style>` block from any existing page when creating a new one. CSS variables defined in `:root`:

| Variable | Value | Use |
|----------|-------|-----|
| `--green` | `#2d5016` | Headings, primary color |
| `--green-mid` | `#4a7c2f` | Links, hover states |
| `--green-light` | `#e8f0e0` | Badges, callout backgrounds |
| `--amber` | `#c87941` | Section labels, tagline |
| `--bg` | `#f8f7f3` | Page background |
| `--muted` | `#5a5a5a` | Body text, secondary content |
| `--border` | `#e0ddd5` | Card and section borders |

## Adding a new page

1. Copy an existing `tools/*.html` as a starting point
2. Update `<title>`, `<meta name="description">`, `<h1>`, and body content
3. Keep the `<nav><a href="../index.html">← Aaron Good</a></nav>` at the top
4. Add a card for it in `index.html`
5. Update `CHANGELOG.md` under `[Unreleased]`

## Content origins

The four articles in `tools/` were originally published on trailheadcounseling.net under `/tools-for-counselors/`. They were noindexed on that site on 2026-05-08 and ported here. The `.docx` files were downloaded from the Squarespace CDN at that time.
