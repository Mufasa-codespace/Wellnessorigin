# Logo size fix delta

## Problem
`images/brand/logo-botanical.png` (701×735, mark + “Wellness Origin” wordmark) rendered too small in the desktop header to read the wordmark.

## Fix (CSS / layout only — logo file untouched)
Updated `css/site.css` header brand sizing:

| State | Logo height (rendered) | Header height |
|-------|------------------------|---------------|
| Desktop default (1280) | **80px** | **100px** |
| Desktop sticky scrolled | **56px** | **72px** |
| Mobile (390) | **52px** | **68px** |

- Proportions preserved via `height` + `width:auto` + `aspect-ratio:701/735` + `object-fit:contain` (no stretch/crop).
- Nav does not overlap the brand (measured gap ~491px at 1280).
- Footer mark nudged to 72px for parity; still not inverted.

## Screenshots refreshed
- `shots/header-desktop.png`
- `shots/header-desktop-scrolled.png`
- `shots/header-mobile.png`
- `shots/home-desktop.png`
- `shots/home-mobile.png`
- Copied into `QA/screenshots/`

## Not changed
- Logo PNG itself
- No git push / deploy

## Measured rendered sizes (Playwright)
```json
{
  "desktop_top": {
    "logoH": 80,
    "logoW": 76.3,
    "headerH": 100,
    "gapBrandNav": 491.4,
    "overlap": false
  },
  "desktop_scrolled": {
    "logoH": 56,
    "logoW": 53.4,
    "headerH": 72,
    "scrolledClass": true
  },
  "mobile_top": {
    "logoH": 52,
    "logoW": 49.6,
    "headerH": 68
  }
}
```
