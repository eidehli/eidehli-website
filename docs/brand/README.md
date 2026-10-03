# Brand assets

Source: 2009 profile manual (`input/Eidehli logo/Profil_manual/eidehli_profil_manual.pdf`, private, not in git).

## Logo files
| File | Use |
|---|---|
| `site/assets/logo/eidehli-logo.svg` | Primary (stacked) logo — refined, no reflection |
| `site/assets/logo/eidehli-logo-horizontal.svg` | Secondary (horizontal) logo — page header |
| `site/assets/logo/eidehli-symbol.svg` | Symbol only — favicon, app icons |
| `docs/brand/*-classic.svg` | Faithful versions with the original reflection under the symbol (archive / alternative) |

## How they were produced (2026-10-03)
1. Original colour PDFs (`Primær/pdf`, `Sekundær/pdf`, `Symbol/pdf`) converted with `pdftocairo -svg`.
2. Caption glyphs, "CONSULTING" glyphs and the rule line removed; for refined versions the masked reflection image removed.
3. viewBox cropped to the rendered pixel bounds (+1 pt margin) using headless Chromium.
4. Optimised with `svgo --multipass`; gradient stops thinned from ~145 to 16 per gradient (visually identical).
Wordmark glyphs are outlined Zapfino, so no font licence is needed for the logo.

## Colours (from the manual)
| Token | RGB | Hex |
|---|---|---|
| Navy (symbol dark) | 0 43 92 | `#002B5C` |
| Light blue (symbol light) | 120 139 175 | `#788BAF` |
| Ink (wordmark/text) | 35 31 32 | `#231F20` |
| Greys | 70 69 71 / 99 100 102 / 147 149 152 / 173 175 178 | `#464547` `#636466` `#939598` `#ADAFB2` |

Accent harmonies in the manual (use sparingly): orange CMYK 0/50/100/0, green 53/17/100/1, magenta 34/96/34/5, blue 80/56/0/0.

## Typography
Manual: Zapfino (logo/headings only) and Futura Light (body). Futura is a paid web font; the site uses **Jost** (free, SIL Open Font License), self-hosted from `site/assets/fonts/` with its licence alongside (decided in step 4).
