# TRIZ Deep Reference: Advanced Tools

This file covers the full TRIZ toolkit beyond the 40 Principles. Load the section relevant to your current problem.

---

## Table of Contents
1. [Ideal Final Result (IFR)](#1-ideal-final-result-ifr)
2. [39 Engineering Parameters & Contradiction Matrix](#2-contradiction-matrix)
3. [4 Separation Principles (Physical Contradictions)](#3-separation-principles)
4. [Su-Field Analysis (Substance-Field Modeling)](#4-su-field-analysis)
5. [76 Standard Solutions](#5-76-standard-solutions)
6. [ARIZ — Algorithm for Inventive Problem Solving](#6-ariz)
7. [Trimming](#7-trimming)
8. [S-Curves & Technology Evolution Patterns](#8-s-curves--evolution-patterns)
9. [Nine-Box Thinking (Time & Scale)](#9-nine-box-thinking)
10. [Effects Database](#10-effects-database)

---

## 1. Ideal Final Result (IFR)

**Purpose**: Anchor the solution search toward perfection. Prevents over-engineering and anchors divergent thinking.

**The IFR Statement Template**:
> *"The [X] performs [desired function] by itself, without any additional cost or harm, while preserving all useful functions."*

**How to Apply**:
1. Ignore current constraints entirely
2. Describe the system as if it functions perfectly, for free, with zero side effects
3. Work backward: what is stopping us from reaching this ideal?
4. The gap between current state and IFR reveals the real contradiction

**Example**:
- Problem: Ice on aircraft wings must be removed (anti-icing system is heavy, costly, consumes energy)
- IFR: "The ice removes itself"
- Insight: The IFR points toward coatings that prevent adhesion or heating systems embedded in the wing surface — the wing does the work itself

**IFR in Business**:
- "The product sells itself" → leads to PLG, viral loops, word-of-mouth mechanics
- "The code writes itself" → leads to code generation, low-code tools
- "The support resolves itself" → leads to self-service, community knowledge bases

**Ideality Formula**:
> Ideality = Sum of useful functions / (Sum of harmful functions + Sum of costs)

Increase ideality by: adding useful functions, reducing harmful effects, reducing cost — or combining all three.

---

## 2. Contradiction Matrix

**Purpose**: Given a technical contradiction (improving A worsens B), the matrix recommends which of the 40 Inventive Principles to try.

**The 39 Engineering Parameters** (both rows and columns of the matrix):

| # | Parameter | # | Parameter |
|---|-----------|---|-----------|
| 1 | Weight (moving) | 21 | Power |
| 2 | Weight (stationary) | 22 | Energy loss |
| 3 | Length (moving) | 23 | Substance loss |
| 4 | Length (stationary) | 24 | Information loss |
| 5 | Area (moving) | 25 | Time loss |
| 6 | Area (stationary) | 26 | Amount of substance |
| 7 | Volume (moving) | 27 | Reliability |
| 8 | Volume (stationary) | 28 | Measurement accuracy |
| 9 | Speed | 29 | Manufacturing precision |
| 10 | Force | 30 | Harmful side effects |
| 11 | Stress / Pressure | 31 | Harmful effects on object |
| 12 | Shape | 32 | Ease of manufacture |
| 13 | Stability of composition | 33 | Ease of operation |
| 14 | Strength | 34 | Ease of repair |
| 15 | Duration (moving) | 35 | Adaptability |
| 16 | Duration (stationary) | 36 | Device complexity |
| 17 | Temperature | 37 | Difficulty of detection |
| 18 | Illumination | 38 | Extent of automation |
| 19 | Energy use (moving) | 39 | Productivity |
| 20 | Energy use (stationary) | | |

**How to Use the Matrix**:
1. Identify what you want to **improve** → find the row number
2. Identify what gets **worse** as a result → find the column number
3. The matrix cell lists 2–4 recommended Inventive Principle numbers
4. Look up each in the 40-principles.md reference and apply them to your problem

**Common High-Value Matrix Cells** (for quick reference):
- Improve **Speed** (9) without worsening **Reliability** (27) → Principles 10, 13, 28, 38
- Improve **Strength** (14) without worsening **Weight** (1) → Principles 1, 8, 15, 40
- Improve **Productivity** (39) without worsening **Complexity** (36) → Principles 5, 12, 35, 26
- Improve **Ease of operation** (33) without worsening **Adaptability** (35) → Principles 15, 34, 1, 16

**Online Tool**: https://www.triz40.com — interactive matrix for any parameter combination

---

## 3. Separation Principles (Physical Contradictions)

**When to Use**: The same element must have two contradictory properties simultaneously.
> Example: A drill bit must be HARD (to cut) and SOFT (to flex without breaking)

The four separation strategies:

### Separation in Time
The object has property A at time T1 and property B at time T2.
- ABS brakes: locked AND unlocked — alternating 14 times/second
- Deployable solar panels: folded during launch, expanded in orbit
- Business: Freemium — free during acquisition, paid after retention

### Separation in Space
The object has property A in one location, property B in another.
- Bicycle tire: hard outer surface (durability) + soft inner tube (comfort)
- Wing profile: thick at root (strength) + thin at tip (aerodynamics)
- Business: Centralized strategy, decentralized execution

### Separation Between System and Subsystem (or Super-system)
The system as a whole has property A, but its parts have property B.
- A chain is FLEXIBLE (system), but each link is RIGID (subsystem)
- A crowd is UNPREDICTABLE (system), but each person is PREDICTABLE (individual)
- Business: A platform is OPEN (system), but each transaction is SECURE (subsystem)

### Separation Upon Condition
The object has property A under condition C1, property B under condition C2.
- Photochromic lenses: dark outdoors (UV present), clear indoors (UV absent)
- Shape memory alloys: one shape below Tg, another above Tg
- Business: Dynamic pricing — high price at peak demand, low price at off-peak

---

## 4. Su-Field Analysis (Substance-Field Modeling)

**Purpose**: Model a technical system as interactions between Substances (S) and Fields (F) to identify harmful, missing, or inefficient functions.

**Core Concept**:
Every technical function involves:
- **S1** = Object (what receives the action)
- **S2** = Tool (what performs the action)
- **F** = Field (energy/force enabling the interaction): Mechanical, Thermal, Chemical, Electrical, Magnetic, Acoustic, Biological, Gravitational

**Notation**:
- `S2 --F→ S1` = S2 acts on S1 via field F (useful function)
- `S2 ==F⇒ S1` = harmful interaction
- `S2 --F-→ S1` = insufficient interaction (dashed = weak)

**The 4 Problem Patterns**:

1. **Incomplete System** (missing a field or substance):
   - The interaction exists but is insufficient → Add a new F, or modify S2
   - Or introduce a new S3 between S2 and S1

2. **Harmful Function**:
   - S2 acts on S1 with harmful effect → Introduce S3 to neutralize, or modify S2

3. **System Needs to Be Improved** (upgrade useful + eliminate harmful simultaneously):
   - Introduce S3 as a modifier between S2 and S1
   - Or change the field type

4. **Measurement Problem**:
   - Needs a measurement / detection function → Use a "ferrofield" model or detection field

**Business Model Translation**:
- S1 = Customer (the object of the business function)
- S2 = Product/Service (the tool)
- F = Value delivery mechanism
- Harmful function = friction, churn, support cost
- Missing function = unmet need, feature gap

---

## 5. 76 Standard Solutions

**Purpose**: A structured lookup for solving Su-Field problems. Organized into 5 classes.

### Class 1: Build or Improve a Substance-Field System (13 solutions)
- 1.1: Build a complete Su-Field (if incomplete, add the missing element)
- 1.2: Introduce an additive (S3) to make S1 modifiable
- 1.3: Transition to a super-system or sub-system
- Key: If the interaction is insufficient, first try modifying S2 or the field; then introduce a new substance

### Class 2: Eliminate Harmful Effects (6 solutions)
- 2.1: Introduce S3 between S1 and S2 to block harmful field
- 2.2: Modify S1 or S2 to reduce sensitivity
- 2.3: Use a copy of S1 instead of S1 directly
- Key: Always look for solutions using existing resources before adding new components

### Class 3: System Transitions (Applying to Super/Sub-Systems) (6 solutions)
- 3.1: Transition to a supersystem (combine with another system)
- 3.2: Transition to a subsystem (break into smaller elements)
- 3.3: Transition to a more advanced state (e.g., micro or nano level)

### Class 4: Standards for Detection and Measurement (17 solutions)
- 4.1: Use an existing field to detect / measure
- 4.2: Create a copy for measurement
- 4.3: Use resonance frequency

### Class 5: Standards for Introducing Substances and Fields (17 solutions)
- 5.1: Use existing substances in the system
- 5.2: Use "smart" materials (shape memory, bi-metals, phase change)
- 5.4: Use ferromagnetic particles + magnetic field (very powerful combination)
- 5.5: Transition to the supersystem (combine with environment)

**Practical Approach**: Rather than memorizing all 76, use the Su-Field model to identify your problem class (1–5), then explore solutions within that class.

---

## 6. ARIZ — Algorithm for Inventive Problem Solving

**Purpose**: ARIZ (Algoritmichesky Resheniya Izobretatelskikh Zadach) is Altshuller's most powerful and complex tool. Use it when all other TRIZ tools have failed to resolve a contradiction.

**When to Use ARIZ**: Only for Level 4–5 problems (fundamental breakthroughs). Most problems are solved with the Contradiction Matrix or Standard Solutions first.

### ARIZ-85C: Simplified 9-Part Structure

**Part 1: Problem Analysis**
1.1 State the mini-problem (IFR without introducing new substances or fields)
1.2 Identify the conflict zone (where the contradiction manifests)
1.3 Intensify the conflict (amplify it to its extreme)
1.4 Define the ideal action (what needs to happen in the conflict zone)
1.5 Define the physical contradiction (the element must be X AND not-X)

**Part 2: Analysis of the Physical Contradiction Model**
2.1 Define what the conflicting element must do
2.2 Define why it cannot do it
2.3 What is preventing the solution? (resources vs. constraints)

**Part 3: Ideal Final Result and Physical Contradiction**
3.1 State the IFR-2 (intensified: the conflicting element performs the function itself)
3.2 Physical contradiction stated in substance-field terms
3.3 Use the Separation Principles to resolve

**Part 4: Mobilize and Use Substance-Field Resources**
4.1 Identify all available resources (substances and fields in and around the system)
4.2 Create a "smart little men" (SLM) model — visualize the conflict zone as a crowd of agents, some following the law, some rebelling
4.3 Propose how to reorganize the SLM model to resolve the conflict

**Part 5: Apply Knowledge Base**
5.1 Check Standard Solutions
5.2 Check Effects Database (physical, chemical, biological effects)

**Part 6: Change or Replace the Initial Problem**
If no solution found: reframe the super-problem

**Part 7: Analyze the Solution Concept**
7.1 Verify it resolves the contradiction
7.2 Check it doesn't introduce new contradictions
7.3 Estimate solution quality against IFR

**Part 8: Maximum Use of the Solution**
8.1 How can this solution be applied to other problems?
8.2 What improvements does it suggest for the supersystem?

**Part 9: Analysis of the Problem-Solving Process**
9.1 Compare your actual path with the algorithm — what worked, what didn't?

**Smart Little Men (SLM) Model**: One of ARIZ's most creative tools. Imagine the conflicting zone populated by tiny intelligent agents. Ask: "What would the SLMs need to do to resolve the conflict?" This bypasses analytical fixedness and reveals novel physical configurations.

---

## 7. Trimming

**Purpose**: Simplify a system by eliminating components while maintaining their useful functions — using only the remaining components.

**When to Use**: Cost reduction, simplification, weight reduction, reducing failure points, designing a next-gen product.

**The 3 Trimming Rules**:

**Rule A**: If a component performs NO useful function for any other component → trim it directly.

**Rule B**: If a component's useful function can be performed by another component that already exists in the system → trim it and assign the function to the other component.

**Rule C**: If a component performs a function that the user/super-system can perform → trim it and assign the function to the user or environment.

**Trimming Process**:
1. Create a Function Model (list every component and the function it performs for each other component)
2. Identify each component's "value" (useful functions it provides)
3. Apply Rules A, B, C systematically
4. For each trimmed component, solve the resulting contradiction (how does the system still perform the lost function?)

**Example**:
- Traditional elevator: requires elevator car, cables, motor, shaft, operator
- Trim the operator → function reassigned to automation (push-button)
- Trim the cable → function reassigned to hydraulics or magnetic levitation
- Each trim creates a new design challenge solved by TRIZ

**Business Trimming**:
- Trim: Remove a product feature / department / process step
- Assign function: Can another feature / team / automation handle it?
- Uber trimmed: car ownership (driver owns the car), dispatchers (algorithm does it), fleet management (surge pricing does it)

---

## 8. S-Curves & Evolution Patterns

**Purpose**: Understand where a product/technology is in its evolutionary lifecycle and predict what innovations are coming next.

**The S-Curve**:
All technical systems evolve through 4 stages:
```
Performance
    |                          ___________
    |                    _____/
    |               ____/
    |          ____/
    |_________/
    |________________________> Time
    Stage 1   2      3      4
    Infancy  Growth Maturity Decline
```

**Stage 1 — Infancy**: Low performance, high inventor count, rapid patent filing, breakthrough inventions (Level 4–5). Requires Level 3–5 TRIZ.

**Stage 2 — Growth**: Rapid performance improvement, investment floods in, principles are clear. Requires Level 2–3 TRIZ.

**Stage 3 — Maturity**: Performance plateau, incremental improvements, intense competition on cost. Requires Level 1–2 TRIZ or SIT.

**Stage 4 — Decline**: New supersystem emerges and replaces this technology. Time to innovate at the supersystem level.

**8 Patterns of Technical Evolution** (Altshuller):
1. Stages of evolution (S-curve)
2. Evolution toward increased ideality
3. Non-uniform development of sub-systems
4. Evolution toward increased dynamism and controllability
5. Increased complexity then simplification
6. Evolution with matching and mismatching elements
7. Evolution toward macro to micro level (macro → micro → field)
8. Evolution toward the supersystem

**Business Application**:
- Are you at Stage 2 (invest, capture market) or Stage 3 (differentiate or die)?
- If Stage 3: Use Trimming + IFR to leap to the next curve
- If Stage 4: Use Su-Field analysis to identify which supersystem is replacing you

---

## 9. Nine-Box Thinking (Thinking in Time and Scale)

**Purpose**: Expand the problem-solving perspective across time and system levels to find hidden resources and solutions.

**The 9-Box Grid**:

| | Past | Present | Future |
|---|------|---------|--------|
| **Supersystem** | | Current focus | |
| **System** | | ← You are here → | |
| **Subsystem** | | | |

**How to Use**:
1. Place your current problem in the center (System, Present)
2. Look at each box and ask: "What resources exist here? What happened here? What will happen here?"
3. Solutions often hide in unexpected boxes

**Example**: Problem with a current product (System, Present)
- Supersystem-Past: What did the ecosystem look like before? What was lost?
- Subsystem-Future: What will the components evolve into?
- Supersystem-Future: What will the environment/market demand?

---

## 10. Effects Database

**Purpose**: When you know WHAT needs to happen (e.g., "I need to measure temperature without contact") but not HOW, the Effects Database maps physical, chemical, geometric, and biological effects that can perform that function.

**Categories of Effects**:
- **Physical**: electricity, magnetism, acoustics, optics, thermal, mechanical, radiation
- **Chemical**: reactions, phase changes, dissolution, catalysis
- **Biological**: enzymes, microorganisms, growth processes
- **Geometric**: shape effects, topology, symmetry

**How to Use**:
1. State the required function as: "I need to [verb] [object] using [available resource]"
2. Look for effects that have been used to achieve that function in other fields
3. Transfer the principle into your domain

**Online resource**: https://www.triz-journal.com/effects-database/ and various commercial TRIZ software tools (TechOptimizer, TriSolver, GoldFire)

---

*Reference: Genrich Altshuller, "The Innovation Algorithm: TRIZ, Systematic Innovation and Technical Creativity" (1999); Yuri Salamatov, "TRIZ: The Right Solution at the Right Time" (1996); Darrell Mann, "Hands-On Systematic Innovation" (2002).*
