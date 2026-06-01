# Security & Trust

> We touch clients' financial and operational data and can take actions in their systems. Trust
> is part of the product and a real buying factor. This is our posture + the path to maturity.

## Principles
- **Data stays in the client's systems** wherever possible; least-privilege access on every connector.
- **We don't train on client data.**
- **Role-based access** — match the client's existing permissions; separate see / approve / configure.
- **Human-in-the-loop** for anything that matters; **never auto-move money** without approval + rigor.
- **Full audit trail** — every action traceable to its source (email, transaction, rule).

## Practical controls
- Secrets in a secret store / env vars — **never** in the repo (see `.gitignore`).
- Per-client credentials scoped to only what the automation needs.
- Draft-state writes + reconciliation before anything is finalized.
- Logging + monitoring of agent actions; alerting on anomalies.
- Parallel-run new automations before trusting them (esp. anything feeding accounting/CPA).

## Maturity path
- **Now:** clear data-handling practices + a DPA/security addendum in client contracts (see `../legal/`).
- **As we move up-market:** pursue **SOC 2 Type II** (table stakes for larger clients), formal
  RBAC, vendor security reviews. (Sapien/peers lead with SOC 2 + "data never leaves your systems.")

## Client-facing answer (plain English)
"Otira works inside your own systems, asks before anything important, and logs everything it does,
so you can always see and verify its actions. We never move money on our own."

## TODO
- [ ] Draft the security/data-handling addendum for client contracts.
- [ ] Decide SOC 2 timing based on target client size.
