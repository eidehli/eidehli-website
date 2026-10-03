# eidehli.com

Company website for **Eidehli AS** (org.nr 890 724 442), replacing the old Google Sites page.

- `site/` — the static website that is published (plain HTML/CSS, no build step, no tracking, no cookies).
- `docs/` — plan, decisions log and operating notes.
- `input/` — private source material (CVs, original logo files). Excluded from git; lives only on the owner's Mac.

The site is designed, written and maintained by Claude on behalf of Einar Dehli. See `docs/PLAN.md` for scope and `docs/DECISIONS.md` for the rationale behind choices.

## Site structure
| Path | Content |
|---|---|
| `site/index.html` | English page (default) — also redirects Norwegian-language browsers to `no/` |
| `site/no/index.html` | Norwegian page |
| `site/assets/css/site.css` | All styling (brand colours and type scale at the top) |
| `site/assets/fonts/` | Jost web font + licence |
| `site/assets/img/` | Founder portrait (optimised, metadata stripped) |
| `site/assets/logo/` | Logo files |
| `site/favicon.svg`, `favicon-32.png`, `apple-touch-icon.png` | Browser tab and home-screen icons |
| `site/assets/img/og-image.png` | Link-preview image (1200×630) used when the site is shared |
| `site/404.html` | "Page not found" page (EN + NO); sets its own base address so it works on both the temporary and the final address |
| `site/robots.txt`, `site/sitemap.xml` | Search-engine hints (point to www.eidehli.com) |
| `.github/workflows/pages.yml` | Publishes `site/` to GitHub Pages on every push to `main` |

Text changes: edit both language pages and keep `docs/content.md` in step. To preview locally: `cd site && python3 -m http.server` and open http://localhost:8000 (opening the file directly blocks the web font in some browsers).

## Publishing
- Repository: https://github.com/eidehli/eidehli-website (public). `input/` is never committed.
- Every push to `main` that touches `site/` publishes automatically via GitHub Actions (`Publish site`).
- Address: **https://www.eidehli.com/** (custom domain set in repo Settings → Pages, HTTPS enforced). eidehli.com and the old https://eidehli.github.io/eidehli-website/ forward to it. DNS records: see `docs/PLAN.md`.
- Canonical, hreflang, Open Graph and sitemap URLs are absolute and point to www.eidehli.com; all links between pages stay relative.
