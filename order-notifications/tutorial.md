---
title: Order Notifications tutorial
description: Setup tutorial for the Order Notifications Shopify app.
permalink: /order-notifications/tutorial/
---

<article class="document" markdown="1">
<p class="eyebrow">Setup tutorial</p>

# Set up Order Notifications

This tutorial walks through the first working notification. It assumes the app
is already installed from Shopify and opens inside the Shopify admin.

## 1. Create a recipient rule

Open Order Notifications and choose **Create rule**. A rule describes one
operational handoff: who should be notified, which orders qualify, and what the
recipient is allowed to see.

Choose the closest role preset:

- **Supplier** for vendor-specific fulfillment.
- **Warehouse / 3PL** for fulfillment teams.
- **Internal team** for staff who need order context.
- **Service provider** for external partners.
- **Manager / Owner** for oversight.

## 2. Choose filters

Add filters only when the recipient should receive a subset of orders. Common
filters include vendor, product, payment status, shipping country, and minimum
order total.

If a supplier should only see their own products, enable the supplier-focused
item visibility mode and keep the rule scoped to that supplier's items.

## 3. Select visible details

Review the privacy options before sending anything. Select only the details that
recipient needs to act:

- Items
- Shipping region
- Customer contact
- Pricing
- Notes

Unselected details are not included in the rendered notification.

## 4. Pick Email or Slack

For Email, enter the destination email address. For Slack, paste the
incoming-webhook URL for the channel that should receive order alerts.

Keep destinations current. Messages sent to a configured destination are treated
as delivered to that destination.

## 5. Send a test

Use **Send test** before activating the rule. Confirm that:

- The message arrives in the expected inbox or Slack channel.
- The message contains the selected fields only.
- The recipient can understand what action they should take.

## 6. Activate the rule

Activate the rule when the test looks correct. New matching orders will now
trigger notifications. Delivery status is visible in the app's activity view.

## 7. Troubleshoot delivery

If a message does not arrive, check:

- The rule is active.
- The order matches the filters.
- The destination email address or Slack webhook is correct.
- The message did not land in spam or a restricted Slack channel.

For help, email [ilia@kaziamov.com](mailto:ilia@kaziamov.com) with the store
domain, rule name, approximate time, and what you expected to happen. Do not
send customer data, Shopify API credentials, or Slack tokens.

</article>
