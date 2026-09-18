# Typography

Canonical tokens: `brand/brand.json` → `typography.tokens`.  
**Font family is not confirmed**—do not assign Elementor global fonts from guesses alone.

## Observed (desktop mockup + logo)

| Role | Treatment | Confidence |
|------|-----------|------------|
| Logo wordmark | Bold sans, navy + sky on `.nl` | **high** |
| Logo tagline | Regular, smaller, navy | **high** |
| Hero H1 | Large bold navy, sentence case | **high** |
| Section H2 | Bold navy | **high** |
| Body | Regular sans, readable ~16px | **high** |
| Nav | Semibold sans | **medium** |
| Buttons | Bold, sentence case, often with `>` chevron | **high** |
| Product title / price | Semibold | **high** |
| Footer | White, regular/small on navy | **high** |
| Testimonial quote | Italic (observed in mockup) | **medium** |

## Implementation tokens (inferred single values)

| Token | Size | Weight | Line height | Confidence |
|-------|------|--------|-------------|------------|
| `text-display` | 40px | 700 | 1.15 | medium |
| `text-h1` | 38px | 700 | 1.2 | medium |
| `text-h2` | 30px | 700 | 1.25 | medium |
| `text-h3` | 22px | 600 | 1.3 | medium |
| `text-body` | 16px | 400 | 1.6 | medium |
| `text-body-sm` | 14px | 400 | 1.5 | medium |
| `text-nav` | 16px | 600 | 1.2 | medium |
| `text-button` | 16px | 700 | 1.0 | medium |
| `text-caption` | 12px | 400 | 1.4 | medium |

Letter spacing: default `0` unless client brand guide says otherwise (**not observed**).

## Font family

| Item | Value | Confidence |
|------|--------|------------|
| Category | Sans-serif | **high** |
| Named family | **Unknown** | — |
| Candidates | Montserrat, Open Sans | **low** each |

Removed: duplicate `type-*` naming, `type-overline` (not observed), tight weight on Poppins as equal candidate.

## Elementor (future)

Map Primary Headline → `text-h1`, Secondary → `text-h2`, Text → `text-body`, buttons → `text-button`.
