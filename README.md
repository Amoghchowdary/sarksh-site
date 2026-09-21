# SARKSH GROW Website v29

Product-first SARKSH GROW website with SARKSH Trade, SARKSH Stream and SARKSH Velocity.

## v29 changes — 2026-09-21
- Fixed SARKSH Velocity and all shared product/SEO pages so CSS, favicons, logos and internal navigation use relative paths. Pages now render correctly when opened locally and when deployed at `https://www.sarksh.in/`.
- Preserved canonical URLs and absolute schema/OG URLs for SEO.
- Added Google Identity Services front-end integration to `login.html`.
- Added `assets/js/google-auth-config.js` and `assets/js/google-auth.js`.
- Existing password + email OTP authentication and the current Apps Script endpoint remain intact.
- Google Sign-In activates after adding the account-specific OAuth Web Client ID and a production `googleLogin` verifier to the Apps Script/backend. See `GOOGLE_SIGNIN_SETUP.md`.

## Local preview
Run `npm start` and open `http://localhost:8080/sarksh-velocity.html`.

## Deploy
Deploy the contents of this folder to the GitHub Pages repository root.
