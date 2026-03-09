---
name: Jimmy's Evolving Skill
version: 1.0.0
description: "A self-evolving skill framework that learns from every interaction. Domain-agnostic — apply to any use case by filling in the Core Instructions section. The skill captures what works, what doesn't, and gets smarter over time."
last_evolution: 2026-03-09
---

# Jimmy's Evolving Skill

## Core Instructions

> **This section is intentionally empty.** Fill it with domain-specific instructions when you apply this skill to a use case. Each instruction should be a clear, actionable rule. Tag new instructions as (NEW), promote to (HIGH) after 3+ successful uses.
>
> Example format:
> - **CI-001 (HIGH):** When generating executive summaries, lead with the decision needed, then context, then options.
> - **CI-002 (NEW):** Use bullet points only when listing 4+ items; otherwise write in prose.

---

## Known Patterns

> **Starts empty.** As you use this skill, patterns are added here as simple conditional rules the agent matches against incoming requests. Keep this list under 20 entries. Format:
>
> - **P-001 (HIGH):** When asked to [input type] → apply [approach]. Last validated: [date]

---

## Evolution Protocol

**This is the entire meta-system. Three steps. That's it.**

### After every non-trivial task, run the Evolution Check:

1. **Pattern miss?** — Did this input fail to match any pattern listed above? (If the agent had to improvise an approach, the answer is yes.)
2. **Instruction gap?** — Did the agent do something not covered by Core Instructions? (If it made up a rule on the fly, the answer is yes.)
3. **User correction?** — Did the user correct, reject, or rework the output? (Look for: "that's wrong," explicit edits, "change X to Y," "try again," or any rework request.)

**If all three are NO** → done, move on.
**If any are YES** → run the Evolve step below.

### Evolve (only when the check triggers):

1. Open `EVOLUTION.md` in this skill's directory
2. Append a new entry to the **Learning Log** using the template in that file
3. If the learning represents something the skill should NEVER do, also add it to the **Anti-Pattern Registry**
4. If the learning is significant enough to become a permanent rule, add or update an entry in **Core Instructions** above and log it in the **Changelog**
5. Notify: `[LEARNING CAPTURED] [one-line summary of what was learned]`

### Rules:
- **Silence is approval.** If the user moves on without correcting, the output was fine. Do not prompt for feedback.
- **Core Instruction changes that remove or contradict an existing instruction require user confirmation.** New additions are autonomous.
- **Anti-patterns are permanent.** They don't decay.
- **Read EVOLUTION.md only when entering Evolve.** Don't read it on every interaction — that's wasted context.
- **Keep this file lean.** If the Evolution Protocol section ever exceeds 50 lines, something went wrong.
