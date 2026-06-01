# Strategy

> The core thesis, the business model, and the decisions we've converged on.

## The thesis

Every small/mid-sized business runs on a handful of systems — **email, an ERP, QuickBooks,
maybe a vendor portal or two** — plus a few people doing slow, manual, error-prone work
between those systems. The systems are commodities. **The value (and the IP) is in the layer
that sits between them**: a model of how *this specific company* runs, wired into its tools,
that can read, decide, and act.

We build that layer, then build automations on top of it, then hand the client a **coworker**
they can tag in Slack/email to get work done.

## What we are NOT building

- **Not an ERP.** Too messy, too long to build, and the market will have moved by the time
  it ships. ERPs are also where incumbents (NetSuite, Intuit IES, Doss) are already fighting.
- **Not a generic chatbot.** A bare LLM doesn't connect to live systems, doesn't know the
  business's rules, and can't show its work or take real actions safely.

## The architectural insight

> Build the intelligence layer **before** data goes into the ERP and **after** it comes out.
> Then the ERP is just a commodity **system of record**.

```
  Inbound (email, PDFs, vendor msgs)
            │
     ┌──────▼───────┐
     │  OUR LAYER    │  ← context graph + connectors + automations
     │ (the coworker)│
     └──────▲───────┘
            │
         ERP / QBO        ← commodity system of record
            │
     ┌──────▼───────┐
     │  OUR LAYER    │  ← reporting, monitoring, outbound actions
     └──────────────┘
```

## The business model: forward deployment

A **platform + custom implementation** hybrid (same model as Varick):

1. **Embed & map** — sit with the client, learn the team, tools, and how work actually flows.
2. **Connect** — build/configure connectors (MCPs) into their existing systems. No migration.
3. **Contextualize** — encode their data, rules, definitions, and exceptions into a context layer.
4. **Automate** — ship use cases (reporting + automations) custom to them.
5. **Hand off + retain** — they own a coworker they can extend; we charge an **initiation fee**
   for the build (~4–8 weeks) and an **ongoing retainer + licensing** to maintain & expand.

### What's reusable vs. custom (the margin question)

| Reusable (the platform / IP) | Custom per client (the services) |
|---|---|
| Connector library (how we integrate QuickBooks, email, common ERPs) | The specific context graph (this company's rules/data) |
| The *method* for gathering company context | Per-system config & edge cases (e.g., your Traverse vs. mine) |
| Confidence-scoring + human-approval + audit framework | The chosen use cases / automations |
| Reporting/automation scaffolding (spin up in ~½ day once layer exists) | Data quality reconciliation |

**Honest take:** it is *not* fully reusable. Every engagement needs real implementation work,
which is *why* we charge for it — but the connectors and method compound across clients.

## The end-state vision

A **company sandbox**: a Claude/agent instance on the client's VM/droplet holding all their
data + logic + connectors, with **live-updated context** and curated **memory/learning**.
Anyone at the company tags it (Slack/email) and it does the task. Each new client makes our
playbook sharper.

## Go-to-market

- **Start in ONE vertical: wine.** Cameron is 2nd-gen wholesale with a deep warm network;
  the industry is complex, antiquated, and underserved by tech. (See `industry-research/wine.md`.)
- **Stay opportunistic** about warm SMB leads in adjacent import/distribution businesses
  (e.g., Davis — baby products on Amazon; see `industry-research/toys-and-baby-products.md`).
- **Land 1–2 lighthouse clients** to build credibility, surface unknowns, and stand up the team.
- **Horizontal playbook:** once the playbook works, what changes by industry is mostly the
  *systems* — and every system is an API. Learn APIs, not industries.

## Target customer (ICP) — current view

- **Wine importers/distributors, ~$10–30M revenue, ~dozen employees.** (Note: Intuit defines
  $10–30M as "mid-market," so this is a real, money-backed segment, not "too small.")
- Value prop is **two-sided**: (1) replace/avoid back-office headcount (hard-dollar ROI), and
  (2) **quality of life** — give an owner 10–20 hours/week back (sells even with no layoffs).

## Open strategic questions

- **Service vs. platform** — how much can we truly productize? Affects margins and fundraising story.
- **Lead use case** — which automation do we lead with in-market? (Leading candidate: email→order/intake.)
- **Cameron's role** — customer, cofounder, or both? Make it explicit.
- **The engineer** — our critical dependency; nothing that moves money ships without one.
- **Plain-English explanation** — translate this whole thing for an SMB owner who's never heard "MCP."

## Related docs
- What we sell → [`offerings.md`](offerings.md)
- Who's already doing this → [`competitive-research.md`](competitive-research.md)
- Who to talk to → [`customer-discovery.md`](customer-discovery.md)
