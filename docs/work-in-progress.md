# Redesign work-in-progress status

## Current tree

`redesign/` is the **local 30-page review build** imported from the attached review archive. It supersedes the earlier two-page WIP that was captured at **2026-11-06 22:02:49 +04** (Asia/Dubai). That earlier freeze is recorded in `docs/CAPTURE_TIMESTAMP.txt`. The two-page HTML files were not imported; `source-snapshot/`, `docs/design-guide.md`, and `branding/original-logo.png` from that handoff were kept.

This is still a **review build**, not a finished website and not a live deployment. It is not a Webflow migration (that work is separate). It is not pixel-perfect.

### Present in `redesign/`

| Item | Status |
|------|--------|
| HTML pages | **30** routes, listed in `redesign/QA/route-qa.md` |
| Base CSS / JS | `redesign/css/site.css`, `redesign/js/site.js` |
| Active botanical logo | `redesign/images/brand/logo-botanical.png` on every page header and footer |
| Favicon / default OG | `redesign/images/brand/favicon.png`, `redesign/images/brand/og-default.jpg` |
| Archived wide logo | `redesign/images/brand/archive/original-logo.png` (not used in the UI) |
| QA notes | `redesign/QA/NOTES.md`, `redesign/QA/route-qa.md` |
| Screenshots | `redesign/QA/screenshots/` |
| Lab Lighthouse | `redesign/QA/lighthouse-home.json` (local `http://127.0.0.1:8765` only) |
| Redirect notes | `redesign/redirect-map.txt` |

Route QA in the archive reports HTTP 200 for those 30 pages and 0 broken local assets **at check time** against a local static server. That check is not a production crawl.

### Logo selection

The user selected **Concept 02 — botanical wellness** as the primary logo for the active redesign. That selection supersedes using the original wide logo as the primary mark.

| File | Role |
|------|------|
| `branding/primary-logo-transparent.png` | Transparent export. Same bytes as `redesign/images/brand/logo-botanical.png`, which the 30 pages already reference. |
| `branding/primary-logo.png` | Cream/white-background export. Same bytes as `redesign/images/brand/logo-botanical-bg.png`. Not swapped into the header or footer. |
| `branding/original-logo.png` | Archived reference only. |

Header, footer, and mobile header rules in `redesign/css/site.css` size that mark with a fixed height, `width: auto`, and `object-fit: contain`. No invert filter is applied. `source-snapshot/` was not edited to use this logo.

**Known pending issue:** on desktop the header draws the near-square mark at about 56×56 CSS pixels, so the wordmark is too small to read comfortably. The local builder is fixing that separately. This import does not claim a pixel-perfect header.

### Known review limits

- **Contact form:** review-only. Fields do not submit to a backend, email endpoint, or form service. See `redesign/QA/NOTES.md`.
- **Core Web Vitals:** no field data (CrUX / Search Console) was measured. The Lighthouse file is a lab run only.
- Booking still points at the Mindbody widget noted in `redesign/README.md`. Offline review does not make third-party booking, reviews, or analytics fully functional.
- `source-snapshot/` remains the archived public-site download (30 readable texts, 86 images). It is not flattened into the served redesign root.
