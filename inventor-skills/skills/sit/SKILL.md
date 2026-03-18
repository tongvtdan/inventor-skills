---
name: sit
description: "Apply SIT (Systematic Inventive Thinking) to generate creative, practical, and breakthrough innovations by working inside the existing constraints of a product, service, or business. Use whenever someone wants to innovate a product or service, generate creative ideas from existing resources, apply structured creativity, says 'think inside the box', 'generate innovations for X', 'apply SIT', 'subtraction method', 'task unification', 'attribute dependency', 'what can we innovate about our product', 'creative product ideas', 'innovation workshop', 'Drew Boyd method', 'inside the box thinking'. Also triggers on: systematic inventive thinking, closed world, function follows form, product innovation templates, multiplication technique, division technique, feature innovation."
---

# SIT — Systematic Inventive Thinking

SIT is a structured creativity methodology developed in Israel in the 1990s (Roni Horowitz, Jacob Goldenberg, Amnon Levav). It evolved from TRIZ but simplified the approach into **five thinking tools** anyone can apply, even without engineering background.

The core counter-intuitive insight: **the best innovations hide inside the box** — within your existing product, components, and constraints — not outside them.

**Evidence**: ~70% of successful consumer product innovations align with SIT templates. Companies using SIT training generate 4.84× more inventive solutions than control groups.

**Users**: Johnson & Johnson, GE, Procter & Gamble, SAP, Philips, Wharton, INSEAD.

---

## The Core Principles Behind SIT

### Principle 1: Closed World
Work **only** with components, attributes, and resources that already exist within — or immediately adjacent to — the product or situation. No external elements.

Why this works: The farther you reach outside your current system for a solution, the more complex, costly, and disconnected the result becomes. Constraint forces creativity to find elegant solutions in plain sight.

### Principle 2: Function Follows Form
Reverse the normal problem-solving direction. Instead of *problem → solution*, SIT works *form → function*:
1. Modify the product/system (even hypothetically — in strange, counterintuitive ways)
2. Then ask: "What would this new form be useful for? Who would want this?"

This exploits a cognitive finding by psychologist Ronald Finke (1992): people are better at identifying the value of **existing configurations** than finding optimal solutions for defined problems. Generate the form first, discover the function second.

### Principle 3: Path of Most Resistance
Deliberately pursue the counterintuitive, uncomfortable, or seemingly absurd. The obvious routes are already taken. Productive innovation often starts from what feels wrong.

---

## The Five SIT Thinking Tools

**Read `references/five-tools.md` for full step-by-step instructions and examples for each tool.**

### Quick Reference

| Tool | Core Move | Classic Example |
|------|-----------|-----------------|
| **Subtraction** | Remove an essential component; find a new way to restore its function | Walkman → no recording → pocket music player |
| **Multiplication** | Copy a component; alter the copy in a meaningful way | Single camera → triple camera (wide/telephoto/macro) |
| **Division** | Break a component into parts; relocate or resequence them | Remote control = TV control function divided and moved |
| **Task Unification** | Assign an additional function to an existing component | Smartphone = phone + camera + GPS + bank |
| **Attribute Dependency** | Create a relationship between two previously independent attributes | Photochromic lens = darkness depends on UV light level |

---

## SIT Problem-Solving Workflow

Work through these steps. The key is **generating virtual products first**, then evaluating them — not starting from a problem.

### Step 1 — Define the System

Ask the user:
- What is the **product, service, or business** you want to innovate?
- What are its **key components** (physical parts, features, steps, people, data)?
- What are its **key attributes** (properties of those components: size, speed, color, price, timing, frequency)?

Create a simple inventory list. This is the "closed world" — your innovation canvas.

Example (smartphone):
- Components: screen, battery, camera, microphone, speaker, SIM card, OS, apps
- Attributes: screen brightness, battery capacity, camera resolution, price, weight

### Step 2 — Select a Tool (or Try All Five)

For each SIT tool, apply it systematically to each component. Don't pre-judge — generate freely first.

If the user has a specific goal (simplify, reduce cost, enter new market, add value), guide them toward the most relevant tool:
- **Simplify / reduce cost** → Subtraction
- **Add capability without adding components** → Task Unification
- **Create new product variants** → Multiplication or Division
- **Create smart / adaptive behavior** → Attribute Dependency

### Step 3 — Apply the Tool (Function Follows Form)

For each tool application:
1. **Modify the form** (remove / multiply / divide / unify / link attributes)
2. Ask: *"What is this new configuration? What could it be useful for? Who needs this?"*
3. Don't discard ideas that seem absurd — push through to find the hidden value
4. If no value is found: move to the next component

Aim for **5–10 virtual product concepts** per session.

### Step 4 — Filter and Develop

From all generated concepts:
1. **Feasibility**: Can this be built with existing technology and resources?
2. **Market fit**: Does someone need this? Is there an unmet job-to-be-done here?
3. **Novelty**: Is this genuinely different from existing solutions?
4. **Closed world check**: Does it use only existing or adjacent resources?

Select the top 2–4 concepts for further development.

### Step 5 — Output an Innovation Brief

Use the output format below. Save as a markdown document.

---

## Output Format

```markdown
## SIT Innovation Session: [Product/Service Name]

### System Map
**Components**: [list]
**Key Attributes**: [list]

### Tool Applications

#### [Tool Name]: [Component Modified]
- **Modification**: [what was done]
- **Virtual Product**: [what it becomes]
- **Potential Function / Market**: [who needs this, what job does it do]
- **Feasibility**: High / Medium / Low

[Repeat for each tool applied]

### Top Innovation Concepts
| # | Tool | Concept | Value Proposition | Feasibility |
|---|------|---------|------------------|-------------|
| 1 | | | | |
...

### Recommended Next Steps
[Validation experiments, prototypes, user tests]
```

---

## SIT vs. TRIZ — When to Use Which

| Situation | Use SIT | Use TRIZ |
|-----------|---------|----------|
| Innovation without deep technical knowledge | ✓ | |
| Fast ideation session (30–60 min) | ✓ | |
| Engineering design contradiction | | ✓ |
| Product feature innovation | ✓ | |
| Physical/technical system optimization | | ✓ |
| Consumer product ideation | ✓ | |
| Breakthrough on a hard constraint | | ✓ |
| Business model innovation | ✓ | |
| Both — deeper problem | | ✓ SIT → TRIZ |

**Recommended combined approach**: Start with SIT for fast creative generation, then apply TRIZ to resolve contradictions in the most promising concepts.

---

## SIT for Business Model Innovation

SIT tools map directly to business model components:

- **Subtraction**: Remove a step in the value chain your competitor considers essential
  → Amazon removed bookstores. Netflix removed late fees. Uber removed car ownership.

- **Multiplication**: Duplicate a revenue stream or customer touchpoint with variation
  → AWS duplicated internal infrastructure as an external product

- **Division**: Separate a bundled offer into parts; sell or use them differently
  → LinkedIn divided its user base (recruiters vs. candidates) into separate value propositions

- **Task Unification**: Make a customer action also perform a business function
  → TripAdvisor: user reviews = content marketing + SEO + trust = unified with usage

- **Attribute Dependency**: Link pricing, features, or access to a customer behavior or attribute
  → Usage-based pricing (pay per API call), dynamic pricing (Uber surge), freemium (convert at behavior threshold)

---

## Reference Files

- `references/five-tools.md` — Step-by-step guide for each of the 5 SIT tools with detailed examples, templates, and application patterns
