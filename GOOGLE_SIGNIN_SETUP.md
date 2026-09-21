# SARKSH GROW — Google Sign-In activation

The website now contains the Google Identity Services front-end integration, but the OAuth credential and the production server-side verifier are account-specific and therefore are not hard-coded into this public website package.

## 1. Create the Google OAuth Web client

In Google Auth Platform / Google Cloud Console, create an **OAuth 2.0 Client ID → Web application**.

Authorized JavaScript origins:

- `https://www.sarksh.in`
- `https://sarksh.in` (only if you serve this origin directly)
- `http://localhost:8080` for local testing

Do not put a client secret in this GitHub Pages repository.

## 2. Add the Web Client ID

Open `assets/js/google-auth-config.js` and replace:

`REPLACE_WITH_GOOGLE_WEB_CLIENT_ID.apps.googleusercontent.com`

with the Web Client ID. The official Google button will then render automatically.

## 3. Add the backend action

The login page sends the Google ID token to the existing Apps Script web app as:

- `action = googleLogin`
- payload JSON: `{ "credential": "<Google ID token>" }`

The backend must verify the token **server-side** before creating a SARKSH session. Verify at least: signature, `aud` equals your Web Client ID, issuer, expiry, and use `sub` as the durable Google account identifier. Do not trust a client-side decoded token.

Expected successful JSON response:

```json
{
  "ok": true,
  "sessionToken": "SARKSH_SESSION_TOKEN",
  "email": "customer@example.com",
  "userId": "Customer-ABC123",
  "name": "Customer Name",
  "googleSub": "GOOGLE_ACCOUNT_SUB"
}
```

The current password + OTP flow remains untouched. Google Sign-In is an additional entry path, not a replacement for OTP on sensitive account actions.

## Security note

Do not use Google's `tokeninfo` endpoint as the production verifier. Google documents it as a debugging/testing aid and notes that it may be throttled. Use a production JWT/OIDC verifier on a backend that can validate Google's signing keys correctly, then issue your own SARKSH session token.
