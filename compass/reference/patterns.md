# Compass Patterns—techniques and anti-patterns

The working catalog behind the three disciplines. Pull from here when building a flow or when prescribing a fix in a review. Ordered the way the disciplines apply: Orientation → Path Economy → Continuity.

Orientation is the load-bearing discipline—it's the literal promise. When two fixes compete for attention, the one that restores the user's bearings wins.

---

## Orientation patterns (Discipline 1—load-bearing)

How to make sure the user can always answer *Where am I? How far is left? How do I get back, or out?*

- **Progress as milestones, not a tally.** A stepper that reads "Step 2 of 4" promises an end the user can picture. "12 of 47 complete" reads as a sentence. Frame progress as a small count of named, achievable stages; if the real count is large, group it ("Account → Payment → Review", not "field 14 of 38"). Defer to [Focal](../../focal) for whether any one step is overloaded—Compass owns the count of steps, not the contents of one.
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
| **Collapse adjacent steps** | Two thin screens fit comfortably on one without overload | Merge name + email into one screen—*defer to [Focal](../../focal) for whether the merged screen is now too heavy* |

**Choosing well:**
- The best step is the one the user never has to take. Before adding a screen, ask whether its answer can be inferred, defaulted, or deferred.
- Count honestly. "This is a 7-step flow that needs 3" is a finding; "feels long" is a feeling.
- Shortening a path is a [Focal](../../focal) handoff at the boundary: Compass merges *screens*, Focal judges whether the merged screen overloads. Don't collapse steps so aggressively that each screen breaks One Screen, One Purpose.

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
The exception that proves the rule: there's no single destination, so "how far is left" doesn't apply, and **Never Lost reduces to *always know where you are and how to get home*.** Orient by position-in-space (filters applied, current view, breadcrumb) and guarantee an easy return to a known anchor. Don't force a funnel onto a space meant for roaming. (Journey-level sibling of [Focal](../../focal)'s exploration register.)

---

## Flow-state care

The states most flows neglect—where a journey is interrupted, aborted, broken, or finished. Each is a Compass surface with its own orientation, economy, and continuity demands.

- **Interruption and resume.** Users leave mid-flow—a call, a closed laptop, a dead battery. Persist progress and let them re-enter where they stopped, oriented ("You're on step 3 of 4"), with prior input intact. Resume is a Continuity promise; breaking it is the single most common reason a started flow is never finished.
- **Partial completion.** A flow abandoned at step 3 isn't a failure to discard—it's progress to honor. Save the draft, the half-filled cart, the in-progress application; surface it on return so the user picks up rather than starts over. The fastest path to finishing is not making them re-do what's done.
- **Error mid-flow.** When a step fails (payment declined, validation, a server error), keep the user *in the flow* and *in place*. Name the actual problem, offer the fix, preserve everything already entered, and keep Back and exit live. An error that boots the user to step one, or to a dead screen, converts a recoverable hiccup into an abandonment.
- **Returning from a success screen.** The end of a flow is a transition, not a wall. A success screen needs a clear next move—back to the hub, on to the obvious next task, or out—never a celebratory dead end the user has to use the browser Back to escape. End on a high *and* on a door (peak-end, the journey-level sibling of [Focal](../../focal)'s peak-end care).

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
- **The needless round-trip**—two screens bounce the user back and forth, each doing half a job. *(Path Economy)* Collapse into one—then check with [Focal](../../focal) that the merged screen isn't overloaded.
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

See [../SKILL.md](../SKILL.md) for the disciplines and the Flow Spec, and [review.md](review.md) for the three-discipline audit and scorecard.