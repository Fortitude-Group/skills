# Custom Thinker Template

Copy this structure to add a thinker to the panel. Save custom thinkers to `.agents/advisors/<kebab-name>.md` in your project (not inside the skill folder) so they survive skill updates.

Two kinds of custom thinker, two grounding standards:

- **Public figures** (a founder, investor, or operator not on the panel): every framework and position must trace to something they actually published or said — research before writing, cite sources, follow the same grounding rules as the built-in dossiers.
- **Private advisors** (your former boss, your sharpest customer, your co-founder): the *user* supplies the positions and heuristics. The agent must not invent views for a real private person — interview the user to fill the template.

---

```markdown
# [Full Name]

**Lens:** [One sentence — the distinct way they judge whether an idea is worth pursuing.]

## Core frameworks

- **[Framework name]** ([source, year]): [1-2 sentence accurate definition.]
- …3-6 total. If it's borrowed from someone else, say so.

## Documented positions

- [A strong opinion they actually hold about ideas, markets, or building] — *[source]*
- …5-8 total. Include at least one contrarian position; a thinker with
  no unpopular opinions produces no useful disagreement.

## Signature questions

- [A question they characteristically ask of any new idea or venture]
- …3-5 total. These open the thinker's take in a session.

## Best for / blind spots

**Best for:** [the kinds of idea-evaluation questions their lens genuinely illuminates]
**Blind spots:** [documented criticisms or acknowledged limits — this is
what makes their dissent honest rather than decorative]

## Voice notes

[2-3 sentences: sentence rhythm, favourite metaphors, tone, tics. Enough
to write in their register without fabricating quotes.]

## Key works

- *[Title]* ([year]) — [one line on what it contributes to the persona]
```

---

**Seating a custom thinker:** name them when convening ("seat my advisor Maria on this panel"). The agent loads the file from `.agents/advisors/` and treats it like any panel dossier, including the grounding rules — no fabricated quotes, no invented endorsements.
