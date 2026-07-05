# Install inventor-skills

## Codex

Install this repository as a Codex plugin/skill source:

```text
https://github.com/tongvtdan/inventor-skills
```

Codex reads:

- `.codex-plugin/plugin.json`
- `skills/triz/SKILL.md`
- `skills/sit/SKILL.md`
- `skills/inventor-pipeline/SKILL.md`

Test prompts:

```text
Invent a low-cost, clinically credible body recomposition measurement flow using SIT + TRIZ.
```

```text
Apply TRIZ to this contradiction: improving onboarding personalization increases release complexity.
```

```text
Use SIT to generate retention loops for WaistProof.
```

## Claude Desktop / Claude Code

Install from this repo:

```bash
/plugin install tongvtdan/inventor-skills
```

Claude reads:

- `.claude-plugin/plugin.json`
- `skills/triz/SKILL.md`
- `skills/sit/SKILL.md`
- `commands/innovate.md`
- `commands/solve-contradiction.md`
- `commands/invent.md`

Test commands:

```text
/inventor-skills:innovate Our project management SaaS for remote teams
```

```text
/inventor-skills:solve-contradiction We need to personalize onboarding but it increases dev complexity
```

```text
/inventor-skills:invent A healthcare wearable that is clinically accurate but cheap enough for home use
```

## Manual Install

Copy the folders into the relevant local skill/plugin directory:

- `skills/`
- `commands/` if your Claude environment supports slash commands
- `.codex-plugin/` for Codex metadata
- `.claude-plugin/` for Claude metadata
