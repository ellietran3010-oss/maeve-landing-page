# MAEVE — Build Your Presence

Static landing page (single `index.html`, Tailwind via CDN — no build step).

Merged from two Stitch exports:
- `maeve_refined_behind_maeve_layout` (desktop) — shown at `md:` (≥768px) via `#desktop-view`
- `maeve_mobile_responsive_landing_page` (mobile) — shown below `md:` via `#mobile-view`

Both blocks share one `<header>`/nav and one `<footer>`. Nav/menu links use `#tribes`, `#philosophy`,
`#behind`, `#leads` for the desktop sections and `#tribes-m`, `#philosophy-m`, `#behind-m`, `#leads-m`
for the mobile sections, since both breakpoints have their own copy/layout for these sections.

## Known limitation

Images are hotlinked from Stitch's temporary `lh3.googleusercontent.com/aida...` preview CDN. These
are not guaranteed to stay available long-term. Before relying on this page for real traffic, download
the images and host them yourself (e.g. in an `/images` folder) and update the `src`/`background-image`
URLs.

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
