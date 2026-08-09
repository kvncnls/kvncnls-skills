# Flywheel—single-file bundle

This is the complete **Flywheel** skill as one self-contained document—the spine plus every reference—so you can use it in any AI coding agent, not only Claude Code.

*Generated from `flywheel/` at commit `318fb1b`. If the repo has moved on, regenerate rather than edit this file: it is a build artifact, not the source.*

**How to use it**
- **Claude Code**—you don't need this file; install the `flywheel/` folder from the repo for `/flywheel` and on-demand loading. This bundle is for everything else.
- **Codex (CLI)**—append it to your project's `AGENTS.md`, which Codex loads automatically: `cat flywheel.md >> AGENTS.md`.
- **ChatGPT**—create a Custom GPT and paste this into *Instructions*, or upload it as a *Knowledge* file. A Project works the same way.
- **Cursor / Windsurf / Cline**—add it as a rules file, e.g. `.cursor/rules/flywheel.md`.

Everything below is the skill, including the full 0–4 / 16 scoring rubrics.

---

# Flywheel

**Growth is how hard you push. Retention is how heavy the wheel is.**

A product's journey is usually drawn as a funnel—attention narrowing to trust, to activation, to value, to payment. But look at the last stage. People who return and bring others feed the top again. The chain closes. It is not a funnel, it is a wheel.

That changes what design is for. A funnel asks how to lose fewer people on the way down. A wheel asks how much energy the system stores, and whether each turn is easier than the last.

Four properties of a real flywheel decide everything here:

- **It is hardest to start.** At rest, inertia is highest, and the first turn costs the most.
- **Every push adds to what is already stored.** Force accumulates rather than dissipating.
- **Its mass keeps it turning between pushes.** A heavy wheel coasts; a light one stops the moment you stop pushing.
- **Friction steals what is stored.** An unmaintained wheel slows even while you push.

**The four plays are the four parts of the wheel**, and they run in this order:

| Play | The part | The question |
|---|---|---|
| **1. Trust** | the first push | Is this relevant, credible, and worth continuing? |
| **2. Friction** | drag on the bearing | Can I reach value without getting lost or exposed? |
| **3. Wins** | the power stroke | Did this improve my situation, and what now? |
| **4. Emotion** | the mass | How did that feel, and do I prefer it? |

The order is not a preference. Emotional polish cannot rescue a product that feels untrustworthy, and a perfectly timed referral prompt cannot rescue a product nobody reached value in. **You cannot add mass to a wheel that never started turning.**

---

## When to use

Flywheel is for **the yield on attention you already have**—turning visits into trust, trust into activation, activation into value, and value into return. Onboarding, first-run, activation paths, empty states, success states, upgrade and referral moments, re-entry, win visibility.

It is **not** for:
- Single-screen structure, hierarchy, or clutter—that is Focal.
- Getting the user through a multi-screen path without getting lost—that is Compass.
- Paid acquisition, channel strategy, marketing copy, or SEO. Flywheel improves what happens *after* attention arrives; it does not generate attention.
- Analytics instrumentation, event schemas, research protocols, or experiment statistics. It tells you which measurement would settle a question; it does not build the measurement.

**Scope.** Flywheel is a *lens* for the transitions between stages of a relationship—where value is lost and how a stage earns the next one. It decides which stage is leaking, why, and what to change. The execution of color, typography, spacing, and motion is left to your own design system.

**Flywheel cannot manufacture product-market fit.** It prevents a valuable product from hiding its value behind uncertainty, effort, silence, or forgettability. If the product does not solve a real problem, every play below will make a well-designed thing nobody wants.

---

## Diagnose first—which play do you need?

Never run all four plays by default. Find the stage that is losing people, and run that play. Walk this tree top to bottom and take the first match.

```
Where does the product lose people?
├── They arrive and leave without engaging ............... TRUST
│     the wheel never starts
├── They engage but never reach first value ............. FRICTION
│     drag steals the push
├── They reach value but do not return or convert ....... WINS
│     the power stroke lands and nothing is stored
└── They return for a while, then drift away ............ EMOTION
      the wheel has no mass
```

**If two stages both leak, take the earliest.** Loss compounds downstream: a fix at Wins is wasted on people who never got past Friction. This is the same reason the plays are ordered.

### Diagnosing with data, and without it

**With funnel data**, the leak is where the drop-off is. Compare stage-to-stage conversion, and prefer cohorts with a shared start point over aggregate averages. Read distributions, not means—a median time-to-value can hide a long tail of people who are stuck.

**Without data**, which is the common case, diagnose from the artifact using the play's own audit checks, and say plainly which measurement would confirm it. Never stall for want of numbers, and never present a heuristic finding as a measured one—say the finding was diagnosed from the artifact, and name the metric that would confirm it. Both output templates have a slot for exactly that.

### Two modifiers

**Stakes.** In finance, health, children's products, employment, housing, education, identity, and safety, raise the standard. Protective friction is a growth foundation in these contexts, not a conversion problem—durable trust matters more than immediate completion, and a removed safeguard costs more than it earns.

