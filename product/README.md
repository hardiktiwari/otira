# Product

Where the **actual platform code** lives — the reusable engine plus per-client configuration.
This is an artifact (code), distinct from the *know-how* in [`../skills/dev`](../skills/dev/SKILL.md)
and [`../skills/ai-strategy`](../skills/ai-strategy/SKILL.md).

> Empty for now — populated once we have an AI engineer (see `../docs/decisions.md` D7).

## Planned layout (monorepo)
```
product/
  connectors/        # reusable integrations (email, QuickBooks, ERPs, data feeds) — the IP
  context/           # context-graph builder + schema (the "company brain")
  engine/            # intake & reconciliation pipeline; confidence + approval + audit
  agent/             # the coworker (runs on a client VM / "company sandbox")
  app/               # client-facing web app: inbox queue, dashboards, chat
  clients/<client>/  # per-client config ONLY (not core code) — gitignore if sensitive
```

## Principles
- **Reusable engine vs. per-client config** — keep them separate so client #2 is mostly config.
- **Safe writes** — drafts, idempotency, retries, reconciliation; never auto-move money.
- **Postgres** for real state (replaces CSV/JSON pipelines from the prototype era).
- Document every new connector so it joins the reusable library (`connectors/`).

## Reference prototype
Cameron's "DBO" (email → action → QBO/PO) informs the engine design.
See [`../docs/industry-research/wine.md`](../docs/industry-research/wine.md).
