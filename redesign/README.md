# Wellness Origin Indianapolis — local review build

Static review prototype imported under `redesign/` in this repository. It is a 30-page local review build, not a finished pixel-perfect site and not a Webflow migration.

## Preview
From this directory:

```bash
python3 -m http.server 8765
```

Open http://127.0.0.1:8765/

## Palette (from logo)
- Violet `#5c6299` / soft `#8b8db8` / mist `#f3f1f8`
- Sage `#5f9a74` / deep `#4a7d5c`
- Ink `#1a1918` · paper `#faf9f6` · line `#e6e2dc`

## Key paths
- `index.html` — homepage
- `spa-services/facials/` — representative deep service page
- `css/site.css`, `js/site.js`
- `images/brand/logo-botanical.png` — active logo (transparent botanical mark, 701×735)
- `images/brand/archive/original-logo.png` — archived wide logo (not used in UI)
- `images/brand/favicon.png`, `images/brand/og-default.jpg` — favicon / default OG
- `redirect-map.txt`
- `QA/NOTES.md`, `QA/route-qa.md` — review notes and local route check
- `QA/screenshots/` — review screenshots
- `QA/lighthouse-home.json` — lab Lighthouse only (no field Core Web Vitals)

## Booking
Mindbody Appointments widget id `dd2977661c9` on `book-now/`.


## Branding
Active mark: `images/brand/logo-botanical.png` (nearly square, transparent PNG).  
Archived (do not use in UI): `images/brand/archive/original-logo.png`.  
Header/footer CSS sizes the mark by height with `object-fit: contain` so proportions stay intact; no invert filter on the footer (keeps botanical colors).

The desktop header currently draws that near-square mark at about 56×56 CSS pixels, so the wordmark is too small. That size is a known pending fix and is not the final header.
