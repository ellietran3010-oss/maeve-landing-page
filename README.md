# MAEVE — Build Your Presence

Static landing page (single `index.html`, Tailwind via CDN — no build step).

Merged from two Stitch exports:
- `maeve_refined_behind_maeve_layout` (desktop) — shown at `md:` (≥768px) via `#desktop-view`
- `maeve_mobile_responsive_landing_page` (mobile) — shown below `md:` via `#mobile-view`

Both blocks share one `<header>`/nav and one `<footer>`. Nav/menu links use `#tribes`, `#philosophy`,
`#behind`, `#leads` for the desktop sections and `#tribes-m`, `#philosophy-m`, `#behind-m`, `#leads-m`
for the mobile sections, since both breakpoints have their own copy/layout for these sections.

## Images

All images are self-hosted in `/images` (cropped from the original Stitch full-page screenshots after
Stitch's temporary `lh3.googleusercontent.com/aida...` preview links expired). The 4 mobile-only photos
(hero/tribe1, "Always Busy", "Rebuilding Herself", founder sketch) reuse the equivalent desktop photos,
since no high-resolution source for the original mobile-specific photos was available locally. If you
still have access to the original Stitch project, you can swap in the real mobile photos by replacing
the files in `/images` (keep the same filenames, or update the `src`/`background-image` references in
`index.html`).

## Deploy to Vercel

No build step needed — this is a static file.

1. Push this folder to a GitHub repo.
2. In the [Vercel dashboard](https://vercel.com/new), import the repo.
3. Framework preset: **Other** (or "Static"). Leave build command empty, output directory `.`.
4. Deploy.

Or via CLI, from this folder:

```bash
npx vercel login
npx vercel --prod
```
