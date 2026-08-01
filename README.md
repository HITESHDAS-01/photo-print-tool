# Photo Print Layout — Deployable Microtool

AstroJS + Tailwind v4 version of the photo/ID-card A4 print layout tool, built
for deployment as a Cloudflare Pages microtool site (per your
`microtool-website-builder` workflow).

## What's in here

- `src/components/PhotoPrintTool.astro` — the actual tool (ported 1:1 from
  the single-file HTML version — same features: photo upload, size presets,
  ID Card auto-layout, print/PDF export)
- `src/pages/index.astro` — landing page: tool + SEO content (intro,
  how-it-works, size reference table, FAQ with schema.org markup)
- `src/layouts/Layout.astro` — SEO meta tags, dark mode (no-flash), PWA
  registration
- `public/manifest.json`, `public/sw.js`, `public/icons/` — PWA support
  (installable, works offline after first visit)
- `public/robots.txt` — update the sitemap URL once you have a real domain

## Run it locally

```bash
npm install
npm run dev
```

Opens at `http://localhost:4321`.

## Before you deploy

1. **Pick a domain** — following your keyword research process
   (`ahrefs.com/keyword-generator`, `instantdomainsearch.com`). Given this
   tool's angle (arranging *multiple* photos/ID cards on one page for
   printing — not AI background removal like most passport-photo sites),
   good keyword directions to test: "photo print layout", "print multiple
   photos one page", "id card print pdf", "passport photo sheet maker".
   Note: the plain "passport photo maker" niche is already crowded with big
   AI background-removal tools — your ID-card + India-specific angle is the
   differentiator, lean into that in the domain/copy.
2. Update `astro.config.mjs` → replace `site: 'https://your-domain-here.com'`
   with your real domain.
3. Update `public/robots.txt` → replace the sitemap URL with your real domain.
4. Generate a proper `og-image.png` (1200x630) and drop it in `public/` —
   referenced in `Layout.astro` for social sharing previews.

## Deploy

Follow **Phase 6 onward** of your `microtool-website-builder` skill:
Cloudflare Pages connect → build command `npm run build`, output dir `dist`
→ buy domain → connect custom domain → fix duplicate content (`_headers`
file) → Search Console → Bing Webmaster → AdSense once you have 10+ daily
users.

## Notes

- The tool itself needs no backend — everything (image resize, layout,
  print) runs client-side, so hosting stays free on Cloudflare Pages.
- If you rename/restructure the size presets or layout logic, edit
  `PhotoPrintTool.astro` directly — the `<script>` block there is
  self-contained (no external dependencies).
