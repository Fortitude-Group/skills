# Phase 4 — CONTRACT (Kill Criteria, Dossier, Verdict)

Purpose: convert a surviving candidate into a signed contract: rubric
scores, a verdict from the fixed vocabulary, and — for anything getting
effort — kill criteria with numbers and dates written BEFORE any build.

## Verdict vocabulary (use exactly these)

- **EXTEND** — build as an extension of an existing product (same buyer
  and/or shared tech). Extensions beat new apps; they inherit the
  existing product's GTM. Requires a build scope, not a demand test,
  when the buyer is already proven.
- **TIER-0** — demand test only. A validation build (landing page, lead
  magnet, card-verified pre-orders) with hard caps and kill criteria.
  Nothing behind the paywall gets built.
- **PARK** — not now, with a *written revive trigger* (specific,
  checkable events + a re-check date). Parks without triggers are slow
  kills pretending otherwise; give them triggers or kill them.
- **KILL** — permanent, with cause of death and a salvage clause (what
  research, assets, or audience transfers to the portfolio). Killed
  candidates are only revivable if a written revive path existed at
  kill time.

## Power-path gating (from Phase 3b)

Apply before choosing the verdict:
- **Power-path 0** — no standalone build. At most TIER-0, and only if the
  test is nearly free; usually KILL, or EXTEND as a feature or revenue
  line inside a sibling candidate that has power (e.g. a paid-events
  layer folded into a community product).
- **Power-path 1** — TIER-0 at most, with the Phase 3b **power
  checkpoint** written into the contract as a mandatory gate. Missing it
  is a kill.
- **Power-path 2–3** — normal verdict rules.

Ranking across the board: power-path score first, then EV per build
session, then time-to-first-revenue. Where a ranking breaks a tie on
operator fit or proven willingness to pay, say so.

## Designing Tier-0 kill criteria

Structure every test contract with ALL of:
- **Hypothesis to falsify** — one sentence, naming the buyer, the price,
  and the discovery channel.
- **Build cap** — max build sessions (default 2) and spend cap (default
  small, e.g. £300). The cap IS the point: the test's cost is the price
  of the answer.
- **Timing** — live-by date chosen against a real attention moment
  (guidance publication, enforcement date, news cycle) when one exists;
  test window end date.
- **Checkpoints** — at least one mid-point and one final, each with ALL-
  required numeric gates. Typical gate set: organic impressions/month
  (proves the searches exist), lead-magnet completions, card-verified
  pre-orders (the only WTP evidence that counts — email signups are
  sentiment, cards are money), visitor→pre-order conversion %, and at
  least one **segmentation gate** proving the *paying* segment converted
  (e.g. "≥N pre-orders from commercial buyers, not hobbyists").
- **Calibration** — set the conversion bar higher when the audience is
  precise (weak conversion then means weak willingness-to-pay, not weak
  targeting) and set pre-order counts against the price point so the
  pass threshold represents real committed ARR.
- **Riskiest assumption first** — name the single assumption most likely
  to kill the candidate (venues will pay; teams will switch at renewal;
  organisers will move) and make the first gate test it before any
  product code.
- **Power checkpoint** — carried from Phase 3b (numeric, dated, e.g.
  month 9–18). Mandatory for power-path 1.
- **Instant-kill triggers** — carried forward from Phase 3, plus the
  Phase 3b power kill triggers.
- **Pass action** — what the candidate earns (build effort on normal
  terms; NEVER the flagship slot).
- **Fail action** — permanent kill + where the budget returns (default:
  the flagship) + the salvage clause.
- **Honest prior** — state your probability the test passes. Committing
  a number keeps everyone honest and calibrates future passes.

## Revenue quantification (the EV block)

Every verdict carries these numbers. They are subjective priors made
honest by showing their arithmetic and updating them at checkpoints.

- **P(validation)** — probability the Tier-0 test (or gate zero →
  test chain) passes its final criteria. Anchor it: base rate for
  cold-landing-page tests with card-verified pre-orders is roughly
  20–40%; adjust up for verified deadline pressure, proven paid
  workarounds, and a precise reachable audience; down for free official
  alternatives, loved incumbents, and unproven channels. For EXTEND
  verdicts on a proven buyer, P(validation) may be ~1 but say so.
- **P(GTM traction | validated)** — probability that, given a passed
  test and a shipped product, the operator reaches the Year-1 customer
  target through the named channel. This is where route-to-buyer
  reality bites: a passed test proves demand exists, not that THIS
  operator can harvest it. Require the **first-100-customers line**: one
  sentence naming the specific channel that produces the first hundred
  paying customers. No named channel → cap this probability at 25%.
- **P(revenue)** = P(validation) × P(GTM | validated). State it.
- **Year-1 ARR target** — price × customer count, with the count
  justified against channel maths (search volume, community size,
  pre-order run-rate ×12), never "1% of market".
- **Expected Year-1 ARR** = P(revenue) × ARR target.
- **EV per build session** = Expected Year-1 ARR ÷ total build sessions
  to launch (test + product v0). This is the ranking metric across the
  portfolio — it is how a small-but-nearly-certain extension beats a
  large-but-unlikely new front, and it makes "boil the ocean" answerable
  with arithmetic.
- **Revenue shape modifier** — classify stickiness: RECURRING-STICKY
  (obligation repeats: annual filings, ongoing compliance, per-release);
  RECURRING-SOFT (subscription but cancellable pain); ONE-OFF (deadline
  migration → revenue cliff). ONE-OFF shapes need either a follow-on
  product thesis or a discount to the ARR target; say which.
- **Time-to-first-revenue** — months until first paid invoice under the
  plan. Two candidates with equal EV are ranked by this.

**Update cadence:** re-state the EV block at every checkpoint and phase
boundary; when a test resolves, record predicted vs actual in the scope
file's calibration log and note what the miss teaches about future
priors.

## The dossier

One file per candidate for its whole life, from `assets/dossier-template.md`.
Update in place as phases complete; never fork per phase. Must contain:
verified facts table with source classes and dates; verbatim pain
evidence; competitor scan with search log; adversarial pass with every
attack and its outcome; the Phase 3b 7 Powers report; rubric score table with one-line justifications;
the verdict; the contract (if any); and the salvage/revive clauses.

## Portfolio bookkeeping

After each contract, restate the board: candidates by phase, every
checkpoint date in order, which product holds the flagship slot, and the
single next concrete action. Multiple live tests must not compete for the
same build window — sequence them explicitly.
