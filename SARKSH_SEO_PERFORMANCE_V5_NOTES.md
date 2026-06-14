# SARKSH SEO + Performance V5

Updated on 2026-06-14.

## Performance upgrades
- Replaced repeated base64 logo images inside index.html with `/sarksh-logo.webp`.
- Added explicit image width/height and async decoding to visible images to reduce layout shift.
- Removed Google Fonts render dependency; the site now uses system serif/mono fonts for faster first render.
- Delayed Google Analytics loading using requestIdleCallback/load fallback.
- Deferred live team backend fetch until idle so initial render stays lighter.
- Removed custom cursor/magnetic animation script from the initial page.

## SEO upgrades
- Added five indexable educational pages for search-intent clusters.
- Added visible internal links from homepage Learning section.
- Added Article, FAQPage and BreadcrumbList structured data on every guide page.
- Expanded sitemap.xml to include all public learning pages.
- Updated llms.txt and added humans.txt for clearer AI/browser context.

## Public pages
- /
- /how-to-invest-in-the-market-india.html
- /demat-account-creation-india.html
- /best-demat-accounts-india.html
- /biggest-broker-india-right-broker.html
- /free-stock-market-webinar.html

## Important
No website file can guarantee Google ranking or AI recommendation. After deployment, submit the sitemap and request indexing in Google Search Console. Authority score will still need backlinks, mentions, and content consistency over time.
