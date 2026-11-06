# QA notes — Wellness Origin review build

## Contact form
The contact form on `/contact/` is **review-only**. It does not submit to any backend, email endpoint, or third-party form service. Fields are disabled in the prototype. Guests should call **317-979-1234**, email **support@wellnessorigin.com**, or use **Book Now** (Mindbody widget id `dd2977661c9`).

## Core Web Vitals
**No field Core Web Vitals were verified.** Only lab Lighthouse numbers were collected against a local `http.server` (see `lighthouse-home.json`). Those scores are not CrUX / Search Console field data.

## Route QA
See `route-qa.md` — 30 pages, HTTP 200, 0 broken local assets at check time.

## Logo
Active mark: `images/brand/logo-botanical.png`. Archived wide logo remains at `images/brand/archive/original-logo.png` and is not used in the UI.

Header legibility update (CSS only; logo PNG unchanged). Measured sizes are in `logo-heights.json` and `CHANGES-logo-fix.md`: desktop logo 80px in a 100px header, scrolled 56px in a 72px header, mobile 52px in a 68px header. This remains a review build, not a pixel-perfect final site.
