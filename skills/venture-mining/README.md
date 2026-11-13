# Venture Mining

A Claude skill for finding product ideas people will actually pay for, and for killing the ones they won't, before you've spent a single build session on them.

Ideas are worthless. Validated demand with a buyer you can reach is the product. Everything in this skill follows from that.

It's deliberately adversarial. Most candidates die, and that's the point: a candidate killed by an afternoon of desk research cost you nothing. The few that survive come out with a signed contract (kill criteria with numbers and dates) written BEFORE anyone builds anything.

Built by [Fortitude Omnis Group](https://github.com/Fortitude-Group) for our own product pipeline. It's generic enough for any solo founder or small team once you've written a scope file.

## Why this exists

Agent-built software has made code cheap. One experienced engineer with AI agents can now rebuild something Miro-sized, so "is this too big to build?" has stopped being a useful question. The questions that matter now are:

- Is anyone already spending money on this pain?
- Can *you* reach those buyers, with the sales channels you actually have?
- Once a funded rival copies your code in 30 days (they will), what do you still have that they don't?

Most idea-validation advice skips the second and third questions. This skill doesn't.

## What it does

Ask Claude to find ideas, check an idea, or decide whether to build something, and the skill runs a six-phase pipeline (plus a moat check):

| Phase | Name | What happens | What usually dies here |
|---|---|---|---|
| 0 | **Scope** | A short interview about you: skills, exclusions, the sales channels you can and can't use, your current products. Written once to `SCOPE.md` and reused. | Nothing. But nothing gets mined without it. |
| 1 | **Mine** | Sweep a territory for candidates. Every claim gets checked against a primary source, with a date. | Most candidates |
| 2 | **Drill** | Mine the incumbents' 1 to 3 star reviews and sort every complaint into *structural* (a real opening) or *fixable* (they'll patch it in a sprint). | Anything without a structural opening |
| 3 | **Pressure** | Ten named attacks against the idea, each answered in writing with evidence, or conceded. | Some survivors, often favourites |
| 3b | **Powers** | Hamilton Helmer's 7 Powers check. Is there a durable advantage that isn't the code? Includes a "clone attack". | Anything with no power at 24 months |
| 4 | **Contract** | A verdict, an expected-value block, and kill criteria with numbers and dates, before any build. | Anything whose numbers don't add up |
| 5 | **Handoff** | Spec-ready briefs you can paste straight into GitHub spec-kit (`/speckit.specify`). | Nothing. You've earned it by now. |

Every candidate ends with exactly one verdict:

- **EXTEND**: build it as part of something you already sell (same buyer or same tech). Extensions beat new apps nearly every time.
- **TIER-0**: demand test only. A landing page, a lead magnet and card-verified pre-orders, with hard caps on build sessions and spend. Nothing behind the paywall gets built.
- **PARK**: not now, with a written revive trigger and a re-check date. A park without a trigger is a slow kill pretending otherwise.
- **KILL**: permanent, with the cause of death and a salvage clause saying what research or assets carry over.

## Install

### Claude Code

Copy the skill folder into your personal skills directory:

```bash
git clone https://github.com/Fortitude-Group/skills.git
cp -r skills/skills/venture-mining ~/.claude/skills/
```

On Windows (PowerShell):

```powershell
git clone https://github.com/Fortitude-Group/skills.git
Copy-Item -Recurse skills\skills\venture-mining "$env:USERPROFILE\.claude\skills\"
```

To share it with everyone working on one repo, put it in that project's `.claude/skills/` folder instead. Claude Code picks it up next session.

### Claude.ai and the desktop app

Zip the `venture-mining` folder (the zip should contain the folder, with `SKILL.md` inside it), then upload it under **Settings → Capabilities → Skills**.

### Check it's working

Ask *"Set up a venture-mining scope for me."* If Claude starts interviewing you about your exclusions and sales channels, you're in.

## How to use it

You don't need to name the skill. It triggers on things like "find me an idea", "is this worth building?", "pressure-test this" or "does this have a moat?". These prompts work well:

### First session: write your scope

> Set up a venture-mining scope for me.

