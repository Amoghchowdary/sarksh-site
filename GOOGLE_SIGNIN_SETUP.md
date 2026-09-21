# SARKSH GROW — Google Sign-In setup (V31)

## OAuth client

- Application type: Web application
- Publishing status during testing: Testing
- User type: External
- Web Client ID: `687485921080-fefl8hd7h5ka2dj9t39q2g717t8b602u.apps.googleusercontent.com`
- Authorized JavaScript origins:
  - `https://www.sarksh.in`
  - `https://sarksh.in`
- Authorized redirect URIs: not required for the current Google Identity Services JavaScript callback flow.

## Branding URLs

- Home: `https://www.sarksh.in/`
- Privacy: `https://www.sarksh.in/privacy.html`
- Terms: `https://www.sarksh.in/terms.html`
- Authorized domain: `sarksh.in`

## Testing

While the OAuth app is in **Testing**, add each Google account that should sign in under Google Auth Platform → Audience → Test users.

## Backend requirement

The frontend is configured to send the Google ID credential to the existing Apps Script endpoint using action `googleLogin`. The backend must securely validate that credential and then create/link the SARKSH customer session. Do not trust an ID token merely because it decoded in the browser.

## Security

The OAuth **client secret is deliberately not stored anywhere in this website package**. The browser only needs the Web Client ID. If a secret was exposed, rotate it in Google Auth Platform.
