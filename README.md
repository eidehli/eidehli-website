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

Text changes: edit both language pages and keep `docs/content.md` in step. To preview locally: `cd site && python3 -m http.server` and open http://localhost:8000 (opening the file directly blocks the web font in some browsers).
