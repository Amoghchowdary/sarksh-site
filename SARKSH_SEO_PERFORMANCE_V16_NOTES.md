# SARKSH GROW Website — SEO & Performance V16

## What changed

- Preserved the existing visual design and brand presentation.
- Kept the Google Apps Script backend URL intact in `index.html`, `login.html`, `grath.html`, and `partal.html`.
- Added a shared responsive/performance layer at `/assets/css/sarksh-seo-performance.css`.
- Added passive UX/performance JavaScript at `/assets/js/sarksh-performance.js`.
- Added `scripts/seo-audit.js` and updated `npm run check` to validate core SEO files.
- Expanded the sitemap to include all indexable public pages.
- Added a new Learning Center and three new educational SEO pages:
  - `learning-center.html`
  - `stock-market-risk-management-beginners.html`
  - `trading-vs-investing-india.html`
  - `stock-market-mistakes-beginners-india.html`
- Improved public positioning from “Indian families” toward first-time investors, retail investors, beginner traders and working professionals.
- Tightened homepage title, description, Open Graph and Twitter tags.
- Added/standardized extra metadata for search previews, AI summaries, manifest usage and responsive devices.
- Updated `llms.txt`, `humans.txt`, `site.webmanifest`, `robots.txt`, and `sitemap.xml`.

## Validation completed

- `npm run check` passed.
- JavaScript syntax check passed for shared JS and extracted inline scripts.
- Local HTTP smoke test passed for homepage, sitemap, CSS and JS assets.
- Internal local links and local asset paths were checked.

## Deployment

Upload the full folder contents to GitHub Pages. After deployment:

1. Open `https://www.sarksh.in/sitemap.xml` and confirm it loads.
2. Open Google Search Console.
3. Submit `https://www.sarksh.in/sitemap.xml`.
4. Use URL Inspection for the homepage and new Learning Center.
5. Request indexing for the new public pages.

