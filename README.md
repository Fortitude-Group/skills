# Fortitude Omnis skills

Claude skills we built for our own work at [Fortitude Omnis Group](https://github.com/Fortitude-Group) and use every week. They're open so you can use them too.

A skill is a folder of instructions (a `SKILL.md`, plus whatever reference files and templates it needs) that Claude loads when a task calls for it. You don't have to name it. Ask for the thing, and Claude reaches for the right skill.

## The skills

| Skill | What it does |
|---|---|
| [**venture-mining**](skills/venture-mining/) | Finds product ideas people already pay to solve, and kills the rest before you build anything. Primary-source evidence, ten adversarial attacks, a 7 Powers moat check, and kill criteria with numbers and dates written before the first build session. |

More to come. Each skill has its own README with install steps and example prompts.

## Install

Every skill installs the same way. Clone the repo once:

```bash
git clone https://github.com/Fortitude-Group/skills.git
```

**Claude Code:** copy the skill's folder into `~/.claude/skills/` (or a project's `.claude/skills/` to share it with everyone on that repo):

```bash
cp -r skills/skills/venture-mining ~/.claude/skills/
```

```powershell
Copy-Item -Recurse skills\skills\venture-mining "$env:USERPROFILE\.claude\skills\"
```

**Claude.ai and the desktop app:** zip the skill's folder (keep the folder inside the zip, with `SKILL.md` in it) and upload it under **Settings → Capabilities → Skills**.

## Layout

```
skills/
  <skill-name>/
    SKILL.md        What Claude reads first
    README.md       What humans read first
    references/     Detail Claude opens only when it needs it
    assets/         Templates the skill fills in
```

## Contributing

Spotted a mistake, or used a skill in anger and found a gap? Open an issue or a pull request. Lessons from real use are exactly what these skills are made of.

## Licence

Apache-2.0. See [LICENSE](LICENSE).
