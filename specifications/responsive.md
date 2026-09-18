# Responsive

**Available:** desktop homepage mockup only.

Use Elementor responsive overrides on the **same** containers and `comp-*` components—no duplicate sections unless a future mockup requires it.

---

## Baseline widths (Elementor defaults)

| Device | Width | Spec status |
|--------|-------|-------------|
| Desktop | ≥1025px | **Designed** |
| Tablet | 768–1024px | **Unresolved** |
| Mobile | ≤767px | **Unresolved** |

---

## Desktop-observed (high confidence)

- Boxed content at `layout-content-width`
- Multi-column grids (5, 4, 2) as documented in homepage spec

---

## General principles (medium confidence — not measured)

| Component | Likely change |
|-----------|----------------|
| `comp-usp-feature-panel` | Fewer columns, then stack |
| `comp-carousel-products` | Fewer visible slides; swipe |
| `comp-grid-info-4` | Stack to 1–2 columns |
| `comp-nav-primary` | Collapse to menu toggle |
| `comp-input-search` | Full width under main bar |

Do **not** implement these as facts until tablet/mobile mockups exist.

---

## Touch targets

Minimum ~44px for cart and menu controls (WCAG guidance)—**inferred**, not measured on mockup.

---

## Required assets

- `design/homepage/tablet.png`
- `design/homepage/mobile.png`
- Header menu open state