**Motivation.** Effort must stay proportional to how much the user currently wants the outcome. The same form is reasonable at high motivation and fatal at low. Ask where in the journey the user is before judging whether a step is too much.

---

## The four plays

Each play has its own reference file. Read the one the diagnosis selected; do not read all four.

### 1. Trust—the first push
*Read reference/trust.md.*

The user is deciding whether this is relevant, credible, and worth another minute. Five layers, in order: **relevance** (I recognize the problem), **comprehension** (I understand the mechanism and the next step), **credibility** (the promise is supported), **craft** (this is coherent and maintained), **safety** (I know what will happen and keep control).

Craft is not a substitute for truth. Its job is to make the product's real quality legible.

### 2. Friction—drag on the bearing
*Read reference/friction.md.*

The goal is not zero friction. It is **useful momentum**. Six kinds of friction, and only two of them are waste: accidental and cognitive friction should go, procedural friction should be automated or explained, commitment friction should move after value, and **protective and productive friction should stay**. Removing a safeguard is not a speed improvement; it is the bearing coming out of the wheel.

Define first value before redesigning onboarding. Activation is experiencing value, not completing setup.

### 3. Wins—the power stroke
*Read reference/wins.md.*

Products deliver value silently and then wonder why nobody noticed. A win is a moment the user's situation measurably improves. Find them, make them visible, size the feedback to the magnitude, and place every ask *after* the value it relates to.

An ask before value converts stored momentum into resistance. That is braking your own wheel.

### 4. Emotion—the mass
*Read reference/emotion.md.*

What makes the wheel keep turning between pushes. Name the specific emotion the job calls for—"delight" is not an answer—then build a competent baseline, add reinforcement to ordinary actions, and concentrate peaks on moments that matter. If the baseline is weak, peaks read as cosmetic. If everything is a peak, the product is exhausting.

Retention depends less on novelty than on respectful continuity: restore context on re-entry, show what changed, and never make someone rebuild what they already did.

---

## Routing

- **No argument** → explain the wheel and the four plays briefly, then ask: diagnosing an existing product, or building a stage?
- **`diagnose` / `audit` / `review` (a product, a stage, a screenshot, or a symptom like "nobody comes back")** → load and follow reference/review.md. It scores each play 0–4 against a written rubric, totals to /16 with a band, tags issues P0–P3, and names the leaking stage. That file defines the rubrics, the bands, and the severities—all of them, and nowhere else.
- **`build` (a stage to design)** → run the diagnosis tree to confirm which stage, read that play's reference, then follow **Build** below.
- **A question about one play** → read that play's reference file.

Before emitting either output, read reference/examples.md. It is the calibration for length, tone, and how the locked templates look when filled well.

---

## Build: the five moves

Building a stage needs one input Focal and Compass do not: you cannot design trust or activation in the abstract. Establish the frame first.

1. **Frame it.** What is the product, who is this stage for, and—if the stage is anywhere before value—**what is the first-value event?** Name it as something that changes the user's situation, not as setup completed. "Created an account" is not first value; "imported data and got an actionable insight" is.
2. **Name the stage and its leak.** Which of the four is this, and what is being lost there today (or what would be, if this ships wrong).
3. **Run the play.** Read that reference and apply it. One play, not four.
4. **Place the ask.** If this stage contains a commercial or social ask—upgrade, invite, share, rate, connect—state what value lands before it and why accepting extends that value. If no value lands first, move the ask or cut it.
5. **Run the gates.** Self-check against the **`## Gates`** block of the Stage Spec template below. That block is the single canonical list—read them there, and emit them there. Never restate them in your own words.

**Output—the Stage Spec (use this exact structure).** Every build returns this template verbatim, in this order. Fill the `<…>` slots; keep every fixed label.

```
**Stage:** <name>—the <trust | friction | wins | emotion> play, for <who>.
**First value:** <the event that changes the user's situation>   ·   **Stakes:** low | medium | high

## The leak
- Today: <what is lost here, and the evidence—measured or diagnosed from the artifact>
- Confirm with: <the specific metric that would settle it>

## The design
- <what the user encounters, in order>
- <each element and the job it does for this stage>

## Friction kept
- <any effort deliberately preserved—protective or productive—and why removing it would cost more than it saves>
- None, if nothing here protects the user.

## The ask
- Ask: <the commercial or social ask on this stage, or "None">
- Lands after: <the value the user has just received>
- Declining costs them: <nothing, stated plainly—or name the real consequence>

## Gates
- [ ] First value named as an outcome, not setup
- [ ] The leak is stated with evidence, and the confirming metric is named
- [ ] Every required step has a purpose the user could be told
- [ ] Protective and productive friction preserved
- [ ] Any ask lands after the value it extends, and declining is free
- [ ] Nothing here hides cost, consequence, permission, or reversibility
```

**Gates ship unchecked.** Mark `[x]` only for gates the spec actually satisfies; leave `[ ]` with a short reason for any it does not.

---

