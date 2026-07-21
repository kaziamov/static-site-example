---
title: Order Notifications Shopify App Pricing proof
description: Proof of resolution for the Shopify App Pricing 404 review issue.
permalink: /order-notifications/review-proof-20260721/
---

<article class="document" markdown="1">
<p class="eyebrow">Verified July 21, 2026</p>

# Order Notifications Shopify App Pricing proof

## Summary

The Shopify review screencast showed a Shopify Admin 404 at:

`/charges/order-notifications/pricing_plans`

That page is Shopify's hosted App Pricing plan selection page. It is outside
the Order Notifications app iframe.

Order Notifications no longer sends reviewers or merchants to that hosted page
from the embedded app. Pricing is shown inside the embedded app for this release.

## Current behavior

- The embedded Pricing page now renders plan details and email usage inside the app.
- The app shows the "Manage plan in Shopify" action in a disabled state while the app record is not published.
- The disabled action has no `pricing_plans` link target.
- The app shows a notice explaining that Shopify plan selection is unavailable because the app record is not published yet.
- Opening and reloading `/app/pricing` keeps the reviewer inside the embedded app.

## Production verification

- Shopify Admin app URL: `https://admin.shopify.com/store/devstore222024/apps/order-notifications-11/app`
- App iframe origin: `https://order-notifications.kaziamov.com`
- Verified Worker version: `5c3aa535-d356-4c72-a12c-b7ec308ba3c6`
- Result: embedded Pricing page opens without Shopify Admin 404.
- Result: reloading the embedded Pricing URL keeps the Pricing page visible.
- Result: "Email usage this month" is visible.
- Result: "Shopify plan selection is not available because this app record is not published yet." is visible.
- Result: "Manage plan in Shopify" is visible and disabled.
- Result: no active `pricing_plans` URL is exposed.

## Reviewer note

The hosted Shopify URL can still return Shopify Admin 404 while Shopify cannot
resolve the hosted App Pricing surface for the app record. Order Notifications
does not route merchants to that hosted page from the embedded app, so the
reviewer-facing billing flow remains inside the app and avoids the Shopify Admin
404 shown in the screencast.

</article>
