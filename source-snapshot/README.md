# Wellness Origin Spa — public website archive

**Captured:** 2026-11-06 21:47:51 +04 (Asia/Dubai, UTC+4)  
**Source:** https://wellnessoriginindy.com/  
**Method:** public HTTPS GET via Rank Math sitemap + same-host internal links; ~0.35s delay between pages; max 200 HTML pages.  
**Agent:** CiteSmithArchiveBot (read-only). No logins, form submissions, or site changes.

## What this is
A **readable archive / best-effort offline snapshot** of publicly reachable HTML pages, extracted Markdown text, same-site images, and same-site CSS/JS discovered from those pages.

- **Best for reading content:** `all-page-content.md` and `text/*.md`
- **Best-effort local browsing:** `index.html` → `pages/*.html` (internal links rewritten where assets were saved)
- **Original HTML:** `pages/*.raw.html`

## What this is NOT
- Not a server filesystem dump, WordPress database, Media Library export, or full CMS package.
- Not a fully functioning clone. Mindbody booking, Trustindex reviews, Google Fonts/analytics, Cloudflare email-protection UI, and other third-party embeds were **intentionally excluded** and will not work offline.
- Not private/admin content (`/wp-admin/` disallowed by robots.txt and skipped).

## Counts (this run)
| Item | Count |
|------|------:|
| Unique HTML pages saved (HTTP 200) | **30** |
| Markdown text files | **30** |
| Image files in `images/` | **86** (decodable: 86) |
| CSS files | **57** |
| JS files | **21** |
| Public PDFs found | **0** |
| Archive directory size (pre-zip) | **19.4 MB** |

## Layout
| Path | Contents |
|------|----------|
| `index.html` | Page index for local browsing |
| `pages/*.html` | Offline-rewritten HTML (best-effort) |
| `pages/*.raw.html` | Unmodified downloaded HTML |
| `text/*.md` | Deduplicated readable text per page |
| `all-page-content.md` | Consolidated text for easy review |
| `images/` | Same-site images (WP unsized original preferred when available) |
| `assets/` | Same-site CSS/JS (+ PDFs if any) |
| `raw/` | robots.txt, sitemaps, llms.txt, stats.json |
| `manifest.csv` | URL → local path / HTTP status / kind |

## Pages captured
- https://wellnessoriginindy.com/
- https://wellnessoriginindy.com/accessibility-statement/
- https://wellnessoriginindy.com/author/ericadmin/
- https://wellnessoriginindy.com/blogs/
- https://wellnessoriginindy.com/book-now/
- https://wellnessoriginindy.com/category/treatments/
- https://wellnessoriginindy.com/contact/
- https://wellnessoriginindy.com/eminence-organics-skin-care/
- https://wellnessoriginindy.com/how-professional-facials-can-improve-your-skincare-routine/
- https://wellnessoriginindy.com/laser-hair-removal/
- https://wellnessoriginindy.com/laser-lipo-carmel-indiana/
- https://wellnessoriginindy.com/loyalty-program/
- https://wellnessoriginindy.com/organic-health-food-store/
- https://wellnessoriginindy.com/payment-plans/
- https://wellnessoriginindy.com/privacy-policy/
- https://wellnessoriginindy.com/spa-sales/
- https://wellnessoriginindy.com/spa-services/
- https://wellnessoriginindy.com/spa-services/body-contouring/
- https://wellnessoriginindy.com/spa-services/facials/
- https://wellnessoriginindy.com/spa-services/hyperbaric-oxygen-therapy/
- https://wellnessoriginindy.com/spa-services/ipl-photofacial/
- https://wellnessoriginindy.com/spa-services/laser-dark-spot-removal/
- https://wellnessoriginindy.com/spa-services/laser-tattoo-removal/
- https://wellnessoriginindy.com/spa-services/massage/
- https://wellnessoriginindy.com/spa-services/red-light-therapy/
- https://wellnessoriginindy.com/spa-services/wellness-consulting/
- https://wellnessoriginindy.com/spa-services/wellness-therapies/
- https://wellnessoriginindy.com/terms-conditions/
- https://wellnessoriginindy.com/we-are-hiring-carmel-spa/
- https://wellnessoriginindy.com/what-to-expect-from-laser-hair-removal-treatments/

## Missing / failed page URLs
- https://wellnessoriginindy.com/cdn-cgi/l/email-protection
- https://wellnessoriginindy.com/services/waxing/
- https://wellnessoriginindy.com/spa-sales-memberships/
- https://wellnessoriginindy.com/spa-services/lashes-and-brows/

Notes on failures:
- `/cdn-cgi/l/email-protection` is Cloudflare email obfuscation, not a content page.
- `/spa-sales-memberships/`, `/spa-services/lashes-and-brows/`, `/services/waxing/` returned non-success during crawl (site already had some broken nav targets).

## Other gaps
- **21 Elementor per-post CSS URLs returned HTTP 404** on the live site (referenced in HTML but missing on origin). Offline CSS is therefore incomplete for some Elementor page chrome; content/text/images still captured.
- External images/fonts/scripts (Google, Cloudflare CDN, Elementor CDN, social networks, Mindbody, Trustindex) were not downloaded.
- No public PDF links were discovered on crawled pages.
- Image `srcset` variants were inventoried in `manifest.csv`; when a WordPress `-NNNxNNN` / `-scaled` URL was seen, the unsized original was requested and kept when available (`status=200-via-larger`).

## Coverage
Sitemap listed 29 URLs; crawl also followed same-host internal links. Unique successful HTML pages: 30. Did not hit the 200-page cap. HTTPS only (plain HTTP previously 500'd on apex).

## Integrity
Companion ZIP: `/workspace/citesmith/downloads/wellness-origin-website-2026-11-06.zip`  
Verify with `unzip -t` after packaging.
