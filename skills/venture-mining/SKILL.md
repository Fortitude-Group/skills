---
name: venture-mining
description: A rigorous, evidence-first process for sourcing, validating, and killing product/business ideas — finding pain points people already pay to solve, verifying them against primary sources, pressure-testing them adversarially, checking for durable power beyond the code (Hamilton Helmer's 7 Powers), and producing kill criteria and spec-ready briefs. Use this skill whenever the user wants to find app/SaaS/product ideas, validate or "pressure test" a business idea, mine pain points or regulatory deadlines for opportunities, decide whether to build or kill an idea, write kill criteria or a candidate dossier, run a "mining pass" or "drill", mine an acquirer's portfolio (e.g. Bending Spoons) for products to attack, run a 7 Powers or moat check, or asks anything like "help me find something people will pay for", "is this idea worth building", or "find underserved markets". Trigger even if they just describe a vague idea and ask what you think of it commercially.
---

# Venture Mining

A six-phase pipeline (plus the Phase 3b power check) that turns "help me find an idea" into evidence-backed
build/kill decisions. Its core belief: **ideas are worthless; validated
demand with reachable buyers is the product.** The process is deliberately
adversarial — its job is to kill candidates cheaply before they consume
build effort, and to produce a signed contract (kill criteria) for the few
that survive.

## The six phases

```
0. SCOPE     — who is the operator, what's excluded, what does "good" score
1. MINE      — sweep a territory for candidates; verify against primary sources
2. DRILL     — per candidate: complaint-mine the incumbents, find the wedge
3. PRESSURE  — adversarial pass: argue against it properly, re-verify, gate
3b. POWERS   — 7 Powers verification: durable power that isn't the code? clone attack
4. CONTRACT  — write kill criteria (numbers + dates) BEFORE any build; dossier
5. HANDOFF   — spec-ready brainstorm brief for whatever earned a build/test
```

Phases run in order per candidate, but a session may hold candidates at
different phases. A candidate may die in any phase; most should. Read the
matching reference file when you enter a phase:

- `references/phase-0-scope.md` — operator profile interview + rubric setup
- `references/phase-1-mine.md` — mining methods, search discipline, verification rules
- `references/phase-2-drill.md` — incumbent complaint-mining, structural vs fixable
- `references/phase-3-pressure.md` — adversarial playbook, gate zero, instant-kill triggers
- `references/phase-3b-powers.md` — 7 Powers scoring, code share, clone attack, power-path gating
- `references/phase-4-contract.md` — kill-criteria design, dossiers, verdict vocabulary
- `references/phase-5-handoff.md` — Tier-0 test briefs and spec-kit handoff

Templates to copy, not improvise: `assets/scope-template.md`,
`assets/dossier-template.md`, `assets/tier0-brainstorm-template.md`.

## Where to start

- **No scope file exists in the project/conversation** → Phase 0. Do not
  mine without a scope; unscoped mining produces unusable candidates.
- **User says "find me ideas" / "run a mining pass"** → Phase 1, using the
  existing scope.
- **User brings their own idea** → treat it as a candidate entering Phase 2;
  it gets no exemption from drilling and pressure just because it's theirs.
- **User says "go deeper on X" / "drill X"** → Phase 2 → 3 → 3b → 4 for X.
- **User asks "does X have a moat?" / "7 Powers check"** → Phase 3b for X
  (run Phase 3 first if it hasn't had one).
- **User names an acquirer or portfolio to attack** (e.g. "mine Bending
  Spoons") → Phase 1, method 4 (portfolio-acquirer sweep).
- **A candidate has a TIER-0 or BUILD verdict** → Phase 5.

## Iron rules (apply in every phase)

1. **Primary sources, with dates.** Every deadline, regulation, pricing
   claim, and market fact is verified by search against the most primary
   source available (regulator text, gov announcement, vendor's own
   pricing page — never a blog summary). Record the source date.
   Distinguish "X committed to Y" from "Y is mandated for everyone".
2. **Re-verify at every phase boundary.** A fact verified during MINE can
   die before DRILL — governments delay, competitors launch. The most
   expensive failure mode this process has caught was a flagship deadline
   quietly slipping a year between passes. Never carry a date forward
   unchecked.
3. **No evidence = no candidate.** Verbatim complaints, money already
   spent on workarounds, or a forced deadline. Enthusiasm is not evidence.
4. **A lane is not empty until searched three ways.** Before declaring
   "no one serves this", run at least three differently-phrased competitor
   searches. Every "empty" lane this process has assumed turned out to
   have incumbents.
5. **Free official tools are real competitors.** For compliance-shaped
   products, the regulator's free guidance/toolkit is usually the true
   incumbent. Name it and test against it explicitly.
6. **Kill criteria are written before build, with numbers and dates.**
   No candidate gets build effort without a signed contract specifying
   exactly what signal, by when, or it dies. Verdicts use a fixed
   vocabulary: **EXTEND / TIER-0 / PARK (with revive trigger) / KILL.**
7. **Kills are permanent and cheap; celebrate them.** A candidate killed
   by desk research cost nothing. Frame kills as process victories, write
   a salvage clause (what research/assets transfer elsewhere), and never
   resurrect without the written revive trigger firing.
8. **One flagship at a time.** Whatever currently holds the user's
   go-to-market focus keeps it; new candidates compete for build effort,
   never for the flagship slot. Failed tests return their budget to the
   flagship by default.
9. **Weight route-to-buyer by the operator's actual GTM ability.** The
   scope file says what sales motions the operator can and cannot do.
   Route-to-buyer can veto an otherwise perfect candidate.
10. **Honesty over momentum.** When the evidence kills the user's
    favourite candidate — or one this process previously endorsed — say
    so plainly, lead with it, and show the primary source. The previous
    pass being wrong is the process working, not failing.
11. **Quantify or it didn't happen.** Every candidate that reaches a
    verdict carries an EV block: P(validation), P(GTM traction |
    validated), combined P(revenue), a Year-1 ARR target with the
    customer-count arithmetic shown, expected Year-1 ARR, and EV per
    build session. These are stated priors, not measurements — every %
    must name the assumption behind it, and priors are updated in
    writing at every checkpoint. Candidates are RANKED by power-path
    score first (Rule 12), then by EV per build session, not by
    excitement or rubric total. A calibration log of
    predicted-vs-actual lives in the scope file so priors improve with
    every resolved test. See phase-4 for how to set the numbers.
12. **Power that isn't the code.** Agent-built software makes code cheap,
    so build size is not a filter (a Miro-scale rebuild is feasible for
    one experienced engineer) and code is not a moat. What filters is the
    7 Powers test, distribution and running costs. Every candidate that
    survives Phase 3 gets a Phase 3b report with a power-path score
    (primary power at 24 months, 0–3). Power-path 0 never earns a
    standalone build; power-path 1 makes the power checkpoint mandatory
    in the contract.
13. **Grade every fact's evidence class.** A = primary (filings, official
    statements, regulator text); B = reputable press; C = user or
    competitor content (paraphrase, directional only); D = inference,
    labelled as such. Competitor blogs about an incumbent's decline are
    class C and biased; owner claims ("user base stable") are unverified
    until filings back them. Where the case rests on class C, the Tier-0
    test must generate first-hand evidence before any build.

## Output discipline

- One dossier per candidate (template in assets), updated as it moves
  through phases — never a new document per phase.
- Mining passes end with a ranked candidate list, each with a one-line
  verdict, its power-path score and the evidence class behind it.
- Look for clusters: candidates that share a buyer, a sales motion or a
  technical core are one bet, not several. Say so, and sequence them so
  shared work (e.g. migration tooling, a venue list) is built once.
- Every session ends with a status board: candidates by phase, upcoming
  checkpoint dates, and the single next concrete action.
- Files are the deliverable for dossiers and briefs; conversation is for
  verdicts and reasoning.

## Tone

Direct, evidence-led, unsentimental about ideas, respectful of the
operator's constraints. Scores and verdicts are argued, not asserted.
When the honest answer is "this pass found nothing", say that — and say
what the failure teaches about where to mine next.
