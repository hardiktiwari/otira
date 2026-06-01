# Otira — AI Coworkers for SMBs

> *(Otira is a **provisional** internal codename. The prior name "Keel" was retired — it collides
> with a direct competitor (keel.so). The space is crowded; the name needs formal clearance before
> we commit. See [`docs/brand-naming.md`](docs/brand-naming.md).)*

> We build **AI coworkers** for small and mid-sized businesses via **forward-deployed
> implementations**: a reusable **context layer + connectors** on top of the systems a
> company already uses, then custom **automations** on top. Start vertical (wine), scale
> horizontally. When we leave, the client owns a coworker they can extend.

**Status:** Pre-team, pre-revenue. Validating the idea, lining up 1–2 lighthouse clients,
and hiring/partnering for an AI engineer.

---

## The one-liner (plain English)

Most small businesses run on email, an ERP, and a pile of spreadsheets — and a few people
doing slow, manual, error-prone work. We come in, wire AI into the tools they already use,
teach it how their business actually runs, and build automations that do the repetitive work.
You tag it like a coworker and it gets things done. **Software you adopt → coworkers that
operate for you.**

## How this repo is organized

The repo separates three kinds of things:
**knowledge** (`docs/`), **know-how** (`skills/`), and **artifacts we produce**
(`decks/`, `website/`, `product/`, `legal/`, `finance/`, `assets/`).
> A *skill* is the reusable ability to do something (e.g., "how to build a site"); an *artifact*
> is the thing produced (e.g., the site itself). Don't put artifacts in `skills/`.

### `docs/` — knowledge & strategy
| Path | What's in it |
|---|---|
| [`AGENTS.md`](AGENTS.md) | How AI agents should operate in this repo (read first) |
| [`docs/vision.md`](docs/vision.md) | Vision, mission, principles |
| [`docs/strategy.md`](docs/strategy.md) | Core thesis + "forward deployment" approach |
| [`docs/offerings.md`](docs/offerings.md) | What we sell — platform, use cases, delivery |
| [`docs/business-model.md`](docs/business-model.md) | Revenue streams, pricing, unit-economics shape |
| [`docs/delivery-playbook.md`](docs/delivery-playbook.md) | Repeatable per-client process (our engine) |
| [`docs/competitive-research.md`](docs/competitive-research.md) | Varick, Doss, Sapien, BlackLine, IES, point apps |
| [`docs/customer-discovery.md`](docs/customer-discovery.md) | Discovery questions + people + ICP |
| [`docs/investor-guide.md`](docs/investor-guide.md) | Market, why-now, comps, traction, risks |
| [`docs/one-pager.md`](docs/one-pager.md) | Plain-English explainer |
| [`docs/metrics.md`](docs/metrics.md) | North-star + KPIs |
| [`docs/security.md`](docs/security.md) | Data handling & trust posture |
| [`docs/roadmap.md`](docs/roadmap.md) | Phases + 30/60/90 |
| [`docs/decisions.md`](docs/decisions.md) | Decision log (what + why) |
| [`docs/glossary.md`](docs/glossary.md) | Shared vocabulary |
| [`docs/brand-naming.md`](docs/brand-naming.md) | Naming research, taken names, clearance checklist |
| [`docs/industry-research/`](docs/industry-research/) | Per-vertical research (wine, toys, …) |
| [`docs/meeting-notes/`](docs/meeting-notes/) | Transcripts + synthesized notes |

### `skills/` — reusable know-how
PPT, biz-development, ai-strategy, dev, research, meeting-notes, writing. See [`skills/`](skills/).

### Artifacts — the things we produce
| Path | What's in it |
|---|---|
| [`decks/`](decks/) | Pitch decks & visual artifacts (incl. the HTML overview) |
| [`website/`](website/) | The marketing/pitch site (starter `index.html` is live) |
| [`product/`](product/) | The platform code (connectors, context, engine, agent, app) — once we have an engineer |
| [`legal/`](legal/) | Entity, founder, and client-contract templates + status |
| [`finance/`](finance/) | Pricing/unit-economics model, cap table, runway |
| [`assets/`](assets/) | Logo, brand, images |

## Key terms (so everyone's aligned)

- **ERP** — Enterprise Resource Planning: the central system that runs a business's guts
  (inventory, orders, purchasing, invoicing, accounting). The "system of record."
- **Context layer / context graph** — a structured model of how a specific company runs
  (its data, rules, definitions, exceptions) that AI can use to act reliably. Our core IP.
- **Connectors / MCPs** — the integrations that let our system read/write the client's tools
  (email, ERP, QuickBooks, etc.). Built once, reconfigured per client.
- **Forward deployment** — the delivery model: we embed for a few weeks, build the context
  layer + connectors + automations custom to the client, then leave (with a retainer).
- **Coworker** — the end experience: an AI you tag in Slack/email that does tasks for you.

## Working principles

1. **Don't build an ERP.** Build the intelligence layer *before* data enters and *after* it
   leaves the ERP — the ERP becomes a commodity system of record.
2. **Land narrow, architect broad.** One painful workflow first; build it as instance #1 of a
   reusable engine, not a one-off.
3. **Trust is a feature.** Confidence scores + human approval + full audit trail on every action.
4. **Start in one vertical (wine), but stay opportunistic** about warm SMB leads.
5. **We're PMs — we need a real AI engineer** before we automate anything that moves money.
