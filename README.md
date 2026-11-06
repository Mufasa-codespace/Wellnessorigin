# Wellness Origin

Public import of the Wellness Origin Indianapolis redesign materials. This repository is a review archive. It is not a finished production website, not a Webflow project, and not a deployment.

## Layout

| Path | What it is |
|------|------------|
| `source-snapshot/` | Archived download of the public site (wellnessoriginindy.com), frozen in the handoff package. Not the redesigned site, and not served from the repository root. |
| `redesign/` | Local static review build: **30 HTML pages**. Supersedes the earlier two-page redesign WIP. Intended project root for the separate Vercel project `wellness-origin-redesign`. |
| `branding/` | Logo files. Concept 02 botanical wellness is the selected primary mark. `original-logo.png` is an archived reference only. |
| `docs/` | Design brief, work-in-progress notes, and the earlier handoff timestamp. |

## Redesign completeness

The `redesign/` tree is a local review prototype with one HTML page per current route (home, services, policies, blog index, and the other public routes). It is **not** pixel-perfect and **not** the final site.

- Active logo on all 30 pages (header, footer, favicon, and Open Graph): `redesign/images/brand/logo-botanical.png`. That file matches `branding/primary-logo-transparent.png`.
- Cream/white export of the same mark: `branding/primary-logo.png` (also stored as `redesign/images/brand/logo-botanical-bg.png`). Pages do not use it in the header or footer.
- Archived wide logo, not used in the redesign UI: `branding/original-logo.png` and `redesign/images/brand/archive/original-logo.png`.
- **Pending:** the near-square botanical wordmark is too small in the desktop header. The local builder is fixing that separately. Do not treat the current header size as final.
- Contact form on `redesign/contact/` is **review-only**. It does not submit anywhere.
- **No field Core Web Vitals** were measured. `redesign/QA/lighthouse-home.json` is a lab Lighthouse run against a local static server only.
- QA notes and screenshots: `redesign/QA/`.

Open `redesign/index.html`, or serve the `redesign/` directory with any static file server. Source archive pages stay under `source-snapshot/` (`pages/`, `text/`, `images/`).

## Source snapshot counts

- 30 readable page texts in `source-snapshot/text/`
- 31 saved HTML documents in `source-snapshot/pages/` (includes both `00-index.html` and `index.html`) plus matching `.raw.html` copies
- 86 images in `source-snapshot/images/`
- Supporting same-site CSS/JS under `source-snapshot/assets/`

Content and imagery belong to Wellness Origin and their suppliers. This import is for authorized redesign and review.
