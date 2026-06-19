---
name: compass
description: Use when designing, building, reviewing, or critiquing a multi-screen flow, journey, or navigation in any functional product, app, dashboard, or tool. Compass is the cross-screen lens—it owns the path between screens (navigation, step-count, routing, where "back" goes, state, entry points). Its promise is Never Lost—at every step the user knows where they are, what's left, and how to get back or out. Three disciplines—Orientation (load-bearing), Path Economy (fewest honest steps, no dead ends), and Continuity (context and state survive the seams). Adapts to the flow type (linear, branching, hub-and-spoke, open-ended) and the user's expertise. Pairs with Focal, which designs the individual screens. Triggers on flow, journey, navigation, onboarding, checkout, wizard, multi-step, "too many steps", "back button", "where am I", lost, dead end, routing, breadcrumb, progress. Not for single-screen layout (use Focal), visual styling, copy, code, marketing/landing pages, backend, or non-UI work.
argument-hint: "[build | review] <flow, journey, or description>"
---

# Compass

**Never lost.**

A flow is a sequence of screens with a destination. Good cross-screen UX means the user never has to wonder *Where am I? How far is left? How do I get back, or out?* The moment they can't answer one of those, the flow becomes a maze—and people abandon mazes.

Where [Focal](../focal) sharpens a single screen (one screen, one purpose), Compass guides the **path between screens**. Focal is *within* a screen; Compass is *between* them. Together they cover the whole product: every screen knows its job, and every journey knows its way.

Three disciplines, treated as top priorities, keep the user oriented:

- **Orientation**—at every step, position, progress, and a way back or out.
- **Path Economy**—the fewest honest steps to the destination.
- **Continuity**—context and state survive the seams between screens.

**Orientation is the load-bearing discipline**—it's the literal promise. Economy and Continuity make the journey short and seamless, but a short, seamless journey where the user still feels lost has failed. Weight orientation the most.

---

## When to use

Compass is for **cross-screen flows** in functional products—any platform, any user. Onboarding, signup, checkout, multi-step setup, wizards, dashboards with drill-down, account flows, anything that spans more than one screen. If the user has to *move between screens* to get something done, Compass applies.

It is **not** for:
- Single-screen layout and structure—that's [Focal](../focal). Compass assumes each screen is already sound and focuses on the joins.
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
- **`build` (or a description of a flow to design)** → follow **The four moves** below. Pull techniques from [reference/patterns.md](reference/patterns.md).
- **`review` / `audit` (a flow, a set of screens, a prototype, or a description)** → load and follow [reference/review.md](reference/review.md). It runs the three-discipline audit and produces a scorecard.
- **A question about a specific technique or anti-pattern** → consult [reference/patterns.md](reference/patterns.md).

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

A flow that passes is sound by Compass's standard. Then design each screen with [Focal](../focal), and apply visual styling and motion on top.

---

## Voice (when giving feedback)

- **Lead with the answer, then structure it.** Open every build or review with one line—the verdict, or the flow's destination—then the locked template (the build template is below; the review template is in [reference/review.md](reference/review.md)). Use it verbatim; don't add, remove, reorder, or rename sections.
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

- [reference/review.md](reference/review.md)—the three-discipline flow audit, the Compass scorecard (0–4 per discipline), severity, and output format.
- [reference/patterns.md](reference/patterns.md)—orientation patterns, step-reduction techniques, continuity/state patterns, flow-type playbooks, and the anti-pattern library with fixes.
- [reference/examples.md](reference/examples.md)—a worked flow review and a worked flow build, in the locked output templates.
