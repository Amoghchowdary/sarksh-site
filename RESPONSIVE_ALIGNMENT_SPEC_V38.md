# SARKSH GROW — Production Responsive Alignment Specification (V38)

## Objective
The public website must read as a production financial-technology interface rather than a design prototype. Alignment is governed by one container system, predictable breakpoints, non-overlapping content, stable typography and explicit mobile/tablet rules.

## Official brand assets
- Official company logo: `sarksh-company-logo.png` (exact supplied logo).
- Navigation mark: `bull-only-mark.webp` (bull-only extraction from the official supplied logo to avoid name clutter in compact navigation).
- Homepage bull visual: `bull-hero-home.webp`.

## Viewport classes

### Wide desktop — 1440px and above
- Homepage maximum content width: 1560px.
- Public product/legal pages: 1320px.
- Main side padding: fluid 20px–54px.
- Homepage hero: two columns; text approximately 40–45%, visual approximately 55–60%.
- Three product cards: 3 columns.
- No customer-facing text may overlap the bull artwork.

### Desktop / small laptop — 1181px to 1439px
- Same semantic hierarchy as wide desktop.
- Fluid container narrows automatically.
- Hero remains two columns while there is sufficient space.
- Navigation remains horizontal until the 1180px breakpoint.

### Tablet — 761px to 1180px
- Hero becomes one column.
- Bull visual receives the full content width below the main proposition.
- Product grid becomes 2 columns where space permits, then 1 column.
- Location and Velocity split layouts become single column.
- Navigation collapses into the mobile menu at 1180px to avoid crowded financial-site navigation.

### Mobile — 760px and below
- Page gutter: 16px.
- Single-column document flow throughout.
- Primary/secondary hero actions become full-width controls.
- Bull visual uses a square-ish crop and remains readable without horizontal scrolling.
- Product strip becomes one card per row.
- Contact fields, FAQs, products, Velocity and location stack vertically.
- Footer becomes one column.

### Compact mobile — 480px and below
- Bull-only navigation logo remains compact.
- Headline and section-title clamps reduce without breaking words.
- No horizontal overflow is permitted.
- Touch targets stay at approximately 40px+ height.

## Alignment rules
1. No floating/absolute product cards over the homepage bull visual.
2. Only small non-critical labels may sit over imagery.
3. Every grid child uses `min-width: 0` where long content could force overflow.
4. Page widths are controlled by one container variable per design family.
5. Section headings align to the same left and right content rails.
6. Forms and legal/footer content use the same page rails as the public product pages.
7. Images must preserve aspect ratio and never define the layout width by intrinsic pixel size.
8. Navigation must never wrap into a second line on desktop/tablet.
9. Customer-facing copy must describe the institution/products, not the website design itself.
10. Schema/SEO URLs remain absolute; internal navigation links remain relative and crawlable.

## Validation targets
- 1920 × 1080
- 1440 × 900
- 1366 × 768
- 1024 × 768
- 768 × 1024
- 430 × 932
- 390 × 844
- 360 × 800

## Release rule
A build is not production-ready if any primary text overlaps an image/card, any page introduces horizontal scrolling at the validation widths, or a product card/navigation label is clipped.
