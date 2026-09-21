# SARKSH GROW — Google Sign-In V32

## Google Auth Platform
- OAuth client type: Web application
- Authorized JavaScript origins: `https://www.sarksh.in` and `https://sarksh.in`
- Audience: External
- Publishing status during testing: Testing
- Add every testing Google account under **Audience → Test users**.
- Homepage: `https://www.sarksh.in/`
- Privacy: `https://www.sarksh.in/privacy.html`
- Terms: `https://www.sarksh.in/terms.html`

## Website
`login.html` uses the official Google Identity Services JavaScript library and Google's rendered button. No client secret is present in the website.

## Apps Script backend
The website sends the Google ID credential to the existing Apps Script endpoint with the action `googleLogin`. The existing backend must route that action to a token-verification handler before a SARKSH session is created. A ready-to-integrate MVP patch is included in `backend/GOOGLE_LOGIN_PATCH.gs`.

If Google account selection succeeds but the page says the backend handler is not deployed, add the router branch and handler to the current Apps Script project, then redeploy the web app.

## Branding note
While the OAuth app remains in Testing or before brand verification is completed, Google may display generic/unverified project identity instead of the final SARKSH GROW name/logo in some authorization surfaces.
