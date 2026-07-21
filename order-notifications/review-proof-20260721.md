---
title: Order Notifications Shopify App Pricing proof
description: Proof of resolution for the Shopify App Pricing 404 review issue.
permalink: /order-notifications/review-proof-20260721/
---

<article class="document" markdown="1">
<p class="eyebrow">Verified July 21, 2026</p>

# Order Notifications Shopify App Pricing proof

## Summary

The review screencast showed a Shopify Admin 404 at:

`/charges/order-notifications/pricing_plans`

This URL belongs to Shopify’s hosted App Pricing page and is outside the Order Notifications embedded app.

The issue occurred because the app exposed this link before the app listing and Shopify-hosted pricing page were available.

## Changes implemented

To prevent this issue from occurring again, we made the following changes:

* The Shopify-hosted plan management action is not available while the app is unpublished.
* When the app is unpublished, the app does not render or navigate to any `/pricing_plans` URL.
* Pricing information and current email usage are displayed directly inside the embedded app.
* Reviewers can open and reload `/app/pricing` without leaving the embedded app or encountering a Shopify Admin 404.
* A notice explains that Shopify plan selection will become available after the app is published.
* Once the app is published and Shopify-hosted pricing becomes available, the plan management action will be enabled for merchants.

## Verification

We verified that, while the app is unpublished:

* No active link to Shopify’s hosted pricing page is present.
* Clicking the pricing-related controls cannot initiate navigation to `/charges/order-notifications/pricing_plans`.
* Opening or refreshing `/app/pricing` remains inside the embedded application.
* Merchants and reviewers can still view the available plans and usage information without accessing the unavailable Shopify-hosted page.


</article>
