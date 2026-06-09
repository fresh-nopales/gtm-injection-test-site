# GTM Injection Test Site

A single-page test harness with buttons that push the standard set of GA4 ecommerce events to `window.dataLayer`. Useful for validating Google Tag Manager configurations and tag firing.

## Usage

Open `index.html` (locally or via the GitHub Pages URL) and click any event button. Each click pushes a standard GA4 ecommerce event and logs it in the on-page console.

**Note:** This page intentionally does *not* initialize `dataLayer`. Pushes will fail (and log an error) until you either:

- Add your GTM container snippet to `index.html`, or
- Manually run `window.dataLayer = window.dataLayer || [];` in the browser console.

## Events included

`view_item_list`, `select_item`, `view_item`, `add_to_wishlist`, `add_to_cart`, `remove_from_cart`, `view_cart`, `begin_checkout`, `add_shipping_info`, `add_payment_info`, `purchase`, `refund`, `view_promotion`, `select_promotion`

## Deploying with GitHub Pages

In the repository, go to **Settings → Pages**, set **Source** to **Deploy from a branch**, choose **main / (root)**, and save. The site will be served at `https://fresh-nopales.github.io/gtm-injection-test-site/`.
