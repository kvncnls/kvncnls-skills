# Compass Review—the three-discipline flow audit

Evaluate a flow (or a set of screens) against the three disciplines and the overarching methodology, then return a scorecard with prioritized, concrete fixes. Use when the user asks to review, critique, audit, or "what's wrong with" any multi-screen flow, journey, or navigation in a functional product, app, or tool.

## Input modes

- **A described flow**—the user narrates the steps ("they sign up, pick a plan, then…"). Map it as a sequence, name the destination, and audit the path you reconstruct. If the narration is ambiguous, restate the sequence and ask before scoring—that is a clarifying exchange, not part of the emitted review.
- **A set of screens or screenshots**—read them in order, infer the transitions between them, and critique the joins. You're judging the *seams*, not each screen—a beautiful screen in the wrong order, or one that drops state on the way in, still fails. Per individual screen layout, defer to [Focal](../../focal).
- **A clickable prototype / live URL**—if browser automation is available, walk the flow: click through, hit Back, refresh mid-flow, follow a deep link cold. Otherwise audit the described or captured steps. Always test the transitions, not just the destinations—the failures live between screens.

## Step 0—Notice the journey, name the destination, classify the flow

Before judging, *walk it*. Most people glance at one screen; a reviewer traces the whole path. Count the steps. Read the progress indicators and Back affordances verbatim. Note what each transition carries and what it drops. Try to get lost. The specificity of your observation is the ceiling on the quality of your critique.

Then frame, in one or two sentences each:
- **What is this journey?** Product type, what the flow is for, where it starts and ends.
- **Name the destination.** Settle it as *"This flow gets the user from ___ to ___."* One outcome; it lands in the review template as the **Flow** name plus the biggest-break phrase, and in a build as the Flow line's from-to. If it needs an "and," it's two flows wearing one coat—flag the split now; the gates will show why.
- **What's the user's state?** Anxious, rushed, first-time, returning, interrupted, one-handed? A checkout under time pressure tolerates fewer steps than a leisurely setup. A flow resumed after a phone call must survive the interruption. Name it; the critique must respect it.
- **What's the bar?** Every flow category has an invisible standard set by its best-in-class journey. A checkout is judged against the cleanest checkouts; an onboarding against the clearest onboardings; a multi-step setup against the cleanest wizard in the category. Ask: *what would the best-in-class flow do at this seam?*
- **The flow type.** Classify it by walking the decision tree in **Registers** in [SKILL.md](../SKILL.md)—take the first match, and don't re-derive the categories here. This sets how the gates should be read; see *Adjust for flow type* below. If the tree lands on linear but an unmanaged fork is bolted on, score it linear and flag the rogue fork under Gate 1.

## Adjust for flow type

Read the gates through the flow type you classified in Step 0. The disciplines still apply; their targets move. Scoring a hub-and-spoke or an open-ended space by linear rules produces false failures.

