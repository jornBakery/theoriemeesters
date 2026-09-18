# Design system — Elementor Pro

**Source of truth for tokens:** `brand/brand.json`  
**Component registry:** `specifications/components.md`  
**Not implemented** in WordPress/Elementor yet.

---

## Colors

Use exact token names from `brand/colors.md`. No alternate aliases in specs.

---

## Spacing

| Token | px |
|-------|-----|
| `space-1` | 4 |
| `space-2` | 8 |
| `space-3` | 16 |
| `space-4` | 24 |
| `space-5` | 32 |
| `space-6` | 48 |
| `space-7` | 64 |
| `space-8` | 80 |

**Usage**

| Context | Token |
|---------|--------|
| Default section padding (vertical) | `space-7` |
| Hero section padding (vertical) | `space-8` |
| Grid gap / card gap | `space-4` |
| Heading → body | `space-3` |
| Body → buttons | `space-4` |
| Icon → label (USP) | `space-2` |

Confidence: **medium** (inferred from mockup rhythm).

---

## Layout

| Token | Value | Confidence |
|-------|--------|------------|
| `layout-content-width` | 1200px | medium |
| `layout-gutter` | `space-4` (24px) | medium |
| `layout-grid-gap` | `space-4` | medium |

**Container hierarchy (Elementor flexbox)**

1. Page section container — width 100%, background, vertical padding  
2. Inner container — boxed `layout-content-width`, horizontal padding `layout-gutter`  
3. Row container — flex row, `layout-grid-gap`  
4. Column container — flex column  

**Page canvas:** `color-page` behind sections; many blocks use `color-white` surfaces on top (observed).

---

## Radius & borders

| Token | px | Applies to |
|-------|-----|------------|
| `radius-sm` | 8 | Buttons, inputs, cards, USP panel |
| `radius-pill` | 999 | Product badges, round carousel arrows |
| `border-default` | 1px solid `color-border` | Inputs, subtle dividers |

Confidence: **medium**. Prior spec split 6px buttons / 8px cards without mockup evidence—that split is **removed**.

---

## Typography

Use `text-*` tokens from `brand/typography.md` only.

---

## Grids (desktop, observed)

| Region | Columns | Component |
|--------|---------|-----------|
| Utility bar USPs | 3 | `comp-usp-utility-bar` |
| Hero | 2 | — |
| USP feature panel | 5 | `comp-usp-feature-panel` |
| Product carousel track | 4 visible | `comp-carousel-products` |
| Info band | 4 | `comp-grid-info-4` |
| Footer trust strip | 4 | `comp-usp-trust-strip` |
| Footer main | 5–6 areas | See `footer.md` |

---

## Imagery

| Context | Ratio | Confidence |
|---------|--------|------------|
| Product card image | ~1:1 | medium |
| Hero composite | Landscape cluster | medium |
| Logo lockup | Asset intrinsic | high |

`object-fit: contain` for product images.

---

## Elementor globals (future checklist)

- [ ] Colors from `brand/brand.json`
- [ ] Typography after font confirmation
- [ ] Button styles: `comp-btn-primary`, `comp-btn-secondary`
- [ ] Default boxed container 1200px, gap 24px

---

## Unresolved

- Tablet/mobile gutters and type scale  
- Sticky header  
- Exact `color-text-muted` and success green hex  
