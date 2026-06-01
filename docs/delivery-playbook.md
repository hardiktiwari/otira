# Delivery Playbook (Forward Deployment)

> The repeatable process we run for every client. This *is* the engine — the thing that makes us
> a company, not a one-off shop. Refine it after each engagement.

## Principles
- **Land narrow, architect broad.** Ship one workflow; build it as instance #1 of a reusable engine.
- **Reusable vs. custom:** the connector library + context-gathering *method* carry over; the
  specific context graph and some configs are rebuilt per client.
- **Trust is a feature:** confidence + human approval + audit on every action; rigor for money.

## Phase 0 — Qualify (pre-engagement)
- Confirm pain, connectable systems (APIs vs. CSV), an owner-buyer, and a nameable ROI.
- See `skills/biz-development` and `docs/customer-discovery.md`.
- **Exit:** a signed, fixed-scope discovery sprint.

## Phase 1 — Embed & Map (~1–2 weeks)
- Shadow a real day; map how the target workflow actually runs, step by step.
- Inventory systems, data sources, master data (customers, products, vendors), and rules.
- Collect sample artifacts (real emails/docs, system exports — redacted).
- **Deliverables:** workflow map, system/data inventory, chosen wedge use case, success metric.
- **Exit:** agreement on the first automation and what "correct" means.

## Phase 2 — Connect (~1–2 weeks, overlaps Phase 3)
- Stand up connectors from the **reusable library** (email ingestion, QBO, the client's ERP,
  any data feed). Per client, change configs — not core code.
- Set up the agent environment (the client's VM/"company sandbox"); secrets in a secret store.
- **Deliverables:** working read/write connectors; a safe place for the agent to run.
- **Exit:** the system can read the inputs and write drafts into the right targets.

## Phase 3 — Contextualize (~1–2 weeks)
- Build the **context graph**: master data, business rules, pricing logic, definitions, exceptions.
- Encode matching logic (e.g., messy vendor/SKU names) and the confidence model.
- **Deliverables:** a context layer the automation can rely on; documented rules.
- **Exit:** the system matches/validates against the client's real rules with measurable accuracy.

## Phase 4 — Automate the wedge (~2–4 weeks)
- Ship the use case end-to-end: input → match → validate → draft → human approval → action.
- Implement confidence scoring, approval thresholds, and the audit trail.
- **Deliverables:** a working coworker for one workflow on real data.
- **Exit:** it produces correct, approvable output on live inputs.

## Phase 5 — Harden & parallel-run
- Run alongside the existing manual process; compare outputs; fix edge cases as they compound
  (the hard "20%"). Never cut over money-movement without engineering review.
- **Deliverables:** reliability data; quantified outcomes (hours saved, errors caught).
- **Exit:** client trusts it for the workflow; metrics captured.

## Phase 6 — Hand off & expand (ongoing retainer)
- Hand over the keys; enable the client's team to extend automations.
- Add use cases (invoice→QBO, replenishment→PO, reporting); pursue referrals in their network.
- **Deliverables:** retainer scope; expansion backlog; a reference/case study.

## Per-engagement checklist
- [ ] Fixed scope + success metric agreed
- [ ] Sample data collected (redacted)
- [ ] Connectors reused from library (configs only)
- [ ] Context graph + rules documented
- [ ] Confidence + approval + audit implemented
- [ ] Parallel-run before trust
- [ ] Outcomes quantified + case study
- [ ] Playbook updated with what we learned

## After each engagement
- Promote anything reusable (a new connector, a matching pattern) into the platform/library.
- Note vertical-specific learnings in `docs/industry-research/<vertical>.md`.
- Log notable decisions in `docs/decisions.md`.
