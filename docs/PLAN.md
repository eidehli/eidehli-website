# Plan — temporary company website (2026)

## Purpose
A neutral, credible replacement for the old "Eidehli Consulting" site until a new business plan is decided.
Audience: former colleagues and network, public authorities (Skatteetaten, Brønnøysund etc.), anyone looking up the company.
No hourly consulting is offered any longer; the company's focus is app development. Nothing specific is promised or named.

## Content (one page, English default, Norwegian twin; structure ready for more languages)
1. **Company** — logo + short neutral statement (Norwegian software company developing applications; new products in development).
2. **Founder** — third-person bio of Einar Dehli with photo and LinkedIn link; very brief mention of selected past work.
3. **Contact & company details** — email, postal address, "Org.nr 890 724 442 MVA – Foretaksregisteret" (required for AS websites), note that the site uses no cookies or tracking.

## Design
- Based on the 2009 brand manual: navy `#002B5C`, light blue `#788BAF`, near-black `#231F20`; Futura Light → free web substitute; Zapfino only inside the logo (vector).
- Logo redrawn as SVG with "CONSULTING" removed (nothing in its place).
- Calm, generous whitespace, attention to typographic detail, responsive, accessible.

## Hosting
- GitHub Pages (account `eidehli`), public repo for now; `input/` never committed. Move to a private repo when more content is maintained.
- Repo: https://github.com/eidehli/eidehli-website; every push to `main` touching `site/` republishes automatically.
- Main address: **https://www.eidehli.com/** (live since 2026-10-03). eidehli.com and the old https://eidehli.github.io/eidehli-website/ forward to it; HTTPS enforced (certificate by GitHub, covers www and apex).
- Domain registered at GoDaddy (renewal due 2027-04-27). Only website DNS records change; Google Workspace mail (MX etc.) untouched.

## Steps (owner approval between each)
1. Repo set-up and plan ✅
2. Logo versions ✅ (option B, refined)
3. Texts EN + NO ✅ (docs/content.md)
4. Design and build, preview ✅ (design v1 approved 2026-10-03)
5. Publish on GitHub Pages temporary address ✅ (https://eidehli.github.io/eidehli-website/, approved 2026-10-03)
6. DNS switch at GoDaddy (owner does it, with instructions); verify site + email — site live and verified 2026-10-03; email send/receive test pending
7. Retire old Google Site; final documentation

## DNS at GoDaddy (since 2026-10-03)
Nameservers: GoDaddy (ns11/ns12.domaincontrol.com). Only the website records were changed; mail records untouched.

| Record | Name | Value now | Value before (Google Site) |
|---|---|---|---|
| A ×4 | @ | 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 (GitHub Pages) | 216.239.32.21, 216.239.34.21, 216.239.36.21, 216.239.38.21 |
| CNAME | www | eidehli.github.io | ghs.googlehosted.com |
| TXT | _github-pages-challenge-eidehli | (GitHub domain-verification code) — keep permanently | — (new) |
| MX ×7, TXT (SPF) | @ | Google Workspace mail — unchanged | same |

- Domain eidehli.com is verified on the GitHub account `eidehli` (Settings → Pages → verified domains); prevents others from using it on GitHub Pages.
- Custom domain set in repo Settings → Pages = `www.eidehli.com`, "Enforce HTTPS" on. No CNAME file needed (Actions-based publishing).
- No AAAA (IPv6) records added; optional later (2606:50c0:8000::153 … 8003::153).
- Rollback: put the "before" values back in GoDaddy and clear the custom domain in Pages.
