# Compass—single-file bundle

This is the complete **Compass** skill as one self-contained document—the spine plus every reference—so you can use it in any AI coding agent, not only Claude Code.

**How to use it**
- **Claude Code**—you don't need this file; install the `compass/` folder from the repo for `/compass` and on-demand loading. This bundle is for everything else.
- **Codex (CLI)**—append it to your project's `AGENTS.md`, which Codex loads automatically: `cat compass.md >> AGENTS.md`.
- **ChatGPT**—create a Custom GPT and paste this into *Instructions*, or upload it as a *Knowledge* file. A Project works the same way.
- **Cursor / Windsurf / Cline**—add it as a rules file, e.g. `.cursor/rules/compass.md`.

Everything below is the skill.

---


# Compass

**Never lost.**

A flow is a sequence of screens with a destination. Good cross-screen UX means the user never has to wonder *Where am I? How far is left? How do I get back, or out?* The moment they can't answer one of those, the flow becomes a maze—and people abandon mazes.

Where Focal sharpens a single screen (one screen, one purpose), Compass guides the **path between screens**. Focal is *within* a screen; Compass is *between* them. Together they cover the whole product: every screen knows its job, and every journey knows its way.

Three disciplines, treated as top priorities, keep the user oriented:

- **Orientation**—at every step, position, progress, and a way back or out.
- **Path Economy**—the fewest honest steps to the destination.
- **Continuity**—context and state survive the seams between screens.

**Orientation is the load-bearing discipline**—it's the literal promise. Economy and Continuity make the journey short and seamless, but a short, seamless journey where the user still feels lost has failed. Weight orientation the most.

---

## When to use

Compass is for **cross-screen flows** in functional products—any platform, any user. Onboarding, signup, checkout, multi-step setup, wizards, dashboards with drill-down, account flows, anything that spans more than one screen. If the user has to *move between screens* to get something done, Compass applies.

It is **not** for:
- Single-screen layout and structure—that's Focal. Compass assumes each screen is already sound and focuses on the joins.
- Marketing pages, landing pages, campaigns—persuasion and narrative, not task completion.
- Whole-app sitemaps generated from a spec (deciding *which* screens exist before any flow is drawn).
- Backend, infra, or non-UI work.

**Scope.** Compass is a *lens* for movement and orientation—*the path, the signage, and the seams between screens*—not a renderer. It decides the steps, where the user is told what, and how state carries across. The execution of color, type, motion, and copy is left to your own design system and tooling, and the design of each individual screen is left to Focal.

---

## The methodology—Never Lost

The north star. At every step of a flow, the user can answer three questions without thinking:

1. **Where am I?** (position in the journey)
2. **How far is left?** (progress and scope)
3. **How do I get back, or out?** (a retreat that never traps them)

A flow that answers all three the whole way through feels effortless. A flow that drops even one feels like being lost in a building with no signs.

- **The destination test.** Name the one outcome the flow exists to reach: *"This flow gets the user from ___ to ___."* If it has two destinations, it's two flows—split it.
- **The drop test.** Drop the user onto any screen in the middle of the flow with no memory of how they arrived. Can they tell where they are, what's left, and how to proceed or retreat? If not, orientation has failed at that step.

---

## The three disciplines

### 1. Orientation—where am I, and how do I get out *(load-bearing)*

The user is never without their bearings. This is the promise; the other two disciplines serve it.

- **Show position and progress.** "Step 2 of 4," a breadcrumb, an active nav state. Frame progress as achievable milestones ("Step 2 of 4"), never a demoralizing tally ("12 of 47 done").
- **Always a way back.** A real Back on every screen, and an escape hatch (Cancel / Close / Save & exit) out of every flow. Nothing traps the user—especially modals and multi-step wizards.
- **No dead ends.** Every screen has a clear next step or a clear way out. A screen the user can reach but not leave is a bug, not a state.
- **Signal the current location.** The user should always be able to point at where they are in the app's structure.

