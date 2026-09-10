# Web Development Manager — Technical Assignment

This repository contains two Shopify theme builds from the assignment's Figma file:
[Test 1 — Landing page](#) and [Test 2 — Product card](#), built on top of the Dawn theme.

**Live preview:** https://ocommerce-vuiiets1.myshopify.com/
**Storefront password:** demo

---

## 1. What's in this repo

sections/
  hero-banner.liquid
  drop-teaser.liquid
  text-mask.liquid
  featured-collection-card.liquid
assets/
  section-hero.css

> Note: the product card markup is written directly inside
> `featured-collection-card.liquid` rather than a separate snippet.

These files are designed to sit inside a standard Dawn theme install — copy them into
the matching folders of your own Dawn checkout and they should work without further
wiring, aside from adding the sections through the theme editor.

---


## 2. Test 1 — Landing page

- **Hero** — sections/hero-banner.liquid
- **Drop teaser** — sections/drop-teaser.liquid
- **Display text** — sections/text-mask.liquid

All three are added to the home page in the theme editor, and each is a standalone,
reusable section with its own schema that can be added, removed, and reordered
independently.

**Countdown zero-state:** - When Countdown reaches to zero it will show message The wait is over! 

**Newsletter signup:** wired to Shopify's native customer/newsletter form
(`<form type you used, e.g. {% form 'customer' %}>`), with success and error states
shown inline.

**Display text technique:** `<name the CSS technique, e.g. background-clip: text>`,
with a fallback of `<describe fallback>` for browsers that don't support it.

---

## 3. Test 2 — Product card

- **Grid section:** `sections/featured-collection-card.liquid`

The card markup currently lives inline in this section rather than in a separate
snippet. It is driven entirely by Liquid product/variant data, not hardcoded markup.

**Implemented states:**
- Color swatches, with an overflow indicator past `<N>` colors
- Quick add via AJAX (Cart AJAX API), with handling for a failed request and
  rapid double-clicks
- Clearance badge, Final Sale badge, vendor line, and compare-at price
  (unhidden from Figma and shown conditionally on product data)

**Tested against:** a 1-color product, a 12-color product, a fully sold-out product,
a product with a sold-out single variant, a product with and without a compare-at
price, a very long title, and a product with a missing image.

---

## 4. Responsive behavior

Responsive work so far targets **mobile View**.

Breakpoint used: 600px

Reasoning: This Breakpoint is Used to make site mobile responsive

---

## 5. Accessibility

- Keyboard reachable controls (swatches, quick add, CTA, email form)
- Visible focus states on all interactive elements
- Meaningful alt text on all images
- Logical heading order across both tests
  
---

## 6. Commit history

Commits are structured to show incremental, working progress rather than one large
drop — see the commit log for the build order.
