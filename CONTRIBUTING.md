# Contributing & Workflow

How we work in this repo. Keep it lightweight — we're a small founding team.

## Source of truth & pushing
- **Personal machine = source of truth.** It can push to GitHub.
- **Work machine = drafting only.** A company security policy blocks pushing source code to
  external remotes from the work device, so don't rely on pushing from there.
- Practically: do real work (commit + push) on a personal machine in Cursor.

## Branches
- Solo / early stage: commit straight to `main`.
- When collaborating: `feature/<name>`, `fix/<name>`, `docs/<name>` → PR → merge to `main`.

## Commit messages
`type: summary` (imperative). types: `docs`, `feat`, `fix`, `research`, `chore`.
Examples: `docs: add wine pricing notes`, `research: add Opser to competitive map`.

## Keep the knowledge base current
- New decision? Update the relevant `docs/` file and add a line to `docs/decisions.md`.
- Date research and meeting notes `YYYY-MM-DD`. Use `skills/` and follow `AGENTS.md`.

## Never commit
- Secrets, API keys, `.env`, credentials, or signed contracts / real client data (see `.gitignore`).
