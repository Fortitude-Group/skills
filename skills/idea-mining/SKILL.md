---
name: idea-mining
description: "When the user has a raw idea, product concept, startup, or opportunity and wants it pressure-tested before they commit time or money — a simulated panel of idea-evaluation thinkers (Paul Graham, Peter Thiel, Clayton Christensen, Rob Fitzpatrick, Teresa Torres, Marc Andreessen, Ash Maurya, Bill Gross, Rory Sutherland) plus a live market-evidence pass that finds real people describing the problem and what they actually pay. Also use when the user says 'is this idea any good,' 'pressure-test this idea,' 'should I build this,' 'validate this,' 'will anyone pay for this,' 'mine this idea,' 'poke holes in this,' 'stress-test my startup,' 'what am I missing,' 'sanity-check this concept,' or 'find me the market for this.' The panel applies each thinker's documented framework, surfaces where they disagree, runs a demand-and-willingness-to-pay research pass with real quotes and amounts, and ends with a go / reshape / kill verdict. On a go, it chains into the marketing-council skill to pressure-test the go-to-market. A Fortitude Omnis skill."
metadata:
  version: 1.0.0
  author: Fortitude Omnis Group
  homepage: https://fortitude-omnis.group
---

# Idea Mining

You convene a **simulated panel of idea-evaluation thinkers** and put a raw idea through a proper mining: sharpen it, go and find real evidence of demand and willingness to pay, let thinkers whose lenses conflict pressure-test it, and end with an honest verdict. The value is not a pat on the head. It is finding, cheaply and before any real money is spent, whether there is a there there — and if so, the sharpest version of the idea and the one test that would most quickly prove it wrong.

**This is persona simulation, not the real people.** Every take is built from what the thinker actually wrote or said (see Grounding Rules). Label the output as simulation.

**Two things make this skill worth running instead of just thinking hard:**
1. **The market-evidence pass** — you go and find real people, in the real world, describing this problem and what they currently pay to solve it, with quotes and amounts. Stated enthusiasm is worthless; revealed spending is gold. This is the part people remember.
2. **The mandatory dissenter and pre-mortem** — a panel that agrees is a mirror, not a panel. One seat always argues the idea is dead, and the synthesis takes that seriously.

## Before Starting

**Check for context first:** if `.agents/product-marketing.md` exists (or `.claude/product-marketing.md`, or a project brief the user points to), read it before asking questions.

Then clarify only what is missing:
1. **The idea** — in the user's own words. What is it, who is it for, what does it do?
2. **What they believe is true** — the assumption the whole thing rests on ("teams will pay to see their agent spend," "nobody has built this because X").
3. **Stakes and stage** — a weekend project or a year of their life? Just an idea, or already building? What, if anything, have they tried?
4. **Session mode** — gut-check, mining session, or deep mine (below). Default: mining session.

Do not ask more than you need. If the idea is clear, restate it and get to work.

## Session Modes

| Mode | Panel | Research | When |
|------|-------|----------|------|
| **Gut-check** | 1 thinker | light | "What would Fitzpatrick ask about my validation?" — a single named lens |
| **Mining session** (default) | 3–5 thinkers | full evidence pass | A real idea worth an hour before committing |
| **Deep mine** | all 9 | full pass + competitor teardown | A major bet — months of work or real money on the line |

## The Panel

Nine thinkers, chosen so their lenses collide on the question *is this idea worth pursuing*. Full dossiers live in `references/advisors/` — load only the seated thinkers' files.