> **Fails:** no Back; trapped modals; hidden progress; dead-end screens; "wait, how did I get here?"; a flow with no Cancel.

### 2. Path Economy—the fewest honest steps

Every screen in a flow is a tax on the user. Cut the tax to the minimum the task honestly requires.

- **Fewest steps to the destination.** Cut redundant screens; merge needless round-trips; collapse two steps into one where it doesn't overload (defer to Focal for whether a single screen is overloaded).
- **Defaults skip steps.** Don't ask what you can infer or pre-fill. The best step is the one the user never has to take.
- **No setup walls.** Don't gate the value behind six configuration screens. Get the user to the first real win, then deepen.
- **The honest-path caveat (read this).** Shorten the path by removing *waste*, never by removing *protection*. Skipping a confirmation on a destructive or costly action, hiding a required disclosure, or burying the price to "reduce friction" is a dark pattern, not economy. A step that protects the user or earns their trust is not waste.

> **Fails:** the 7-step flow that's really 3; redundant confirmations; setup walls before first value; branches that dead-end; "friction reduction" that hides cost or consequence.

### 3. Continuity—the seams hold

Moving between screens shouldn't cost the user anything they already gave or already knew.

- **No memory bridge.** A fact the user needs at step 3 is shown at step 3—never "remember the code from the previous screen."
- **State survives.** Back never wipes entered data. A refresh, an interruption, or a return tomorrow resumes where they left off, not at the start.
- **Honor the entry point.** A deep link, a notification, or a search result lands the user *in context*—on the relevant screen mid-flow—not dumped at step one.
- **Preserve the mental model.** Each screen should feel like it came from the last: consistent layout anchors, predictable transitions, the same object in focus.

> **Fails:** form data lost on Back; deep links dumping you at the start; the memory bridge; a "resume" that resets; jarring jumps that break the sense of one continuous task.

---

## How they combine—order of operations

1. **Name the destination** (methodology). One outcome the flow reaches.
2. **Map the path** (Path Economy). The fewest honest steps from entry to destination.
3. **Signpost it** (Orientation). Position, progress, back, and exit on every step.
4. **Join the seams** (Continuity). Carry context and state across each transition.

You can't signpost or join a path you haven't mapped, and you can't map a path without knowing where it ends. Orientation leads the *promise* but comes after the path exists—the signage goes up once the road is laid.

---

## Registers—flow types

The disciplines assume a **linear** flow by default. Three other shapes are legitimate, and the rules bend for them.

| | Linear | Branching | Hub-and-spoke | Open-ended |
|---|---|---|---|---|
| **Shape** | one path, start to end | path forks on user choice | center → detail → back to center | wander a space, no fixed end |
| **Examples** | checkout, onboarding, setup | conditional signup, "what brings you here?" | dashboard → record → dashboard | browse, search-and-refine, exploration |
| **Orientation focus** | progress to the end | which branch + how to switch it | "back to center" is sacred; the hub is home base | "where am I in the space" + easy return, not progress |
| **Economy focus** | cut steps on the one path | prune dead branches; default the common branch | minimize hops to a record and back | let the user roam; don't force a funnel |

