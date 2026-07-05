---
title: Order Notifications FAQ
description: Frequently asked questions for merchants using Order Notifications.
permalink: /order-notifications/faq/
---

<article class="document" markdown="1">
<p class="eyebrow">Merchant FAQ</p>

# Order Notifications FAQ

## What is Order Notifications?

Order Notifications is a Shopify app for operational handoffs. It sends new
order alerts to the people who need to act on an order, such as suppliers,
warehouse teams, service providers, managers, or internal staff.

## Which delivery channels are supported?

The app supports Email and Slack. Email notifications are sent through a verified
sender domain. Slack notifications are sent to incoming-webhook URLs configured
by the merchant.

## Does the app change orders or inventory?

No. The app reads order data to decide who should receive a notification and
what details should be included. It does not modify orders, products, inventory,
customers, discounts, or storefront content.

## What Shopify permissions does it request?

The app requests `read_orders`. It also registers Shopify's mandatory compliance
webhooks: `customers/data_request`, `customers/redact`, and `shop/redact`.

## Why does the app need protected customer data?

Some recipient rules may need customer name, email, shipping city, or shipping
country to complete an operational handoff. Merchants control whether those
fields are included for each recipient. Full street address, phone number, and
unselected order details are not rendered in notifications.

## Can suppliers see only their own items?

Yes. Supplier-oriented rules can be configured so recipients see only their own
line items and only the order fields selected by the merchant.

## How long is notification data retained?

Encrypted order payloads and notification content are deleted within 24 hours of
being processed or sent. Delivery history is kept for 30 days. Audit records are
kept for 90 days and contain no customer-identifying information.

## Is there a storefront script or customer tracking?

No. The app has no storefront component, sets no cookies on the storefront, and
uses no advertising or analytics trackers on customer devices.

## What should I do if a notification was not delivered?

Check that the rule is active, the destination email address or Slack webhook is
current, and the order matches the rule filters. If the issue continues, email
[ilia@kaziamov.com](mailto:ilia@kaziamov.com) with the store domain, approximate
time, and rule name. Do not include customer data or credentials.

## How do I uninstall the app?

Uninstall it from the Shopify admin. Uninstalling revokes the app access token
and deletes recipient configuration and stored delivery connection secrets.

</article>