## Voice (when giving feedback)

- **Emit the exact output template.** Build and diagnose each have a locked structure—the build template is above, the diagnose template is in reference/review.md. Use it verbatim: same sections, same order, same headers, same table columns, same issue-line format. Don't add, remove, reorder, or rename sections; if a section has nothing, keep its header and write "None."
- **Template precedence.** The template is the complete contract for what gets emitted. If any instruction in this skill asks you to produce something the template has no slot for, put it in the nearest slot that fits, or leave it out—never invent a section. A gap like that is a bug in this skill, not a judgment call: name it in one line after the output so it can be fixed. Analysis the template has no room for is still worth doing; it informs the scores even when it isn't printed.
- **Separate measured from diagnosed.** Say which findings come from data and which from reading the artifact. Confidence stated honestly is worth more than confidence borrowed.
- **Be specific and quantitative.** "Six fields before any value is shown" beats "onboarding is too long." Count the steps, name the moment, quote the copy.
- **Name the mechanism, not the symptom.** "Conversion is low" is not a diagnosis. Trust, comprehension, effort, confidence, motivation, value recognition, timing, memory, attachment—pick the one that explains the loss, then fix that.
- **No hedging when the finding is clear.** Severity does the hedging work.

---

## Absolute don'ts

Match-and-refuse. These are not aggressive growth tactics; they are the ways a wheel gets destroyed while appearing to spin faster.

- **Hiding consequence to increase action.** Cost, renewal, permissions, risk, data use, irreversibility, cancellation. Any of these obscured is a P0 regardless of what it does to the metric.
- **An ask before value.** An upgrade prompt at task entry, an invite request before the product is understood, a rating prompt on first launch. Braking your own wheel.
- **Weaponized emotion.** Shame, artificial urgency, fear of missing out around risky behavior, loss-chasing, punitive streaks, guilt-based cancellation flows.
- **Celebration disproportionate to the moment.** Confetti on a routine action reads as juvenile; confetti on a high-stakes financial action before confirming safety reads as a casino.
- **Optimizing screen count instead of understanding.** Combining screens that each held one real decision does not reduce effort, it concentrates it.
- **Claiming value you cannot substantiate.** Invented time-saved numbers, inflated estimates, generic testimonials.
- **Treating every pause as a conversion problem.** Some pauses are people thinking, which is what you want before a consequential choice.
- **A share button in place of something worth sharing.** Shareability is a property of the result, not of the button.

---

## References

- reference/review.md—the four-play audit, the Flywheel scorecard (0–4 per play, /16), severity, and output format.
- reference/trust.md—the trust stack, first-impression touchpoints, message match, performance and accessibility as trust signals.
- reference/friction.md—the six-type friction taxonomy, the friction decision test, defining activation, designing backward from first value.
- reference/wins.md—win types, the win map, making value visible, proportional amplification, timing asks, shareable artifacts.
- reference/emotion.md—the emotional arc, choosing the emotion, baseline vs peaks, endings and re-entry.
- reference/examples.md—a worked diagnosis and a worked build, in the locked output templates.

---

# Flywheel Diagnose—the four-play audit

Find where a product loses the people it already earned, score each play, and name the one stage to fix first. Use when the user asks to diagnose, audit, or review growth, retention, activation, conversion, churn, or a symptom like "nobody comes back."

## Input modes

- **A symptom** ("they sign up and never return")—map it to a stage with the diagnosis tree in the Flywheel spine above, then audit that stage hardest while still scoring all four.
- **Funnel data**—the leak is where the drop-off is. Use cohorts with a shared start point, and read distributions rather than averages.
- **An artifact** (a screenshot, a page, a flow, a product)—diagnose heuristically from the play's own checks. This is the common case and it is legitimate; label it as diagnosed rather than measured.

## Step 0—Frame, then find the leak

Before scoring, establish in one or two sentences each:

- **What is this product, and who is it for?** A growth judgment with no audience is a guess.
- **What is first value?** Name the event that changes the user's situation. If the team has not defined it, say so—that absence is itself a finding, and it caps Friction at 2.
- **What are the stakes?** Low, medium, or high. In finance, health, children's products, employment, housing, education, identity, and safety, protective friction is a foundation and its removal is a defect, not an optimization.
- **Where is the leak?** Walk the diagnosis tree in **the Flywheel spine above**—take the first match, and don't re-derive the categories here. If two stages leak, take the earliest; loss compounds downstream.
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

---

# Trust—the first push

The wheel is at rest and inertia is highest. The user is deciding whether this is relevant, credible, and worth another minute, and they are deciding it before they have read carefully. Most of the energy you spend on attention is lost right here.

**The job:** let a qualified person form an accurate, positive orientation almost immediately.

## The trust stack

Five layers, in this order. A failure at a lower layer cannot be fixed by a higher one—craft on top of an unclear proposition is a well-dressed stranger.

### 1. Relevance—"is this for someone like me?"
The user recognizes the problem, the audience, or the outcome.

