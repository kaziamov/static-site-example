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

The app no longer sends reviewers or merchants to that hosted page while the
current app record is still in review/action-needed state.

## What changed

- The embedded Pricing page now renders plan details and email usage inside the app.
- The app hides the "Manage plan in Shopify" action by default.
- The app exposes no visible link or button that points to `pricing_plans`.
- The hosted Shopify plan page can be enabled later with an explicit runtime flag after publication.

## Production verification

- Shopify Admin app URL: `https://admin.shopify.com/store/devstore222024/apps/order-notifications-11/app`
- App iframe origin: `https://order-notifications.kaziamov.com`
- Worker version: `c56127ca-43b2-4350-bad7-e5c85fc46fdd`
- Result: embedded Pricing page opens without Shopify Admin 404.
- Result: reloading the embedded Pricing URL keeps the Pricing page visible.
- Result: "Email usage this month" is visible.
- Result: "Shopify plan selection is not available for this app record yet." is visible.
- Result: "Manage plan in Shopify" is not visible.
- Result: no visible `pricing_plans` URL is exposed.

## Staging verification

- Shopify Admin app URL: `https://admin.shopify.com/store/devstore222024/apps/first-shipify-app/app`
- App iframe origin: `https://staging-ordn.kaziamov.com`
- Worker version: `4dfabbd4-e961-4e6a-8848-c848f8ee9400`
- Result: embedded Pricing page opens without Shopify Admin 404.
- Result: reloading the embedded Pricing URL keeps the Pricing page visible.
- Result: "Email usage this month" is visible.
- Result: "Shopify plan selection is not available for this app record yet." is visible.
- Result: "Manage plan in Shopify" is not visible.
- Result: no visible `pricing_plans` URL is exposed.

## Reviewer note

The hosted Shopify URL can still return Shopify Admin 404 while Shopify cannot
resolve the hosted App Pricing surface for the app record. To avoid that
reviewer-facing failure mode, Order Notifications now keeps the merchant inside
the embedded app Pricing page until the hosted App Pricing page is explicitly
enabled for the published app record.

</article>
