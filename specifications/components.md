# Component registry — Elementor Pro

One visual pattern = **one** `comp-*` ID. Do not duplicate under informal names (`btn-primary`, `usp-icon-row`, etc.).

Canonical list: `brand/brand.json` → `components.registry`.

---

## Actions

### `comp-btn-primary`

| Property | Token / value | Confidence |
|----------|----------------|------------|
| Background | `color-yellow` | high |
| Text | `color-navy` | medium |
| Typography | `text-button` | medium |
| Radius | `radius-sm` | medium |
| Widget | Button | — |

**Used in:** hero, newsletter submit.

### `comp-btn-secondary`

| Property | Token / value | Confidence |
|----------|----------------|------------|
| Background | `color-white` | high |
| Border | `border-default`, `color-sky` | high |
| Text | `color-sky` | high |
| Widget | Button (outline) | — |

**Used in:** hero.

### `comp-btn-cart`

| Property | Token / value | Confidence |
|----------|----------------|------------|
| Background | `color-yellow` | high |
| Icon | Cart glyph, dark | high |
| Shape | Small square, `radius-sm` | high |
| Widget | WooCommerce add to cart (loop template) | — |

**Used in:** `comp-card-product` only.

### `comp-link-cta`

Sky text link with optional chevron (e.g. “Bekijk alle boeken”).  
**Widget:** Button (link style) or Heading link.  
**Used in:** `comp-section-heading`.

---

## Structure

### `comp-section-heading`

Flex row: `text-h2` title + optional `comp-link-cta` (space-between).  
**Used in:** product carousels.

### `comp-carousel-products`

`comp-section-heading` + carousel with **4** visible `comp-card-product` tiles + circular sky arrow controls.  
**Widget:** Loop Carousel / Products + Theme Builder loop item.  
**Used in:** homepage sections “Populaire theorieboeken”, “Online leren & oefenen” (stacked, not side-by-side).

### `comp-card-product`

White surface, `radius-sm`, stack: image (~1:1) → optional `comp-badge-choice` → title → price → `comp-btn-cart`.  
**Used in:** both product carousels.

---

## USP patterns (do not merge)

| ID | Layout | Distinct because |
|----|--------|------------------|
| `comp-usp-utility-bar` | 3 × single line in header top | Compact, header context |
| `comp-usp-checklist` | Green check + one line | Hero row + “Waarom” column |
| `comp-usp-feature-panel` | 5 × (icon + title + 2 lines) in **rounded panel** | Mid-page feature grid |
| `comp-usp-trust-strip` | 4 × on **navy** footer band | Inverse colors |

**Widgets:** Icon Box / Icon List combinations in flex containers.

---

## Badges

| ID | Style |
|----|--------|
| `comp-badge-choice` | `radius-pill`, sky bg, white text (“Meest gekozen”) |
| `comp-badge-cart-count` | Yellow circle on header cart |

---

## Forms

| ID | Description | Widget |
|----|-------------|--------|
| `comp-input-search` | Header wide search | Search Form (Pro) |
| `comp-form-newsletter` | Email + `comp-btn-primary` | Form (Pro) / ESP plugin |

Both: `color-white` fill, `radius-sm`, `border-default`.

---

## Info / trust blocks

| ID | Description | Widget |
|----|-------------|--------|
| `comp-block-steps` | “Hoe het werkt” numbered steps | Icon Box / containers |
| `comp-block-trustpilot` | Trustpilot summary | Official embed / HTML |
| `comp-block-testimonial` | Quote + author + arrows | Testimonial Carousel |
| `comp-grid-info-4` | **One row:** steps \| Trustpilot \| testimonial \| checklist (`comp-usp-checklist`) | Container 4-col |

Do **not** specify separate full-width “step row” and “three-column trust” sections—the mockup combines these in **one 4-column band**.

---

## Navigation

| ID | Description |
|----|-------------|
| `comp-nav-primary` | Theorieboeken, Online oefenen, Pakketten, Voor wie, Over ons + dropdowns |
| `comp-nav-utility` | Klantenservice (dropdown), Inloggen, cart + `comp-badge-cart-count` |

**Widget:** Nav Menu (Pro), WooCommerce Menu Cart.

---

## Component → homepage map

| Homepage section | Components |
|------------------|------------|
| Header | `comp-usp-utility-bar`, `comp-nav-primary`, `comp-nav-utility`, `comp-input-search` |
| Hero | `text-h1`, `text-body`, `comp-btn-primary`, `comp-btn-secondary`, `comp-usp-checklist` |
| USP features | `comp-usp-feature-panel` |
| Product lists ×2 | `comp-carousel-products` |
| Info band | `comp-grid-info-4` |
| Footer | `comp-usp-trust-strip`, `comp-form-newsletter`, social (footer spec) |

---

## Unresolved

- Focus/hover states  
- Woo loop fields (rating, excerpt) not on card in mockup  
