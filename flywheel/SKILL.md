---
name: flywheel
description: Use when improving how a product converts attention into durable value—the growth and retention side of design. Flywheel finds where a product loses the people it already earned, then applies the play that fixes that stage, across four ordered plays—Trust (the first push), Friction (drag on the bearing), Wins (the power stroke), and Emotion (the mass that keeps it turning). Builds a stage or audits an existing one, scoring each play 0–4. Triggers on growth, retention, activation, onboarding, conversion, churn, drop-off, first impression, time to value, empty state, upgrade prompt, referral, advocacy, "why do users leave", "nobody comes back", "they sign up but never return". Not for single-screen structure (use Focal), multi-screen flows (use Compass), marketing copy, paid acquisition, analytics instrumentation, or research protocols.
argument-hint: "[build | diagnose] <product, stage, or symptom>"
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
- Single-screen structure, hierarchy, or clutter—that is [Focal](../focal).
- Getting the user through a multi-screen path without getting lost—that is [Compass](../compass).
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

**Name first value before you walk the tree.** Branches 2 and 3 are separated by exactly that line, and nothing else—so an undefined first value makes the tree unwalkable, and undefined is the common case. If the team has not named it, name it yourself as the strictest outcome you can defend: the moment the user's situation changes, not the moment setup ends. Say which definition you used, because a looser one moves the whole diagnosis from Friction to Wins and changes every fix that follows. The absence of a team definition is itself a finding—report it.

**If two stages both leak, take the earliest.** Loss compounds downstream: a fix at Wins is wasted on people who never got past Friction. This is the same reason the plays are ordered.

### Diagnosing with data, and without it

**With funnel data**, the leak is where the drop-off is. Compare stage-to-stage conversion, and prefer cohorts with a shared start point over aggregate averages. Read distributions, not means—a median time-to-value can hide a long tail of people who are stuck.

**Without data**, which is the common case, diagnose from the artifact using the play's own audit checks, and say plainly which measurement would confirm it. Never stall for want of numbers, and never present a heuristic finding as a measured one—say the finding was diagnosed from the artifact, and name the metric that would confirm it. Both output templates have a slot for exactly that.

**Pick the confirming metric by what would change the verdict.** Each play's *What to measure* section is a menu; this rule picks from it, and it picks **one**. State it as a comparison, never a level: the completion rate of the exact step you blamed, and the return or conversion rate of the people who clear that step against those who do not. A level only tells you the stage is low. The comparison tells you whether the step you blamed is the reason—which is the claim you actually made.

### Two modifiers

**Stakes.** In finance, health, children's products, employment, housing, education, identity, and safety, raise the standard. Protective friction is a growth foundation in these contexts, not a conversion problem—durable trust matters more than immediate completion, and a removed safeguard costs more than it earns.

**Motivation.** Effort must stay proportional to how much the user currently wants the outcome. The same form is reasonable at high motivation and fatal at low. Ask where in the journey the user is before judging whether a step is too much.

---

## The four plays

Each play has its own reference file. Read the one the diagnosis selected; do not read all four.

### 1. Trust—the first push
*Read [reference/trust.md](reference/trust.md).*

The user is deciding whether this is relevant, credible, and worth another minute. Five layers, in order: **relevance** (I recognize the problem), **comprehension** (I understand the mechanism and the next step), **credibility** (the promise is supported), **craft** (this is coherent and maintained), **safety** (I know what will happen and keep control).

Craft is not a substitute for truth. Its job is to make the product's real quality legible.

### 2. Friction—drag on the bearing
*Read [reference/friction.md](reference/friction.md).*

The goal is not zero friction. It is **useful momentum**. Six kinds of friction, and only two of them are waste: accidental and cognitive friction should go, procedural friction should be automated or explained, commitment friction should move after value, and **protective and productive friction should stay**. Removing a safeguard is not a speed improvement; it is the bearing coming out of the wheel.

Define first value before redesigning onboarding. Activation is experiencing value, not completing setup.

### 3. Wins—the power stroke
*Read [reference/wins.md](reference/wins.md).*

Products deliver value silently and then wonder why nobody noticed. A win is a moment the user's situation measurably improves. Find them, make them visible, size the feedback to the magnitude, and place every ask *after* the value it relates to.

An ask before value converts stored momentum into resistance. That is braking your own wheel.

### 4. Emotion—the mass
*Read [reference/emotion.md](reference/emotion.md).*

What makes the wheel keep turning between pushes. Name the specific emotion the job calls for—"delight" is not an answer—then build a competent baseline, add reinforcement to ordinary actions, and concentrate peaks on moments that matter. If the baseline is weak, peaks read as cosmetic. If everything is a peak, the product is exhausting.

Retention depends less on novelty than on respectful continuity: restore context on re-entry, show what changed, and never make someone rebuild what they already did.

---

## Routing

- **No argument** → explain the wheel and the four plays briefly, then ask: diagnosing an existing product, or building a stage?
- **`diagnose` / `audit` / `review` (a product, a stage, a screenshot, or a symptom like "nobody comes back")** → load and follow [reference/review.md](reference/review.md). It scores each play 0–4 against a written rubric, totals to /16 with a band, tags issues P0–P3, and names the leaking stage. That file defines the rubrics, the bands, and the severities—all of them, and nowhere else.
- **`build` (a stage to design)** → name first value, walk the diagnosis tree to confirm which stage, read that play's reference, then follow **Build** below. That order is fixed: the tree cannot be walked before first value is named.
- **A question about one play** → read that play's reference file.

Before emitting either output, read [reference/examples.md](reference/examples.md). It is the calibration for length, tone, and how the locked templates look when filled well.

---

## Build: the five moves

Building a stage needs one input Focal and Compass do not: you cannot design trust or activation in the abstract. Establish the frame first.

1. **Frame it.** What is the product, who is this stage for, and **what is the first-value event?** Name it as something that changes the user's situation, not as setup completed. "Created an account" is not first value; "imported data and got an actionable insight" is. Name it even when the stage sits after value—the Stage Spec has a slot for it either way, and a stage designed without knowing what value it follows is a stage designed blind.
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

- **Emit the exact output template.** Build and diagnose each have a locked structure—the build template is above, the diagnose template is in [reference/review.md](reference/review.md). Use it verbatim: same sections, same order, same headers, same table columns, same issue-line format. Don't add, remove, reorder, or rename sections; if a section has nothing, keep its header and write "None."
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

- [reference/review.md](reference/review.md)—the four-play audit, the Flywheel scorecard (0–4 per play, /16), severity, and output format.
- [reference/trust.md](reference/trust.md)—the trust stack, first-impression touchpoints, message match, performance and accessibility as trust signals.
- [reference/friction.md](reference/friction.md)—the six-type friction taxonomy, the friction decision test, defining activation, designing backward from first value.
- [reference/wins.md](reference/wins.md)—win types, the win map, making value visible, proportional amplification, timing asks, shareable artifacts.
- [reference/emotion.md](reference/emotion.md)—the emotional arc, choosing the emotion, baseline vs peaks, endings and re-entry.
- [reference/examples.md](reference/examples.md)—a worked diagnosis and a worked build, in the locked output templates.