- **Linear** (default—checkout, onboarding, setup, wizards): score exactly as the gates describe. Progress to the end is sacred; every skippable step is waste.
- **Branching** (conditional signup, "what brings you here?", plan-dependent paths): Orientation must also tell the user *which branch they're on* and *how to change it*—a fork the user can't see or undo fails Gate 1. Under Path Economy, judge whether dead or rarely-taken branches are pruned and whether the common branch is defaulted. Don't penalize the existence of branches; penalize unmanaged ones.
- **Hub-and-spoke** (dashboard → record → dashboard, settings index → detail → index): *"back to the hub" is sacred*—the center is home base, and losing the way back to it is a Gate 1 failure even mid-spoke. Don't score it as a broken linear flow for "having no progress bar"; a hub has no single end. Under Path Economy, count hops out to a spoke and back—minimize them, don't funnel.
- **Open-ended** (browse, search-and-refine, exploration, infinite spaces): the exception that proves the rule. There's no single destination, so *"how far is left" does not apply*—do **not** penalize the absence of a progress indicator under Gate 1. "Never Lost" reduces to *always know where you are in the space, and how to get home*. Under Path Economy, let the user roam; don't force a funnel onto a wander. (This is the journey-level sibling of Focal's exploration register.)
- **Audience / expertise:** weigh who's traveling. Novices want guardrails—guidance, confirmations, one visible path; re-asking a novice is safer than stranding them. Experts want skips, shortcuts, remembered choices, and not to be re-asked; making an expert re-confirm a known step is the economy failure. How many steps feel "economical," and how much signposting feels like hand-holding, both scale with the audience. Don't score a pro flow's terse, skip-heavy path as under-oriented if its users have the route memorized; do score a first-run flow strictly.

A flow you can't classify is usually a linear flow with an unmanaged branch or a hidden hub—score it as linear and flag the structural confusion under Gate 1.

## The three gates

Run each gate in turn. Orientation leads—it's the load-bearing promise. Each produces a 0–4 score and the specific findings behind it.

### Gate 1—Orientation *(load-bearing)*

*At every step, can the user answer where am I, how far is left, and how do I get back or out?*

- Run the **drop test** on every screen: drop the user onto it with no memory of how they arrived. Can they tell where they are, what's left, and how to proceed or retreat? A screen that fails the drop test fails Orientation.
- Check **position and progress**: "Step 2 of 4," a breadcrumb, an active nav state. Is progress framed as achievable milestones, not a demoralizing tally ("12 of 47")?
- Check for a **real Back on every screen** and an **escape hatch** (Cancel / Close / Save & exit) out of every flow—especially modals and wizards. Nothing traps the user.
- Hunt for **dead ends**: a screen the user can reach but not leave is a bug, not a state.
- For branching/hub flows, check that the user can see **which branch they're on** or **how to get back to the hub**.

| Score | Criteria |
|-------|----------|
| 0 | No recovery exists—a true dead end, or a flow the user cannot leave from any screen |
| 1 | A way out exists but is hidden or unlabeled (browser Back only, an unmarked Close); or progress is hidden and the drop test fails on a key screen. A Back that *wipes work* is Gate 3's, not this gate's |
| 2 | Orientable, but one of where-am-I / how-far / how-to-get-back is weak or absent at a step |
| 3 | Clear position, Back, and exit throughout; minor signposting gaps |
| 4 | At every step the user knows where they are, what's left, and how to retreat or escape—the drop test passes everywhere |

Because this discipline is load-bearing, treat a **failed drop test** or a **dead end** as a blocking issue regardless of the total.

### Gate 2—Path Economy

*Is this the fewest honest steps to the destination?*

- **Count the steps**, then count how many the task *honestly* requires. "This is a 7-step flow that needs 3" is the finding.
- Check for **redundant screens**, needless round-trips, and steps that could **merge** without overloading a single screen (defer to Focal for whether the merged screen is too dense).
- Check whether **defaults skip steps**: is the flow asking what it could infer or pre-fill?
- Check for a **setup wall**: is first value gated behind a pile of configuration?
- **Honesty guardrail:** a step that protects the user or earns trust is not waste. Skipping a confirmation on a destructive or costly action, hiding a required disclosure, or burying the price to "reduce friction" is a **dark pattern, not economy**—score that as a failure, not a saving.

| Score | Criteria |
|-------|----------|
| 0 | The path cannot be completed as designed—branches that dead-end, or a required step the user cannot satisfy |
| 1 | Completable but badly bloated (roughly double the honest step count), a setup wall before first value, or a "shortcut" that hides cost or skips protection |
| 2 | Some waste—one or two redundant steps, or a round-trip that should be one screen |
| 3 | Lean path; a default or two could still be inferred |
| 4 | The fewest honest steps; every screen earns its place; nothing protective was cut |

### Gate 3—Continuity

*Do context and state survive the seams between screens?*

- Check for the **memory bridge**: does any step ask the user to carry a fact (a code, a choice, a number) from an earlier screen in their head, rather than showing it where it's needed?
- Test **state on Back and refresh**: does Back wipe entered data? Does a refresh or interruption resume where they left off, or reset to step one?
- Test **entry points**: does a deep link, notification, or search result land the user *in context* on the relevant screen, or dump them at the start?
- Check the **mental model**: do consecutive screens feel like one continuous task—consistent anchors, predictable transitions, the same object in focus—or like jarring jumps?

| Score | Criteria |
|-------|----------|
| 0 | The seams break the task—state lost on Back, deep links dump to step one, the user re-enters everything |
| 1 | A memory bridge on a key step, or a "resume" that resets |
| 2 | Mostly continuous, but one transition drops context or state |
| 3 | Context and state carry well; one rough seam or jarring jump |
| 4 | Nothing the user gave or knew is lost across any seam; every entry point lands in context; the journey feels like one continuous task |

## Scoring rules

Every discipline uses the same integer anchors:

| Score | Canonical label | Shared meaning |
|---:|---|---|
| **0** | **Broken or harmful** | The dimension fails outright, blocks its core outcome, actively inverts the intended behavior, or creates material harm. |
| **1** | **Major failure** | The outcome may remain technically possible, but the dimension is seriously compromised, unreliable, or largely absent. Substantial correction is required. |
| **2** | **Partial or inconsistent** | The basic function exists, with a material weakness, missing decision, or inconsistency that prevents dependable quality. |
| **3** | **Strong** | Deliberate, dependable, context-appropriate professional work with only minor gaps. This is the normal target for good execution. |
| **4** | **Exemplary** | Fully realized and unusually strong for the relevant context, including realistic states and constraints, with no material gaps. |

Score each discipline holistically against its local rubric. Read all checks and evidence, choose the anchor that best describes the dimension overall, apply explicit local caps or prerequisites, and let one severe material failure determine the score when the rubric warrants it. Do not use hidden sub-scores, checklist subtraction, averaging, or half-points. A 4 is exemplary for the dimension being scored; it does not universally require novelty.

Keep the native total: `total = Orientation + Path Economy + Continuity`. Calculate `average = total / 3`, display it rounded to one decimal place, and apply this shared algorithm:

| Band | Average rule | Native total |
|---|---:|---:|
| **Broken** | `average <= 1.5` | `0–4 / 12` |
| **Significant rework** | `1.5 < average < 2.5` | `5–7 / 12` |
| **Solid** | `2.5 <= average < 3.5` | `8–10 / 12` |
| **Excellent** | `average >= 3.5` | `11–12 / 12` |

Then cap the band by the weakest discipline: a minimum of `0` allows only **Broken**, `1` allows at most **Significant rework**, `2` allows at most **Solid**, and `3–4` adds no ceiling. Use the lower-quality result of the average band and this ceiling. The total must equal the exact sum of the three scores.

- **Score 0 vs 1 (Orientation only).** Score **0** when the flow strands the user with no recovery at all—a true dead end, or a flow with no exit anywhere. Score **1** when a way out exists but is hidden or unlabeled (browser Back only, an unmarked Close). Each gate's own rubric governs its 0 and 1; this clause does not carry across disciplines. A Back that *wipes work* is a Continuity failure, scored by Gate 3, not by this clause.
- If more than one independent failure sits in a discipline, score the *worst* one, then list the others as separate issues.
- **The verdict—Never Lost.** Yes or no: at every step, does the user know where they are, what's left, and how to get back or out? The total measures how close the flow gets; the verdict states whether it arrives. A failed drop test or a dead end is a blocker regardless of total.
- **A doubled destination** (the flow needs an "and") is an Orientation failure; assign P0 only when its consequence meets the shared critical definition, and flag it as the split it implies.

Dimension score, overall quality band, issue severity, critical blocker, and the **Never Lost** verdict are separate. Every P0 is a blocker, but a blocker does not automatically rewrite a score to 0; a score of 0 does not automatically imply P0. Non-P0 methodology blockers remain in local caps, sequencing, and handoffs.

## Issue severity

| Priority | Meaning |
|----------|---------|
| **P0 — Critical** | Blocks the core outcome; traps the user; destroys work or state; causes or risks material harm; hides material cost, consequence, permission, or risk; removes informed choice; or uses coercive manipulation. Fix before release. |
| **P1 — Major** | Materially damages comprehension, completion, orientation, trust, value realization, or return for a meaningful share of users. Fix before release. |
| **P2 — Moderate** | Creates real friction, confusion, dilution, or missed value with a viable recovery, workaround, or limited scope. Fix in the next planned pass. |
| **P3 — Minor** | Low-impact craft, consistency, or polish. Fix when time permits. |

Assign severity from consequence, reach, and recoverability. A methodology rule violation is not automatically P0.

**Ordering (one rule):** sort by priority, P0 first. Within the same priority, break ties by type of harm—**Orientation** (the user is lost or trapped) outranks **Path Economy** (the path is longer or less honest than it should be) outranks **Continuity** (a seam drops context or state). Never reorder across priorities; a P0 Continuity issue outranks a P1 Orientation issue.

## Output format—use this exact structure

Every review returns this template verbatim, in this order. Don't add, remove, reorder, or rename sections. Fill the `<…>` slots; keep every fixed label. This block is the single source of truth for the emitted shape—the issue line, the table columns, and the section list exist only here.

```
**Verdict:** <No | Yes> · <the single biggest break, one phrase> · **<total>/12**

**Flow:** <name> · type: <linear | branching | hub-and-spoke | open-ended> · audience: <novice | mixed | expert>
**Context:** <the user's state in a few words> · bar: <the best-in-class comparator you judged against>
**Basis:** <observed from a screenshot or artifact | inferred from code | tested in a prototype or live product | walked from a description | measured from product data> · confirm with: <the fastest validating check>
**Blocker:** <None. | concise blocker reason>

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Orientation | _/4 | <one line> |
| Path Economy | _/4 | <one line> |
| Continuity | _/4 | <one line> |
| **Total** | **_/12 · _._/4** | **<band>** |

## Issues (most severe first)
- **[P0 · Orientation]** <Name>—<observation>. <impact>. **Fix:** <fix>.
- **[P1 · Path Economy]** <Name>—<observation>. <impact>. **Fix:** <fix>.

## Top 3 moves
1. <highest-leverage change>
2. <next>
3. <next>

## Next
- **Structural** (do first): <what changes what the journey *is*—steps to cut or merge, a branch to manage, a dead end to close, state to carry, an entry point to re-route>
- **Executional** (after): <what changes how a step *looks or reads*—indicator weight, Back label wording, transition motion>
- **Hand off**: <anything that is not this flow's problem—single-screen layout or hierarchy goes to Focal; "None" if all of it is Compass's>
```

Filling it:
- **Issues**—repeat the issue line once per issue, tagged **Orientation / Path Economy / Continuity**. `<observation>` may run two or three sentences when you are being specific and quantitative; the rest stay tight. If nothing ranks above P3, write "None above P3." under the header and keep the header.
- **Next**—structural before executional, always: signposting a maze only labels the dead ends. Resolve structural items with the four-move build workflow in [SKILL.md](../SKILL.md) and the techniques in [patterns.md](patterns.md).
- **Single-screen problems are out of scope—route them to [Focal](../../focal).** If an individual screen is overloaded, mis-ranked, or has no clear primary action, that is a within-screen failure for Focal, not a seam for Compass; name it in **Next** and hand it off.
- Re-run the audit after fixes to watch the score climb.
