# Flywheel Diagnose—the four-play audit

Find where a product loses the people it already earned, score each play, and name the one stage to fix first. Use when the user asks to diagnose, audit, or review growth, retention, activation, conversion, churn, or a symptom like "nobody comes back."

## Input modes

- **A symptom** ("they sign up and never return")—map it to a stage with the diagnosis tree in [SKILL.md](../SKILL.md), then audit that stage hardest while still scoring all four.
- **Funnel data**—the leak is where the drop-off is. Use cohorts with a shared start point, and read distributions rather than averages.
- **An artifact** (a screenshot, a page, a flow, a product)—diagnose heuristically from the play's own checks. This is the common case and it is legitimate; label it as diagnosed rather than measured.

## Step 0—Frame, then find the leak

Before scoring, establish in one or two sentences each:

- **What is this product, and who is it for?** A growth judgment with no audience is a guess.
- **What is first value?** Name the event that changes the user's situation. If the team has not defined it, say so—that absence is itself a finding, and it caps Friction at 2.
- **What are the stakes?** Low, medium, or high. In finance, health, children's products, employment, housing, education, identity, and safety, protective friction is a foundation and its removal is a defect, not an optimization.
- **Where is the leak?** Walk the diagnosis tree in **[SKILL.md](../SKILL.md)**—take the first match, and don't re-derive the categories here. If two stages leak, take the earliest; loss compounds downstream.
- **Measured or diagnosed?** State which. Findings from data and findings from reading an artifact carry different weight, and blending them silently is how a heuristic becomes a false certainty.

## The four gates

Score every play, even when only one is leaking—a stage can be strong and still sit behind a broken one, and the reader needs to see that the fix is upstream.

### Gate 1—Trust *(the first push)*

- Can a stranger name who this is for and what changes for them, from the first screen alone?
- Count the competing primary actions. More than one means the screen has not decided.
- For each claim, is the evidence within one scroll of it?
- Do the entry points that carry real traffic preserve the promise that brought the user?
- Is consequence—cost, permission, reversibility—visible before the action that triggers it?

| Score | Criteria |
|-------|----------|
| 0 | Actively repels—misleading claims, hidden cost, or a first encounter that damages trust |
| 1 | Missing—no recognizable audience, outcome, or reason to continue |
| 2 | Functional—the category is clear but the outcome, evidence, or next step is not |
| 3 | Strong—relevant, comprehensible, supported, coherent, and safe |
| 4 | Distinctive—the first encounter itself demonstrates the product's point of view |

### Gate 2—Friction *(drag on the bearing)*

- Is first value defined as an outcome rather than setup? If not, cap this gate at 2.
- Walk each step of the path to first value and name its friction type. Accidental and cognitive friction are waste; protective and productive friction are not.
- Is any commitment asked before value has been delivered?
- Do empty states create a path to value, and do errors preserve the user's work?

| Score | Criteria |
|-------|----------|
| 0 | Protective friction removed, or a required step the user cannot satisfy |
| 1 | A setup wall—value is gated behind configuration the user has no context to complete |
| 2 | Reachable, but padded with accidental or cognitive friction, or first value is undefined |
| 3 | Lean path, purposeful steps, progress preserved, recovery designed |
| 4 | The fewest honest steps; safe inference and defaults do the work; protection intact and explained |

### Gate 3—Wins *(the power stroke)*

- Name the largest win the product delivers. Does the user recognize it happened?
- Does feedback intensity match the magnitude of the win?
- Does every important workflow have a designed ending, or does it stop?
- Does each ask land after the value it extends, and is declining free?

| Score | Criteria |
|-------|----------|
| 0 | Asks precede value, or claimed value cannot be substantiated |
| 1 | Value is delivered silently—the user's situation improves and nothing says so |
| 2 | Wins are acknowledged generically; endings stop rather than close |
| 3 | The main win is visible and proportionate; asks are placed after value |
| 4 | Value is made legible and accumulates; endings open the next action; asks read as continuation |

### Gate 4—Emotion *(the mass)*

- Is the intended emotion named, with the screen and the moment it happens?
- Is the baseline strong enough to carry expressive layers? If Trust or Friction scores below 3, say so here—peaks on a weak baseline read as cosmetic.
- Does re-entry restore context and show what changed?
- Does anything here rely on shame, urgency, streak pressure, or guilt?

