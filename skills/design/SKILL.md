---
name: design
description: Design the visual look-and-feel of Otira's surfaces — the marketing website, client dashboards/app, and deck visuals. Covers brand system (color, type, spacing), UI patterns (cards, nav, forms), and finishes like glassmorphism. Use when designing or restyling a website/UI, choosing a visual direction, or making something look modern and on-brand. Pair with `dev` to build it and `ppt` for slides.
---

# Design

Visual design for everything customers see: the marketing **website**, the client-facing **app**
(inbox/dashboards/chat), and **deck** visuals. This skill is the *look*; `dev` is the *build* and
`ppt` is *slides*.

## Principles (in priority order)
1. **Clarity beats flash.** Our buyers are busy SMB owners. Legibility and obvious next steps win
   over trendy effects. Sell outcomes, not decoration.
2. **One brand system.** Same color, type, and spacing across site, app, and decks — so everything
   feels like one product.
3. **Trust looks calm.** Generous whitespace, high contrast, no clutter. A money-touching product
   should feel composed, not busy.
4. **Accessible by default.** Body text ≥ 4.5:1 contrast; never rely on color alone; visible focus
   states; respect `prefers-reduced-motion`.

## Brand system (current website tokens)
Reuse these so surfaces match — see `website/index.html` `:root`.
- **Ink** `#eef2fb` on dark `#0a0e1a`; **muted** `#97a3c2`; hairline `#283150`.
- **Accent gradient** `linear-gradient(120deg,#6c8cff,#9d7bff 50%,#7af0d0)` — use for ONE element
  per view (primary CTA or a single headline word), not everywhere.
- **Type**: system UI stack; tight tracking on big headings (`letter-spacing:-.02em`), `clamp()` for
  fluid sizes. **Spacing/radius**: 8px rhythm; cards `border-radius:16px`, buttons `12px`.

## UI patterns
- **Hierarchy**: one clear H1 per page, outcome-focused; sub ≤ 60ch; one primary CTA, one ghost.
- **Cards/sections**: consistent padding and radius; subtle hover lift (≤ 3px) for interactivity.
- **Forms/queues** (app): clear states (default/approve/edit), confidence shown plainly, every
  action visibly logged — design *reinforces* the trust story in `dev`/`ai-strategy`.

## Finishes: glassmorphism
Frosted-glass panels (translucent fill + `backdrop-filter: blur()` + thin light border + soft
shadow). Looks modern and matches the Apple "Liquid Glass" feel.
- **Needs color behind it** to read as glass — place ambient gradient blobs behind panels.
- **Protect legibility**: keep blobs low-opacity and put dense text on near-opaque areas. Don't
  frost critical reading content over busy backgrounds.
- Always include `-webkit-backdrop-filter` (Safari). Reference implementation: `website/index.html`.

```css
.glass{
  background:rgba(255,255,255,.06);
  -webkit-backdrop-filter:saturate(160%) blur(16px);
  backdrop-filter:saturate(160%) blur(16px);
  border:1px solid rgba(255,255,255,.14);
  box-shadow:0 8px 32px rgba(2,6,23,.45), inset 0 1px 0 rgba(255,255,255,.08);
}
```
Use sparingly: nav, cards, modals, pills — not full-screen reading surfaces.

## Checklist
- [ ] One brand system (color/type/spacing) reused from existing tokens.
- [ ] One primary CTA per view; accent gradient used once.
- [ ] Body contrast ≥ 4.5:1; visible focus; reduced-motion respected.
- [ ] Effects (glass, blur, motion) don't hurt readability.
- [ ] Looks consistent with the website, app, and decks.

## Related
- Build it → `skills/dev` · Slides → `skills/ppt` · Brand name/domain → `docs/brand-naming.md`.
