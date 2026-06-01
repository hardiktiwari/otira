# Industry Research — Wine Import / Distribution

**Beachhead vertical.** Our warm-network advantage (Cameron, 2nd-gen wholesale, dad 40 yrs in
the industry). Complex, antiquated, underserved by tech.

## How money & product flows
- **Three-tier system (US law):** Producer → Importer/Wholesaler → Retailer must be separate
  companies. Our customers are the **middle tier** (importer/wholesaler). Can't sell to
  consumers; **every state has its own rules**, distributors, and tax/reporting.
- **Buying side:** commit to overseas producers months ahead, in EUR/foreign currency; wine
  ships in containers (6–10 weeks), clears customs, lands at a US warehouse; pay producers on
  terms (60–180 days).
- **Selling side:** distributors order against US warehouse inventory; importer ships,
  invoices, gets paid on terms (30–45 days).
- **Depletions:** when a distributor resells onward to retail. Importers can't see it directly —
  they **buy it as weekly CSV from VIP**. It's the real demand signal (and a constant
  name-matching headache vs. the importer's own SKUs/customers).

## Core systems
- **ERP:** e.g., Traverse (off-the-shelf; clunky, weak reporting).
- **Accounting:** QuickBooks (QBO).
- **Email:** the industry runs on it — orders, price increases, new-vintage releases.
- **Data feed:** VIP iDIG (read-only depletion + on-hand CSV).
- **In-house:** custom React dashboards (e.g., "Echo"), Python/CSV pipelines, DigitalOcean droplets.

## Manual pain (automation targets)
- Back-office data entry from emailed PDFs into ERP + QuickBooks ("shit in, shit out").
- Pricing: a **stack of rules** by state / distributor / program / promotion — subtle, easy to
  model wrong.
- VIP depletion ingestion & SKU/customer name mapping.
- PO tracking (multi-currency, landed cost), open-order/port-date visibility.
- Inventory across many warehouse types (controlled / advisory / winery stock / liquidation).

## Reference prototype — "Direct Bin Ops" (DBO)
Cameron has already built a working prototype for his own importing business:
- Connects to **email**; actionable emails (price increase, new vintage = new product) **or**
  internal triggers (replenishment engine) feed **one engine**.
- Engine decides if action is needed → drops it into an **inbox queue**: *"here's what we think
  this is, accept or edit?"* (both a backend store and a UI).
- **AI confidence scoring**; auto-bypass approval above ~95% for known/recurring items.
- On approve: accounting item → **pushes to QBO via API** (currently draft state); inventory item
  → creates **PO**, updates on-order inventory, tracks payment until PO due.
- Runs on his **DigitalOcean droplet**. He estimates **~80% there**; the hard **20%** is making
  it robust as it compounds (where a real engineer + our platform come in).

## ICP (wine)
- **~$10–30M revenue, ~a dozen employees.** Multi-generational, low tech maturity ("half the
  industry struggles to open PowerPoint"). Automation feels like "wizardry" → high wow factor.
- **Buyer:** owner/operator (often 2nd-gen). Cameron already has **one highly interested lead**.

## Value prop fit
- Replace/avoid slow, error-prone back-office headcount (hard-dollar ROI).
- **Quality of life** for the owner (10–20 hrs/week back) — sells even without layoffs.

## Why now / why underserved
- Antiquated, email-driven, far from any tech investment. Nobody's focusing here. Complexity
  (three-tier, multi-currency, state compliance) is exactly what horizontal platforms avoid.

## Open questions / TODO
- [ ] Confirm Cameron's role (customer / cofounder / both).
- [ ] Get sample order emails + Traverse/VIP exports (redacted) for the email→order build.
- [ ] Map the pricing-rule engine carefully (riskiest to model wrong).
- [ ] List warm customer intros from Cameron's network.
