---
title: Order Notifications documentation
description: Additional documentation for Order Notifications merchants and reviewers.
permalink: /order-notifications/docs/
---

<article class="document" markdown="1">
<p class="eyebrow">Additional documentation</p>

# Order Notifications documentation

## Resource map

| Resource | URL |
|---|---|
| Privacy policy | [/order-notifications/privacy/](/order-notifications/privacy/) |
| Terms of service | [/order-notifications/terms/](/order-notifications/terms/) |
| FAQ | [/order-notifications/faq/](/order-notifications/faq/) |
| Changelog | [/order-notifications/changelog/](/order-notifications/changelog/) |
| Setup tutorial | [/order-notifications/tutorial/](/order-notifications/tutorial/) |
| Support | [/order-notifications/support/](/order-notifications/support/) |

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

</article>
