# Phase 3b — POWERS (7 Powers verification)

Purpose: decide whether the candidate has a path to durable power that
is NOT the code. Agent-built software has made code cheap: a funded
rival with AI agents can rebuild most products in weeks, so a candidate
whose only advantage is its software has no business behind it. Phase 3
asks "can this win customers?"; Phase 3b asks "can it keep them once
someone copies it?". Run it for every candidate that survives Phase 3,
before the Phase 4 verdict.

Framework: Hamilton Helmer's *7 Powers*. A power needs BOTH a **benefit**
(it improves cash flow: lower cost, higher price, or lower churn) AND a
**barrier** (rivals can't or won't copy it). Benefit without barrier is
just a good idea that will be copied.

## The seven powers

| Power | Benefit | Barrier | Typical stage it can appear |
|---|---|---|---|
| Scale economies | Unit cost falls with volume | Rival can't reach the volume without ruinous losses | Takeoff |
| Network economies | Each user adds value for the others | Rival can't reach critical mass in that network | Takeoff |
| Counter-positioning | A new model the incumbent can't copy | Copying would damage the incumbent's existing business | Origination |
| Switching costs | Customers lose value by leaving (data, workflows, integrations, retraining) | Rival must compensate customers to move | Takeoff |
| Branding | Customers pay more for the same thing because of who sells it | Only built through long, consistent history | Stability |
| Cornered resource | Preferential access to a valuable asset (data, people, licences, relationships) on attractive terms | The access itself can't be bought or copied | Origination |
| Process power | Embedded organisation and know-how that lowers cost or raises quality | Takes years to replicate, even when visible | Stability |

New entrants almost always originate with **counter-positioning** or a
**cornered resource**, then must convert into switching costs, network
economies or scale by takeoff. A plan that relies on branding or process
power in year one is fiction for a solo operator.

## Step 1 — Score each power at three horizons

For each of the seven, score **benefit** and **barrier** 0–3 at **Day 1**,
**24 months** and **5 years**. The power's score at each horizon is the
LOWER of the two (benefit 2 with barrier 0 scores 0). Write it as
`benefit/barrier/score`, e.g. `2/1/1`.

- 0 — none
- 1 — weak: real but small, or easily eroded
- 2 — solid: material benefit, barrier costs a rival real money or time
- 3 — strong: decisive; a rival would need to change who they are

Every non-zero cell needs a one-line **mechanism and evidence** (what
creates it, what proves it, evidence class). Unevidenced scores are 0.

## Step 2 — Code-share estimate

Estimate the share of the customer value that is the code itself, i.e.
what a clone gets for free. Over ~50% is high and is the candidate's
honest weak spot; say so. An operator's technical edge (rendering,
audio, routing, security) usually counts as code here, however rare it
feels. The clone test discounts it.

## Step 3 — The clone attack

Assume a **funded rival with AI agents, £500k and 30 days**. Write:
- **(a) What they get:** usually the whole product surface.
- **(b) What they don't get:** the data customers have built, hand-
  recruited supply, relationships, history, trust. This is the moat, if
  there is one.
- **(c) Cheapest neutralisation:** the cheapest move by the incumbent or
  an adjacent player that removes the candidate's reason to exist (a
  pricing change, a free tier, a bundle).

## Step 4 — Incumbent-feature attack, power view

Phase 3 asked whether an adjacent platform could ship this as a feature.
Here ask what stops the incumbent: capability, or its business model?
"They could, but it would break their per-seat revenue" is counter-
positioning and counts. "They could and they would" is a kill signal.

## Step 5 — Verdict line, power plan and gating

Write one **verdict line** at the top of the report:

`primary power <name> | 24-month score <n> | code share ~<x>% | clone attack: <one clause on what is and isn't cloneable>`

Then name:
- **Primary power** (the one the business is built to reach) and a
  **secondary**.
- **Power-path score** = the primary power's **24-month** score (0–3).
  This is the number that gates and ranks.
- **Leading indicator** — the metric that shows the power forming
  (boards per paying team, verified stops per region, apps under
  management).
- **Power checkpoint** — a numeric, dated gate proving the power exists
  (e.g. "50 paying teams averaging 40+ boards, 60%+ net revenue retention,
  by month 18"). It goes into the Phase 4 contract.
- **Power kill triggers** — events that remove the power (incumbent drops
  per-seat pricing; a platform bundles it free). Added to the
  instant-kill list.
- **Cheapest score-raising action** — the one move that most raises the
  power-path score for the least build effort (e.g. "ship the importer
  first; every incumbent repricing email becomes our acquisition
  channel"), with a rough build-session estimate.

**Gating (applied in Phase 4):**
- **Power-path 0** — no credible power. Never earns a standalone build.
  Capped at TIER-0, and in practice usually KILL, or EXTEND as a feature
  or revenue line inside a sibling candidate that does have power.
- **Power-path 1** — TIER-0 at most, and the power checkpoint is
  MANDATORY in the contract. Missing it is a kill.
- **Power-path 2–3** — normal verdict rules apply.

## Shortcuts

- For a group of obviously weak candidates (e.g. a portfolio sweep), a
  table row per candidate is enough: best attack, power-path with one
  clause of reasoning, verdict. Full reports are for anything heading to
  TIER-0 or better.
- Window check: crowded refugee markets close. If the obvious
  counter-positions are already occupied by winners that absorbed the
  last exodus (Obsidian after Evernote), power-path is 0 for any new
  entrant, however easy the build.

## Report format (copy into the dossier, section 5b)

```
**Verdict line:** primary power … | 24-month score … | code share ~…% | clone attack: …

| Power | Day 1 (B/Bar/Score) | 24 months | 5 years | Mechanism and evidence |
|---|---|---|---|---|
| Scale economies | 0/0/0 | | | |
| Network economies | | | | |
| Counter-positioning | | | | |
| Switching costs | | | | |
| Branding | | | | |
| Cornered resource | | | | |
| Process power | | | | |

**Code-share estimate:** ~…%. [why; the honest weak spot]
**Clone attack (funded rival, agents, £500k, 30 days):** (a) … (b) … (c) …
**Incumbent-feature attack, power view:** …
**Primary power:** … **Secondary:** … **Leading indicator:** …
**Power checkpoint:** … by month …
**Power kill triggers:** …
**Cheapest score-raising action:** … (~n build sessions)
**Gating result:** power-path n, so …
```
