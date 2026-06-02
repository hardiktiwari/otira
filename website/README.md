# Website

The marketing / pitch site for Otira. This is an **artifact (a codebase)**, not a skill — the
*how-to* lives in [`../skills/dev`](../skills/dev/SKILL.md) and [`../skills/ppt`](../skills/ppt/SKILL.md);
the *site itself* lives here.

## Status
`index.html` — a lean, single-file starter landing page (no build step). Open it in a browser
or deploy as a static site. Good enough to show prospects today; upgrade later.

## Stack decision
- **Now:** single static `index.html` (inline CSS) — zero dependencies, instant to host/share.
- **Later (when it needs forms/CMS/blog):** migrate to a static framework (Astro/Next static
  export) and deploy on a static host (Vercel/Netlify) or the existing DigitalOcean droplet
  behind Caddy. Keep it fast and outcome-focused (cf. Varick/Doss/Sapien sites).

## Content principles
- Plain English, no jargon (no "MCP"/"forward deployment" — see [`../docs/one-pager.md`](../docs/one-pager.md)).
- Lead with the owner's pain and the outcome. One clear CTA: **book a call**.
- Sections: hero → how it works → use cases → "vs. just using ChatGPT" → trust/security → FAQ → CTA.

## Deploy (later)
- Static host: drag-and-drop or connect the repo.
- Or droplet: copy files behind Caddy/Nginx; point the domain (see `../docs/brand-naming.md` for
  domain TODO).

## TODO
- [ ] Decide + register domain for Otira (e.g. otira.ai / otira.com / getotira.com) and run the clearance checklist in `../docs/brand-naming.md`.
- [ ] Add real logo + favicon (see `../assets/`).
- [ ] Wire the "Book a call" button to a scheduling link.
- [ ] Add 1–2 quantified proof points once the first deployment is live.
