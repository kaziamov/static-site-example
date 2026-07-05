---
title: Order Notifications privacy policy
description: Privacy policy for the Order Notifications Shopify app.
permalink: /order-notifications/privacy/
---

<article class="document" markdown="1">
<p class="eyebrow">Effective July 4, 2026</p>

# Order Notifications privacy policy

## Who we are

Order Notifications is operated by Ilia Kaziamov, an individual entrepreneur
registered in Georgia (I/E ILIA KAZIAMOV) - "we", "us" or "the operator" in
this policy. For anything related to this policy or your data, contact
[ilia@kaziamov.com](mailto:ilia@kaziamov.com).

## What data we access from Shopify

When you install Order Notifications, we request access to your store's order
data (`read_orders`). For each new order, Shopify sends us a minimized set of
fields: order ID and display name, total, currency, payment status, line items,
tags, shipping country/city, customer name and email, and the order note. We
never request the customer's phone number or full street address.

## Data you provide directly

- **Recipient contact details:** the email addresses and Slack incoming-webhook
  URLs of the people and teams you configure as recipients, such as suppliers,
  warehouse staff, or your own team. These are stored encrypted.
- **Notification settings:** recipient rules, filters, and the order fields
  each recipient is allowed to see.
- **Support correspondence:** anything you send to our support address.

We do not ask you for information about your customers, and you should not
include customer data in support requests.

## Data from your customers

We collect nothing from your customers directly. The app has no storefront
component, sets no cookies on your storefront, and uses no tracking technologies
on customer devices. Customer data reaches us only inside the minimized order
payload described above, relayed by Shopify.

## Cookies and sessions

The embedded admin app uses functional session cookies solely to keep you signed
in while you use the app inside the Shopify admin. We use no advertising or
analytics trackers.

## How we use data

You configure one or more recipients, such as a supplier, warehouse, internal
team, or manager. Each recipient sees only the order fields you explicitly
choose to share with them. For example, a supplier might see only their own line
items and the shipping country, never the customer's name or the order total.

We use order data only to render and send those notifications and to show you
delivery status. We do not build customer profiles or analytics, we do not use
the data for any other purpose, and we do not sell it to anyone.

## Our role in data processing

For personal data contained in your store's orders, you, the merchant, are the
data controller and we act as a data processor on your instructions. Your
recipient rules determine what is processed and who receives it. We process this
data only to provide the app's functionality and we honor Shopify's mandatory
privacy webhooks described below. This policy also serves as our data protection
agreement with you.

## How long we keep it

- Encrypted order payloads and notification content are deleted within 24 hours
  of being processed or sent.
- Recipient configuration is kept until you delete it or uninstall the app.
- Delivery history is kept for 30 days so you can see what was sent.
- Audit records are kept for 90 days for security purposes and contain no
  customer-identifying information.
- Shopify access tokens are kept only while the app is installed and are purged
  immediately when you uninstall.

## Service providers (subprocessors)

We use a small set of infrastructure and delivery providers to run the app:

- **Shopify** - the commerce platform; source of order data and billing.
- **Google Cloud (Pub/Sub)** - receives new-order webhooks from Shopify and
  queues them for our workers; data in the queue is encrypted in transit and at
  rest.
- **Cloudflare** - serves and secures the embedded admin app and holds its
  session data.
- **Resend** - email delivery; receives the rendered notification message and
  the recipient's email address, not your raw order data.
- **Slack** - only if you configure a Slack recipient; receives the rendered
  message at the incoming-webhook URL you provide.

Application data, including settings, queued notifications, and delivery
history, is stored on our own backend infrastructure. We do not sell your data,
and we share it only with the providers listed above, only as needed to deliver
the service.

## Where data is processed

We are established in Georgia and are not established in the European Union. Our
backend infrastructure, including the application database and workers, is
located in Georgia. The providers listed above process data in the United States
and other regions where they operate. Wherever data is processed, it is
protected by the safeguards described in this policy: field minimization,
encryption in transit and at rest, and short retention windows.

## Security

Sensitive fields, including Shopify access tokens, queued order payloads,
notification content, and recipient destinations, are encrypted at rest. All
traffic uses TLS, and requests between our edge and backend are signed. Access
to production data is limited to the operator, and security-relevant actions are
recorded in an audit log.

## Your rights (GDPR and similar laws)

We implement Shopify's mandatory privacy webhooks. When you or your customers
request data access or deletion through Shopify (`customers/data_request`,
`customers/redact`, `shop/redact`), we respond automatically: stored
notification content for the affected customer is redacted and shop data is
deleted on schedule. You can also email us at
[ilia@kaziamov.com](mailto:ilia@kaziamov.com) to request a copy or deletion of
the data we hold for your store.

## Uninstalling

Uninstalling the app revokes our access token immediately and deletes your
recipient configuration and any stored delivery connection secrets.

## Changes to this policy

We may update this policy as the app evolves. The current version is always
published at this URL with its effective date. If a change materially affects
how we handle your data, we will notify installed merchants by email.

## Contact

Questions about this policy or your data:
[ilia@kaziamov.com](mailto:ilia@kaziamov.com) (Ilia Kaziamov,
I/E ILIA KAZIAMOV, Georgia).

</article>
