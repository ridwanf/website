# AGENTS.md

Personal portfolio site for **Ridwan Fansuri**, built from the **Folio** template (Laurent Begey / ThemeWagon). Static HTML + Tailwind CDN + Alpine.js, served by a minimal Express server, deployed to GitHub Pages (`ridwanfansuri.com`).

## Commands

```sh
node server.js          # serve the site locally at http://localhost:3000
```

No build step — Tailwind (play CDN) and Alpine.js (jsDelivr) load at runtime.

## Architecture

- One standalone HTML page per route: `index.html` (home), `projects.html`, `blog.html`, `blog-article.html`, `case-study.html`.
- No shared partials/includes. `<head>`, nav, footer, inline `<style>` and `<script>` are **copy-pasted across all 5 files**. Theme or nav changes must be applied to every page.
- All CSS/JS is inline in each HTML file (Tailwind config, custom utilities, Alpine state, scroll-reveal observers). There are no separate `.css`/`.js` files.
- Local images live in `imgs/` (kebab-case names; `.jpeg` for photos, `.png` for screenshots). Other imagery comes from Unsplash / pravatar.
- Root-level `robots.txt`, `sitemap.xml`, and `favicon.svg` are served as-is by GitHub Pages.
- `server.js` serves the whole directory with `express.static` on port 3000 (Express 5).
- Deployment is GitHub Pages via the `CNAME` (`ridwanfansuri.com`).

## Conventions

- **Two divergent Alpine/CSS conventions exist — match the file you're editing:**
  - `index.html`: state via `x-data="app()"` (a `function app()`), class-based keys (`s`, `sc`, `mm`, `dark`), custom utilities `.nl`, `.card-h`, `.stag`, `.d1–d4`; reveal class is `.reveal .in`.
  - `projects.html`, `blog.html`, `blog-article.html`, `case-study.html`: inline Alpine object literals (or `projects()`), classes `.nav-link`, `.btn-primary`, `.photo-frame`; reveal class is `.reveal .visible`.
- Tailwind CDN compiles only class strings that appear literally in the source. Classes injected inside Alpine `x-for`/`:class` templates must also exist as full class names somewhere in the source.
- Every page `<head>` carries SEO tags: `<link rel="canonical">` (own URL), `og:*` + `twitter:*` (share image = `imgs/profile.jpeg`), `<link rel="icon" href="/favicon.svg">`, and the Tailwind CDN script is loaded with `defer`. Icon-only nav buttons need a static `aria-label` (Alpine `:aria-label` alone is invisible to crawlers).
- Styling system: `darkMode: 'class'`, fonts PT Sans (display) + DM Sans (body), accent color `#FF6B2B` (`accent` / `accent-light`).
- Keep the "Developed by Laurent Begey • Distributed by ThemeWagon" footer credit. `projects.html` uses a shorter footer without it — intentional, don't "fix".

## Known issues / pitfalls

- **Footer year bug:** `index.html`, `blog.html`, `blog-article.html`, `case-study.html` use `<span id="yr">` but scripts query `getElementById('year')` — the year is never rendered on these pages (only `projects.html` matches).
- `index.html` has large commented-out sections (About, Testimonials, Contact) with leftover template copy.
- Secondary pages still contain **template placeholder content** ("Eliott", fictional clients/projects like Novu/Finlo/Orea). These are demo placeholders — don't rewrite them as if intentional without being asked. Their head copy (titles/descriptions) is still placeholder and too short for SEO (30–60 / 120–160 chars) — update it when those pages get migrated to real content.
- Tailwind CDN runtime means dynamic classes work, but be careful with literal class strings inside Alpine templates (see Conventions).
- `imgs/property-pulse.png` is ~664 KB — worth optimizing if touched.

## Customization status

- `index.html` is fully personalized (hero, brand `ridwanfansuri`, links, real portfolio cards → `seocheck.ridwanfansuri.com`, `property-pulse.ridwanfansuri.com`).
- `projects.html`, `blog.html`, `blog-article.html`, `case-study.html` are largely un-migrated template demo content.
