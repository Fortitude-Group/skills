# Idea Mining

**A Claude skill that pressure-tests a raw idea before you spend a month of your life on it.**

It sharpens the idea into one testable line, goes and finds real people describing the problem and what they actually pay to solve it, puts the idea in front of a panel of nine thinkers whose views genuinely clash, and gives you a straight **go, reshape, or kill** with the evidence behind it.

It is the front door. Once an idea survives the mining, it hands straight over to the **Marketing Council** skill, which pressure-tests how you take it to market. That hand-off is built in and integral, so Marketing Council is a required companion. It is a separate, independently authored skill that you install alongside this one. Idea Mining references it and depends on it, it does not bundle or replace it.

Idea Mining is a Fortitude Omnis skill.

---

## Why it exists

Most idea validation is a comfort blanket. You describe your idea, a few friends say "oh nice," and you take that as a green light. It isn't one. People are polite, and polite is not the same as paying.

This skill does two things that thinking hard on your own cannot.

**It finds real evidence of demand.** Before anyone on the panel says a word, it searches the places people are honest, the Reddit threads and the three-star reviews and the pricing pages and the job ads, and it comes back with actual quotes and actual numbers. What do people pay for the thing they use today? What have they said, in writing, that they would pay? It keeps stated willingness to pay ("I'd totally buy that") apart from revealed willingness to pay (money that already moves), because only one of those is worth anything. If it cannot find a single person complaining about the problem, that is a finding, and a loud one.

**It argues with you.** One seat on the panel always takes the other side, and every session runs a pre-mortem where that seat tells you the idea is dead a year from now and exactly why. A panel that agrees with you is a mirror, and a mirror will happily watch you waste a year.

The output is not a pat on the head. It can, and when the evidence isn't there it will, tell you to kill the idea.

## How a session runs

1. **Sharpen.** The idea is restated as one line: for whom, doing what job, instead of what they do today, worth doing now because, and by you because. The single belief the whole thing rests on is named. If it can't be said this cleanly, that vagueness is the first finding.
2. **The market-evidence pass.** It goes and gathers real demand and willingness-to-pay evidence, with sources (see below).
3. **The panel.** Three to five thinkers are seated, always with a dissenter, each applying their own documented framework to the idea and the evidence.
4. **The disagreement map.** Where the panel genuinely conflicts, and what evidence would settle each argument.
5. **Assumptions and pre-mortem.** The handful of things that must be true, ranked by risk, and the dissenter's account of why it's dead in twelve months.
6. **The verdict.** Go, reshape, or kill, with a confidence level, the sharpest version of the idea, and the single cheapest test to run next. On a go or reshape, it hands off to the Marketing Council.

## The market-evidence pass

This is the part people remember, and the part that makes the skill worth running instead of guessing.

The skill searches for, and cites, four things: the problem in real customers' own words, what people do about it today and what that costs them, willingness to pay in actual numbers (incumbent prices, "we spend $900 a month on X," "I'd happily pay $50 for something that did Y"), and a rough signal of how many people are in the same pain. Every quote and figure carries a source. Stated willingness to pay is labelled separately from revealed, because a promise is cheap and a payment is not. Nothing here is invented. A fabricated customer quote or price is the worst thing the skill could produce, so if the evidence is thin, it says so rather than manufacturing it.

## The panel

Nine thinkers, each chosen because their lens on "is this idea any good" collides usefully with the others. The takes are a simulation, built only from what each person has actually published or said, and the skill labels them as such every time. Full dossiers, with sourced frameworks, contrarian positions, blind spots and voice notes, live in `references/advisors/`.

**Paul Graham**, co-founder of Y Combinator. Brings the builder's optimism: the best startup ideas are *noticed* by living in the future, not invented at a whiteboard, and the only thing that matters early is to make something a small number of people really want. In a session he pushes past "is this a good startup idea?" to "who wants this right now, and will they use it today?" Evidence: his essays at paulgraham.com, especially *How to Get Startup Ideas* (2012) and *Do Things that Don't Scale* (2013).

**Peter Thiel**, co-founder of PayPal and Palantir, investor. Brings the contrarian and the moat: what important truth do very few people agree with you on, where is the secret, and is there a path to a monopoly rather than a commodity knife-fight. He is the seat that asks why, if this is such a good idea, it hasn't already been done. Evidence: *Zero to One* (2014) and his CS183 Stanford lectures.

**Clayton Christensen**, Harvard Business School professor, the disruption theorist. Brings Jobs to Be Done: people don't want your product, they want the progress it makes for them, so what job is a customer really hiring this to do, and can it get a foothold by serving people the incumbents ignore. Evidence: *The Innovator's Dilemma* (1997) and *Competing Against Luck* (2016). He died in 2020, so his positions are fixed to his published work.

**Rob Fitzpatrick**, founder and author, the panel's evidence enforcer. Brings *The Mom Test*: customers lie to be nice, so talk about their life and past behaviour, never pitch, and chase commitment and advancement (their time, their reputation, their money) rather than compliments. He is the one who will tell you that "ten people said they love it" is worthless, and name the real signal to seek instead. Evidence: *The Mom Test* (2013).

**Teresa Torres**, product-discovery coach. Brings continuous discovery: don't stake the whole idea on one big validation, break it into its riskiest assumptions and test them, weekly, against real customers. She supplies the discipline that keeps the mining honest over time. Evidence: *Continuous Discovery Habits* (2021) and her Product Talk writing.

