# SARKSH GROW SEO + Webinar Booking Update

## SEO changes completed

- Updated homepage title and meta description for finance education, market webinars, and Hyderabad intent.
- Added index/follow robots meta for homepage.
- Added Open Graph and Twitter Card metadata for better sharing previews.
- Added geo metadata for Telangana/Hyderabad relevance.
- Added JSON-LD structured data for Organization, FinancialService, WebSite, WebPage, and FAQPage.
- Added a visible FAQ section so the structured FAQ content is also present on the page.
- Updated sitemap to keep only the public homepage as the SEO target.
- Added noindex/nofollow meta to login.html, partal.html, and grath.html so admin/functional pages do not compete with the public homepage in Google.

## Where webinar booking details go

The Free Webinar form posts to the existing Google Apps Script endpoint in index.html:

```js
https://script.google.com/macros/s/AKfycbwgN-10CS3Me0EUNWsANT4ivQEL-nDhRRS1LxOD1al_bWT-MoKgjv4K0BKxGTIWjvi-/exec
```

The form sends:

- name
- phone
- email
- interest = free-webinar
- topic
- preferredTime
- message containing topic + slot + question
- originalMessage
- source = sarksh.in
- type = webinar_booking

For backward compatibility, the topic and preferred slot are also inserted into the `message` field. This means even if the Apps Script currently stores only basic contact columns, the booking details should still be visible in the message column.

For clean operations, update the connected Google Sheet / Apps Script later to include separate columns: Lead Type, Topic, Preferred Time, Source, Created At.
