---
title: Order Notifications changelog
description: Public changelog for merchant-facing Order Notifications updates.
permalink: /order-notifications/changelog/
---

<article class="document" markdown="1">
<p class="eyebrow">Public changelog</p>

# Order Notifications changelog

This changelog summarizes merchant-facing and review-relevant updates. Internal
implementation notes are kept out of this page unless they affect setup,
privacy, delivery behavior, or app review evidence.

## July 5, 2026

### Settings persistence and save behavior

- Fixed a critical settings-save issue so merchants can persist delivery and
  rule configuration reliably.
- Reconciled the current UI against the v2 product target and recorded the
  remaining release-readiness work.

## July 4, 2026

### Legal docs and App Store review package

- Prepared the privacy policy and terms of service for public App Store
  submission.
- Added legal ownership answers and review-facing support copy.
- Prepared near-complete App Store listing content, including pricing, resource
  URLs, and screenshot plan.

### Slack connection workflow

- Added Slack connection guidance and improved the Slack setup flow for
  merchants who route order alerts to team channels.

### Production deployment preparation

- Prepared and verified production deployment material for the live app
  environment.
- Added proof and audit updates for the Slack and Pub/Sub delivery path.

## July 3, 2026

### Release gate and runtime checks

- Re-ran production preflight and local release-gate checks.
- Added runtime consistency evidence across the design target, cloud deployment,
  and delivery path.
- Added fail-fast guards for production auth and email sender configuration.

## July 2, 2026

### Listing and pricing updates

- Prepared App Store listing copy v2.
- Recorded managed pricing plan evidence.
- Fixed save-bar behavior and prepared listing screenshots.
- Added direct Resend email delivery notes.

## June 30, 2026

### Admin UI and architecture foundation

- Implemented the redesigned admin UI.
- Wired the availability-class contract and Edge/backend integration plan.
- Added Cloudflare Workers, Hyperdrive, and async FastAPI deployment notes.

</article>
