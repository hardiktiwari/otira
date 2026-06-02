# AGENTS.md — Operating Guide for AI Agents

This repo is the operating system for our company, **Otira**: we build **AI
coworkers for SMBs via forward-deployed implementations**. Read this before doing work here.
*(Otira is our **finalized** company name. The earlier "Keel" was retired due to a direct-competitor
collision. Domain selection is still open — see [`docs/brand-naming.md`](docs/brand-naming.md).)*

## What this project is
A reusable **context layer + connectors** on top of the systems a company already uses, plus
custom **automations** on top — delivered hands-on, then handed off. Beachhead vertical: **wine**.
Full thesis: [`docs/strategy.md`](docs/strategy.md).

## Read-first map
- New to the project? Read `README.md` → `docs/strategy.md` → `docs/offerings.md`.
- Researching a competitor → `docs/competitive-research.md` (use the `research` skill).
- Researching/serving a vertical → `docs/industry-research/`.
- Talking to a customer → `docs/customer-discovery.md` (use the `biz-development` skill).
- Why did we decide X? → `docs/decisions.md`. **Log new decisions there.**
- Unsure of a term → `docs/glossary.md`.

## Which skill for which task
| Task | Skill |
|---|---|
| Build a deck / one-pager | `skills/ppt` |
| Discovery call, qualifying, objections, pricing | `skills/biz-development` |
| Design context layer / connectors / automations / trust | `skills/ai-strategy` |
| Build connectors, agent, dashboards, write-backs, website | `skills/dev` |
| Research a competitor or market | `skills/research` |
| Turn a meeting transcript into notes + doc updates | `skills/meeting-notes` |
| Write explainers, exec/investor comms, outreach | `skills/writing` |

## How to behave in this repo
1. **Separate fact from suggestion.** When extracting from a meeting/source, clearly mark what
   was *said* vs. your own *recommendation*. (We care about this.)
2. **Plain English for customers.** No "MCP"/"forward deployment" jargon in customer-facing
   material — define ERP/context-layer in plain words. See `docs/one-pager.md`.
3. **Trust is a feature.** Any automation that acts must assume confidence scoring + human
   approval + audit trail; anything moving money needs engineering rigor (never "just rip it").
4. **Land narrow, architect broad.** Build each client workflow as instance #1 of a reusable
   engine — separate reusable "engine" from per-client "config."
5. **Keep docs current.** If a conversation changes the plan, update the relevant doc and add a
   line to `docs/decisions.md`.
6. **Never commit secrets.** Respect `.gitignore`; keep credentials out of the repo.
7. **Honest over optimistic.** Flag risks, gaps (esp. the engineer gap), and partial reusability.

## Conventions
- **Three kinds of things:** knowledge (`docs/`), know-how (`skills/` as `SKILL.md`), and
  **artifacts we produce** (`decks/`, `website/`, `product/`, `legal/`, `finance/`, `assets/`).
  A skill is the *ability* to do something; an artifact is the *thing produced*. Never put
  artifacts (a website, a deck, contracts, product code) inside `skills/`.
- Cross-link related docs. Date research and meeting notes (`YYYY-MM-DD`).
- Company name is **Otira** (finalized; domain TBD — see `docs/brand-naming.md`).
- **Never commit secrets or signed contracts with real client data** (respect `.gitignore`).