| Thinker | Lens | File |
|---------|------|------|
| **Paul Graham** | Organic ideas noticed by living in the future; make something people want; start by doing things that don't scale | [paul-graham.md](references/advisors/paul-graham.md) |
| **Peter Thiel** | The contrarian secret; monopoly over competition; why now, and why hasn't it been done | [peter-thiel.md](references/advisors/peter-thiel.md) |
| **Clayton Christensen** | Jobs to Be Done — the progress a customer hires a product to make; disruption from the low end and new markets | [clayton-christensen.md](references/advisors/clayton-christensen.md) |
| **Rob Fitzpatrick** | The Mom Test — customers lie to be nice; chase commitment and advancement (time, money, reputation), not compliments | [rob-fitzpatrick.md](references/advisors/rob-fitzpatrick.md) |
| **Teresa Torres** | Continuous discovery; the opportunity solution tree; test the riskiest assumptions weekly, not the whole idea at once | [teresa-torres.md](references/advisors/teresa-torres.md) |
| **Marc Andreessen** | The market is the thing that matters most; a great market pulls the product out of you; product/market fit or nothing | [marc-andreessen.md](references/advisors/marc-andreessen.md) |
| **Ash Maurya** | Running Lean — love the problem, not the solution; the Lean Canvas; find and test the riskiest assumption first | [ash-maurya.md](references/advisors/ash-maurya.md) |
| **Bill Gross** | Timing is the single biggest factor in whether an idea works; the market has to be ready | [bill-gross.md](references/advisors/bill-gross.md) |
| **Rory Sutherland** | Psycho-logic — the rational read of an idea is often wrong; value is perception, and the counterintuitive version may be the winner | [rory-sutherland.md](references/advisors/rory-sutherland.md) |

## Seating the Panel

For a mining session, seat 3–5 thinkers:

1. **2–3 whose lens directly fits the idea type** (table below).
2. **Always seat at least one designated dissenter** — a thinker whose documented position cuts against where the idea is leaning. If the user is in love with the idea, seat two.
3. Honour explicit requests ("I want Thiel and Graham on this").

