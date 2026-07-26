# Ecommerce Tools static site

Static public site for Ecommerce Tools legal, support, and Shopify App Store
resource pages.

Production domain:

<https://apps.kaziamov.com>

## Current app resources

Order Notifications:

- Developer website: <https://apps.kaziamov.com/ecommerce-tools/>
- Privacy policy: <https://apps.kaziamov.com/ecommerce-tools/order-notifications/privacy/>
- Terms of service: <https://apps.kaziamov.com/ecommerce-tools/order-notifications/terms/>
- FAQ: <https://apps.kaziamov.com/ecommerce-tools/order-notifications/faq/>
- Changelog: <https://apps.kaziamov.com/ecommerce-tools/order-notifications/changelog/>
- Tutorial: <https://apps.kaziamov.com/ecommerce-tools/order-notifications/tutorial/>
- Additional app documentation: <https://apps.kaziamov.com/ecommerce-tools/order-notifications/docs/>
- Support: <https://apps.kaziamov.com/ecommerce-tools/order-notifications/support/>

## Structure

- `_config.yml` - GitHub Pages/Jekyll configuration.
- `_layouts/default.html` - shared page shell.
- `_includes/` - reusable head, header, and footer fragments.
- `assets/site.css` - site styling.
- `ecommerce-tools/index.md` - Ecommerce Tools hub page (`/ecommerce-tools/`).
- `ecommerce-tools/order-notifications/` - public app-specific pages.
- `CNAME` - custom domain for GitHub Pages.

## Deploy

The repository includes `.github/workflows/pages.yml` for GitHub Pages Actions.
In the repository settings, configure Pages to deploy from GitHub Actions and
set the custom domain to `apps.kaziamov.com`.

## Local preview

If Jekyll is installed locally:

```sh
jekyll serve
```

Then open <http://127.0.0.1:4000>.

This site does not require Node, a frontend build step, or a database.
