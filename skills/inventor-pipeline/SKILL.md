---
name: inventor-pipeline
description: "Run Codex-native invention workflows that combine SIT and TRIZ. Use when the user asks to invent something, run the full invention pipeline, generate breakthrough concepts, convert /innovate, /solve-contradiction, or /invent style prompts, turn an opportunity into an invention brief, or produce ranked concepts with prototype steps. Also trigger for founder/product challenges where structured ideation plus contradiction resolution would create a more shippable solution."
---

# Inventor Pipeline

This skill adapts the original command workflows into Codex-native conversational modes.

Use this as the orchestration layer:

- **Innovate**: SIT divergence for a product, service, process, offer, or business model.
- **Solve**: TRIZ contradiction resolution for a specific trade-off.
- **Invent**: SIT divergence followed by TRIZ resolution for the top concepts.

When the user mentions SIT or TRIZ directly, prefer the detailed sibling skills:

- `../sit/SKILL.md`
- `../triz/SKILL.md`

## Mode Selection

Use **Innovate** when the user asks for ideas, product innovation, feature concepts, business model moves, or "think inside the box."

Use **Solve** when the user describes a contradiction:

- improving X makes Y worse
- must be A and not-A
- needs speed and quality
- needs accuracy and low cost
- needs personalization and simplicity

Use **Invent** when the user asks for a full pipeline, an invention brief, a breakthrough concept, or a next-generation product.

## Innovate Mode

Apply SIT to the subject.

1. Define the system: components, attributes, users, constraints, and business goal.
2. Apply all five SIT tools:
   - Subtraction
   - Multiplication
   - Division
   - Task Unification
   - Attribute Dependency
3. Generate at least 8 concepts, with at least one from each tool.
4. Rank the top 3 to 5 by:
   - retention, revenue, or activation impact
   - feasibility for a solo builder
   - novelty
   - speed to prototype
5. Produce an Innovation Brief in markdown.

## Solve Mode

Apply TRIZ to the contradiction.

1. Clarify the system and the contradiction type.
2. Define the Ideal Final Result.
3. For technical contradictions, map improving and worsening parameters to the 39 TRIZ parameters.
4. For physical contradictions, use separation in time, space, level, or condition.
5. Generate 4 to 8 solution concepts.
6. Rank by closeness to the Ideal Final Result and speed to test.
7. Produce a TRIZ Analysis Report in markdown.

## Invent Mode

Run the complete pipeline.

### Phase 1: SIT Divergence

Generate 8 to 12 concepts from the current system using all five SIT tools.

### Phase 2: Concept Selection

Select the top 3 concepts using founder-grade criteria:

- Creates retention, revenue, or activation lift.
- Can be prototyped in days.
- Uses existing or adjacent resources.
- Avoids platform, hardware, or regulatory complexity unless it is the moat.

### Phase 3: TRIZ Resolution

For each top concept:

1. Identify the main contradiction it introduces.
2. Apply TRIZ principles or separation strategies.
3. Generate 2 to 3 resolutions.
4. Choose the fastest credible prototype.

### Phase 4: Invention Brief

Output one concise brief per top concept:

```markdown
## Invention Brief: [Concept Name]

### User Outcome
[What the user gets that they could not easily get before]

### SIT Origin
- Tool: [Subtraction / Multiplication / Division / Task Unification / Attribute Dependency]
- Concept: [Short description]

### Key Contradiction
- Type: [Technical / Physical / Business]
- Improving: [X]
- Worsening: [Y]

### Ideal Final Result
[The system performs the function with minimal cost, complexity, or harm]

### TRIZ Resolution
[Principle or separation strategy applied]

### MVP Prototype
[Smallest buildable version]

### Business Bet
[Retention, revenue, activation, or distribution upside]

### Next 3 Steps
1. [Build/test step]
2. [Build/test step]
3. [Build/test step]
```

## Operating Bias

For founder and product work, bias toward shippable concepts:

- prefer 1 to 2 week prototypes
- prefer local-first or lightweight backend designs
- avoid solutions that require large teams, enterprise sales, or heavy hardware unless the user explicitly wants that path
- always connect the invention to retention, revenue, activation, or distribution
