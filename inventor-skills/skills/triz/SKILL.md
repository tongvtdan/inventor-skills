---
name: triz
description: "Apply TRIZ (Theory of Inventive Problem Solving) to systematically resolve technical and business contradictions, generate breakthrough innovations, and solve hard design or product problems. Use whenever someone faces a contradiction, trade-off, or says things like 'improving X makes Y worse', 'we need a real breakthrough not just iteration', 'I'm stuck on a hard problem', 'apply TRIZ', 'inventive principles', 'contradiction matrix', 'how do we innovate beyond incremental improvement', 'eliminate this limitation', 'resolve this design conflict'. Also triggers on: ARIZ, Su-Field, trimming, functional analysis, ideality, S-curves, 40 principles, 39 parameters, technical contradiction, physical contradiction, innovation methodology, invention."
---

# TRIZ — Theory of Inventive Problem Solving

TRIZ is a systematic innovation methodology developed by Soviet inventor Genrich Altshuller, who analyzed 400,000+ patents across industries and extracted the universal patterns behind inventive solutions. Its core insight: **problems and solutions repeat across industries** — so if you characterize your problem correctly, you can apply proven strategies without pure trial-and-error.

Used by Samsung, Boeing, Intel, NASA, Siemens, GE, and FPT Software. Works for engineering, product, software, architecture, and business problems.

---

## When to Apply TRIZ

- You have a **technical contradiction**: improving one parameter worsens another
- You have a **physical contradiction**: the same element must have two opposing properties
- You need a **breakthrough**, not incremental optimization
- You're **stuck** — no amount of brainstorming or iteration is working
- You need to **eliminate** a component while maintaining its function (Trimming)
- You want to understand **where a technology/product is heading** (S-Curves)
- You're doing **root-cause analysis** of system failures

---

## Core TRIZ Toolkit — When to Use Each

| Tool | Best For | Complexity | Reference |
|------|----------|------------|-----------|
| **40 Inventive Principles + Matrix** | Two parameters conflict (e.g., strength vs. weight) | Low–Medium | `references/40-principles.md` |
| **Physical Contradictions + Separation** | Same parameter must be two things at once | Low–Medium | `references/triz-tools.md` §3 |
| **Ideal Final Result (IFR)** | Defining the perfect solution to anchor direction | Low | `references/triz-tools.md` §1 |
| **Trimming** | Simplification, cost reduction, elegance | Medium | `references/triz-tools.md` §7 |
| **Su-Field Analysis** | Harmful or missing functions between components | Medium | `references/triz-tools.md` §4 |
| **76 Standard Solutions** | Structured fix after Su-Field modeling | Medium | `references/triz-tools.md` §5 |
| **S-Curves & Evolution** | Lifecycle positioning, predicting next innovation | Low–Medium | `references/triz-tools.md` §8 |
| **Nine-Box Thinking** | Expanding solution search across time and scale | Low | `references/triz-tools.md` §9 |
| **ARIZ** | Most complex, Level 4–5 problems, all else failed | High | `references/triz-tools.md` §6 |

---

## TRIZ Problem-Solving Workflow

Work through these steps conversationally. Confirm understanding at each step before proceeding.

### Step 1 — Define the Specific Problem

Ask the user:
- What system, product, or process is involved?
- What do you want to **improve** (desired parameter)?
- What gets **worse** as a result (worsening parameter)?
- What **constraints** exist (cost, materials, time, regulation)?
- What is the **context** — engineering, product, software, business?

Listen carefully for the hidden contradiction.

### Step 2 — Classify the Contradiction Type

**Technical Contradiction**: Improving Parameter A worsens Parameter B.
> *"Increasing bridge strength increases weight"*

**Physical Contradiction**: The same element must have two opposing properties simultaneously.
> *"A coffee cup must be HOT (to keep coffee warm) AND COLD (to be holdable)"*

**No clear contradiction**: Define the **Ideal Final Result** first (Step 3), then work backward to find it.

### Step 3 — Define the Ideal Final Result (IFR)

Before any solutions, state the ideal:
> *"The [X] performs [required function] by itself, with zero added cost or harm."*

Ask: *"What would perfect look like if there were no constraints at all?"*

This is not wishful thinking — it's a navigation anchor. The gap between current reality and IFR reveals what needs to be solved.

Read `references/triz-tools.md §1` for the full IFR technique.

### Step 4 — Apply the Right Tool

**For Technical Contradictions**:
1. Map your **improving parameter** to its number in the 39-parameter list (`references/triz-tools.md §2`)
2. Map your **worsening parameter** similarly
3. The Contradiction Matrix recommends 2–4 Inventive Principles — look each up in `references/40-principles.md`
4. Interpret each principle for your specific problem
5. Generate at least one concrete solution concept per principle

