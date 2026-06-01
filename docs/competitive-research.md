# Competitive Research

> Who's in this space, what they do, and where our open lane is.
> Last updated: 2026-05-31.

## The map (analyze vs. act × SMB vs. enterprise)

```
                 ENTERPRISE / MID-MARKET
                          ▲
        Sapien            │      Doss (ERP replacement)
        BlackLine         │      Intuit IES
   (ANALYZE) ─────────────┼───────────────── (ACT)
        Point apps        │      Varick (forward-deployed agents)
                          │      ► US (wine, SMB, forward-deployed)
                          ▼
                        SMB
```

**Our open lane:** *act/automate* + *SMB* + *vertical (wine)* + *forward-deployed*. Most
funded players cluster in *analyze* and/or *enterprise*.

---

## Varick Agents — our closest model
- **What:** Forward-deployed AI agent systems built on top of a company's existing software.
  "No generalized software, no migrations." Finance Ops / Revenue Ops / Logistics Ops packages.
- **Model:** Service-based delivery; embed → design → deploy on client's stack → optimize.
  6–12 weeks to production. Pricing after discovery, ~90% cheaper than the FTE cost.
- **Shape:** small team, well-funded.
- **Pick up:** the 4-step delivery model; outcome-based selling; "<20 hrs of client effort"
  framing; department-as-package GTM.

## Doss (doss.com) — ERP replacement route
- **What:** AI-native "Adaptive ERP" / Operations Cloud. Composable no-code ERP alternative
  (tables/forms/workflows) + Dossbot AI copilot + built-in BI. Plugs into QuickBooks/NetSuite.
- **ICP:** mid-market consumer goods / F&B / manufacturing / distribution, $20–250M revenue.
- **Funding:** ~$73M total (Series B $55M; investors incl. Intuit Ventures).
- **Difference from us:** Doss wants to *be* the operations system (adopt their platform). We
  layer on top of what you already run, done-for-you, and leave you self-sufficient.
- **Why-us vs. Doss:** no platform adoption; vertical depth (Doss is "less ideal for highly
  specialized verticals"); smaller/cheaper surgical entry.

## Sapien (sapien.ai) — AI analytics for finance/ops
- **What:** AI *analytics* layer. Connects to ERP + ops data, learns a "Company Context Model,"
  answers FP&A/ops questions: variance, gross margin, driver forecasts, anomaly detection,
  budget vs. actuals, monitoring. Emphasis on **traceability** ("see where every number came from").
- **ICP:** mid-market → Fortune 500; complex multi-site (manufacturing, F&B, pharma, energy,
  CPG, financial services); strong **PE-portfolio** land-and-expand motion.
- **Funding:** ~$8.7M seed (General Catalyst, Neo; angels from OpenAI/Google/Stripe/Ramp).
- **Difference from us:** Sapien **analyzes** (read-mostly); we **act** (read + write/automate).
  They're up-market & product-led; we're SMB, vertical, forward-deployed.
- **Pick up:**
  - "Company Context Model" framing for our context layer.
  - **Verifiability as a headline feature** (source transactions + logic behind every output).
  - Objection-killer: *"data doesn't need to be clean, it just needs to exist."*
  - Their crisp **"vs. ChatGPT/Claude"** comparison — reuse for our plain-English pitch.
  - **PE-portfolio expand** → our analog is the **wine network** (land one, referrals compound).
  - Early **security signals** (SOC 2, "data never leaves your systems," RBAC).
  - **Quantified ROI** proof points ("$12M error caught," "30+ hrs saved/week").

## BlackLine — incumbent FinOps reporting
- **What:** Large (~3–4k employees) financial reporting/close platform on top of QuickBooks/ERPs.
  Dashboards & views on P&L; financial close automation.
- **Relevance:** what "point on top of the ERP" looks like at scale; analysis-heavy, enterprise.

## Coworker.ai — naming/positioning comp
- **What:** "Your AI coworker" positioning. Watch how they frame the coworker experience.

## Intuit IES (Intuit Enterprise Suite) — incumbent moving in
- **What:** Intuit's push into mid-market ERP with agents on top.
- **Gap we exploit:** ERP-native agents **don't reach data outside the ERP** (email, etc.) and
  won't sit with you to build a custom context layer. ERPs also guard their data.

## Point apps (AP automation, dashboarding, etc.)
- **What:** Single-purpose apps bought on top of an ERP once a company hits ~100+ employees;
  each ≈ ⅓ the cost of an employee.
- **Relevance:** how mid-size firms buy today; we aim to be the connected layer beneath several
  of these, for smaller companies that can't stitch point apps together.

## Direct competitors — forward-deployed AI ops for SMBs (THE crowded lane)
> Found via naming research 2026-05-31. These are doing **almost exactly our model**
> (AI coworker/overlay on existing systems, no migration, forward-deployed, "pick one
> workflow," confidence + approval + audit). This lane is hot and getting crowded fast.

- **Opser** (opser.com) — "AI-native workspace for operations-heavy businesses… forward-deployed
  engineers build it with you… sits on top of QuickBooks/HubSpot/Outlook… pick one workflow,
  automate in weeks." Nearly identical pitch.
- **Wend AI** (wendai.ai) — "AI workforce agent that joins your team… overlay on your ERPs/CRMs/TMS,
  no rip-and-replace… learns from corrections… SOC 2, audit trails." Nearly identical.
- **Operio** (operio.work) — "AI operations team… we sit down, learn your business, load your
  docs… specialist agents… you approve." Forward-deployed, SMB.
- **Hearth AI** (hearthai.co) — "custom AI tools for small business… we understand your operation
  from the inside, build in weeks, one-page price, work inside your existing setup." Our SMB pitch.
- **Augie / goAugment** (goaugment.com) — "AI teammate for supply chain & B2B/wholesale
  distribution… quote-to-cash, email/EDI intake → ERP, no rip-and-replace, trains only on your
  data, Knowledge Hub." Very close; funded; distribution-focused (adjacent to wine).
- **Runwell** (runwellsystems.com) — custom integrated digital systems for SMBs, deployed to your
  infra, "fully yours," background AI agents.
- **CloveOS** (cloveos.com) — agents that observe ops + act; 200+ integrations via MCP; on-prem option.
- **Vertical logistics ones** (CargoAi, Draying/Draya, CargoFL, Cargofy, Cargio) — email→order /
  quote-to-cash automation inside freight/drayage/courier niches.

**Implication:** "AI coworker on top of your systems, forward-deployed" is no longer a novel wedge.
Differentiation must come from **(a) a specific vertical we own** (wine first — deep three-tier/
compliance/depletion logic competitors won't touch), **(b) warm-network distribution** (Cameron),
and **(c) execution/trust quality**. Revisit positioning with this in mind; "we overlay your tools
and automate a workflow" alone is now table stakes.

## Macro notes
- The forward-deployed-AI-ops-for-SMB space is **saturated** (see above) — naming and positioning
  must work harder.
- Lots of startups are clustering in **healthcare** right now.
- Many are "doing the same thing" — differentiation is **which use cases you lead with** and
  **which vertical/segment you own first.**
- Watch for **analyze-first players (Sapien) moving into action**, or **enterprise players
  moving down-market** — that's when lanes collide.

## TODO
- [ ] Add: forward-deployment practitioners in tech/CX we've spoken to (names, notes).
- [ ] Add: healthcare implementers (point apps) we referenced.
- [ ] Build the visual competitive map as a shareable artifact (deck/one-pager).