- **Test:** cover everything but the headline and first visual. Can a stranger name who this is for and what changes for them? If they can only name the category, relevance has failed.
- Weak: *"The future of intelligent collaboration."* Strong: *"Turn customer interviews into prioritized product evidence in minutes."* The strong version gives a job, an output, and a reason to care.

### 2. Comprehension—"what is this and what do I do?"
The user understands the mechanism and the next step.

- **Test:** one dominant message per viewport or state, and exactly one primary action. Count the competing calls to action; more than one means the screen has not decided.
- Concrete beats abstract. Product visuals that explain beat visuals that decorate. Labels in the user's language beat internal names.

### 3. Credibility—"is this promise supported?"
Evidence proportional to the claim. A large promise requires strong proof.

- **Test:** for each claim on the screen, name the evidence within one scroll of it. A claim whose proof is three sections away is an unsupported claim at the moment it is read.
- Real screenshots, specific outcomes, named customers, transparent identity, discoverable pricing. Generic testimonials and decorative security badges are not evidence; they are the shape of evidence.

### 4. Craft—"is this maintained and intentional?"
Coherence signals that someone is paying attention, which is the only proxy a new user has for whether the product works.

- Consistent type, deliberate spacing, real alignment, coherent color, components that behave the same way twice.
- **Craft is not a substitute for truth.** Its job is to make the product's actual quality legible. Premium styling over an unclear proposition is the most expensive way to fail this play.

### 5. Safety and control—"what happens if I act?"
The user knows the consequence and keeps agency.

- Clear permissions, preview before commitment, visible fees, reversibility where it exists, honest limitations, explicit confirmation for consequential actions, a way to get help.
- Raise this layer in finance, health, identity, and anything irreversible. **Explaining risk before requesting permission converts better than hiding it, and it is the only version that survives the second visit.**

## First impressions are not the homepage

The first meaningful encounter may be an ad, a social post, a shared artifact, a search result, an app-store listing, an invitation email, a sign-in screen, a wallet-connect modal, a permission request, or an empty state after signup.

Audit the entry points that actually carry traffic, not the one that is easiest to open.

## Message match

When the acquisition promise and the first product state emphasize different things, the user has to reinterpret why they are there—and reinterpretation is where they leave. For each major entry path, check continuity:

| Acquisition promise | Landing message | First product state | Continuity gap |
|---|---|---|---|
| what attracted them | what the page leads with | what the product asks next | what unexpectedly changed |

The goal is conceptual continuity, not identical wording.

## Performance is a trust signal

Slow loading, delayed response, and shifting layout make a product feel unreliable before any content is judged. Treat performance as perceived quality, not only an engineering concern.

Core Web Vitals "good" thresholds, at the 75th percentile: **LCP ≤ 2.5s**, **INP ≤ 200ms**, **CLS ≤ 0.1**. These are guardrails, not a complete measure of how fast something feels.

Also design: immediate input acknowledgment, useful loading states, progressive rendering, stable layout, and clear states for background work.

## Accessibility is trust and reach

An inaccessible conversion path is a growth leak and a quality failure at the same time. Use WCAG 2.2 as the baseline: readable contrast, keyboard access, visible focus, clear labels, sufficient target sizes, error identification and recovery, alternatives for non-text content, reduced-motion support, and authentication that does not depend on a single ability.

## What to measure

Qualified landing continuation, primary-CTA click-through, signup start, invite acceptance, wallet-connect initiation, time to first meaningful interaction, and unprompted comprehension in testing ("what does this do, and who is it for?").

**Do not read bounce rate as a verdict.** A high bounce can mean poor relevance, slow performance, accidental traffic, or a question fully answered on the page.

**Check downstream quality, not only the click.** A message can lift signups while attracting people who never activate—which moves a number and empties the wheel.

## Anti-patterns

- Premium styling over an unclear proposition
- Unsupported superlatives; generic testimonials
- Fake urgency or scarcity
- Decorative security badges with nothing behind them
- Interface imagery that misrepresents the real product
- A polished landing page in front of a neglected product
- Multiple primary actions with no priority
- Hidden pricing, fees, permissions, or consequences
- Motion that delays comprehension

---

# Friction—drag on the bearing

The push landed and the wheel is turning, but effort is stealing it. This play is where most activation is won or lost.

**The job is not zero friction. It is useful momentum.** A bearing with no friction is a bearing that has come out of the wheel—some effort is what keeps the thing safe, understood, and worth having done.

## The six kinds of friction

The whole play turns on telling these apart. Two are waste; four are not.

