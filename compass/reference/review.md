# Compass Review—the three-discipline flow audit

Evaluate a flow (or a set of screens) against the three disciplines and the overarching methodology, then return a scorecard with prioritized, concrete fixes. Use when the user asks to review, critique, audit, or "what's wrong with" any multi-screen flow, journey, or navigation in a functional product, app, or tool.

## Input modes

- **A described flow**—the user narrates the steps ("they sign up, pick a plan, then…"). Map it as a sequence, name the destination, and audit the path you reconstruct. State the steps back so the user can correct your mental model before you score it.
- **A set of screens or screenshots**—read them in order, infer the transitions between them, and critique the joins. You're judging the *seams*, not each screen—a beautiful screen in the wrong order, or one that drops state on the way in, still fails. Per individual screen layout, defer to [Focal](../../focal).
- **A clickable prototype / live URL**—if browser automation is available, walk the flow: click through, hit Back, refresh mid-flow, follow a deep link cold. Otherwise audit the described or captured steps. Always test the transitions, not just the destinations—the failures live between screens.

## Step 0—Notice the journey, name the destination, classify the flow

Before judging, *walk it*. Most people glance at one screen; a reviewer traces the whole path. Count the steps. Read the progress indicators and Back affordances verbatim. Note what each transition carries and what it drops. Try to get lost. The specificity of your observation is the ceiling on the quality of your critique.

Then frame, in one or two sentences each:
- **What is this journey?** Product type, what the flow is for, where it starts and ends.
- **Name the destination.** State it as *"This flow gets the user from ___ to ___."* One outcome. If it needs an "and," it's two flows wearing one coat—flag the split now; the gates will show why.
- **What's the user's state?** Anxious, rushed, first-time, returning, interrupted, one-handed? A checkout under time pressure tolerates fewer steps than a leisurely setup. A flow resumed after a phone call must survive the interruption. Name it; the critique must respect it.
- **What's the bar?** Every flow category has an invisible standard set by its best-in-class journey. A checkout is judged against the cleanest checkouts; an onboarding against the clearest onboardings; a multi-step setup against the cleanest wizard in the category. Ask: *what would the best-in-class flow do at this seam?*
- **The flow type.** Classify it: **linear** (one path, start to end), **branching** (path forks on a user choice), **hub-and-spoke** (a center the user leaves and returns to), or **open-ended** (wander a space, no fixed end). This sets how the gates should be read—see *Adjust for flow type* below. If you can't tell, it's usually a linear flow with an unmanaged branch bolted on—score it linear and flag the rogue fork under Gate 1.

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
| 0 | User is lost or trapped—a dead end, a no-Back screen, or a flow with no exit |
| 1 | Hidden progress, missing Back, or a modal with no escape; the drop test fails on a key screen |
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
| 0 | A maze—far more steps than the task needs, or branches that dead-end |
| 1 | Bloated path; a setup wall before first value; or a "shortcut" that hides cost or skips protection |
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

## The scorecard

Present scores as a table. Be honest—a 4 means genuinely seamless, not "fine."

| Discipline | Score | Key finding |
|------------|-------|-------------|
| Orientation | ?/4 | [specific finding] |
| Path Economy | ?/4 | [specific finding] |
| Continuity | ?/4 | [specific finding] |
| **Total** | **?/12** | **[band]** |

**Bands:** 11–12 ship it · 8–10 solid, fix the weak discipline · 5–7 significant rework · 0–4 broken.

**The verdict—Never Lost.** This becomes the **Verdict** line at the very top of the output (see Output format): at every step, does the user know where they are, what's left, and how to get back or out—yes or no? The total measures how close the flow gets; the verdict states whether it arrives. **A failed drop test or a dead end is blocking regardless of total**—a flow can score moderately and still fail the verdict if it strands the user at one step.

## Issues and severity

List the issues found, ordered by severity, not by discipline. Tag each:

| Priority | Meaning |
|----------|---------|
| **P0** | Loses or traps the user, or breaks trust (dead end, no Back, lost state, hidden cost)—fix now |
| **P1** | Causes real confusion or bloat (hidden progress, a setup wall, a memory bridge)—fix before release |
| **P2** | Annoyance with a workaround—next pass |
| **P3** | Polish—if time permits |

Order issues by *type* of harm, most severe first: **Orientation** (the user is lost or trapped) → **Path Economy** (the path is longer or less honest than it should be) → **Continuity** (a seam drops context or state). A user who is lost outranks a path that is merely long.

For each issue:
> **[P? · Discipline] Name**—what happens (factual, specific, counted; quote the labels). Why it loses *this* user in *this* state, and how it costs the flow its promise. The concrete fix.

## Output format—use this exact structure

Every review returns this template verbatim, in this order. Same sections, same headers, same table columns, same issue-line format. Don't add, remove, reorder, or rename sections. Fill the `<…>` slots; keep each fixed label.

```
**Verdict:** <never lost—yes or no> · <the single biggest break, one phrase> · **<total>/12**

**Flow:** <name> · type: <linear | branching | hub-and-spoke | open-ended> · audience: <novice | mixed | expert>

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Orientation | _/4 | <one line> |
| Path Economy | _/4 | <one line> |
| Continuity | _/4 | <one line> |
| **Total** | **_/12** | **<band>** |

## Issues (most severe first)
- **[P0 · Orientation]** <Name>—<observation>. <impact>. **Fix:** <fix>.
- **[P1 · Path Economy]** <Name>—<observation>. <impact>. **Fix:** <fix>.
(if nothing above P3, write "None above P3." and keep this header)

## Top 3 moves
1. <highest-leverage change>
2. <next>
3. <next>
```

Bands: **11–12** ship it · **8–10** solid, fix the weak discipline · **5–7** significant rework · **0–4** broken. **A failed drop test or a dead end is blocking regardless of total.** Tag issues with the discipline names **Orientation / Path Economy / Continuity**.

## Next steps

Close by sorting the fixes into two buckets and ordering the work:

- **Structural**—the destination is unclear or doubled, steps to cut or merge, a branch to manage, a dead end to close, state to carry across a seam, an entry point to re-route. These change what the *journey is*. Resolve them first with the four-move build workflow in [SKILL.md](../SKILL.md), and pull techniques from [patterns.md](patterns.md).
- **Executional**—the visual weight of a progress indicator, the wording of a Back label, the motion of a transition, the styling of a screen. These change how a step *looks or reads*. Apply them in your own design system once the path is sound.

Always fix structural before executional: signposting a maze only labels the dead ends. **Single-screen problems are out of scope—route them to [Focal](../../focal).** If an individual screen in the flow is overloaded, mis-ranked, or has no clear primary action, that's a within-screen failure for Focal, not a seam for Compass; note it and hand it off. Re-run the audit after fixes to watch the score climb.