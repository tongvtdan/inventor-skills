# inventor-skills

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-3-blue)](#skills)
[![Claude Commands](https://img.shields.io/badge/claude_commands-3-green)](#claude-commands)

Systematic invention skills for Codex and Claude.

Use SIT to generate practical product, business, and feature concepts from existing constraints. Use TRIZ to resolve hard technical, product, and business contradictions. Use the combined inventor pipeline when you want ranked concepts with prototype steps.

Built on Genrich Altshuller's TRIZ work and Drew Boyd/Jacob Goldenberg's SIT method, then tuned for founder-speed product work: ship in days, connect ideas to retention or revenue, and avoid unnecessary complexity.

## Quick Start

### Codex

Ask naturally:

```text
Invent a low-cost, clinically credible body recomposition measurement flow using SIT and TRIZ.
```

```text
Apply TRIZ to this contradiction: improving onboarding personalization increases release complexity.
```

```text
Use SIT to generate new retention loops for WaistProof.
```

### Claude

Use the included slash commands:

```text
/inventor-skills:innovate Our B2B SaaS project management tool for remote teams
```

```text
/inventor-skills:solve-contradiction We need to personalize onboarding but it increases dev complexity
```

```text
/inventor-skills:invent A healthcare wearable that is clinically accurate but cheap enough for home use
```

Or trigger skills conversationally:

```text
Apply TRIZ to the contradiction between battery life and screen brightness.
Use SIT to generate new ideas for our coffee shop brand.
What does the Contradiction Matrix recommend for improving speed without reducing reliability?
```

## Installation

### Codex

Install this repository as a Codex plugin/skill source:

```text
https://github.com/tongvtdan/inventor-skills
```

The Codex manifest is at `.codex-plugin/plugin.json` and points to `./skills/`.

### Claude Desktop / Claude Code

Install from the repository:

```bash
/plugin install tongvtdan/inventor-skills
```

The Claude manifest is at `.claude-plugin/plugin.json`. Claude commands are in `./commands/`; skills are in `./skills/`.

### Manual

Copy the folders you need:

- `skills/triz/`
- `skills/sit/`
- `skills/inventor-pipeline/` for Codex-style orchestration
- `commands/` for Claude slash commands

## Skills

| Skill | Agent | What It Does |
|-------|-------|-------------|
| `triz` | Codex + Claude | Resolve technical, physical, software, product, and business contradictions. |
| `sit` | Codex + Claude | Generate practical innovations using the five Systematic Inventive Thinking tools. |
| `inventor-pipeline` | Codex | Orchestrate SIT divergence plus TRIZ contradiction resolution into ranked invention briefs. |

## Claude Commands

| Command | What It Does |
|---------|-------------|
| `/inventor-skills:innovate [product/service/challenge]` | Full SIT session: applies all 5 tools, generates 8-12 concepts, and ranks the best ideas. |
| `/inventor-skills:solve-contradiction [trade-off]` | TRIZ analysis: maps contradiction, applies IFR and relevant principles, and outputs solutions. |
| `/inventor-skills:invent [challenge]` | Full pipeline: SIT divergence -> top concepts -> TRIZ resolution -> invention brief. |

## Structure

```text
inventor-skills/
├── .claude-plugin/
│   └── plugin.json
├── .codex-plugin/
│   └── plugin.json
├── assets/
│   ├── inventor-icon.png
│   └── inventor-icon-square.png
├── skills/
│   ├── inventor-pipeline/
│   │   └── SKILL.md
│   ├── triz/
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── 40-principles.md
│   │       └── triz-tools.md
│   └── sit/
│       ├── SKILL.md
│       └── references/
│           └── five-tools.md
├── commands/
│   ├── innovate.md
│   ├── solve-contradiction.md
│   └── invent.md
├── INSTALL.md
└── README.md
```

## Product Bias

These skills are most useful when invention needs to become a shippable product move:

- Retention loops for health and behavior tracking apps
- Subscription features with clear user utility
- Hardware/software trade-offs such as ESP32, BLE, battery, enclosure, accuracy, and cost
- AI-powered product systems such as Prompt-Flow or MPM Framework
- Patentable concepts that can later move into `patent-skills`

## From Invention to Patent

Once you have an invention brief, use [patent-skills](https://github.com/tongvtdan/patent-skills) to turn it into prior art searches, claims, and filing strategy.

```text
inventor-skills -> Invention Brief -> patent-skills -> IP strategy / claims / filing draft
```

## Author

Dan Tong — Inventor, entrepreneur, and IP strategy enthusiast — tongvtdan@gmail.com

## License

MIT. See [LICENSE](LICENSE).
