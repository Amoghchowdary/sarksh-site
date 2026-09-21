# SARKSH GROW Website — V32

Production website package for `www.sarksh.in`.

## Current public product family
- SARKSH Trade
- SARKSH Stream
- SARKSH Velocity (SARKSH Data / historical market intelligence)

## V32 focus
- Rebuilt public layout alignment and responsive grids.
- Rebuilt product page CSS with inline critical CSS fallback.
- Correct legal entity: SARKSH GROW FIN-TECH PRIVATE LIMITED.
- Stronger internal linking and canonical SEO structure.
- Updated exact-address Google Maps query and Business Profile link.
- Official Google Identity Services button on the login page.
- OAuth Web Client ID configured; no client secret is stored in frontend files.
- Apps Script Google-login integration patch included under `backend/`.
- Legacy product URLs are noindex redirect stubs only, to protect old backlinks while removing them from the active product portfolio.

Run `npm run check` before deployment.