| Kind | What it is | Default action |
|---|---|---|
| **Accidental** | Effort from poor execution—duplicate fields, unclear labels, broken validation, lost progress, repeated auth, needless context switching | **Remove it.** It serves nobody. |
| **Cognitive** | Effort to understand options, terminology, state, or consequence—dense screens, jargon, ambiguous choices, too many simultaneous decisions | **Reduce, sequence, or explain it.** |
| **Procedural** | Steps a process genuinely requires—account setup, verification, data import, configuration | **Remove what is inherited, automate what is safe, explain what remains.** |
| **Commitment** | Effort that asks the user to invest or decide—choosing a plan, inviting a team, entering payment, publishing | **Move it after value and confidence.** |
| **Protective** | Effort that prevents harm—transaction preview, destructive-action confirmation, permission explanation, risk acknowledgment | **Preserve it.** Make it clear and proportionate, never smaller. |
| **Productive** | Effort that increases ownership, quality, or future value—naming a project, choosing a goal, reviewing an AI output | **Keep it when future value exceeds present cost.** |

**Removing protective friction is not a speed improvement.** It raises completion and transfers the cost to the user, where it returns as support load, refunds, and lost trust. In finance, health, identity, and anything irreversible, protective friction *is* the growth foundation.

## The friction decision test

For every step, field, screen, and decision, answer all seven. If you cannot name the purpose, remove or redesign it.

1. What user or business purpose does this serve?
2. What would fail if it were gone?
3. Can the product infer it or defer it?
4. Does the user understand why it is required?
5. Is this the right moment to ask?
6. Does it increase safety, confidence, or future value?
7. Is the effort proportional to the user's motivation *right now*?

Question 7 is the one teams skip. The same form is reasonable from someone who arrived ready to buy and fatal from someone still deciding whether the product is real.

## Define activation before redesigning onboarding

Onboarding is not a set of introductory screens. It is the path from expectation to first credible value.

**Name the first-value event as a change in the user's situation, not a completed setup step.**

| Weak activation | Strong activation |
|---|---|
| Created an account | Generated and used a meaningful output |
| Completed the tutorial | Completed the first successful transaction |
| Reached the dashboard | Imported data and received an actionable insight |
| Enabled notifications | Invited a collaborator who participated |

**Validate it.** If people who complete your activation event do not retain better than people who do not, the event does not represent value and every decision built on it is aimed at the wrong target.

## Design backward from first value

1. **Name the first-value event.** What changes for the user?
2. **List true prerequisites.** What must exist before it can happen?
3. **Cut inherited steps.** Which requirements exist only because the process was built that way?
4. **Infer what is safe.** What can defaults, imports, or context supply?
5. **Defer secondary setup.** What can wait until after value?
6. **Explain what remains.** Why is each surviving step needed?
7. **Preserve progress.** Can they leave and resume?
8. **Make completion visible.** Do they recognize that value occurred?

Step 8 is the handoff to the Wins play. Value the user does not notice did not land.

## Progressive disclosure

Show what is needed now; reveal depth when it becomes useful. Appropriate for advanced settings, secondary analytics, technical detail, fee composition, optional configuration, and expert controls.

**Never defer anything that materially affects consent, cost, risk, or expected outcome.** That is not disclosure, it is concealment, and it is a P0 under this skill's don'ts.

## Defaults, empty states, errors

**A good default** is safe, commonly useful, easy to understand, easy to change, and transparent when consequential. Defaults that benefit the business at the user's expense are a dark pattern wearing a convenience costume.

**An empty state is an activation surface**, not a notice that nothing exists. It should say what will appear here, why it will be useful, offer one primary path to create or import it, and reassure about effort or reversibility.

**Errors decide whether effort is lost.** An effective error says what happened, what was and was not completed, whether data or money is safe, what to do next, whose fault it is, and how to get help. Never blame the user for a system they could not reasonably understand.

## What to measure

Onboarding completion, step-level abandonment, time to first value, sessions to first value, error rate, backtracking, repeated attempts, support contact during activation, and activation rate by acquisition source.

**Use distributions, not averages.** A median hides the tail of people who are stuck, and the tail is the leak.

Compare retention of activated versus non-activated users—that comparison is what validates the activation definition itself.

## Anti-patterns

- Optimizing the number of screens instead of the amount of understanding
- Removing information required for informed consent
- Treating every pause as a conversion problem
- Forcing setup before demonstrating value
- Long educational carousels disconnected from action
- Collecting information "for later" with no stated use
- Requiring notification permission before establishing relevance
- Showing expert complexity to beginners by default
- Hiding important detail in the name of simplicity

---

# Wins—the power stroke

Energy enters the system here. The user's situation actually improved, and this play decides whether they notice, whether it accumulates, and what they are invited to do next.

**The job:** find the moments the product genuinely improves someone's situation, make them unmistakable, and place every ask after the value it extends.

## What counts as a win

Not every completed task. A win is a moment of meaningful improvement, and it comes in six kinds—teams usually design for the first and ignore the rest.

| Kind | Examples |
|---|---|
| **Functional** | A task completes, time is saved, an error is prevented |
| **Insight** | A pattern becomes visible, uncertainty drops, a recommendation enables action |
| **Progress** | A milestone lands, a capability unlocks, a project advances |
| **Social** | A collaborator responds, work is recognized, a contribution helps the group |
| **Financial** | Money saved or earned, risk reduced, a transaction succeeds |
| **Identity** | The user feels more capable, disciplined, expert, or part of a group they value |