**Open-ended is the exception that proves the rule:** there's no single destination, so "how far is left" doesn't apply and "Never Lost" reduces to *always know where you are and how to get home*. (This is the journey-level sibling of Focal's exploration register.)

**Expertise dial:** novices want guardrails—guidance, confirmations, one clear path. Experts want skips, shortcuts, remembered choices, and not to be re-asked. How many steps feel "economical" scales with who's traveling.

---

## Routing

- **No argument** → explain Never Lost and the three disciplines briefly, then ask: building a new flow, or reviewing an existing one?
- **`build` (or a description of a flow to design)** → follow **The four moves** below. Pull techniques from reference/patterns.md.
- **`review` / `audit` (a flow, a set of screens, a prototype, or a description)** → load and follow reference/review.md. It runs the three-discipline audit and produces a scorecard.
- **A question about a specific technique or anti-pattern** → consult reference/patterns.md.

---

## Build: the four moves

For each flow, in order. Write the answers down—they are the spec.

1. **Name the destination.** *"This flow gets the user from ___ to ___."* One outcome. Note the flow type and audience.
2. **Map the fewest honest steps.** List every screen the user must pass through. Cut redundant ones, merge round-trips, default what you can—but keep every step that protects or informs.
3. **Signpost every step.** For each screen: position/progress, a real Back, and an escape hatch. No dead ends.
4. **Join the seams.** For each transition: what context carries forward, what state must survive Back/refresh, and where entry points (deep links) land.

Then run the gates:
- [ ] One destination, no "and"?
- [ ] Every step earns its place (no waste), and nothing protective was cut?
- [ ] Every screen shows where-you-are and offers back + exit?
- [ ] No memory bridge; state survives Back and resume; deep links land in context?
- [ ] Drop test passes on every screen?

A flow that passes is sound by Compass's standard. Then design each screen with Focal, and apply visual styling and motion on top.

---

## Voice (when giving feedback)

- **Lead with the answer, then structure it.** Open every build or review with one line—the verdict, or the flow's destination—then the locked template (the build template is below; the review template is in reference/review.md). Use it verbatim; don't add, remove, reorder, or rename sections.
- **Be specific and quantitative.** "This is a 7-step flow that needs 3" beats "too many steps." Count the steps, name the dead ends, quote the labels.
- **Be decisive.** "The user is trapped on step 3"—not "the user might feel stuck."
- **Factual first, then judgment, then the fix.** What happens, why it loses the user, what it should be.
- **Tie every issue to a discipline,** and to how it costs the user their bearings.

---

## Build output—the Flow Spec (use this exact structure)

Every build returns this template verbatim, in this order. Fill the `<…>` slots; keep every fixed label.

```
**Flow:** <name>—gets the user from <entry> to <destination>.
**Type:** linear | branching | hub-and-spoke | open-ended   ·   **Audience:** novice | mixed | expert

## Steps
1. <screen>—<its job> [+ default/skip that removes a step, if any]
2. <screen>—<its job>
(fewest honest steps; note any you merged or cut)

## Orientation
- Position/progress: <how each step shows where-you-are and how far is left>
- Back + exit: <the Back and the escape hatch available on every step>

## Continuity
- Carries forward: <context passed across steps>
- Survives: <state kept on Back / refresh / resume>
- Entry points: <where deep links / notifications land>

## Gates
- [x] One destination, no "and"
- [x] Every step earns its place; nothing protective cut
- [x] Where-am-I + back + exit on every step
- [x] No memory bridge; state survives; deep links land in context
- [x] Drop test passes on every screen
```

---

## Absolute don'ts

- **Dead ends.** (Orientation) Every screen has a next step or a way out.
- **No Back, or a trapped modal.** (Orientation) A real Back and an escape hatch, always.
- **Hidden progress.** (Orientation) In a multi-step flow, show where they are and how far is left.
- **The setup wall.** (Path Economy) Don't gate first value behind a pile of configuration.
- **Shortening the path by hiding cost or skipping protection.** (Path Economy) That's a dark pattern, not economy.
- **The memory bridge.** (Continuity) Never make the user carry a fact between screens in their head.
- **Losing state on Back.** (Continuity) Back is not a reset.
- **Deep link to step one.** (Continuity) Land the user where they were headed, in context.

---

## References

- reference/review.md—the three-discipline flow audit, the Compass scorecard (0–4 per discipline), severity, and output format.
- reference/patterns.md—orientation patterns, step-reduction techniques, continuity/state patterns, flow-type playbooks, and the anti-pattern library with fixes.
- reference/examples.md—a worked flow review and a worked flow build, in the locked output templates.


---

# Compass Review—the three-discipline flow audit

Evaluate a flow (or a set of screens) against the three disciplines and the overarching methodology, then return a scorecard with prioritized, concrete fixes. Use when the user asks to review, critique, audit, or "what's wrong with" any multi-screen flow, journey, or navigation in a functional product, app, or tool.

## Input modes

- **A described flow**—the user narrates the steps ("they sign up, pick a plan, then…"). Map it as a sequence, name the destination, and audit the path you reconstruct. State the steps back so the user can correct your mental model before you score it.
- **A set of screens or screenshots**—read them in order, infer the transitions between them, and critique the joins. You're judging the *seams*, not each screen—a beautiful screen in the wrong order, or one that drops state on the way in, still fails. Per individual screen layout, defer to Focal.
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

- **Structural**—the destination is unclear or doubled, steps to cut or merge, a branch to manage, a dead end to close, state to carry across a seam, an entry point to re-route. These change what the *journey is*. Resolve them first with the four-move build workflow in SKILL.md, and pull techniques from patterns.md.
- **Executional**—the visual weight of a progress indicator, the wording of a Back label, the motion of a transition, the styling of a screen. These change how a step *looks or reads*. Apply them in your own design system once the path is sound.

Always fix structural before executional: signposting a maze only labels the dead ends. **Single-screen problems are out of scope—route them to Focal.** If an individual screen in the flow is overloaded, mis-ranked, or has no clear primary action, that's a within-screen failure for Focal, not a seam for Compass; note it and hand it off. Re-run the audit after fixes to watch the score climb.

---

# Compass Patterns—techniques and anti-patterns

The working catalog behind the three disciplines. Pull from here when building a flow or when prescribing a fix in a review. Ordered the way the disciplines apply: Orientation → Path Economy → Continuity.

Orientation is the load-bearing discipline—it's the literal promise. When two fixes compete for attention, the one that restores the user's bearings wins.

---

## Orientation patterns (Discipline 1—load-bearing)

How to make sure the user can always answer *Where am I? How far is left? How do I get back, or out?*

- **Progress as milestones, not a tally.** A stepper that reads "Step 2 of 4" promises an end the user can picture. "12 of 47 complete" reads as a sentence. Frame progress as a small count of named, achievable stages; if the real count is large, group it ("Account → Payment → Review", not "field 14 of 38"). Defer to Focal for whether any one step is overloaded—Compass owns the count of steps, not the contents of one.
- **Breadcrumbs and active state.** On hub-and-spoke and any nested structure, the user must be able to point at where they are: a breadcrumb trail back to the hub, a highlighted nav item, a screen title that matches the link they followed. Recognition beats recall—the path home should be readable, not remembered.
- **A real Back on every screen.** Not just the browser button, and not a Back that secretly resets. Every screen in a flow has a visible, reliable way to the previous step. If Back would lose work, that's a Continuity failure too (see below)—fix both.
- **Escape hatches and Cancel.** Every flow needs a way *out*, not just back: Cancel, Close, "Save & exit," or "Do this later." Back retreats one step; the escape hatch leaves the flow entirely. A multi-step wizard with no Cancel is a trap with a polite face.
- **Never-trap modals.** A modal is the easiest place to strand someone. Every modal closes—an X, an explicit Cancel, click-outside, or Esc—and closing it returns the user to a known place, not a blank. A modal that opens another modal that has no close is the canonical maze.
- **No dead ends.** Every screen has a clear next step *or* a clear way out. A screen the user can reach but not leave is a bug, not a state—success screens, error screens, and edge-case screens included.
- **The drop test.** Drop the user onto any screen mid-flow with no memory of how they arrived. Can they tell where they are, what's left, and how to proceed or retreat? Run it on every screen. The screen that fails the drop test is exactly the screen where users report feeling lost.

**Test:** strip a screen of its content and leave only its signage—the title, the progress indicator, the Back, the exit. Can a stranger say what flow this is, where in it they sit, and how to leave? If not, orientation has failed before any step is taken.

---

## Step-reduction techniques (Discipline 2—Path Economy)

Every screen in a flow is a tax on the user. Cut the tax to the minimum the task *honestly* requires. Match the technique to *why* a step exists.

| Technique | Use when | Example |
|-----------|----------|---------|
| **Merge round-trips** | Two screens bounce the user back and forth, each doing half a job | Pick item → separate confirm screen → back to list, collapsed into pick-and-confirm in place |
| **Smart defaults that skip a step** | One choice is right for most users | Pre-selected shipping method, pre-filled country from locale, "remember this" honored |
| **Infer rather than ask** | The system already knows or can derive the answer | Detect card type from the number; pull name from the signed-in account; geolocate the city |
| **First value before setup** | Value is gated behind configuration | Show the populated app with sensible defaults, defer settings to when they're relevant |
| **Prune dead branches** | A fork leads somewhere with no real continuation | Remove the option that dead-ends; or give that branch a real next step |
| **Collapse adjacent steps** | Two thin screens fit comfortably on one without overload | Merge name + email into one screen—*defer to Focal for whether the merged screen is now too heavy* |

**Choosing well:**
- The best step is the one the user never has to take. Before adding a screen, ask whether its answer can be inferred, defaulted, or deferred.
- Count honestly. "This is a 7-step flow that needs 3" is a finding; "feels long" is a feeling.
- Shortening a path is a Focal handoff at the boundary: Compass merges *screens*, Focal judges whether the merged screen overloads. Don't collapse steps so aggressively that each screen breaks One Screen, One Purpose.

**The honesty caveat—read this.** Shorten the path by removing *waste*, never by removing *protection*. Skipping a confirmation on a destructive or costly action, hiding a required disclosure, auto-opting the user into something, or burying the price to "reduce friction" is a **dark pattern, not economy**. A step that protects the user or earns their trust is not waste—it is load-bearing. If removing a step makes the flow shorter but the user worse off, you have not practiced Path Economy; you have laundered a trap as a convenience.

---

## Continuity patterns (Discipline 3)

Moving between screens shouldn't cost the user anything they already gave or already knew. The seams between screens are where flows leak.

- **No memory bridge.** Never make the user carry a fact from one screen to the next in their head. If step 3 needs the code, the amount, or the choice from step 1, *show it on step 3*. The tell is any instruction shaped like "remember this for later."
- **Preserve state on Back.** Back is a retreat, not a reset. Returning to a previous step shows everything the user already entered, still filled in. A Back that wipes the form teaches users to fear the button that's supposed to be their safety net.
- **Survive refresh and resume.** An accidental reload, a closed tab, a return tomorrow—the flow picks up where it was left, not at step one. Persist progress so "resume" actually resumes. A "resume" that resets is worse than no resume, because it promised.
- **Land deep links in context.** A notification, a shared URL, a search result, or an email link drops the user *on the relevant screen, mid-flow*—already oriented—not dumped at the entrance to find their own way back. If the link says "your order shipped," it lands on that order, not the home screen.
- **Preserve the mental model across transitions.** Each screen should feel like it came from the last: stable layout anchors, the same object kept in focus, predictable forward/back motion. A jarring jump—a different layout, a lost selection, a surprise full-screen takeover—breaks the sense of one continuous task even when no data was lost.

**Test:** at each seam between two screens, ask what the user knew and had on the first that they need on the second. If anything required must be re-entered, re-found, or re-remembered, the seam leaks—close it by carrying it forward.

---

## Flow-type playbooks

The disciplines assume a **linear** flow by default. The other three shapes are legitimate; one short play each.

**Linear**—*one path, start to end (checkout, onboarding, setup).*
Make the end visible from the start: a milestone stepper so "how far is left" is answerable on every screen. Spend your Economy budget on the single path—every step you cut is felt by every user. Back walks the path in reverse with state intact; the escape hatch leaves the whole flow.

**Branching**—*path forks on user choice (conditional signup, "what brings you here?").*
Orientation owns two extra jobs: show *which branch* the user is on, and offer a cheap way to *switch it* if they forked wrong. Economy means defaulting the common branch and pruning any branch that dead-ends. The drop test is sharpest here—a user dropped mid-branch must still know which fork they took.

**Hub-and-spoke**—*center → detail → back to center (dashboard → record → dashboard).*
"Back to center" is sacred: the hub is home base, and every spoke returns to it predictably (breadcrumb, a persistent "Back to dashboard," the same hub state they left). Economy is measured in *hops*—minimize the taps to reach a record and return. Don't trap the user deep in a spoke with no clear road home.

**Open-ended**—*wander a space, no fixed end (browse, search-and-refine, exploration).*
The exception that proves the rule: there's no single destination, so "how far is left" doesn't apply, and **Never Lost reduces to *always know where you are and how to get home*.** Orient by position-in-space (filters applied, current view, breadcrumb) and guarantee an easy return to a known anchor. Don't force a funnel onto a space meant for roaming. (Journey-level sibling of Focal's exploration register.)

