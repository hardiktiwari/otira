---
name: meeting-notes
description: Turn a raw meeting transcript or notes into a structured synthesis and update the relevant repo docs. Use when the user pastes/shares a transcript or notes from a customer, cofounder, advisor, or competitor conversation and wants the signal extracted and filed.
---

# Meeting Notes → Synthesis

Convert messy transcripts into structured notes that update our knowledge base.

## When to use
- The user pastes a transcript or shares notes/a recording link and says "extract," "summarize,"
  "see what we can pick up," or "capture this."

## Process
1. **Create the note** in `docs/meeting-notes/` named `YYYY-MM-DD-short-topic.md`, using
   [`../../docs/meeting-notes/_template.md`](../../docs/meeting-notes/_template.md).
2. **Extract, separating fact from suggestion:**
   - **Key facts** = what was actually said.
   - **Our take** = your own recommendations, clearly labeled as additions (we care about this —
     never blend your ideas into "what they said").
3. **Pull out:** TL;DR, decisions, action items, people to follow up, doc updates needed.
4. **Propagate:** update `strategy.md`, `offerings.md`, `competitive-research.md`,
   `industry-research/*`, or `customer-discovery.md` as warranted; log decisions in `decisions.md`.
5. **Index it** in `docs/meeting-notes/README.md`.

## Guardrails
- If asked to "listen" to live audio: you can't — only work from pasted text, a file in the repo,
  or a shared doc link. Say so plainly.
- Don't invent attributions or numbers. Quote/paraphrase faithfully; flag uncertainty.
- Keep customer-identifying details handled respectfully; redact where appropriate.
