# Homepage — desktop

**Reference:** `design/homepage/desktop.png`  
**Tokens / components:** `brand/brand.json`, `specifications/components.md`  
**Do not build** until approved.

---

## Page shell

| Setting | Value | Confidence |
|---------|--------|------------|
| Canvas background | `color-page` | medium |
| Content width | `layout-content-width` | medium |
| Header/footer | Theme Builder | high |

---

## Section A — Header (Theme Builder)

See `specifications/header.md`.

---

## Section B — Hero

| Item | Detail |
|------|--------|
| Purpose | Value prop + CTAs + trust checks + product visual |
| Surface | `color-white` (on `color-page`) | medium |
| Layout | Boxed → 2 columns (~45% / ~55%) | medium |

**Observed copy (verify before publish)**

- H1: *Bereid je slim voor op je CBR-theorie-examen*
- Primary CTA: *Bestel jouw theorieboek >*
- Secondary CTA: *Start direct met oefenen >*

**Components:** `text-h1`, `text-body`, `comp-btn-primary`, `comp-btn-secondary`, `comp-usp-checklist` (4 items), hero image (composite books/devices).

**Padding:** `layout-section-padding-hero` vertical; column gap `space-6`.

---

## Section C — USP feature panel

| Item | Detail |
|------|--------|
| Purpose | Five product/service differentiators |
| Layout | Boxed **rounded panel** (`color-panel`), **5 columns** | high |
| **Not** full-bleed gray band | Prior spec incorrect | — |

Each cell: navy line icon + bold title + short description (2 lines).

**Component:** `comp-usp-feature-panel` only.

**Padding:** panel inner `space-5`; section vertical `layout-section-padding`.

---

## Section D — Carousel: Populaire theorieboeken

**Component:** `comp-carousel-products`

- Title: *Populaire theorieboeken*
- Link: *Bekijk alle boeken* (`comp-link-cta`)
- 4 book product cards, side arrows

---

## Section E — Carousel: Online leren & oefenen

**Component:** `comp-carousel-products` (second instance, **stacked below** Section D)

- Title: *Online leren & oefenen*
- Device mockup cards; optional `comp-badge-choice`

**Correction:** Product blocks are **sequential full-width carousels**, not two columns in one row.

---

## Section F — Info grid (4 columns)

**Component:** `comp-grid-info-4` (single section)

| Col | Content | Sub-component |
|-----|---------|---------------|
| 1 | Hoe het werkt — steps 1–3 | `comp-block-steps` |
| 2 | Trustpilot 9.2 / reviews | `comp-block-trustpilot` |
| 3 | Testimonial quote | `comp-block-testimonial` |
| 4 | Waarom Theoriemeesters? checklist | `comp-usp-checklist` |

**Correction:** Not separate full-width “Hoe het werkt” + 3-col trust row.

Background: `color-white` or `color-page` (mockup subtle—**medium** confidence).

---

## Section G — Footer (Theme Builder)

See `specifications/footer.md`.

---

## Section order

| Order | Section | Component(s) |
|-------|---------|--------------|
| A | Header | (Theme Builder) |
| B | Hero | buttons, checklist |
| C | USP panel | `comp-usp-feature-panel` |
| D | Books carousel | `comp-carousel-products` |
| E | Online carousel | `comp-carousel-products` |
| F | Info grid | `comp-grid-info-4` |
| G | Footer | trust strip, newsletter, etc. |

---

## WooCommerce (future)

Dynamic product data only; carousels need category/query rules from client.

---

## Unresolved

- Hero body paragraph exact text  
- All USP panel strings  
- Product query per carousel  
- Mobile/tablet layout  