**For Physical Contradictions**:
Apply one or more of the 4 Separation Principles (`references/triz-tools.md §3`):
- **In Time**: Property A at moment T1, Property B at moment T2
- **In Space**: Property A at location L1, Property B at location L2
- **Between levels**: System has A, its parts have B
- **Upon condition**: Property A under condition C1, Property B under condition C2

**For Simplification / Cost Reduction**:
Use Trimming (`references/triz-tools.md §7`) — remove components while reassigning their functions.

**For Complex System Problems**:
Use Su-Field analysis → then apply 76 Standard Solutions (`references/triz-tools.md §4–5`).

**For Positioning / Strategy**:
Use S-Curves to understand lifecycle stage, then predict the required level of innovation (`references/triz-tools.md §8`).

### Step 5 — Generate Solution Concepts

For each recommended Inventive Principle or Separation strategy:
1. Name the principle and its definition
2. Explain concretely how it applies to this problem
3. Generate 1–2 solution concepts
4. Note: feasibility, novelty, new contradictions introduced

Aim for **4–8 distinct solution concepts** across all principles. Diverge first, converge later.

### Step 6 — Evaluate and Rank Solutions

For each concept:
- Does it fully **resolve** the contradiction (not just compromise)?
- How close is it to the **IFR**?
- Does it introduce **new contradictions**? (if yes → apply TRIZ again to those)
- Is it **testable / prototypable** soon?

Rank the top 2–3. Identify what would need to be true for each to work.

### Step 7 — Output a TRIZ Analysis Report

Use the output format below. Save as a markdown document.

---

## Output Format

```markdown
## TRIZ Analysis: [Problem Title]

### Problem Statement
[Clear, specific description of the system and the challenge]

### Contradiction
- **Type**: Technical / Physical
- **Improving parameter**: [what you want better]
- **Worsening parameter**: [what gets worse]
  OR
- **Physical contradiction**: [X must be A AND B simultaneously]

### Ideal Final Result
[Statement: "The X performs Y by itself, without cost or harm"]

### Tools Applied
[Which TRIZ tools were used and why]

### Recommended Principles / Strategies
[From matrix, separation principles, or other tools]

### Solution Concepts
| # | Principle/Strategy | Solution Concept | Feasibility | Novelty |
|---|-------------------|-----------------|-------------|---------|
| 1 | | | | |
| 2 | | | | |
...

### Top Recommendation
[Best 1–2 solutions with rationale]

### New Contradictions Introduced (if any)
[What TRIZ iterations are needed next]

### Next Steps
[Experiments, prototypes, or further TRIZ analysis]
```

---

## TRIZ for Business & Product Problems

TRIZ was born in engineering but maps powerfully to business. Key translations:

| Engineering Parameter | Business / Product Analog |
|----------------------|--------------------------|
| Speed (9) | Time-to-market, response latency, decision velocity |
| Reliability (27) | Uptime, NPS, churn consistency |
| Strength (14) | Moat, brand defensibility |
| Ease of operation (33) | User experience, onboarding friction |
| Adaptability (35) | Configurability, personalization |
| Complexity (36) | Technical debt, organizational complexity |
| Productivity (39) | Revenue per employee, feature output per sprint |

**Business Contradiction Example**:
> "We need deep personalization (adaptability ↑) but it increases complexity and maintenance cost (complexity ↑, productivity ↓)"
→ Contradiction Matrix → Principles #1 Segmentation, #3 Local Quality, #15 Dynamics, #35 Parameter Changes
→ Solution concepts: Rules-based personalization (segmentation), smart defaults (local quality), adaptive ML (dynamics)

---

## TRIZ in Architecture and Design

TRIZ applies to architectural design through four lenses:
1. **Contradiction**: The building must be OPEN (light, views, connection to nature) AND CLOSED (energy efficient, private, secure)
2. **Ideality**: Toward a building that performs all functions without conventional mechanical systems
3. **Function**: Remove structural elements while maintaining stability (Trimming → shell structures, tensegrity)
4. **Resource Optimization**: Use ambient resources (sun, wind, rain, thermal mass) as the "field" in the Su-Field model

Note: In architecture, the "ideal" is culturally and contextually defined — TRIZ must be combined with design judgment, not applied mechanically.

---

## Reference Files

- `references/40-principles.md` — All 40 Inventive Principles with descriptions, examples, and business translations
- `references/triz-tools.md` — Deep reference: Contradiction Matrix, IFR, Su-Field, 76 Standards, ARIZ, Trimming, S-Curves, Nine-Box, Effects Database
