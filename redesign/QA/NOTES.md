# QA notes — Wellness Origin review build

## Contact form
The contact form on `/contact/` is **review-only**. It does not submit to any backend, email endpoint, or third-party form service. Fields are disabled in the prototype. Guests should call **317-979-1234**, email **support@wellnessorigin.com**, or use **Book Now** (Mindbody widget id `dd2977661c9`).

## Core Web Vitals
**No field Core Web Vitals were verified.** Only lab Lighthouse numbers were collected against a local `http.server` (see `lighthouse-home.json`). Those scores are not CrUX / Search Console field data.

## Route QA
See `route-qa.md` — 30 pages, HTTP 200, 0 broken local assets at check time.

## Logo
Active mark: `images/brand/logo-botanical.png`. Archived wide logo remains at `images/brand/archive/original-logo.png` and is not used in the UI.

**Pending:** the near-square botanical wordmark is too small in the desktop header (the mark is drawn at about 56×56 CSS pixels). The local builder is fixing that separately. This review build is not a pixel-perfect final.
