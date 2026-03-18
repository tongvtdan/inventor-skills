# Install inventor-skills

## Claude Cowork (desktop)

1. Open Claude desktop and go to **Settings → Plugins**
2. Click **Add Marketplace**
3. Enter the GitHub URL:
   ```
   https://github.com/tongvtdan/inventor-skills
   ```
4. Click **Install**
5. The plugin is now active — skills and commands are immediately available

---

## Claude Code (CLI)

```bash
/plugin install tongvtdan/inventor-skills
```

---

## Test it

Once installed, try these commands in any Claude conversation:

```
/inventor-skills:innovate Our project management SaaS for remote teams

/inventor-skills:solve-contradiction We need to personalize onboarding
but it increases dev complexity and slows our release cycle

/inventor-skills:invent A healthcare wearable that is clinically accurate
but cheap enough for home use
```

Or trigger the skills conversationally:

```
Apply TRIZ to the contradiction between battery life and screen brightness.
Use SIT to generate new ideas for our coffee shop brand.
What does the Contradiction Matrix say for improving speed without reducing reliability?
```

---

## What's included

| Command | Description |
|---------|-------------|
| `/inventor-skills:innovate` | Full SIT session — 5 tools, 8–12 concepts, ranked Innovation Brief |
| `/inventor-skills:solve-contradiction` | TRIZ analysis — Contradiction Matrix, IFR, 4–8 solution concepts |
| `/inventor-skills:invent` | Full pipeline: SIT divergence → TRIZ resolution → Invention Brief |

| Skill | Auto-triggers on |
|-------|-----------------|
| `triz` | Contradictions, trade-offs, "improving X makes Y worse", ARIZ, Su-Field, S-curves |
| `sit` | "Think inside the box", "apply SIT", feature ideation, Drew Boyd method |

---

## Related

- **[patent-skills](https://github.com/tongvtdan/patent-skills)** — turn your invention into a patent application
