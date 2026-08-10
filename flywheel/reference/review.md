# Flywheel Diagnose—the four-play audit

Find where a product loses the people it already earned, score each play, and name the one stage to fix first. Use when the user asks to diagnose, audit, or review growth, retention, activation, conversion, churn, or a symptom like "nobody comes back."

## Input modes

- **A symptom** ("they sign up and never return")—map it to a stage with the diagnosis tree in [SKILL.md](../SKILL.md), then audit that stage hardest while still scoring all four.
- **Funnel data**—the leak is where the drop-off is. Use cohorts with a shared start point, and read distributions rather than averages.
- **An artifact** (a screenshot, a page, a flow, a product)—diagnose heuristically from the play's own checks. This is the common case and it is legitimate; label it as diagnosed rather than measured.

## Step 0—Frame, then find the leak

Before scoring, establish in one or two sentences each:

- **What is this product, and who is it for?** A growth judgment with no audience is a guess.
- **What is first value?** Name the event that changes the user's situation. If the team has not defined it, define it yourself by the rule in **[SKILL.md](../SKILL.md)**—the tree below cannot be walked without it. Then do both: print your definition in the Product line, and report the team's absence of one as its own finding. It caps Friction at 2.
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
| 4 | Exemplary—the first encounter itself demonstrates the product's point of view with unusual clarity for this context |

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
| 4 | Exemplary—the fewest honest steps; safe inference and defaults do the work; protection intact and explained |

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
| 4 | Exemplary—value is made legible and accumulates; endings open the next action; asks read as continuation |

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
| 4 | Exemplary—a coherent personality across success and failure; re-entry restores momentum; the experience is recognizable without the logo |

## Scoring rules

Every play uses the same integer anchors:

| Score | Canonical label | Shared meaning |
|---:|---|---|
| **0** | **Broken or harmful** | The dimension fails outright, blocks its core outcome, actively inverts the intended behavior, or creates material harm. |
| **1** | **Major failure** | The outcome may remain technically possible, but the dimension is seriously compromised, unreliable, or largely absent. Substantial correction is required. |
| **2** | **Partial or inconsistent** | The basic function exists, with a material weakness, missing decision, or inconsistency that prevents dependable quality. |
| **3** | **Strong** | Deliberate, dependable, context-appropriate professional work with only minor gaps. This is the normal target for good execution. |
| **4** | **Exemplary** | Fully realized and unusually strong for the relevant context, including realistic states and constraints, with no material gaps. |

Score each play holistically against its local rubric. Read all checks and evidence, choose the anchor that best describes the play overall, apply explicit prerequisite caps, and let one severe material failure determine the score when the rubric warrants it. Do not use hidden sub-scores, checklist subtraction, averaging, or half-points. A 4 is exemplary for the play being scored; recognizability remains relevant where Emotion's local rubric requires it.

Keep the native total: `total = Trust + Friction + Wins + Emotion`. Calculate `average = total / 4`, display it rounded to one decimal place, and apply this shared algorithm:

| Band | Average rule | Native total |
|---|---:|---:|
| **Broken** | `average <= 1.5` | `0–6 / 16` |
| **Significant rework** | `1.5 < average < 2.5` | `7–9 / 16` |
| **Solid** | `2.5 <= average < 3.5` | `10–13 / 16` |
| **Excellent** | `average >= 3.5` | `14–16 / 16` |

Then cap the band by the weakest play: a minimum of `0` allows only **Broken**, `1` allows at most **Significant rework**, `2` allows at most **Solid**, and `3–4` adds no ceiling. Use the lower-quality result of the average band and this ceiling. The total must equal the exact sum of the four scores.

- **A dark pattern is a critical blocker regardless of total.** Hiding cost, permission, risk, or reversibility to increase action; weaponizing emotion; or removing informed choice must be tagged P0 and named in **Blocker**. Do not mechanically force an unrelated play to 0; score the play using its rubric.
- **The earliest leaking stage governs the recommendation.** A 1 at Trust and a 1 at Emotion is a Trust problem; fixing Emotion first spends effort on people who never arrive. A P0 at a later stage does not move **Fix this first**—every P0 is something to *stop doing*, and stopping is not where you invest.
- **Do not average away a safety or accessibility failure.** Give it its own issue line and blocker state when warranted rather than hiding it inside the total.

Dimension score, overall quality band, issue severity, critical blocker, and the earliest leaking stage are separate. A P0 is always a blocker, but a blocker does not automatically rewrite a score to 0; a score of 0 does not automatically imply P0. The earliest leaking stage still governs **Fix this first**.

## Issue severity

| Priority | Meaning |
|----------|---------|
| **P0 — Critical** | Blocks the core outcome; traps the user; destroys work or state; causes or risks material harm; hides material cost, consequence, permission, or risk; removes informed choice; or uses coercive manipulation. Fix before release. |
| **P1 — Major** | Materially damages comprehension, completion, orientation, trust, value realization, or return for a meaningful share of users. Fix before release. |
| **P2 — Moderate** | Creates real friction, confusion, dilution, or missed value with a viable recovery, workaround, or limited scope. Fix in the next planned pass. |
| **P3 — Minor** | Low-impact craft, consistency, or polish. Fix when time permits. |

Assign severity from consequence, reach, and recoverability. A methodology rule violation is not automatically P0.

**Ordering (one rule):** sort by priority, P0 first. Within the same priority, break ties by stage order—Trust, then Friction, then Wins, then Emotion—because upstream fixes change the population that reaches everything downstream. Never reorder across priorities.

## Output format—use this exact structure

Every diagnosis returns this template verbatim, in this order. Don't add, remove, reorder, or rename sections. Fill the `<…>` slots; keep every fixed label. This block is the single source of truth for the emitted shape.

```
**Verdict:** <the leaking stage> · <the one biggest loss, one phrase> · **<total>/16**

**Product:** <what it is, for whom> · first value: <the event, or "undefined"> · stakes: <low | medium | high>
**Basis:** <observed from a screenshot or artifact | inferred from code | tested in a prototype or live product | walked from a description | measured from product data> · confirm with: <the fastest validating check>
**Blocker:** <None. | concise blocker reason>

## Scorecard
| Play | Score | Key finding |
|---|---|---|
| Trust | _/4 | <one line> |
| Friction | _/4 | <one line> |
| Wins | _/4 | <one line> |
| Emotion | _/4 | <one line> |
| **Total** | **_/16 · _._/4** | **<band>** |

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
- **Basis**—never claim measurement you do not have. Use the controlled basis vocabulary in the template, and name the fastest confirming metric or behavior.
