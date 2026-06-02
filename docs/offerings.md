# Offerings

> What we actually sell, the use cases we deliver, how we deliver, and how we price.

## The product (what the client gets)

1. **A context layer** — a living model of how their business runs (data + rules + exceptions).
2. **Connectors** — secure read/write integrations into their existing systems (email, ERP,
   QuickBooks, vendor portals, Slack…). No migration.
3. **Automations & a coworker** — custom workflows on top, plus an agent they can tag to get
   work done. When we leave, they own it and can extend it.

## Use case catalog

Two buckets. We lead with one painful automation, then expand.

### Reporting / analysis
- Custom dashboards & views on top of ERP/QBO data (P&L, margin, sales by rep/brand/region).
- Goals vs. actuals; forecasts; stock cover / inventory visibility.
- Proactive monitoring & anomaly alerts (margin compression, cost overruns).

### Automation / action (higher value, higher stakes)
- **Email → order/intake draft** — inbound PDF/email → parsed → matched to SKUs & customer →
  pricing & inventory verified → draft created for human approval. *(Lead candidate.)*
- **Invoice → ERP/QuickBooks posting** — recognize a recurring vendor invoice, post to the
  right place, push payment initiation to QBO (with approval thresholds).
- **Replenishment → PO** — reorder logic creates the PO, updates on-order inventory, tracks
  payment until the PO is due.
- **Action-on-email** — price increases, new product/vintage releases, etc., routed to a queue.

> **Reference prototype:** Cameron's "Direct Bin Ops (DBO)" already implements a version of the
> first three for wine. See [`industry-research/wine.md`](industry-research/wine.md).

## Trust & safety (a core part of the offering)

Because automations can *act* (not just report), trust is a feature we sell:
- **Confidence scoring** on every recognized action.
- **Human-in-the-loop approval**, with auto-approve only above a high confidence threshold
  (e.g., 95%) for low-risk, repetitive items.
- **Full audit trail** — every action traceable to its source (email, transaction, rule).
- **Money-movement guardrails** — anything paying/transferring funds requires engineering
  rigor + explicit approval. We do not "just rip it."
- **Security posture** — data stays in the client's systems; role-based access; we don't train
  on client data. (Plan for SOC 2 as we move up-market.)

## Delivery model — forward deployment

| Phase | Duration | Output |
|---|---|---|
| Discovery & mapping | ~1–2 weeks | Workflow map, target use case, data/system inventory |
| Build (connectors + context + use case #1) | ~3–6 weeks | A working automation on the client's real data |
| Harden & expand | ongoing | More use cases, reliability, parallel-run |
| Handoff & retainer | ongoing | Client owns the coworker; we maintain & extend |

## Pricing (working model)

- **Initiation / implementation fee** for the build (anchored to the FTE cost it replaces — a
  point app is typically ~⅓ of one employee's cost; a forward-deployed coworker should be
  priced against the headcount and hours it saves).
- **Ongoing retainer + licensing** to manage, monitor, and add use cases.
- Frame value as: replaced headcount *and* reclaimed owner time (quality of life).

## What makes this defensible

- We connect to **data outside the ERP** (email, etc.) that ERP-native agents ignore.
- We **sit with the client** and build the custom context layer — incumbents won't.
- We **act**, not just analyze (vs. Sapien/BlackLine). See [`competitive-research.md`](competitive-research.md).
- Vertical depth (wine) where horizontal platforms treat the domain as an edge case.