Identity wins are the most durable and the least designed for. They are also what makes a product hard to switch away from, because the alternative has to replace how the user sees themselves, not just what they can do.

## Build a win map

Map the core journey and record every candidate:

| Journey moment | User goal | Evidence of success | Likely emotion | Current feedback | Appropriate next action |
|---|---|---|---|---|---|
| first analysis completes | understand a theme | prioritized themes appear | relief, clarity | generic "Done" toast | save, share, or analyze another source |

Then rank each on **magnitude** (how meaningful), **frequency** (how often), **distinctiveness** (does this product create it in a way others do not), **visibility** (does the user recognize it), **shareability** (is there a natural artifact), and **commercial relevance** (does it support deeper use or payment).

Work the highest magnitude × visibility gap first: a large win the user does not notice is the cheapest fix available anywhere in the wheel.

## Make value visible

Products deliver value silently, then wonder why nobody upgraded. Make the change legible with a before-and-after, time or effort saved, progress toward a stated goal, a meaningful summary, a durable artifact, a clear state change, or evidence of risk reduced.

**The value statement must be credible.** Invented numbers and inflated estimates destroy the trust the earlier plays paid for. If you cannot substantiate "saved you 3 hours," show what was produced instead.

## Amplify proportionally

Feedback intensity must match the magnitude of the win.

| Win magnitude | Response |
|---|---|
| Routine completion | Clear confirmation and a next step |
| Meaningful progress | Summary, progress visualization, restrained motion |
| Major milestone | Stronger celebration, reflection, or a shareable artifact |
| High-stakes success | Reassurance, records, consequences, and control—**before** any celebration |

Over-celebrating routine actions reads as juvenile or manipulative. Under-playing a real achievement reads as indifference. Confetti on a large financial transaction reads as a casino, which is the opposite of what a high-stakes win needs.

## Design the ending

Teams invest in starting tasks and abandon what happens after. A strong ending answers: did it work, what changed, where is the result, is anything still processing, what should I do next, and can I undo, export, share, or continue.

**Closure without a dead end.** The end of a workflow is the highest-energy moment in the whole wheel; leaving the user there with nothing to do wastes it.

## Time asks after value

Growth asks are upgrade, subscribe, invite, share, rate, review, connect a source, adopt an adjacent feature. Before showing one, verify all five:

1. The user has received recognizable value.
2. The ask relates to the value just received.
3. Accepting helps them continue or extend that value.
4. Declining costs them nothing and creates no confusion.
5. The frequency is proportionate.

The sequence is: **outcome occurs → the interface confirms what changed → the emotion is reinforced → a useful next step → then, maybe, an ask.**

The ask should feel like continuation, not extraction. An ask placed before value converts stored momentum into resistance—the user learns that this product interrupts rather than delivers, and that lesson is expensive to unteach.

## Shareable artifacts

Word of mouth is easier when the product makes something that carries value outside it: a result card, a report, a visual summary, a milestone, a public profile, a before-and-after.

A shareable artifact is useful or expressive to the sender, makes sense to the recipient, protects private information, carries enough context to stand alone, preserves attribution without becoming an ad, and leads the recipient somewhere sensible.

**A share button does not make an experience shareable.** The underlying result has to be worth sending. In financial and health contexts, design privacy-preserving artifacts or none—never encourage public sharing of balances, positions, or conditions.

## What to measure

Completion of the core value event, repeat use after a win, upgrade conversion following specific wins, feature adoption after contextual prompts, invite and share initiation *and completion*, recipient engagement with shared artifacts, time from first win to second win.

The comparison that matters: users prompted **after a meaningful win** versus users prompted at arbitrary or time-based moments. That single test settles most arguments about placement.

## Anti-patterns

- Prompting for a rating on first launch
- Asking for invites before the product is understood
- Putting every meaningful result behind a paywall
- Manufacturing celebration without real achievement
- Confetti on high-risk actions before confirming safety
- Claiming value that cannot be substantiated
- Interrupting the user before they have inspected the result
- Making a share artifact primarily an advertisement
- Treating every completed action as an upsell opportunity

---

# Emotion—the mass

What keeps the wheel turning between pushes. A light wheel stops the moment you stop spending; a heavy one coasts. Everything in this play is about how much the experience stores.

**The job:** create an experience people prefer, remember, return to, and describe—not one they can merely operate.

**Do not run this play on a broken baseline.** Emotional treatment on top of a product that is unclear, slow, or untrustworthy reads as cosmetic, and users correctly discount it. If Trust or Friction is scoring below 3, fix that first.

## The arc

> **Insight → emotion → interaction → memory**

The user recognizes something (relevance, progress, possibility), that recognition produces a feeling, the feeling supports an action, and the result becomes easy to recall and associate with the product. Growth happens when memory changes future behavior: return, preference, recommendation, resistance to switching.

## Name the emotion

**"Delight" is not an answer.** It is a placeholder that lets a team skip the decision. Name the feeling the job actually calls for, and let the product's context choose it rather than the brand's wish to seem exciting.