Claude asks only what it doesn't already know: solo or team, your stack, whether building or selling is your real bottleneck (for most AI-assisted solo builders it's selling), what's off-limits (employer conflicts, sales motions you won't do, markets that need an accreditation you can't get), and what you already run. The result is `SCOPE.md`. Keep it in the project. It also holds your shortlist, your graveyard of kills and a calibration log, so later sessions start where the last one stopped.

### Find candidates

> Run a mining pass on UK regulatory deadlines 2026 to 2028.

> Run a mining pass. Non-legislative pain only: platform shocks and incumbents going downhill.

> Mine outward from my unfair advantages.

> Mine the Bending Spoons portfolio.

There are four mining methods, and Claude tells you which one it's running:

1. **Deadline-driven demand.** Regulations, end-of-life dates and pricing cliffs that *force* people to spend by a date. The deadline does the selling, which is lovely if marketing isn't your strong suit. The highest hit rate of the four.
2. **Complaint mining.** Bad reviews of the top incumbents, forum threads asking "why is there no tool that…", and recurring paid gigs on Upwork and Fiverr (a recurring paid gig is pre-SaaS demand).
3. **Boring vertical SaaS.** Niche industries with money and 2005-era software. Heads up: AI-assisted micro-SaaS founders have colonised this territory since about 2023, so the competitor search happens during the pass, not afterwards.
4. **Platform shocks and incumbent decay.** Pricing revolts, licence changes, acquisitions followed by neglect, API shutdowns. This includes a *portfolio-acquirer sweep*: serial acquirers follow a predictable sequence (deal, layoffs within weeks, repricing 3 to 12 months later, usage pricing at the second renewal), so you can place each product on that timeline and look for windows that are opening, not ones the last exodus already closed.

A pass ends with a ranked list. Every entry has evidence attached, an honest note on the attack Claude can already see coming, a provisional moat score and a provisional verdict. Kills are reported with their cause of death, because kills are deliverables too.

### Go deep on one

> Drill [candidate].

> Do the full treatment on [candidate].

Got your own idea? Say so. It enters at the drill and gets no special treatment for being yours.

### Argue against it

> Run the adversarial pass on [candidate].

The ten attacks: the deadline slips, the first panic wave already happened (and the incumbents absorbed it), a free official tool already does it, the incumbents are loved, every adviser in the country is already blogging about it, it's a feature not a company, it needs a sales motion you can't do, it depends on scraping (a treadmill, not a moat), revenue falls off a cliff after the deadline, and a key input is controlled by someone else. If that last one lands, the candidate gets a **gate zero**: desk research with a deadline that has to pass before any build at all.

### Check the moat

> Run the 7 Powers check on [candidate].

> Does [candidate] have a moat?

Each of the seven powers (scale economies, network economies, counter-positioning, switching costs, branding, cornered resource, process power) gets scored 0 to 3 for benefit and for barrier, at day 1, 24 months and 5 years. Then come three more checks:

- **Code share:** how much of the value a clone gets for free. Over about 50% is the honest weak spot, and yes, your clever rendering engine counts as code here.
- **The clone attack:** a funded rival with AI agents, £500k and 30 days. What do they get? What don't they get? What's the cheapest move that removes your reason to exist?
- **The incumbent, power view:** is the incumbent stopped by what it *can* do, or by its business model? Only the second one helps you.

The output is a **power-path score** (0 to 3), and it gates everything. 0 never earns a standalone build. 1 caps the verdict at TIER-0 and makes a dated power checkpoint mandatory. 2 and 3 follow the normal rules.

### Sign the contract

> Write the kill criteria for [candidate].

> Show me the portfolio table.

Anything getting effort gets a contract: the hypothesis to falsify, a build cap (2 sessions by default), a spend cap, a live-by date, checkpoints where ALL the numeric gates have to pass, and what happens on pass and on fail. Card-verified pre-orders are the only willingness-to-pay evidence that counts. Email signups are sentiment. Cards are money.

Every verdict also carries an **EV block**, and every percentage names the assumption behind it:

- P(validation): anchored to a 20 to 40% base rate for cold landing-page tests
- P(traction, given validation): capped at 25% unless you can name the channel that brings the first 100 paying customers
- Year-1 ARR target, with the customer-count arithmetic shown (never "1% of the market")
- **EV per build session**, which is how the portfolio gets ranked once the power-path score has done its job