**Marc Andreessen**, co-founder of Netscape and Andreessen Horowitz. Brings the market-first hammer: the market is the single thing that matters most, a great market pulls the product out of you, and a brilliant team in a weak market still loses. He is the seat that asks whether the market is real and big enough to be worth it. Evidence: *The Pmarca Guide to Startups* (2007), especially "The only thing that matters," and "Why Software Is Eating the World" (2011).

**Ash Maurya**, author and creator of the Lean Canvas. Brings the discipline of turning a vague idea into a set of falsifiable assumptions and testing the riskiest first: love the problem, not the solution, because life's too short to build something nobody wants. Evidence: *Running Lean* (2010, third edition 2022) and *Scaling Lean* (2016). The Lean Canvas adapts Alexander Osterwalder's Business Model Canvas, and the method builds on Steve Blank and Eric Ries.

**Bill Gross**, founder of Idealab. Brings timing: across more than two hundred companies he scored, timing was the single biggest predictor of whether an idea worked, ahead of team, idea, business model and funding. He is the seat that asks not "is this a good idea" but "is the world ready for it, and is being early just another way of being wrong." Evidence: his 2015 TED talk, *The single biggest reason why startups succeed*, and Idealab's history.

**Rory Sutherland**, vice-chairman of Ogilvy UK, behavioural-science evangelist. Brings psycho-logic: the rational reading of an idea is often the wrong one, value is largely perception, and the fattest opportunities hide exactly where everyone else has applied the same obvious logic. He is the antidote to a panel that has over-indexed on cold rationality, the one who argues the counterintuitive version might be the winner and that you can create value by changing perception, not the product. Evidence: *Alchemy: The Surprising Power of Ideas That Don't Make Sense* (2019) and his TED talks, including "Life lessons from an ad man" (2009) and "Perspective is everything" (2011).

You can seat whoever you like, name the panel yourself, and add your own thinker (a founder you rate, or your toughest customer) with the template in `references/advisor-template.md`.

## How the voices are kept honest

The whole thing rests on not making things up, so the grounding rules are strict and non-negotiable.

- Every session opens with a line saying it is a simulation, each take built from the thinker's published frameworks, not their actual review of your idea.
- No fabricated quotes are put in a thinker's mouth. A line is quoted only when it is genuinely documented, and it is attributed. Otherwise the position is paraphrased with its source named.
- No thinker is made to endorse or condemn your specific venture. They are simulated *applying their framework* to it, nothing more.
- The market quotes and prices are real or they are not used. That is the point of the evidence pass, and inventing a willingness-to-pay quote would poison the one thing the skill exists to get right.
- Each take is the strongest honest version of that thinker's view, never a strawman for the synthesis to knock down.

## Modes

Three modes, matched to the stakes: a one-thinker **gut-check** ("what would Fitzpatrick ask about my validation?"), a full **mining session** (the default, three to five thinkers and the full evidence pass), and a **deep mine** that seats all nine and adds a competitor teardown for a real bet.

## Install

Clone this repo, then copy the `idea-mining` folder into your Claude skills directory.

- **Claude Code:** `~/.claude/skills/idea-mining/`, or a project's `.claude/skills/`.
- **Claude.ai and the desktop app:** zip the `idea-mining` folder (with `SKILL.md` inside it) and upload it under **Settings → Capabilities → Skills**.
- Install the required companion skill **Marketing Council** alongside it, from wherever you obtained it, so the two can chain. Idea Mining still runs without it, it just tells you to install it rather than handing over.

That is the whole install. The skill loads itself when you describe an idea and ask for it to be tested. Try "pressure-test this idea before I commit," "will anyone actually pay for this?", or "mine this idea, then run it past the marketing council."

## Handing it out

This is a self-contained folder. Zip it, drop it in a repo, or add it to a plugin marketplace, and anyone can drop it into their skills directory and use it. It runs on any Claude client that can search the web, and it degrades gracefully if a deeper research skill or the Marketing Council is not installed.

It has one companion dependency, the **Marketing Council** skill, for the go-to-market stage. Do not bundle or redistribute Marketing Council with this package. It is separately authored and not ours to ship. Point people to install it themselves, and Idea Mining will chain into it once it is present.

## Credits and sources

The frameworks belong to the people who built them, and this skill only applies them. Named works, by thinker:

- Paul Graham, essays at paulgraham.com (*How to Get Startup Ideas*, *Do Things that Don't Scale*, and others).
- Peter Thiel, *Zero to One* (2014, with Blake Masters), and the CS183 lectures.
- Clayton Christensen, *The Innovator's Dilemma* (1997), *Competing Against Luck* (2016).
- Rob Fitzpatrick, *The Mom Test* (2013).
- Teresa Torres, *Continuous Discovery Habits* (2021).
- Marc Andreessen, *The Pmarca Guide to Startups* (2007), *Why Software Is Eating the World* (2011).
- Ash Maurya, *Running Lean* (2010, 2022), *Scaling Lean* (2016).
- Bill Gross, *The single biggest reason why startups succeed* (TED, 2015).
- Rory Sutherland, *Alchemy* (2019) and his TED talks.

Read the primary sources. They are better than any simulation of them.

## Licence

Apache-2.0, like the rest of this repo. See [LICENSE](../../LICENSE). Please don't present a simulated take as the real person's opinion.
