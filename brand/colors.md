# Brand colors

Canonical tokens live in `brand/brand.json`. Use **only** these names across specifications.

Sources: `brand/logos/logo.png`, `brand/logos/favicon.svg`, `design/homepage/desktop.png`.

| Token | Hex | Source | Confidence | Usage |
|-------|-----|--------|------------|--------|
| `color-navy` | `#01203F` | Observed (logo SVG/PNG, headings, footer) | **high** | Headings, logo text, footer bg, road in mark |
| `color-sky` | `#54A3D8` | Observed | **high** | `.nl`, links, outline buttons, badges |
| `color-sky-light` | `#81BBE1` | Observed (logo SVG) | **medium** | Accents; hover TBD |
| `color-yellow` | `#F1CA0A` | Observed | **high** | Primary CTAs, cart UI |
| `color-yellow-hover` | `#F6D22D` | Observed (SVG variant) | **medium** | Hover TBD |
| `color-white` | `#FFFFFF` | Observed | **high** | Header, cards, inputs |
| `color-page` | `#F4F7FA` | Inferred | **medium** | Page canvas (mockup) |
| `color-panel` | `#E8EEF4` | Inferred | **medium** | USP feature panel fill |
| `color-border` | `#DEDEDE` | Inferred | **medium** | Borders, dividers |
| `color-text` | `#01203F` | Inferred | **medium** | Body copy often matches navy in mockup |
| `color-text-muted` | `#5A6572` | Inferred | **low** | Secondary copy—not measured |
| `color-text-inverse` | `#FFFFFF` | Observed | **high** | Footer on navy |
| `color-success` | — | Unresolved | **low** | Checkmarks / Trustpilot—do not hard-code until confirmed |

## Removed / avoided duplicates

- ~~`primary-navy` / `primary-navy-deep`~~ → single **`color-navy`** (footer does not require a second navy hex in specs until measured).
- ~~`neutral-bg-alt` at `#F4F4F4`~~ → split into **`color-page`** (canvas) and **`color-panel`** (USP box).
- ~~Separate Trustpilot green token~~ → use widget defaults until approved.

## Elementor global mapping (future)

| Global | Token |
|--------|--------|
| Primary | `color-navy` |
| Secondary | `color-sky` |
| Text | `color-text` |
| Accent | `color-yellow` |

Custom globals: `Sky Light`, `Page`, `Panel`, `Border`, `Text Muted`, `Text Inverse`.

## Principles (observed)

1. Yellow = primary commerce actions only.
2. Sky = navigation affordances and secondary actions.
3. Navy = structure, trust, footer containment.
