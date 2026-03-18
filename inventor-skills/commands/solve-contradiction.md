---
description: Apply TRIZ to resolve any technical, physical, or business contradiction
argument-hint: "<describe the contradiction or trade-off>"
---

## Invocation

```
/inventor-skills:solve-contradiction
/inventor-skills:solve-contradiction We need to personalize onboarding but it increases dev complexity
/inventor-skills:solve-contradiction Battery life improves when screen brightness decreases — need both high
/inventor-skills:solve-contradiction Stronger material means heavier product
```

Apply the TRIZ (Theory of Inventive Problem Solving) methodology to resolve the following contradiction or problem: $ARGUMENTS

Follow the TRIZ skill workflow:
1. Clarify the system and the contradiction (technical or physical)
2. Define the Ideal Final Result (IFR)
3. Map parameters to the 39 Engineering Parameters and apply the Contradiction Matrix, OR apply the 4 Separation Principles for physical contradictions
4. Generate 4–8 solution concepts from the recommended Inventive Principles
5. Rank solutions against the IFR and feasibility

Output a complete **TRIZ Analysis Report** using the format defined in the TRIZ skill.

If $ARGUMENTS is empty or unclear, ask the user to describe the contradiction — what they want to improve, what gets worse as a result, and any known constraints.
