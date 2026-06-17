SARKSH GROW - CLEAN GITHUB PAGES DEPLOYMENT PACKAGE

IMPORTANT:
Upload the CONTENTS of this sarksh-site-main folder to the repository root.
Do not upload the folder itself as /sarksh-site-main/.

Why the previous live page looked broken:
The HTML referenced /assets/css/sarksh.css and /assets/js/sarksh.js, but the assets folder was missing from the uploaded GitHub files. Browsers then rendered plain unstyled HTML.

This package fixes that risk in two ways:
1) Public pages include critical CSS and JS inline.
2) The /assets/css/sarksh.css and /assets/js/sarksh.js files are also included as backup.

After upload:
1. In GitHub repo, delete old root files that are not in this package.
2. Upload/replace all files from this package.
3. Wait for GitHub Pages deployment.
4. Open https://www.sarksh.in/?v=8 in Incognito.
5. Press Ctrl + Shift + R.

Preserved:
- Apps Script backend URL intact.
- GA4 gtag ID G-7YPG40KX6L intact.
- Internal pages login.html, partal.html, grath.html preserved.