---

## Flow-state care

The states most flows neglect—where a journey is interrupted, aborted, broken, or finished. Each is a Compass surface with its own orientation, economy, and continuity demands.

- **Interruption and resume.** Users leave mid-flow—a call, a closed laptop, a dead battery. Persist progress and let them re-enter where they stopped, oriented ("You're on step 3 of 4"), with prior input intact. Resume is a Continuity promise; breaking it is the single most common reason a started flow is never finished.
- **Partial completion.** A flow abandoned at step 3 isn't a failure to discard—it's progress to honor. Save the draft, the half-filled cart, the in-progress application; surface it on return so the user picks up rather than starts over. The fastest path to finishing is not making them re-do what's done.
- **Error mid-flow.** When a step fails (payment declined, validation, a server error), keep the user *in the flow* and *in place*. Name the actual problem, offer the fix, preserve everything already entered, and keep Back and exit live. An error that boots the user to step one, or to a dead screen, converts a recoverable hiccup into an abandonment.
- **Returning from a success screen.** The end of a flow is a transition, not a wall. A success screen needs a clear next move—back to the hub, on to the obvious next task, or out—never a celebratory dead end the user has to use the browser Back to escape. End on a high *and* on a door (peak-end, the journey-level sibling of Focal's peak-end care).

---

## Anti-pattern library

Each entry: the tell—the discipline it breaks—the fix.

- **The trapped modal**—a dialog with no X, no Cancel, no Esc, no click-outside. *(Orientation)* Give every modal a close that returns to a known place.
- **The dead-end screen**—a screen the user can reach but not leave; no next step, no way out. *(Orientation)* Every screen gets a clear next step or an exit—success and error screens included.
- **The hidden progress bar**—a multi-step flow with no indication of position or length. *(Orientation)* Add a milestone stepper; show where they are and how far is left.
- **The demoralizing tally**—progress shown as "12 of 47" instead of named stages. *(Orientation)* Reframe as a small count of achievable milestones; group the rest.
- **The phantom Back**—a Back button that resets the flow or wipes entered data. *(Orientation + Continuity)* Make Back a true retreat that preserves state.
- **The mystery location**—nested screens with no breadcrumb or active state; "how did I get here?" *(Orientation)* Add a trail or active nav so the user can point at where they are.
- **The setup wall**—first value gated behind six configuration screens. *(Path Economy)* Get the user to one real win on sensible defaults; defer setup to when it's relevant.
- **The phantom flow**—a 7-step flow that's honestly 3, padded with redundant confirm-and-return screens. *(Path Economy)* Merge the round-trips; cut the steps the task doesn't require.
- **The needless round-trip**—two screens bounce the user back and forth, each doing half a job. *(Path Economy)* Collapse into one—then check with Focal that the merged screen isn't overloaded.
- **The dead branch**—a fork leads to a screen with no real continuation. *(Path Economy)* Remove the branch, or give it a genuine next step.
- **The friction-hiding shortcut**—a step removed by burying the price, skipping a confirmation, or auto-opting the user in. *(Path Economy)* Restore it. This is a dark pattern, not economy—protection is never waste.
- **The memory bridge**—step 3 needs a fact only shown on step 1. *(Continuity)* Carry the context forward; show it where it's needed.
- **The state-eating Back**—returning to a step shows it blank instead of as the user left it. *(Continuity)* Persist input across Back and forward.
- **The amnesiac resume**—a "resume" or refresh that drops the user back at step one. *(Continuity)* Persist progress so resume actually resumes.
- **The deep link to nowhere**—a notification or shared URL dumps the user at the home screen instead of the relevant screen. *(Continuity)* Land them in context, mid-flow, already oriented.
- **The jarring jump**—a transition that changes layout, loses the focused object, or surprises with a takeover. *(Continuity)* Keep layout anchors and the in-focus object stable across the seam.

---

## Quick reference card

```
DESTINATION  "This flow gets the user from ___ to ___."   (one outcome, no "and")
STEPS        fewest honest steps · merge round-trips · default/infer/defer · no dead branches
ORIENT       every screen: where-am-I + how-far-left + a real Back + an exit
CARRY        no memory bridge · state survives Back/refresh/resume · deep links land in context
NEVER        trap a modal · hide progress · shorten by hiding cost or skipping protection
```

*Defaults for a linear flow. On hub-and-spoke, "back to center" is sacred; on open-ended, drop "how-far-left" and guarantee a way home.*

See ../SKILL.md for the disciplines and the Flow Spec, and review.md for the three-discipline audit and scorecard.

---

# Compass Examples

Two worked examples showing the quality bar and the locked output templates in use—one **review**, one **build**. They share a narrative: the review flags a maze-like checkout that traps the user, loses their data, and strands returning shoppers; the build redesigns that same flow so the user is never lost. Illustrative, not a real product.

---

## Example 1—Review: a maze-like checkout

**Input (what was handed in):** the checkout flow of a storefront. A 6-step wizard (Cart → Account → Shipping → Billing → Review → Confirm) that opens inside a full-screen modal with no Close. Each step replaces the last; the only Back is the browser's, which wipes everything entered. Shipping cost and taxes appear for the first time on step 5. A "Sign in to continue" wall blocks step 2 for everyone. Returning users who tap the emailed "Resume your order" link land on step 1 with an empty cart. There is no step indicator anywhere.

**Compass's output:**

```
**Verdict:** No · the user is trapped in a modal, loses data on Back, and returning links dump them at step one · **3/12**

**Flow:** Storefront checkout · type: linear · audience: mixed

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Orientation | 1/4 | No step indicator, no in-flow Back, no Close—the modal traps the user |
| Path Economy | 1/4 | 6 steps for a 3-step job; a sign-in wall gates checkout; cost hidden until step 5 |
| Continuity | 1/4 | Back wipes entered data; the "Resume" deep link lands at step 1 with an empty cart |
| **Total** | **3/12** | **broken** |

## Issues (most severe first)
- **[P0 · Orientation]** Trapped modal—the flow opens in a full-screen modal with no Close and no in-flow Back; only the browser Back, which exits the whole modal. The user is trapped: no way out that isn't "lose everything." **Fix:** a real Back on every step and a persistent "Save & exit"—nothing should trap the user in a modal.
- **[P0 · Continuity]** Back wipes data—browser Back wipes every field entered so far; the user re-types shipping and billing from scratch. **Fix:** persist step state so Back returns to the previous step with its data intact. Back is not a reset.
- **[P0 · Continuity]** Resume lands empty—the emailed "Resume your order" link deep-links returning users to step 1 with an empty cart; the order they were resuming is gone. **Fix:** the deep link lands them on the step they left, cart and entered data restored. Honor the entry point.
- **[P1 · Path Economy]** Sign-in wall—a "Sign in to continue" wall blocks step 2 for everyone, including first-time buyers who don't have an account. **Fix:** offer guest checkout; collect the email at shipping and invite account creation *after* the purchase, not as a gate before it.
- **[P1 · Path Economy]** Six steps for three—a job that's honestly three (identify, pay, confirm) is spread across six screens. Account and Billing are separable steps that each demand a full round-trip. **Fix:** merge Account into Shipping (one contact-and-address screen) and Billing into Review (pay where you confirm)—three steps, not six.
- **[P1 · Path Economy]** Cost hidden until step 5—shipping cost and taxes appear for the first time on step 5 (Review), after the user has invested five screens. **Fix:** show the running total from the first step it can be estimated. Surfacing cost early is honest economy; hiding it to shorten the felt path is the dark pattern—the honest-path caveat, not friction reduction.
- **[P2 · Orientation]** No step indicator—nothing tells the user where they are or how far is left. The drop test fails on every screen. **Fix:** a "Step 2 of 3" marker or labeled progress on every step.

## Top 3 moves
1. Free the user—add a real Back and a "Save & exit" to every step, and persist state so Back and resume never lose data.
2. Cut six steps to three honest ones, drop the sign-in wall for guest checkout, and surface the total from the start.
3. Fix the "Resume" deep link to land returning users on the step they left, cart restored—and add a "Step X of 3" indicator throughout.
```

---

## Example 2—Build: the redesigned checkout

**Input:** "Redesign the checkout flow we just reviewed—fewer steps, full orientation, nothing lost."

**Compass's output:**

```
**Flow:** Storefront checkout—gets the user from a full cart to a confirmed order.
**Type:** linear   ·   **Audience:** mixed

## Steps
1. Cart—review items and see the running total (subtotal + estimated shipping/tax) before committing [default: skip if entered from a "Buy now" deep link with one item]
2. Details—contact email + shipping address on one screen; guest by default, "create an account" offered, not required [merged the old Account + Shipping steps]
3. Pay & confirm—payment, final total, and the confirm action on one screen [merged the old Billing + Review steps; order placed here]
(six steps cut to three honest ones; sign-in wall removed—account creation moved to after purchase)

## Orientation
- Position/progress: a "Step 1/2/3 of 3" marker labeled Cart · Details · Pay on every screen; the running total is visible from step 1 forward
- Back + exit: a real Back on steps 2 and 3 that returns to the prior step intact; a persistent "Save & exit" on every step that preserves the cart and drops the user back on the storefront—no trapping modal

## Continuity
- Carries forward: cart contents and running total carry from step 1; email and shipping address carry from step 2 into the step-3 total and confirmation
- Survives: Back returns to the previous step with its fields intact; a refresh or a return tomorrow resumes on the last step reached with the cart and entered data restored—never a reset
- Entry points: the emailed "Resume your order" link lands on the exact step the user left, cart and details restored; a "Buy now" deep link enters at step 2 with the single item already in the cart

## Gates
- [x] One destination, no "and"
- [x] Every step earns its place; nothing protective cut
- [x] Where-am-I + back + exit on every step
- [x] No memory bridge; state survives; deep links land in context
- [x] Drop test passes on every screen
```

---

**Why these two:** the review never just lists problems—it ties every issue to a discipline and ends on three ranked moves. The build never returns prose—it returns the same Flow Spec every time. And the second example resolves the first: "cut six steps to three, free the user, restore the resume link" becomes an actual three-step flow where the user always knows where they are, what's left, and how to get back or out. That is the whole method in motion—never lost, in both directions.

Note the honest-path line running through both: the review's fix for hidden cost is to *surface* the total earlier, and the build shows it from step 1. Shortening the felt path by hiding the price or dropping the sign-in protection would be a dark pattern, not Path Economy. The cuts here remove waste (redundant round-trips, a needless gate), never protection.

Once the path is sound by Compass's standard, design each screen with Focal—see review.md for the full scorecard method and patterns.md for the step-reduction and continuity patterns behind these fixes. The spine is in ../SKILL.md.