When a test resolves, tell Claude. Predicted versus actual goes into the calibration log in `SCOPE.md`, and the next set of guesses gets better.

### Hand it to a build

> Generate the brainstorm briefs for everything with a build or test verdict.

One brief per workstream, written to paste straight into `/speckit.specify`. A TIER-0 brief describes a *test site*, never the product. Its out-of-scope section exists to stop build excitement sneaking features into a validation page. Keep the dossier in the same folder. Three weeks into a build it's the note that says why this exists and when to kill it.

## The iron rules

These apply in every phase. Each one came from a real mistake in a real mining session.

1. **Primary sources, with dates.** Regulator text and vendors' own pricing pages, never a blog summary.
2. **Re-verify at every phase boundary.** The most expensive miss this process ever caught was a flagship deadline that quietly slipped a year between two passes.
3. **No evidence, no candidate.** Enthusiasm isn't evidence.
4. **A lane isn't empty until you've searched it three ways.** Every "empty" lane so far turned out to have incumbents.
5. **Free official tools are real competitors.** For anything compliance-shaped, the regulator's free toolkit is usually the actual incumbent.
6. **Kill criteria before build, with numbers and dates.**
7. **Kills are permanent and cheap. Celebrate them.**
8. **One flagship at a time.** New candidates compete for build effort, never for the flagship's go-to-market slot.
9. **Weight route-to-buyer by what you can actually do.** It can veto an otherwise perfect idea.
10. **Honesty over momentum.** When the evidence kills a favourite, say so first and show the source.
11. **Quantify it or it didn't happen.** Every verdict carries an EV block.
12. **Power that isn't the code.** Build size isn't a filter. Power, distribution and running costs are.
13. **Grade every fact's evidence.** A is primary, B is reputable press, C is user or competitor content (directional only), D is inference and gets labelled as such.

## What you get out of it

All of these are files, so they last longer than the conversation:

- **`SCOPE.md`**: who you are, what's off-limits, the scoring rubric, your shortlist, your calibration log and the graveyard.
- **One dossier per candidate**: verified facts with sources and dates, verbatim pain quotes, the competitor scan and search log, the adversarial pass, the 7 Powers report, rubric scores, the EV block, the verdict and the contract. It's updated in place as the candidate moves through the phases, never forked.
- **Brainstorm briefs**: spec-kit ready, one folder per workstream.
- **A status board** at the end of every session: candidates by phase, upcoming checkpoint dates and the single next action.

## What's in the folder

```
venture-mining/
  SKILL.md                         The orchestrator: phases, where to start, the 13 iron rules
  references/
    phase-0-scope.md               Operator interview and rubric setup
    phase-1-mine.md                The four mining methods and search discipline
    phase-2-drill.md               Complaint mining, structural versus fixable
    phase-3-pressure.md            The ten attacks, gate zero, instant-kill triggers
    phase-3b-powers.md             7 Powers scoring, code share, the clone attack
    phase-4-contract.md            Verdicts, kill criteria, the EV block
    phase-5-handoff.md             Spec-ready briefs
  assets/
    scope-template.md              SCOPE.md template
    dossier-template.md            One-per-candidate dossier
    tier0-brainstorm-template.md   Spec-kit brief
```

Claude reads `SKILL.md` first and only opens a phase's reference file when it gets to that phase, so the skill stays light on context.

## Things to know

- **It searches the web a lot.** A mining pass typically spends 6 to 10 searches, and every phase boundary re-checks the facts it depends on. It works best with web search switched on.
- **It's UK-leaning in its examples** (pounds, UK regulators). The method works anywhere. Point it at your own jurisdiction in the scope file.
- **The percentages are priors, not measurements.** They're there to make the reasoning visible and arguable. If a number turns up without its assumption, ask for it.
- **Expect it to kill things you like.** That's the job, and it's a lot cheaper here than after three build sessions.

## Credits

The power check in Phase 3b is built on Hamilton Helmer's *7 Powers: The Foundations of Business Strategy* (2016). Read the book. The skill's version is a scoring shortcut, not a substitute.

## Contributing

Found a rule that should be an iron rule? Lost money to an attack the pressure phase doesn't run? Open an issue or a pull request. The skill is basically a calibration log in its own right, and lessons from live sessions belong in it.