| Context | Useful emotions |
|---|---|
| Financial | Safety, control, confidence, progress |
| Creative tool | Possibility, flow, pride, surprise |
| Collaboration | Connection, momentum, recognition |
| Health | Reassurance, agency, consistency, hope |
| Developer tool | Competence, speed, clarity, mastery |
| Learning | Curiosity, progress, capability |
| Marketplace | Confidence, anticipation, satisfaction |

**Test:** name the emotion, the screen, and the second it happens. If you cannot point to the moment, the emotion is a brand adjective, not a design decision.

In high-stakes contexts, calm outperforms excitement. Trustworthy restraint is an emotional choice, not the absence of one.

## Three levels, not one

1. **Baseline**—clear, stable, responsive, accessible, coherent. Non-negotiable.
2. **Reinforcement**—helpful feedback and a consistent personality during ordinary actions.
3. **Peak**—distinctive treatment for meaningful outcomes and transitions.

If the baseline is weak, peaks feel cosmetic. **If everything is a peak, the product is exhausting** and nothing reads as significant. Concentrate peaks on the moments the Wins play identified as high magnitude.

## The levers

**Motion** explains cause and effect, preserves spatial continuity, directs attention, and gives weight to a milestone. It must never obscure status, delay an essential action, or ignore reduced-motion preferences.

**Feedback** makes the product feel attentive: immediate acknowledgment of input, a clear processing state, specific success confirmation, graceful recovery, visible saved state.

**Language** carries more emotional load than visuals in most products. Good emotional copy clarifies before it charms, matches the seriousness of the moment, never blames the user, recognizes real progress, and sounds like one coherent personality—including during failure, which is when personality is actually tested.

**Personalization** works when it reflects meaningful context: goals, progress, recent work, role-relevant guidance, milestones. It fails when it feels invasive, exposes sensitive information, or manufactures intimacy the relationship has not earned.

**Human touches**—considered empty states, contextual encouragement, honest limitations, defaults that anticipate real situations—work because they communicate care, not because they are cute.

## Endings and re-entry

This is where retention is actually built, and it is the most neglected surface in most products.

**At the end of a session:** confirm progress, preserve state, clarify what is next, and leave the user with confidence rather than ambiguity.

**At re-entry:** restore context, show what changed since they left, help them continue, and never make them reconstruct work they already did.

**Retention depends less on novelty than on respectful continuity.** A product that remembers where you were beats a product that greets you with something new. Most churn framed as "boredom" is actually the cost of repeatedly rebuilding context.

## Why this is the moat

Features and visual patterns are copied quickly. A coherent experience is hard to copy because it emerges from many connected decisions: product values, language, interaction rhythm, visual identity, feedback, support behavior, community, progress model, and how failure is treated.

The moat is not any single animation. It is the accumulated relationship—which is exactly what "mass" means in this model.

## What to measure

Emotion is measured through behavior and direct research, never assumed from aesthetic preference.

Retention and return frequency, voluntary sharing, how users describe the product unprompted, preference against alternatives, satisfaction after key workflows, confidence before and after a task, perceived control, switching intent, support sentiment, re-engagement after a milestone.

**Do not treat a single satisfaction score as proof of attachment.** Ask what people say when they are not being surveyed.

## Anti-patterns

- Confetti substituting for meaningful feedback
- Excessive motion; motion that delays comprehension
- Playful copy during serious failure or financial loss
- Mascots covering confusing UX
- Gamification disconnected from the user's actual goals
- Artificial urgency
- Emotional pressure to prevent cancellation
- Streaks that punish healthy breaks
- Personalization from sensitive data without clear value
- Novel interactions that reduce comprehension
- Brand expression that makes accessibility secondary

---

# Flywheel Examples

Two worked examples in the locked output templates—one **diagnosis**, one **build**. They share a narrative: the diagnosis finds a product losing people before first value, and the build redesigns the stage it names. These set the bar for length, specificity, and tone; the templates set the shape.

---

## Example 1—Diagnose: a team analytics product with a retention complaint

**Input:** *"People sign up and never come back. We think we need better re-engagement emails."* The product turns support tickets into themed insight reports. Signup is email plus a 6-field workspace setup, then a required CSV upload with no sample data, then an empty dashboard reading "No reports yet." First report takes about 4 minutes to generate, and completes with a toast reading "Done." No analytics beyond signup counts.

**Flywheel's output:**

