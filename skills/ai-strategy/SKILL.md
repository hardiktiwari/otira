---
name: ai-strategy
description: Design the company's AI approach — the context layer, connectors/MCPs, automation patterns, and trust/safety guardrails. Use when scoping a client's automations, designing the context graph, choosing what to automate, or defining confidence/approval/audit patterns.
---

# AI Strategy

How we think about building reliable AI coworkers on top of a client's existing systems.

## The layered model
Build intelligence **before** data enters the ERP and **after** it leaves; the ERP is a
commodity system of record. (See [`../../docs/strategy.md`](../../docs/strategy.md).)

## The three building blocks
1. **Context layer (the "company brain")** — a structured, living model of how the company runs:
   master data, business rules, definitions, exceptions, org structure. This is our core IP.
   *(Inspiration: Sapien's "Company Context Model.")*
2. **Connectors / MCPs** — read/write integrations to email, ERP, QuickBooks, portals, Slack.
   Built once, reconfigured per client. **Every system is just an API.**
3. **Automations / agent** — workflows on top, plus a coworker the client tags in Slack/email.

## MCP vs. agent pipeline (don't confuse them)
- **MCP** = a standard way to expose tools/data to an AI assistant (good when a *human* drives it).
- **Unattended automation** (email → action with no human) = a **backend agent pipeline**
  (webhook → parse → LLM extract → lookups/validate → write draft). MCP is optional plumbing.
- Don't let "learn MCP" block progress — it's a tool, not the project.

## Automation design patterns
- **Intake & reconciliation engine:** unstructured input → extract → match to master data →
  validate against rules → write structured draft → report. (The reusable core.)
- **Trigger sources:** external (inbound email/doc) **and** internal (e.g., replenishment logic).
- **Inbox queue:** recognized action + info + accept/edit, with an audit trail.

## Trust & safety (non-negotiable)
- **Confidence scoring** on every action; auto-approve only above a high threshold (~95%) for
  low-risk recurring items; everything else waits for a human.
- **Human-in-the-loop** approval as the default.
- **Full traceability** — every output/action links to its source (email, transaction, rule).
- **Money movement** requires engineering rigor + explicit approval. Never "just rip it."
- **Security:** data stays in the client's systems; role-based access; don't train on client data;
  plan for SOC 2 as we move up-market.

## Scoping a client's automations
1. Find the highest-pain, bounded workflow (the wedge).
2. Confirm the inputs/outputs and the master data needed to match against.
3. Define "correct" and the approval threshold with the client.
4. Build it as instance #1 of the reusable engine (separate engine vs. client config).
5. Parallel-run before trusting it; expand from there.

## The honest gap
A capable operator can get ~80% there alone; the hard **20%** is robustness as automations
compound. That's where a real **AI engineer** + our platform earn their keep.
