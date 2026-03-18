# inventor-skills

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-2-blue)](#skills)
[![Commands](https://img.shields.io/badge/commands-3-green)](#commands)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> **Invent systematically. Think inside the box.**

TRIZ and SIT innovation frameworks for Claude — resolve trade-offs, generate breakthrough ideas, and invent on demand using `/innovate`, `/solve-contradiction`, and `/invent`.

Built on the intellectual foundations of Genrich Altshuller (TRIZ, 400,000+ patents analyzed) and Drew Boyd & Jacob Goldenberg (SIT, *Inside the Box*). Applied at Samsung, Boeing, NASA, GE, P&G, and FPT Software.

---

## Quick Start

```
/innovate Our B2B SaaS project management tool for remote teams

/solve-contradiction We need to personalize onboarding (improves activation)
but it increases dev complexity and slows our release cycle

/invent A healthcare wearable that is clinically accurate but cheap enough for home use
```

Or trigger skills conversationally:
```
Apply TRIZ to the contradiction between battery life and screen brightness.
Use SIT to generate new ideas for our coffee shop brand.
What does the Contradiction Matrix recommend for improving speed without reducing reliability?
```

---

## Installation

### Claude Cowork (desktop)
1. Download [`inventor-skills.plugin`](../../releases/latest/download/inventor-skills.plugin) from the latest release
2. Open the file — Claude desktop shows an install prompt
3. Press **Accept** — skills and commands are immediately available

### Claude Code (CLI)
```bash
# Install from this repo
/plugin install tongvtdan/inventor-skills
```

### Manual (any Claude interface)
Copy the `skills/triz/` and `skills/sit/` folders into your Claude skills directory.

---

## Skills

Skills auto-trigger when Claude detects a relevant request. You can also invoke them explicitly by mentioning TRIZ or SIT.

<details>
<summary><strong>triz</strong> — Theory of Inventive Problem Solving (2 reference files)</summary>

Resolve contradictions using the world's most systematic innovation methodology — developed from analysis of 400,000+ patents across every engineering domain.

**Triggers on**: contradictions, trade-offs, "improving X makes Y worse", "apply TRIZ", inventive principles, ARIZ, Su-Field, trimming, S-curves, ideality, physical contradiction, technical contradiction

**Tools inside**:
- `40-principles.md` — all 40 Inventive Principles with descriptions, examples, and business translations mapped to the 39 Engineering Parameters
- `triz-tools.md` — deep reference: Contradiction Matrix, IFR, Su-Field, 76 Standard Solutions, ARIZ, Trimming, S-Curves, Nine-Box Thinking, Effects Database

**Workflow**: Problem definition → Contradiction classification → Ideal Final Result → Matrix / Separation Principles → 4–8 solution concepts → TRIZ Analysis Report

</details>

<details>
<summary><strong>sit</strong> — Systematic Inventive Thinking (1 reference file)</summary>

Generate creative, practical innovations by working with what already exists. SIT's core insight: the best solutions hide *inside* the box, not outside it.

**Triggers on**: "think inside the box", "apply SIT", feature ideation, product innovation, Drew Boyd method, innovation workshop, function follows form, closed world, attribute dependency, subtraction method

**Tools inside**:
- `five-tools.md` — step-by-step playbook for all 5 SIT tools with classic product examples, business model translations, and combination patterns

**Workflow**: System map (components + attributes) → 5 tools applied → virtual product concepts → filter by feasibility + market fit → Innovation Brief

</details>

---

## Commands

Commands are user-initiated slash commands. Use them for structured, on-demand innovation sessions.

| Command | What It Does |
|---------|-------------|
| `/innovate [product/service/challenge]` | Full SIT session — applies all 5 tools, generates 8–12 innovation concepts, delivers ranked Innovation Brief with next steps |
| `/solve-contradiction [describe trade-off]` | TRIZ analysis — maps to Inventive Principles, generates 4–8 solution concepts, outputs a TRIZ Analysis Report |
| `/invent [challenge]` | Full pipeline: SIT divergence → top-3 concepts → TRIZ contradiction resolution → complete Invention Brief per concept |

### Example outputs

`/innovate` → Innovation Brief with system map, concepts per tool, feasibility ranking, validation experiments

`/solve-contradiction` → TRIZ Analysis Report with contradiction type, IFR statement, recommended principles, solution table, top recommendation

`/invent` → Invention Brief combining the SIT concept + contradiction found + TRIZ resolution + IFR + prototype steps

---

## Methods

### TRIZ — 7 Core Tools

| Tool | Use When |
|------|----------|
| 40 Inventive Principles + Contradiction Matrix | Two parameters conflict (improving one worsens another) |
| Physical Contradictions + 4 Separation Principles | Same element must have two opposing properties |
| Ideal Final Result (IFR) | Define what perfect looks like — then work backward |
| Trimming | Simplify, reduce cost, eliminate components while preserving function |
| Su-Field Analysis + 76 Standard Solutions | Harmful or missing functions between system components |
| S-Curves & 8 Evolution Patterns | Where is this technology in its lifecycle? What comes next? |
| ARIZ | For the hardest problems — when all other tools fail |

### SIT — 5 Thinking Tools

| Tool | Core Move | Classic Example |
|------|-----------|-----------------|
| Subtraction | Remove an essential component; find new value in the absence | Walkman (removed recording) → pocket music player |
| Multiplication | Copy a component; alter the copy meaningfully | Single camera → triple-lens system (wide/telephoto/macro) |
| Division | Break into parts; relocate or resequence | Remote control = TV control function divided and moved |
| Task Unification | Give an existing component an additional unrelated task | Smartphone = phone + camera + GPS + bank |
| Attribute Dependency | Link two previously independent attributes | Photochromic lens = darkness depends on UV level |

~70% of successful consumer product innovations align with one of these five SIT templates (Goldenberg & Mazursky, 2002).

---

## Structure

```
inventor-skills/
├── .claude-plugin/
│   └── plugin.json               ← Plugin manifest
├── skills/
│   ├── triz/
│   │   ├── SKILL.md              ← TRIZ workflow + tool selection guide
│   │   └── references/
│   │       ├── 40-principles.md  ← All 40 Inventive Principles + business translations
│   │       └── triz-tools.md     ← IFR, Matrix, Su-Field, ARIZ, Trimming, S-Curves
│   └── sit/
│       ├── SKILL.md              ← SIT workflow + 5-tool quick reference
│       └── references/
│           └── five-tools.md     ← Step-by-step guide for all 5 SIT tools
├── commands/
│   ├── innovate.md               ← /innovate command
│   ├── solve-contradiction.md    ← /solve-contradiction command
│   └── invent.md                 ← /invent command
├── .github/
│   └── workflows/
│       └── release.yml           ← Auto-packages .plugin on git tag push
├── .gitignore
└── README.md
```

---

## From Invention to Patent

Once you've generated a breakthrough concept with `/invent`, the natural next step is protecting it. Use **[patent-skills](https://github.com/tongvtdan/patent-skills)** — a companion Claude plugin that guides you through prior art search, patent claim drafting, and filing preparation.

**Workflow**:
```
/invent → Invention Brief
       → /prior-art-search    (patent-skills: check what's already filed)
       → /draft-claims        (patent-skills: structure independent + dependent claims)
       → /patent-brief        (patent-skills: full provisional application draft)
```

> **patent-skills** is designed to work alongside inventor-skills. You bring the invention; it helps you protect it.
> → [github.com/tongvtdan/patent-skills](https://github.com/tongvtdan/patent-skills)

---

## Advisory Foundation

These skills encode the methodology of:

- **Genrich Altshuller** — TRIZ creator, analyzed 400,000+ patents across 50+ years (1946–1998)
- **Drew Boyd & Jacob Goldenberg** — SIT framework, *Inside the Box: A Proven System of Creativity for Breakthrough Results* (2013)
- **Roni Horowitz, Amnon Levav** — Original SIT research, Technion & SIT Ltd.
- **Darrell Mann** — *Hands-On Systematic Innovation* (2002), TRIZ in software and business
- **Paweł Huryn** — Product Strategy Canvas integration

Used in production at Samsung R&D, Boeing, NASA, GE, P&G, Johnson & Johnson, SAP, Philips, FPT Software.

---

## Contributing

Pull requests are welcome. To add examples, reference cases, or additional TRIZ/SIT content:

1. Fork the repo
2. Create a branch: `git checkout -b feat/your-addition`
3. Edit the relevant `SKILL.md` or `references/*.md` file
4. Submit a PR with a brief description of what you added and why

Please keep skill files under 3,000 words. Put detailed content in `references/`.

---

## Related Resources

- [TRIZ Journal](https://www.triz-journal.com) — research papers and case studies
- [TRIZ40 Interactive Matrix](https://www.triz40.com) — online Contradiction Matrix tool
- [SIT Ltd.](https://www.sitsite.com) — official SIT training and certification
- [Drew Boyd's Blog](https://drewboyd.com) — SIT practitioner insights
- [pm-skills](https://github.com/phuryn/pm-skills) — PM skills plugin (reference architecture for this repo)
- [anthropics/skills](https://github.com/anthropics/skills) — official Claude skills repository
- [patent-skills](https://github.com/tongvtdan/patent-skills) — patent application companion plugin *(coming soon)*

---

## License

MIT — free to use, modify, and distribute.

See [LICENSE](LICENSE) for full terms.