```
**Verdict:** Friction · people never reach a first report, so there is nothing to come back to · **6/16**

**Product:** support-ticket analytics for support and product teams · first value: undefined · stakes: low
**Basis:** diagnosed from the artifact · confirm with: share of signups that generate a first report, and 4-week retention split by whether they did

## Scorecard
| Play | Score | Key finding |
|---|---|---|
| Trust | 3/4 | The outcome is legible and the promise is specific; nothing here explains why loss happens later. |
| Friction | 1/4 | A setup wall—6 configuration fields and a required CSV upload stand between signup and any evidence the product works. |
| Wins | 1/4 | A 4-minute generation ends in a "Done" toast; the report's actual value is never stated. |
| Emotion | 1/4 | No emotional design at all, and with Friction at 1 the baseline could not carry one yet anyway. |
| **Total** | **6/16** | **the wheel is not turning** |

## Issues (most severe first)
- **[P1 · Friction]** The setup wall—6 workspace fields and a CSV upload sit before any output. None can be answered well by someone who has not seen a report, and the upload demands data they may not have exported yet. This is commitment friction placed before value. **Fix:** ship a sample dataset that generates a real report in one click; defer all 6 fields until after the first report exists, and infer the workspace name from the email domain.
- **[P1 · Wins]** The silent power stroke—the product's whole value arrives after a 4-minute wait and is announced by a toast reading "Done." The user is not told what was found, how many tickets were read, or what changed. The single largest win in the product is invisible. **Fix:** replace the toast with the result—themes found, tickets analyzed, the top theme stated in one line—and a next action that extends it.
- **[P1 · Emotion]** Re-engagement aimed at people who never got value—the proposed fix emails users who never reached a first report. Mail asking someone to return to a product that never worked for them is pressure substituting for a reason, and it burns the address for the day the product is actually ready. **Fix:** do not build it. Every hour here belongs at Friction until first-report rate moves.
- **[P2 · Trust]** No evidence near the claim—the promise is specific but nothing on the page shows a real report. **Fix:** put an actual output on the first screen; it does double duty as proof and as comprehension.
- **[P2 · Friction]** The empty state is a notice—"No reports yet" states a fact and offers no path. **Fix:** make it the activation surface: what will appear here, why it is useful, and one button that runs the sample.

## Fix this first
Friction. Nothing downstream can be evaluated until people reach a first report—the Wins finding is real but affects only the small group that survives setup today, and the Emotion play cannot add mass to a wheel that has not turned once. Re-engagement email is the last thing to build, not the first.

## Next
- **Now**: cut the path to first report to one click on sample data; defer the 6 fields; turn the empty state into the entry point.
- **After it moves**: replace the "Done" toast with the result and a next action, then place the upgrade ask after the second report.
- **Hand off**: the 6-field setup form is a single-screen structure problem once it is repositioned—Focal.
```

---

## Example 2—Build: the first-report stage

**Input:** "Design the first-report experience the diagnosis called for."

**Flywheel's output:**

```
**Stage:** First report—the friction play, for a support lead evaluating the product in their first session.
**First value:** a themed report generated from real tickets, read and understood   ·   **Stakes:** low

## The leak
- Today: 6 workspace fields and a required CSV upload stand between signup and any output, and the empty state offers no path. Nobody sees a report without exporting data first.
- Confirm with: share of signups generating a first report within 24 hours, and 4-week retention split on that event.

## The design
- Signup asks for email only. The workspace name is inferred from the domain and shown as editable text, not a field to fill.
- The first screen after signup is a live report built from a sample support dataset, already generated—not an invitation to generate one. The user reads an actual output before doing any work.
- One primary action: "Run this on your tickets." It opens the upload, now framed as replacing sample data with real data, which is a different and easier decision than uploading into a void.
- The 4-minute generation shows what it is doing—tickets read, themes forming—rather than an indeterminate spinner, because a wait the user can see is a wait they will sit through.
- Completion states the result: themes found, tickets analyzed, the top theme in one sentence, and the report itself. No toast.
- The 6 workspace fields move behind a "Workspace settings" link, prefilled with safe defaults, reachable but never blocking.

## Friction kept
- The upload step itself. It is procedural, not accidental—the product cannot analyze tickets it does not have—and it now sits after the user has seen what the analysis produces, where it reads as worth doing.
- Naming the report before saving it. Productive friction: a named report is one the user returns to and finds again, and the cost is a few seconds against a durable gain.

## The ask
- Ask: None on this stage.
- Lands after: n/a—the first upgrade ask belongs after the *second* report, when the user has evidence the product works repeatedly rather than once.
- Declining costs them: nothing.

## Gates
- [x] First value named as an outcome, not setup
- [x] The leak is stated with evidence, and the confirming metric is named
- [x] Every required step has a purpose the user could be told
- [x] Protective and productive friction preserved
- [x] Any ask lands after the value it extends, and declining is free
- [x] Nothing here hides cost, consequence, permission, or reversibility
```

---

**Why these two:** the diagnosis refuses the question it was asked. The user came for re-engagement email and the honest answer is that there is nothing to re-engage *to*—which is what "fix this first" exists to say. Note that the re-engagement finding is a P1, not a P0: it is a misdirected investment, not a dark pattern, and P0 is reserved for the ethical floor so that it keeps its meaning. The build then resolves it: the sample report inverts the whole stage, because a user who has already seen an output is making a completely different decision when asked to upload.

Note what stayed. Two frictions were preserved and named—the upload and the report name—because this play is not about removing effort, it is about making the remaining effort obviously worth it. And note what was refused: no ask on the stage at all, because nothing has happened twice yet.
