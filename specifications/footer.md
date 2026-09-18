# Footer — Theme Builder

**Reference:** `design/homepage/desktop.png`  
**Components:** `comp-usp-trust-strip`, `comp-form-newsletter`, social icon row  

---

## Structure (observed)

```
┌──────────────────────────────────────────────────────────────┐
│ comp-usp-trust-strip (navy, 4 columns)                       │
├──────────────────────────────────────────────────────────────┤
│ MAIN (navy): Brand+social │ Link cols │ … │ Newsletter      │
└──────────────────────────────────────────────────────────────┘
```

**Correction:** Social icons sit in the **brand column** in the mockup, not a separate bottom bar only. A distinct copyright bar is **not clearly visible**—treat as unresolved.

---

## Zone 1 — `comp-usp-trust-strip`

- Background: `color-navy`
- 4 equal columns: white icon + short white text (shipping, delivery, guarantee, iDEAL/payment themes observed)
- Padding vertical: `space-4`

---

## Zone 2 — Main footer

Background: `color-navy`, text `color-text-inverse`.

| Area | Content | Confidence |
|------|---------|------------|
| Brand column | **White logo** (observed), short about text, **social icons** (FB, IG, YT, TikTok) | high |
| Link columns | Headings e.g. Producten, Voor wie, Klantenservice, Over ons + links | medium |
| Newsletter | “Meld je aan voor de nieuwsbrief” + `comp-form-newsletter` | high |

Typography: column headings `text-body-sm` semibold; links `text-body-sm`.

Inner layout: boxed `layout-content-width`, gap `space-5`.

---

## Logo

Mockup shows **white footer lockup**—asset `lockup-footer-white` required (`brand/logo-usage.md`). Full-color navy wordmark on navy is **not** used in the mockup footer.

---

## Unresolved

- Exact link lists and URLs  
- Copyright / legal line if off-canvas  
- Mobile column stack / accordion  
- Payment icon row (if any beyond USP strip)  
