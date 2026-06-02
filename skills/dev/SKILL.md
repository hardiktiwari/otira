---
name: dev
description: Build the company's technical stack — connectors/MCPs, the agent/sandbox on a VM, client dashboards, safe write-backs to ERP/QuickBooks, and the marketing website. Use when implementing or reviewing any code for connectors, automations, the client-facing surface, or the website.
---

# Development

Engineering playbook for building reliable AI coworkers. **Note:** the founders are PMs — this
skill guides the work, but anything that moves money needs a real AI engineer (see below).

## Reference architecture
```
 UI layer (client browser)        ← dashboards / inbox queue / chat window
        │
 Backend + agent layer            ← context graph + automation pipelines + connectors
        │                            (Claude/agent on a VM/droplet = "company sandbox")
 Systems of record                ← ERP, QuickBooks (QBO), email, portals
```
- **Cursor is the workshop, never the client's product.** The client uses a web app.
- Reference prototype stack (Cameron's DBO): React + Vite + Tailwind on a DigitalOcean droplet,
  Express/Node API, Clerk auth, Python pipeline, QBO via API (draft state). A real build adds a
  proper **Postgres** database.

## Connectors / MCPs
- Build a **reusable connector library**; per client, change configs, not code.
- Start with: **email ingestion** (webhook), **QuickBooks Online API**, common ERPs (e.g., Traverse),
  data-feed ingestion (CSV → standardize → match).
- Treat writes as first-class: idempotency, draft states, retries, and reconciliation.

## The agent / "company sandbox"
- An agent instance on the client's VM with the context graph + connectors + curated memory.
- Live-updated context; logged actions; tag-to-act via Slack/email.

## Client-facing surface (the "layer they use")
- A real web app: inbox queue (accept/edit), dashboards, and a chat window to the agent.
- Keep it deployable on the client's existing stack; no migration.

## Safety engineering (hard requirements)
- Confidence thresholds + human approval gates; **never** auto-move money without rigor + approval.
- Full audit log of every action and its source.
- Role-based access; secrets in env/secret stores (see `.gitignore`); least privilege on connectors.
- Parallel-run new automations before cutover; especially anything feeding accounting/CPA.

## Website (marketing)
- For the visual look-and-feel (brand system, UI patterns, glassmorphism), use `skills/design`.
- Modern, fast, outcome-focused (cf. Varick/Doss/Sapien sites). Static site or simple framework.
- Sections: hero (outcome), how-it-works (embed → connect → contextualize → automate → handoff),
  use cases, "vs. just using ChatGPT," security, FAQ, book-a-call.
- Deploy simply (e.g., static host / droplet behind a reverse proxy).

## Standards
- Version everything in this repo; meaningful commits; no secrets committed.
- Prefer Postgres for real state; typed APIs; tests around write-backs and matching logic.
- Document each connector and automation so it's reusable for the next client.

## The engineer gap (read this)
Before promising any production automation that touches money or mission-critical ops, bring on
an **AI engineer** accountable for the code, debugging, and reliability. AI coding tools amplify
that person — they don't replace the judgment.
