# SARKSH Favicon Fix Notes

This package fixes the Google favicon issue by replacing the previous embedded `data:image/...` favicon with real public files at the website root.

## Files added
- `favicon.ico`
- `favicon-48x48.png`
- `favicon-96x96.png`
- `apple-touch-icon.png`
- `android-chrome-192x192.png`
- `android-chrome-512x512.png`
- `sarksh-favicon.png`
- `site.webmanifest`
- `robots.txt`
- `sitemap.xml`

## HTML pages updated
- `index.html`
- `grath.html`
- `login.html`
- `partal.html`

## Deployment steps
1. Upload/commit all files in this folder to the GitHub Pages repository root.
2. Confirm these open in browser after deployment:
   - `https://www.sarksh.in/favicon.ico`
   - `https://www.sarksh.in/favicon-48x48.png`
   - `https://www.sarksh.in/site.webmanifest`
   - `https://www.sarksh.in/robots.txt`
   - `https://www.sarksh.in/sitemap.xml`
3. In Google Search Console, use URL Inspection for `https://www.sarksh.in/` and request indexing.
4. Wait for Google to recrawl. Google can take several days to several weeks to refresh the favicon in Search.

Important: keep the favicon URLs stable. Do not rename them repeatedly, because Google recommends stable favicon URLs.
