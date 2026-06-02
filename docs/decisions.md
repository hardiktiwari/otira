# Decision Log

> Running record of key decisions — what, why, and when. Append new entries; don't rewrite
> history. When a decision is reversed, mark the old one **Superseded** and add a new entry.

**Format:** `### D# — Title` · Date · Status (Active / Superseded / Revisit) · Context ·
Decision · Revisit-if.

---

### D1 — Don't build an ERP; build the layer around it
- **Date:** 2026-05-31 · **Status:** Active
- **Context:** ERPs are slow, messy, and where incumbents (NetSuite, Doss, Intuit IES) fight.
- **Decision:** Build the intelligence layer *before* data enters and *after* it leaves the
  ERP; treat the ERP as a commodity system of record.
- **Revisit if:** A client's ERP is so poor that data quality blocks value end-to-end.

### D2 — Forward-deployment delivery model
- **Date:** 2026-05-31 · **Status:** Active
- **Context:** Need fast value + reusable IP; pure SaaS too slow, pure consulting doesn't scale.
- **Decision:** Platform (reusable connectors + context method) + custom implementation (embed,
  build, hand off). Initiation fee + retainer/licensing.
- **Revisit if:** Reusability proves high enough to go product-led, or low enough to reprice.

### D3 — Start vertical: wine (stay opportunistic on warm SMB leads)
- **Date:** 2026-05-31 · **Status:** Active
- **Context:** Cameron's deep warm network; complex, antiquated, underserved industry.
- **Decision:** Beachhead = wine import/distribution; keep open to adjacent warm leads (e.g., Davis).
- **Revisit if:** Wine traction stalls or a stronger vertical/network emerges.

### D4 — ICP: ~$10–30M revenue SMBs
- **Date:** 2026-05-31 · **Status:** Active
- **Context:** Real pain + budget; matches Intuit's "mid-market" definition; avoids 1–2 person cos.
- **Decision:** Target ~$10–30M, ~dozen employees, low tech maturity, owner-operator buyer.
- **Revisit if:** Discovery shows the value/ROI lands better above or below this band.

### D5 — Lead wedge: email → order/intake automation
- **Date:** 2026-05-31 · **Status:** Active
- **Context:** Highest-pain, bounded, high-wow; Cameron's DBO already proves a version.
- **Decision:** Lead go-to-market with email→order/intake; expand to invoice→QBO, replenishment→PO.
- **Revisit if:** Discovery surfaces a higher-pain bounded workflow.

### D6 — Trust pattern: confidence + human approval + audit
- **Date:** 2026-05-31 · **Status:** Active
- **Context:** Automations act on real operations/money; trust is the product.
- **Decision:** Every action gets a confidence score; auto-approve only above a high threshold for
  low-risk recurring items; full audit trail; money-movement requires explicit approval + rigor.
- **Revisit if:** Never relax the money-movement guardrail without engineering review.

### D7 — We need an AI engineer before production money-movement
- **Date:** 2026-05-31 · **Status:** Active
- **Context:** Founders are PMs; prototypes ≠ reliable production systems.
- **Decision:** Bring on a strong AI engineer (hire/cofounder/fractional) accountable for the
  code before promising any production automation that touches money or mission-critical ops.
- **Revisit if:** Scope stays strictly read-only/advisory (lower bar).

### D8 — Company name: Otira
- **Date:** 2026-06-01 · **Status:** Active
- **Context:** "Keel" was retired (collides with direct competitor keel.so); "Otira" carried as an
  internal codename with no obvious AI/software collision found in research.
- **Decision:** Finalize the company name as **Otira**. Domain not yet chosen; formal clearance
  (USPTO + handles) still pending before public launch or brand spend (see `brand-naming.md`).
- **Revisit if:** Clearance surfaces a blocking trademark/domain collision.

---

## Open decisions (not yet made)
- **Service vs. platform emphasis** (affects margins + fundraising story).
- **Cameron's role** — customer, cofounder, or both.
- **Raise vs. bootstrap** (services revenue could fund the build).
- **Domain selection for Otira** (name finalized in D8; domain + formal clearance still open).
