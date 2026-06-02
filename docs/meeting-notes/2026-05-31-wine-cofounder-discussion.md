# 2026-05-31 — Wine cofounder/operator discussion

- **Date:** 2026-05-31
- **Participants:** Two founders (PMs) + wine operator (Cameron-profile; built "DBO")
- **Type:** cofounder + customer/operator discussion
- **Source:** transcript (provided)

## TL;DR
- The model crystallized as **platform + forward-deployed implementation**, leaving the client a
  coworker they own.
- The "potential customer" has **already built a working prototype** ("Direct Bin Ops" / DBO).
- **Don't build an ERP** — build the intelligence layer before/after it; ERP = commodity SoR.
- **Start SMB + vertical (wine)**; stay opportunistic on warm leads (Davis).
- They need a **real AI engineer**; founders are PMs.

## Key facts (what was said)
- **DBO:** connects to email; actionable emails (price increase, new vintage) or internal
  triggers (replenishment) feed one engine → inbox queue (accept/edit) → on approve, pushes to
  **QBO via API** (draft) or creates **PO** + updates on-order inventory + tracks payment. AI
  **confidence scoring**; auto-bypass approval >~95%. Runs on a DigitalOcean droplet. ~**80% there**;
  hard **20%** is robustness as it compounds.
- **Model:** "forward deployment" — embed ~4–8 weeks, build context + connectors + use cases,
  leave, then retainer + licensing. IP = reusable connectors (MCPs) + context-gathering method;
  context itself rebuilt per client → "not entirely reusable."
- **Architecture insight:** intelligence layer before data enters ERP and after it leaves →
  ERP becomes a commodity system of record.
- **ICP debate:** one founder was a "big no" on SMBs (thin needs); operator strongly pushed SMB
  (operators "foam at the mouth" — headcount savings + quality of life). Landed on **wine,
  $10–30M, ~dozen employees**. Major accounting/ERP vendors define $10–30M as mid-market.
- **Competitors discussed:** Varick (forward-deployed service, funded), Doss (ERP replacement),
  Coworker.ai, BlackLine (FinOps reporting on QBO), ERP-native agent suites (don't reach
  outside-ERP data), point apps (~⅓ FTE cost). Healthcare is a current startup hotspot.
- **End-state:** a "company sandbox" (Claude/agent on a VM) with data + logic + connectors +
  memory; anyone tags it to act.
- **Next steps agreed:** write the plan down; translate to plain English; land 1–2 clients to
  cut teeth; keep talking to people to learn; find an engineer.

## Decisions made
- See `../decisions.md` D1–D7 (no-ERP, forward deployment, wine vertical, $10–30M ICP,
  email→order wedge, trust pattern, engineer required).

## Our take / recommendations (NOT said — our additions)
- Make **Cameron's role explicit** (customer / cofounder / both) — it drifted during the call.
- Productize the **trust pattern** (confidence + approval + audit) as a sellable feature.
- Borrow from **Sapien**: "Company Context Model" framing, verifiability, "data needn't be
  clean," the "vs. ChatGPT" comparison, network-based land-and-expand. (See competitive-research.)

## Action items
- [ ] Plain-English one-pager (done draft: `../one-pager.md`) — refine as a team.
- [ ] Clarify founder roles + Cameron's role.
- [ ] Chat with Davis (learn, don't pitch).
- [ ] Identify an AI engineer.
- [ ] Collect sample wine order emails + Traverse/VIP exports.

## People mentioned (follow up)
- **Cameron** — wine operator, built DBO; has one highly interested lead.
- **Davis** — baby-products importer (China → Amazon), ~$40–50M, 6-person family business;
  potential customer + investor; Amazon + patent-law angles.
- Forward-deployment practitioners (tech/CX), healthcare implementers — for learning.
