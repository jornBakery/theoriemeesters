# Header — Theme Builder

**Reference:** `design/homepage/desktop.png` (desktop only)  
**Components:** `comp-usp-utility-bar`, `comp-nav-primary`, `comp-nav-utility`, `comp-input-search`  
**Sticky behavior:** unresolved (static mockup)

---

## Structure (observed)

```
┌──────────────────────────────────────────────────────────────┐
│ UTILITY (white) — comp-usp-utility-bar  │ comp-nav-utility   │
├──────────────────────────────────────────────────────────────┤
│ MAIN (white) — Logo │ comp-nav-primary │ search │ cart      │
└──────────────────────────────────────────────────────────────┘
```

**Correction:** Utility bar background is **white** (`color-white`), not gray panel fill.

Optional subtle bottom border: `border-default` (**medium** confidence).

---

## Utility bar — `comp-usp-utility-bar`

**Observed labels (verify):**

- Voor 22:00 besteld …
- Gratis verzending
- 9,2/10 Trustpilot (or similar)

Layout: flex, space-between; left cluster 3 USPs; right: Klantenservice (dropdown), Inloggen, user icon.

Typography: `text-body-sm`.

---

## Main bar

| Element | Detail | Confidence |
|---------|--------|------------|
| Logo | Icon + wordmark, **no tagline** | high |
| Nav | `comp-nav-primary`: Theorieboeken, Online oefenen, Pakketten, Voor wie, Over ons | high |
| Search | `comp-input-search` | high |
| Cart | Icon + `comp-badge-cart-count` | high |

Padding vertical: ~`space-3`–`space-4`. Inner width: `layout-content-width`, gutter `layout-gutter`.

Typography nav: `text-nav`.

---

## Dimensions (inferred)

| Item | Value | Confidence |
|------|--------|------------|
| Combined header height | ~120px | low |
| Search height | ~44px | medium |
| Search radius | `radius-sm` | medium |

---

## Unresolved

- Sticky / shrink on scroll  
- Mobile menu  
- Search scope (products vs site)  
- Asset: `lockup-header` logo file  
