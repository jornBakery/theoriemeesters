# Visual analysis report — Theoriemeesters.nl

**Last updated:** 2026-09-12 (normalization pass)  
**Inputs:** `brand/logos/logo.png`, `brand/logos/favicon.svg`, `design/homepage/desktop.png`  
**Canonical tokens:** `brand/brand.json`  
**Canonical components:** `specifications/components.md` (`comp-*` IDs)

No WordPress or EMCP write operations.

---

## Executive summary

Brand and homepage specs were **reviewed against the logo and desktop mockup** and normalized to a single token set and component registry. Several **internal contradictions from the first pass were corrected** (homepage layout, header utility bar background, USP panel shape, footer logo/social placement, duplicate navy/spacing/radius tokens).

---

## High-confidence findings

### Brand

- Name **Theoriemeesters.nl**; tagline **We leiden je op, om met kennis te slagen.**
- Logo mark: mortarboard, book, road, checkmark; colors **#01203F**, **#54A3D8**, **#F1CA0A** (SVG-aligned).
- Footer uses a **white logo** treatment on navy (observed in mockup).

### Homepage structure (corrected)

1. Header (utility + main)  
2. Hero (2-col, dual CTA, 4 check USPs, composite image)  
3. **Rounded 5-column USP panel** (boxed, not full-bleed gray band)  
4. **Stacked** product carousels: *Populaire theorieboeken* then *Online leren & oefenen*  
5. **Single 4-column info band:** Hoe het werkt | Trustpilot | testimonial | Waarom checklist  
6. Footer: navy USP strip + main columns + newsletter  

### Components

- One pattern → one `comp-*` ID (see `brand/brand.json` registry).
- Yellow primary buttons; sky outline secondary; product card pattern shared by both carousels.

### Header

- Utility bar **white** with 3 USPs; main bar: logo, 5 nav items, search, cart with yellow count badge.

---

## Corrections made in this review

| Issue | Was | Now |
|-------|-----|-----|
| Product sections | Side-by-side in one row | **Two stacked full-width carousels** |
| Trust / steps | Separate full-width sections | **One `comp-grid-info-4` section** |
| USP mid-page | Full-bleed gray ribbon | **`comp-usp-feature-panel`** in rounded panel |
| Utility bar bg | Gray `neutral-bg-alt` | **`color-white`** |
| Footer logo | “Need reversed” guess | **White lockup observed**; asset still required |
| Footer social | Bottom bar only | **Brand column** (bottom legal bar unclear) |
| Color tokens | `primary-navy`, `primary-navy-deep`, `neutral-*` mix | **`color-*` only** in `brand.json` |
| Spacing | `space-2xs`…`space-4xl` overlap | **`space-1`…`space-8`** |
| Radius | 6px buttons vs 8px cards | Unified **`radius-sm` 8px** |
| Component names | `btn-primary`, `usp-icon-row`, etc. | **`comp-*` registry only** |
| Hero copy | “Verify with client” only | **Observed H1/CTAs** recorded (still verify before publish) |
| Success green | Fixed `#22C55E` | **`color-success` unresolved** |
| Font candidates | Montserrat/Poppins medium | **Family unconfirmed**; candidates **low** |

---

## Medium-confidence assumptions (still open)

| Topic | Assumption |
|-------|------------|
| `layout-content-width` | 1200px |
| `layout-gutter` / grid gap | 24px (`space-4`) |
| Section padding | 64px default, 80px hero |
| `color-page` / `color-panel` | #F4F7FA / #E8EEF4 |
| `color-text-muted` | #5A6572 |
| Hero column ratio | ~45% / 55% |
| Product image | ~1:1 in card |
| Carousels | Arrow-controlled sliders |
| Testimonial | Italic quote styling |

---

## Low-confidence assumptions (still open)

| Topic | Assumption |
|-------|------------|
| Named font family | Unknown |
| Header total height | ~120px |
| Search field width | Wide, exact px unknown |
| Minimum logo width | ~140px+ |
| Autoplay on carousels | Not observed |

---

## Missing information

1. Tablet and mobile mockups  
2. Sticky / scroll header behavior  
3. Font files or brand PDF  
4. Logo exports: `lockup-header`, `lockup-footer-white`  
5. Hero and product source photography  
6. Icon SVG set  
7. Full URL map for footer/nav  
8. WooCommerce catalog and carousel query rules  
9. Inner pages (PDP, cart, checkout, account)  
10. Newsletter ESP and GDPR copy  
11. Measured hex for success green and muted text  
12. Copyright / legal footer line (if any)  

---

## Remaining unresolved decisions (user approval)

| # | Decision |
|---|----------|
| 1 | **Confirm font family** (or supply files) before Elementor typography globals |
| 2 | **Approve color tokens** in `brand/brand.json` (`color-page`, `color-panel`, `color-text-muted`) |
| 3 | **Supply `lockup-header`** (no tagline) and **`lockup-footer-white`** |
| 4 | **Confirm homepage section order** after 4-column info band (no extra sections?) |
| 5 | **Product carousel data source** (category, tag, manual, bestsellers) per section |
| 6 | **Sticky header** on/off |
| 7 | **Search scope** (products only vs site) |
| 8 | **Trustpilot** embed tier and account |
| 9 | **Newsletter provider** + consent UI |
| 10 | **Tablet/mobile** layouts—or approve inferred stacking in `responsive.md` |
| 11 | **`color-success`** hex vs Trustpilot default for checks |
| 12 | **Publish strategy** for Theme Builder templates (draft until visual QA) |

---

## Additional assets to improve accuracy

| Asset | Why |
|-------|-----|
| Homepage tablet + mobile | Breakpoints, nav, grids |
| Header menu open | Mobile IA |
| Logo SVG master | Crisp header/footer |
| Figma / token sheet | Exact spacing and colors |
| Product CSV or staging catalog | Carousel content |
| Checkout / cart mockups | Chrome consistency |

---

## Normalization reference

- **Colors:** `brand/colors.md` ↔ `brand/brand.json`  
- **Spacing / layout / radius:** `specifications/design-system.md` ↔ `brand/brand.json`  
- **Typography:** `brand/typography.md` (`text-*`)  
- **Components:** `specifications/components.md` ↔ `brand/brand.json` → `components.registry`  
- **Page map:** `specifications/pages/homepage.md`  

---

## Recommended next steps (not started)

1. Client resolves table in **Remaining unresolved decisions**  
2. Supply missing logo and imagery assets  
3. Optional: tablet/mobile mockups → update `responsive.md`  
4. After approval: set Elementor globals and build drafts via EMCP  
