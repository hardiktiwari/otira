# Business Model

> The narrative model: how we make money, the unit economics shape, and the margin thesis.
> Actual numbers/spreadsheets live in [`../finance/`](../finance/).

## Revenue streams
1. **Initiation / implementation fee** — the forward-deployed build (~4–8 weeks). The bulk of
   early revenue; funds the company before any raise.
2. **Ongoing retainer** — monthly fee to manage, monitor, and keep automations reliable.
3. **Licensing** — for the platform/engine the client keeps using after handoff.
4. *(Later)* **Expansion** — additional use cases / workflows per client.

## Pricing approach
- **Anchor to value, not hours:** the FTE cost replaced + the owner hours reclaimed.
- Reference point: a single point app ≈ ⅓ the cost of one employee; a working coworker that
  replaces real back-office work (or buys back 10–20 owner hours/week) should be priced against
  that headcount, not against lines of code.
- Discuss price **after discovery**, once the use case and ROI are clear.

## Unit economics (shape — fill in real numbers in /finance)
- **Cost to deliver** = engineer + founder time during the 4–8 week build + hosting.
- **Margin driver** = reuse. The connector library + context-gathering method are built once;
  per client we change configs. Client #2 onward should cost much less to deliver than #1.
- **Capacity** = how many concurrent engagements one engineer + the platform can support.

## The honest tension
This sits between **services** (custom, high-touch, lower margin) and **product** (reusable,
scalable, higher margin). Our bet: enough reusability (connectors + method) to earn product-like
margins over time, while forward deployment wins trust and the first clients. Validate the
reuse % during client #1 — it determines the whole margin and fundraising story.

## Funding stance
- **Short term:** initiation fees can fund the build → reduce/avoid an early raise.
- **Long term:** decide raise vs. bootstrap based on traction and how product-like the margins look.
- Comps for context in [`competitive-research.md`](competitive-research.md) and
  [`investor-guide.md`](investor-guide.md).
