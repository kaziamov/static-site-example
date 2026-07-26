---
title: Order Notifications documentation
description: Additional documentation for Order Notifications merchants and reviewers.
permalink: /ecommerce-tools/order-notifications/docs/
---

[Order Notifications](/ecommerce-tools/order-notifications/) ·
[Privacy](/ecommerce-tools/order-notifications/privacy/) ·
[Terms](/ecommerce-tools/order-notifications/terms/) ·
[FAQ](/ecommerce-tools/order-notifications/faq/) ·
[Changelog](/ecommerce-tools/order-notifications/changelog/) ·
[Tutorial](/ecommerce-tools/order-notifications/tutorial/) ·
[Docs](/ecommerce-tools/order-notifications/docs/) ·
[Support](/ecommerce-tools/order-notifications/support/)

<p class="meta">Additional documentation</p>

# Order Notifications documentation

## Resource map

| Resource | URL |
|---|---|
| Privacy policy | [/ecommerce-tools/order-notifications/privacy/](/ecommerce-tools/order-notifications/privacy/) |
| Terms of service | [/ecommerce-tools/order-notifications/terms/](/ecommerce-tools/order-notifications/terms/) |
| FAQ | [/ecommerce-tools/order-notifications/faq/](/ecommerce-tools/order-notifications/faq/) |
| Changelog | [/ecommerce-tools/order-notifications/changelog/](/ecommerce-tools/order-notifications/changelog/) |
| Setup tutorial | [/ecommerce-tools/order-notifications/tutorial/](/ecommerce-tools/order-notifications/tutorial/) |
| Support | [/ecommerce-tools/order-notifications/support/](/ecommerce-tools/order-notifications/support/) |

## Permissions

- OAuth scope: `read_orders`.
- App-specific topics: `orders/create`, `app/uninstalled`.
- Mandatory compliance topics: `customers/data_request`, `customers/redact`,
  `shop/redact`.
- Protected customer fields may include customer name, customer email, shipping
  city, and shipping country when selected by a merchant rule.
- Full street address and customer phone number are not requested.

## Data minimization

Order Notifications is built around per-recipient visibility. A merchant chooses
which fields each recipient can see. For example, a supplier can receive their
own line items and shipping country without seeing customer email or order
total.

Webhook payloads are minimized to the fields required for routing and message
rendering. Notification payloads are encrypted and deleted within 24 hours after
processing or delivery.

## Delivery behavior

The app supports Email and Slack delivery. Shopify order events are processed in
a duplicate-safe delivery path so a replayed Shopify event does not send the
same message twice.

Delivery failures are retried automatically where safe to do so. Merchants can
review recent delivery status in the activity view.

## App review notes

For Shopify review, use the public URLs on this site and the support email
[support@kaziamov.com](mailto:support@kaziamov.com). Test credentials, store access,
and inbox details must be supplied through the approved private submission
channels, not committed to this repository.
