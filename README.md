# fehermosilla.com

Personal landing + interactive research cases for Felipe Hermosilla — Partner Success & Revenue Operations Lead.

The site is **plain static HTML** (self-contained pages, no build step needed). It lives in `public/`, which Astro copies verbatim to the deploy output — so the existing Cloudflare Pages pipeline (`astro build`) keeps working without config changes.

## Pages

- `public/index.html` — landing (bilingual EN/ES, dark hero, metrics, experience, research, stack, contact)
- `public/articulo-vino.html` — research case: wine-plant discrete-event simulation (scrollytelling)
- `public/articulo-basquet.html` — research case: basketball fan research (NPS, regression quadrant)

## Features

- Bilingual EN/ES toggle, persisted in localStorage, shared across pages
- Scroll-driven storytelling, view transitions, side mini-TOC, reduced-motion safe
- Design tokens: paper #F4F2EA · ink #17160F · vermilion #EA3D14 · Space Grotesk / Inter / JetBrains Mono

## Local dev

Open `public/index.html` directly, or `npm install && npm run dev`.

## Deploy

Auto-deploys from `main` to Cloudflare Pages.

## Notes

- `src/data/cv.json` is currently unused by the site (content lives in the HTML). Update or remove at will.
- OG image is SVG; rasterize to PNG if a platform rejects it: `rsvg-convert public/og-blueprint.svg -o public/og.png`.
