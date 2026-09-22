# Figs n Olives · Wateen Store

Staging build of the **Wateen** storefront (Tin Zaitoon): a fig, date, walnut, kalonji and extra virgin olive oil spread.

Single-file static prototype, ported from the Claude artifact. It mirrors the Shopify theme structure so the UX carries over at hand-off.

## Staging

https://ahmadsaeed10.github.io/figs-n-olives-store/

Deployed by `.github/workflows/pages.yml` on every push to `main` or `claude/**`. The page carries `noindex` while it's staging.

## What's inside

| Route | Page |
| --- | --- |
| `#home` | Landing: hero, buy box, ingredients, story, verse, serving ideas, texture, claims, reviews, FAQ |
| `#product` | PDP with gallery, spec accordions |
| `#cart`, `#checkout`, `#confirmed` | Cart, checkout (bank / COD / card), WhatsApp order hand-off |
| `#story`, `#faq`, `#contact` | Content pages |
| `#shipping`, `#returns`, `#privacy`, `#terms` | Policy drafts |

The **Handoff notes** toggle (bottom left) reveals photo briefs, Shopify section mapping and placeholder highlights.

## Configuration

Edit `CONFIG` and `VARIANTS` at the top of the `<script>` in `index.html`: shipping fee, free-delivery rules, payment methods, WhatsApp number, bank details, claims gate, prices.

## Before launch

- Replace bank details (`CONFIG.bank`) and contact placeholders.
- Staff order notifications: set in Shopify › Settings › Notifications to `aroosa.work0903@gmail.com`. Deliberately not in the public page source.
- Confirm claims (`CONFIG.claims`), nutrition, storage and shelf life after lab testing.
- Legal review of policy drafts.

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```
