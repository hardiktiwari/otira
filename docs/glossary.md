# Glossary

Shared vocabulary. Keep plain-English definitions here so customer material stays jargon-free.

## Our model
- **AI coworker** — an agent the client tags (Slack/email) that does real tasks for them.
- **Context layer / context graph / "company brain"** — a structured, living model of how a
  specific company runs (data, rules, definitions, exceptions). Our core IP.
- **Connector** — an integration that lets our system read/write a client tool (email, ERP, QBO…).
- **MCP (Model Context Protocol)** — a standard way to expose tools/data to an AI assistant;
  one optional way to build connectors. *(Internal term — avoid in customer material.)*
- **Forward deployment** — our delivery model: embed, build custom, hand off, then retain.
  *(Internal term — say "we set it up for you and then you own it" to customers.)*
- **Intake & reconciliation engine** — the reusable core: unstructured input → extract → match
  to master data → validate against rules → write structured draft → report.
- **Company sandbox** — an agent instance on the client's VM holding their data + logic +
  connectors + memory; anyone tags it to act.

## Business / ops
- **ERP (Enterprise Resource Planning)** — the central system that runs a business's core ops
  (inventory, orders, purchasing, invoicing, accounting). The "system of record."
- **System of record** — the authoritative source of truth for a type of data.
- **QBO** — QuickBooks Online; common SMB accounting system.
- **AR / AP** — Accounts Receivable (money owed to the company) / Accounts Payable (money owed out).
- **PO / Sales Order** — Purchase Order (we buy) / Sales Order (a customer buys from the client).
- **Landed cost** — true per-unit cost after freight + duties + taxes + warehousing.
- **FTE** — Full-Time Employee; we anchor pricing to the FTE cost we replace.
- **ICP** — Ideal Customer Profile.

## Wine industry
- **Three-tier system** — US law: Producer → Importer/Wholesaler → Retailer as separate
  companies. Our wine customers are the middle tier.
- **Depletion** — when a distributor resells onward to retail; the real demand signal.
- **VIP (iDIG)** — third-party provider of weekly depletion/on-hand data (CSV feed).
- **SKU** — Stock Keeping Unit; a unique product code.
- **DBO (Direct Bin Ops)** — Cameron's email-driven automation prototype for wine. See
  [`industry-research/wine.md`](industry-research/wine.md).

> Add terms as they come up. If a term is "internal only," mark it so it never leaks into
> customer-facing material.