| Score | Criteria |
|-------|----------|
| 0 | Emotion is weaponized—shame, false urgency, punitive streaks, guilt-based retention |
| 1 | Absent—functional, forgettable, and identical to its alternatives |
| 2 | A consistent surface, but no designed peak and no continuity on return |
| 3 | A named emotion, a competent baseline, peaks on moments that matter |
| 4 | A coherent personality across success and failure; re-entry restores momentum; the experience is recognizable without the logo |

## Scoring rules

Score each play 0–4 using its gate rubric above. Be honest—a 4 means genuinely distinctive, not "fine."

- **Bands** (the only band list in this skill; look the string up from here): **13–16** ship it · **10–12** solid, fix the weak play · **7–9** significant rework · **0–6** the wheel is not turning.
- **The Total must equal the four scores summed**, and its band string must be one of the four above, verbatim.
- **A dark pattern is blocking regardless of total.** Hiding cost, permission, risk, or reversibility to increase action; weaponizing emotion; removing informed choice. Score that gate 0, tag it P0, and name it in the Verdict phrase—a wheel spun by deception is not storing energy, it is borrowing against trust. The band still prints; P0 is what carries the urgency.
- **The earliest leaking stage governs the recommendation.** A 1 at Trust and a 1 at Emotion is a Trust problem; fixing Emotion first spends effort on people who never arrive. A P0 at a later stage does not move **Fix this first**—every P0 is something to *stop doing*, and stopping is not where you invest.
- **Do not average away a safety or accessibility failure.** Give it its own issue line rather than folding it into a gate score, where a strong play would hide it.

## Issue severity

| Priority | Meaning |
|----------|---------|
| **P0** | Hides consequence, weaponizes emotion, or removes informed choice—fix now, regardless of metrics |
| **P1** | Costs a large share of people at the leaking stage—fix before spending more on attention |
| **P2** | Real loss with a workaround, or a win left invisible—next pass |
| **P3** | Polish—if time permits |

**Ordering (one rule):** sort by priority, P0 first. Within the same priority, break ties by stage order—Trust, then Friction, then Wins, then Emotion—because upstream fixes change the population that reaches everything downstream. Never reorder across priorities.

## Output format—use this exact structure

Every diagnosis returns this template verbatim, in this order. Don't add, remove, reorder, or rename sections. Fill the `<…>` slots; keep every fixed label. This block is the single source of truth for the emitted shape.

```
**Verdict:** <the leaking stage> · <the one biggest loss, one phrase> · **<total>/16**

**Product:** <what it is, for whom> · first value: <the event, or "undefined"> · stakes: <low | medium | high>
**Basis:** <measured from data | diagnosed from the artifact> · confirm with: <the metric that would settle it>

## Scorecard
| Play | Score | Key finding |
|---|---|---|
| Trust | _/4 | <one line> |
| Friction | _/4 | <one line> |
| Wins | _/4 | <one line> |
| Emotion | _/4 | <one line> |
| **Total** | **_/16** | **<band>** |

## Issues (most severe first)
- **[P0 · Trust]** <Name>—<observation>. <what it costs>. **Fix:** <fix>.
- **[P1 · Friction]** <Name>—<observation>. <what it costs>. **Fix:** <fix>.

## Fix this first
<the single leaking stage, and why fixing anything downstream is premature>

## Next
- **Now**: <the change at the leaking stage>
- **After it moves**: <what becomes worth doing once that stage holds>
- **Hand off**: <single-screen structure goes to Focal; multi-screen path goes to Compass; "None" if all of it is Flywheel's>
```

Filling it:
- **Issues**—repeat the issue line once per issue, tagged **Trust / Friction / Wins / Emotion**. `<observation>` may run two or three sentences when being specific and quantitative; the rest stay tight. If nothing ranks above P3, write "None above P3." under the header and keep the header.
- **Fix this first**—one stage, never a list. The whole point of the diagnosis is to refuse to work on four things at once.
- **Basis**—never claim measurement you do not have. "Diagnosed from the artifact" with a named confirming metric is a stronger answer than a borrowed number.
