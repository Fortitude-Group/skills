# Phase 0 — SCOPE

Purpose: capture who the operator is, what is off-limits, and how
candidates will be scored — once, in a reusable scope file. Every later
phase reads this file; nothing is mined without it.

## Interview the operator

Ask only what isn't already in the conversation. Cover:

1. **Operator context.** Solo or team? Skills and stack? Build throughput
   vs go-to-market ability — which is the real bottleneck? (For most
   AI-assisted solo builders, building is cheap and marketing is the
   bottleneck; weight everything accordingly.) Time and cash constraints.
2. **Hard exclusions.** Employer conflicts (industries that create legal
   or career risk), sales motions the operator cannot or will not do
   (e.g. relationship/field sales, phone-trust selling), markets gated by
   accreditation an independent can't get, and any sourcing channels that
   destroy information advantage (public idea marketplaces).
3. **GTM abilities.** What routes to buyers are realistic: SEO/content,
   developer communities, app stores, marketplaces, existing audience?
   What's impossible: cold outbound, founder personal brand, trade shows?
4. **Portfolio.** Existing products, their state, and which one holds the
   flagship/GTM slot. Extensions of existing products beat new fronts —
   record what "synergy" concretely means (shared tech, shared buyer).
5. **Revenue shape.** Recurring vs one-off preference, price-point
   comfort zones, B2B vs B2C tolerance.

## Build the scoring rubric

Default criteria (adapt weights to the operator, keep all seven):

- **Pain evidence** — verbatim complaints, forced deadlines, money
  already spent on workarounds.
- **Deadline pressure** — is there a date? How near, how real, verified
  against what primary source?
- **Willingness to pay** — who holds budget, at what price point, proven
  by whom already charging.
- **Competition** — who's there; which lane (price tier, segment,
  channel) is genuinely open.
- **Route to buyer** — reachable with the operator's actual GTM
  abilities? This criterion may VETO.
- **Conflict check** — hard-exclusion overlap. Binary.
- **Portfolio synergy** — extends an existing product/buyer/tech vs
  opens a new front.

Score 1–5 each in dossiers. Alongside the rubric, every candidate gets a
**power-path score** (0–3) from Phase 3b; it gates verdicts and ranks
before EV. Do not use build size as a filter: with agent-built software,
"too big to build" is rarely true for an experienced operator. Filter on
power, distribution and running costs instead. Record any veto rules ("route-to-buyer < 3
kills regardless of total").

## Output

Write `SCOPE.md` from `assets/scope-template.md`, confirm it with the
user, and treat it as standing instructions. Revisit only when the
operator's situation changes — but re-read it at the start of every
mining pass, because candidates that ignore scope waste everyone's time.