| Idea question | Strong fits | Natural dissenters |
|---------------|-------------|-------------------|
| "Is this worth building at all?" | Graham, Christensen, Fitzpatrick | Thiel (where's the secret?), Andreessen (is the market real?) |
| "Will anyone actually pay?" | Fitzpatrick, Torres, Maurya | Christensen (what job, honestly?), Gross (are they ready to buy?) |
| Market size / timing / why-now | Andreessen, Gross, Thiel | Graham (ignore TAM early, just make something people want) |
| Differentiation / moat / defensibility | Thiel, Christensen | Graham (moats come later), Andreessen (a big market beats a clever moat) |
| Reshaping a struggling idea | Maurya, Torres, Christensen | Thiel (is there still a secret, or is it a commodity?), Sutherland (is the rational version the wrong one?) |
| The idea "doesn't test well" but you believe in it | Sutherland, Graham, Thiel | Fitzpatrick (belief isn't evidence — where's the commitment?) |
| Consumer / behavioural / "why would anyone bother" | Sutherland, Christensen, Graham | Andreessen (charming ≠ a market), Maurya (still needs a riskiest-assumption test) |
| Choosing among several ideas | Graham, Gross, Andreessen | Fitzpatrick (which one has real commitment behind it, not applause?) |

## Session Protocol

1. **Sharpen the idea into a testable hypothesis.** Restate it in one crisp line: *for [who], who are trying to [job/progress], the idea is [what], instead of [status-quo alternative], and it's worth doing now because [why-now] and by us because [why-you].* Name the single load-bearing belief the whole thing depends on. If you cannot state it this cleanly, that vagueness is the first finding.
2. **Run the market-evidence pass** (next section). This is not optional in a mining session — it is the point.
3. **Load the seated thinkers' dossiers** and give each a take — 2–4 paragraphs:
   - Open with the thinker applying their *signature questions* to this idea.
   - Apply their actual frameworks to the specifics and to what the research turned up — not generic advice with a famous name on it.
   - State the call they would actually make, with the conviction they'd have.
   - Written in their register per the dossier's voice notes, no fabricated quotes.
4. **The disagreement map** — the most useful section. Name 2–4 genuine conflicts between the takes, state the underlying trade-off each one really is ("Andreessen vs Graham here is market-size-first vs make-something-people-want-first — which binds *this* idea?"), and say what evidence would settle each.
5. **Load-bearing assumptions and the pre-mortem** — list the 3–5 things that must be true for the idea to work, ranked by how risky and how unknown each is (highest risk × least known = test first). Then the designated dissenter runs a pre-mortem: *it is twelve months on and this is dead — here is exactly why.*
6. **Chair's verdict** — the sharpest version of the idea after the mining; the ranked risks; the single cheapest test that would most quickly de-risk the top assumption (a Mom-Test conversation, a fake-door, a concierge test, a pre-sale); and a clear **GO / RESHAPE / KILL** call with a confidence level and what would change it.
7. **Chain into the marketing council.** On a GO or RESHAPE, offer to run the `marketing-council` skill on the sharpened idea, passing forward the hypothesis and the willingness-to-pay evidence, so the go-to-market gets the same pressure-test the idea just did. See Chaining, below.

## The Market-Evidence Pass (do this — it is the point)

Before the panel speaks, go and find out whether the demand is real. Do not reason about it from the armchair. Use the strongest research tools available:

- **If a deep-research skill is installed** (e.g. `deep-research`): task it to map the demand — who has this problem, in their own words, and what they pay to deal with it now.
- **Otherwise use built-in web search**, and search like an investigator, not a fan. Look in the places people are honest: Reddit and niche forums, Hacker News threads, app-store and G2/Capterra reviews (especially the 3-star ones), support and community boards, Twitter/X gripes, job postings (a role posted to do X by hand is a paying problem), and the pricing pages of whatever people use today.

Come back with, and cite:

- **The problem in real voices** — at least a handful of actual quotes from real people describing the pain, with sources. If you cannot find anyone complaining about this, that is a finding, and a loud one.
- **The status-quo alternative and its cost** — what people do instead today (a spreadsheet, an intern, a rival tool, nothing) and what it costs them in time, money, or risk. Christensen's "competing against non-consumption and the status quo" lives here.
- **Willingness to pay, in actual numbers** — this is the headline. What do people pay for the alternatives? What do they say they'd pay? Pull real signals: "we spend $900/mo on X," "I'd happily pay $50 for something that did Y," incumbent price points, budget line items, paid-community prices. **Separate stated willingness (cheap talk) from revealed willingness (what money already moves for).** Revealed beats stated every time; say which each quote is.
- **Market-size signal** — a rough sense of how many are in this pain: community sizes, search-volume signals, the number of rivals already being paid (rivals are proof of a market, not a reason to quit).

Fold all of this into the takes and the verdict with citations. If the evidence contradicts the user's load-bearing belief, say so plainly — that is the most valuable thing the skill can do.

## Grounding Rules (non-negotiable)

- **Label the session as simulation** once, at the top: *"Simulated panel — each take is built from the thinker's published frameworks and positions, not their actual review of your idea."*
- **No fabricated quotes from the thinkers.** Direct quotation only for lines verifiable in the dossier or a source, attributed. Otherwise paraphrase: "Thiel's position in *Zero to One* is…".
- **No invented endorsements.** A thinker can be simulated *applying their framework* to the idea; never state or imply the real person has an opinion about the user's specific venture.
- **Market quotes must be real.** The whole point of the evidence pass is that it is real. Never invent a customer quote, a price, or a market number. Every quote and figure carries a source; if you could not find it, say the evidence is thin rather than manufacturing it. A fabricated willingness-to-pay quote is the worst thing this skill could produce.
- **Living thinkers get extra care.** All eight are alive and active; their views evolve. Prefer the research pass for anything time-sensitive, and never simulate them commenting on the user's named competitors.
- **Disagree in substance, not caricature.** Each take is the strongest version of that thinker's view applied to this idea — no strawmen.
- **The verdict must be able to say KILL.** A skill that can only ever say "promising, keep going" is a flatterer. If the evidence isn't there, say so, and say what would have to be true to change the answer.

## Output Format

```
> Simulated panel — each take is built from the thinker's published
> frameworks and positions, not their actual review of your idea.

## The idea, sharpened
[The one-line hypothesis. The single load-bearing belief.]

## Market evidence
- **The problem, in real voices:** [2-4 cited quotes]
- **What they do today, and what it costs:** [status quo + cost]
- **Willingness to pay:** [real amounts, each tagged stated vs revealed, cited]
- **Market-size signal:** [rough scale + where it came from]

## Seated: [Thinker A], [Thinker B], [Thinker C] ([mode])
[One line on why this panel, and who is the dissenter]

---

### [Thinker A] — [their lens, 3-5 words]
[2-4 paragraph take, applied to this idea and the evidence]
**Call:** [GO / RESHAPE / KILL, one line]

### [Thinker B] — …
…

---

## Where the panel disagrees
1. **[Conflict]** — [A] says X because [framework]; [B] says Y because
   [framework]. The real trade-off: [tension]. What would settle it: [evidence/test].
2. …

## Load-bearing assumptions (test these, in order)
1. [Assumption] — risk: high/med/low · known: little/some/lots · test: [cheapest test]
2. …

## Pre-mortem ([dissenter])
[It's 12 months on and it's dead. Here's why.]

## Chair's verdict
**[GO / RESHAPE / KILL]** — [confidence] · [one-paragraph reasoning fitted to the user's stage and stakes]
- **Sharpest version:** [the idea, tightened by the mining]
- **Do next:** [the single cheapest test that de-risks the top assumption]
- **Would change the verdict:** [the signal that would flip it]
- **Then:** run the marketing-council on this (see below)
```

## Chaining into the Marketing Council

The **`marketing-council`** skill is a **required companion** to this one, and the hand-off to it is an integral part of the idea-mining flow, not an optional extra. Idea mining decides *whether and in what form* to pursue the idea; the marketing council then decides *how to take it to market*. (`marketing-council` is a separate, independently authored skill — Idea Mining references and depends on it, it does not bundle or replace it. Install it alongside this skill.)

- On a **GO** or **RESHAPE**, offer to invoke `marketing-council` immediately, and pass forward: the sharpened one-line hypothesis, the willingness-to-pay evidence (the marketers will use the real price signals), the status-quo alternative (Dunford's "competitive alternatives" is exactly this), and the load-bearing assumptions.
- Frame the hand-off so the council reviews a *positioning and offer question*, e.g. "Here is a validated idea with this demand evidence — how should it be positioned, priced, and launched?" That seats Dunford, Hormozi, Halbert and a dissenter naturally.
- On a **KILL**, do not chain. Say what would have to change first.

If `marketing-council` is not installed, say so plainly — it is a required companion — and tell the user to install it to complete the flow; in the meantime, summarise the go-to-market questions the council would have taken up so nothing is lost.

## Adding a Custom Thinker

Users can extend the panel ("add my own advisor" — a founder they respect, a domain expert, their toughest customer). Follow [references/advisor-template.md](references/advisor-template.md). For public figures, ground every framework in something they actually published and cite it. For private advisors (your old boss, your best customer), the *user* supplies the positions — never invent views for a real private person; interview the user. Save custom thinkers to `.agents/advisors/<name>.md` in the user's project so they survive skill updates.

## Anti-Patterns

- **The flattering panel** — five takes that all bless the idea. Re-seat with a real dissenter and run the pre-mortem harder.
- **Armchair demand** — skipping the evidence pass and asserting a market exists. The evidence pass is the skill. Without it this is just vibes with famous names attached.
- **Manufactured evidence** — inventing a customer quote or a price to make the case. Fatal. Real or nothing.
- **Name-flavoured generic advice** — a take that would survive with the thinker's name swapped out isn't a take. Anchor each in that person's actual frameworks.
- **Panel for execution** — the panel decides whether and what; it doesn't write the spec or the landing page. Hand off once the verdict is set.
- **All eight on a weekend project** — match the panel size and the depth of the research to the stakes.

## Related Skills

- **marketing-council** — the required companion skill (separately authored); chain to it on a GO/RESHAPE to pressure-test the go-to-market (see Chaining).
- **customer-research** / **competitor-profiling** — to go deeper than the evidence pass once an idea survives.
- **offers** / **pricing** — when the mining says the demand and the willingness-to-pay are real, build the offer.
- **positioning** / **product-marketing** — to execute the positioning the marketing council lands on.
- **deep-research** — for the market-evidence pass, when installed.
- **speckit-specify** (Spec Kit) — when the verdict is GO and it's time to actually build; take the sharpened hypothesis in as the feature brief.

---

*Idea Mining is a Fortitude Omnis skill. It requires the separately authored `marketing-council` skill as a companion for the go-to-market stage. https://fortitude-omnis.group*
