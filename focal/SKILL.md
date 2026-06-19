---
name: focal
description: Use when reviewing, designing, or decluttering the UX of any functional product, app, dashboard, or tool screen—any platform, any user (novice or expert). Focal is the structure-and-attention lens—it decides what belongs on a screen, what to cut, and how to rank it, across three disciplines—Information Architecture (what's on the screen, how it's organized), Progressive Disclosure (limit what competes at a decision point; reveal complexity only when needed), and Visual Hierarchy (weight matches importance)—culminating in one methodology, One Screen, One (Primary) Purpose. Adapts to the screen's register (task, hub, exploration) and the user's expertise. Triggers on cluttered, overwhelming, "too much on screen", "simplify this screen", "what's the primary action", one screen one purpose, IA, dashboard, admin, onboarding, settings. Not for visual styling (color, type, spacing), motion, design research, code generation, marketing/landing pages, backend, or non-UI work.
argument-hint: "[build | review] <screen, flow, file, or description>"
---

# Focal

**One screen, one (primary) purpose.**

Good UX guides attention. People don't read a screen, they orient on it—scanning for where they are, what matters, and what to do next. Every screen, the moment it appears, has to answer three questions: *Where am I? What matters here? What do I do?* The faster and more certainly it answers, the better it works—whether it's a phone app glanced at one-handed or a dashboard an expert lives in all day. Only the pace and the density change.

Focal's answer is a single methodology: **every screen serves one primary purpose.** A screen with one job is glanceable; a screen with three is a puzzle. Simple, clean UX is not a style—it is the visible result of every screen knowing its one job.

Three disciplines, treated as top priorities, are how you earn that outcome:

- **Information Architecture**—what belongs on the screen, and how it's organized.
- **Visual Hierarchy**—what wins attention once it's there.
- **Progressive Disclosure**—what's shown now, and what waits.

```
                 ┌────────────────────────────────────────────┐
   the outcome   │      ONE SCREEN, ONE (PRIMARY) PURPOSE       │
                 └────────────────────────────────────────────┘
                        ▲              ▲               ▲
   the means     Information      Progressive       Visual
                 Architecture     Disclosure        Hierarchy
                 what belongs     what shows now     what wins
```

Get all three right and the screen settles onto its single purpose on its own. Miss any one and the purpose blurs. **Progressive Disclosure is the load-bearing discipline**—a screen with the right structure and clear hierarchy decays the instant you let complexity pile on, so weight it the most.

---

## When to use

Focal is for **functional interfaces**—the screens of an app, product, or tool, on any platform (mobile, web, desktop, tablet), for any user (first-timer or expert). Onboarding, feeds, home screens, settings, dashboards, admin panels, checkout, editors, consoles. If a person is on the screen trying to *do* something, Focal applies.

It is **not** for:
- Marketing pages, landing pages, campaigns—design there is persuasion and narrative, not task completion, so "one screen, one purpose" and the working-memory limit bend too far to guide you.
- Backend, infra, or non-UI work.

Dense, expert tools (dashboards, IDEs, trading terminals) **are** in scope—high density is right when the audience can read it. The methodology bends for them, never breaks, through two modifiers covered below: the screen's **register** and the user's **expertise** (experts read dense displays as a few familiar chunks; first-timers can't).

**Scope.** Focal is a *lens* for structure and attention—*what belongs on a screen and how it's ranked*—not a full visual-design system. It tells you the screen's purpose, its single primary action, its information structure, and its hierarchy. The execution of color, typography, spacing, and motion is left to your own design system and tooling. Get the methodology right first: visual polish lands far better on a screen that already knows its one job.

---

## The methodology—One Screen, One (Primary) Purpose

The north star. Every screen earns its place by serving exactly one primary purpose.

- **The one-sentence test.** Finish this sentence: *"This screen exists so the user can ______."* If you need the word "and," you have two screens. Split them, or demote one job to a secondary path and route it elsewhere.
- **The single primary action.** Exactly one action gets primary visual treatment per screen. Two primary buttons is usually two purposes wearing one screen. Everything else is secondary (visible, quieter) or tertiary (a link, a menu item, deferred). *Genuine exceptions:* binary-choice screens (Accept / Decline) and dual-mode screens (a map's browse + search) carry two co-equal actions by nature—don't force a demotion the domain refuses. And on hub and exploration screens, "primary action" reads differently; see **Registers**, below.
- **Why this is the whole game.** A person holds one intent at a time. A screen that matches that intent feels effortless; a screen that hedges across three feels like work. The three disciplines below are simply the three ways a screen loses its single purpose—and the three ways to defend it.

---

## The three disciplines

These describe the **task screen**—the default screen type, where the user is completing a single job. Hub and exploration screens bend them; see **Registers**, below.

### 1. Information Architecture—what belongs, and how it's organized

A screen is a unit of intent. IA decides which content and actions belong on it, how they're grouped and labeled, and where the screen sits in the larger flow. Get this wrong and no amount of hierarchy or polish can rescue the screen—it is organizing the wrong things.

- **One job per screen.** If content serves a different intent, it belongs on a different screen. Split by *intent*, not by content type or by your data model.
- **Group by relatedness.** Things used together live together. Proximity is the cheapest, strongest signal that two elements belong to the same idea.
- **Label in the user's words.** Navigation, sections, and actions named in plain language the user already owns—never system or domain jargon. Recognition beats recall.
- **Co-locate a decision and its inputs.** Everything needed to make a choice is present where the choice is made. Never force the user to remember a fact from a previous screen (the "memory bridge").
- **Merge needless round-trips; split overloaded screens.** Two screens that each do half a job should be one. One screen doing three jobs should be three.
- **Orientation.** The user always knows where they are and how to get back. Findability is structure, not decoration.

> **Fails:** the kitchen-sink screen (three jobs at once); structure that mirrors the database instead of the user's intent; orphan content with no clear home; jargon labels; the memory bridge across screens.

### 2. Progressive Disclosure—show now, defer the rest *(load-bearing)*

Reveal complexity only when the user needs it. Working memory is the hard constraint, not screen real estate. This is the discipline that *keeps* a screen on its single purpose over time.

- **The working-memory rule.** Humans hold about **4 items** in working memory at once (Miller's Law, revised by Cowan). At any single decision point, count the distinct options, fields, or facts the user must hold simultaneously:
  - **≤4**—within budget.
  - **5–7**—group or defer.
  - **8+**—overloaded; users skip, misclick, or abandon.
- **Count chunks, not raw elements.** A group the user recognizes as one unit—a familiar toolbar, a labeled section—counts as one. Expertise grows chunk size: a pro tool can show dense data because its users read it as a few learned groups, where a first-run screen cannot. The budget is ~4 *chunks*, and who the user is sets how large a chunk can be.
- **The disclosure triage.** For every element, decide **Now / On-demand / Never.**
  - *Now*—needed to complete the primary action this visit. It stays.
  - *On-demand*—needed by some users sometimes. Defer it behind a reveal (see [reference/patterns.md](reference/patterns.md)).
  - *Never*—nobody needed it; you assumed they would. Cut it.
- **Defer the rare, surface the common.** Smart defaults plus an "Advanced" reveal beats a wall of equal options. Ten settings shown at once is a wall; three with "More options" is a path.
- **The disclosure trap (read this).** Progressive disclosure is *deferral, not burial*. Hiding the primary action, the price, a required field, or a consequence behind a tap is a dark pattern, not disclosure. Never defer what the user needs *now* to act or to trust the screen. Disclosure reduces *choice overload*, never *honesty*.

> **Fails:** the wall of options; an onboarding form that asks everything up front; settings exposed before they're relevant; the primary action or price buried behind a reveal.

### 3. Visual Hierarchy—what wins attention

Once the right things are on the screen and the rest deferred, rank what remains. Importance is communicated by visual weight: the heaviest element is the most important one—always, with no exceptions you didn't make on purpose.

- **The squint test.** Blur your eyes (or the screenshot). Can you still tell what's #1, what's #2, and how things group? If everything has the same weight, you have a list, not a hierarchy.
- **The 3-second test.** A first-time user should be able to name the most important thing on screen within ~3 seconds.
- **Weight must match importance.** The most common hierarchy bug: decoration (a hero image, an illustration, a giant logo) outweighs the primary action. Visual weight is a budget—spend it on what the user came to do.
- **The focusing mechanism.** One element must be the visual entry point that says *start here*. If the eye bounces between equally-weighted regions, the single purpose isn't being expressed.
- **The hierarchy ladder.** Use the *fewest* dimensions that achieve clear ranking, in this order: **space → weight → size → color.** Reach for color last; it is the loudest and easiest to overuse.
- **The shape of a good screen:** one primary element, two to three secondary, everything else ambient. When every element is loud, none is.

> **Fails:** hierarchy carried by color alone; the "visual noise floor" where everything has equal weight; decoration outweighing function; six type sizes that read as one.

---

## Registers—when the rules shift

The disciplines above assume the **task screen**: the default, and the most common. Two other screen types are legitimate, and applying task rules to them is a mistake—it flattens screens that are *supposed* to hold many things. Identify the register first; it changes what "one purpose" means and how the disciplines bind.

- **Task**—the user is completing a single job. *Default; everything above applies as written.* One purpose, one primary action, ≤4 at a decision point. (Checkout, compose, a signup step, a settings detail, any form.)
- **Hub**—the user is choosing where to go. The single purpose *is routing*; many destinations is correct, not clutter. (Home screen, profile, settings index, account screen, app root.)
- **Exploration**—the user is browsing for its own sake. Abundance is the point; the goal is dwell and discovery, not a fast exit. (Feeds, discover/browse tabs, search results, a photo or product grid.)

The methodology still holds—*one screen, one purpose*—but "purpose" reads differently per register, and the working-memory limit **relocates** rather than disappears:

| | Task | Hub | Exploration |
|---|---|---|---|
| **The one purpose** | complete one job | route to the one thing | browse one kind of content |
| **Primary action** | one action wins | the most-likely destination wins | the content is the hero; "keep looking" is the action |
| **Where ≤4 binds** | the whole decision point | per group / per row (not the total destination count) | per item (each card holds ≤4 facts), not the item count |
| **Hierarchy** | one primary, 2–3 secondary | rank destinations by likelihood | one content type dominates; chrome recedes |

Note that ≤4 never vanishes—it moves. A settings index with 9 rows is fine (hub); a settings *row* cramming 9 facts is not. A feed with 200 posts is fine (exploration); a feed *card* with 9 competing elements is not.

The trap runs both ways: flattening a hub or feed down to a single action (now it does its job badly), **or** letting a task screen sprawl into a hub because you skipped the one-sentence test. When you can't tell which register you're in, you're usually looking at a task screen wearing too many hats—split it.

---

## How they combine—order of operations

Apply them in this order. Skipping ahead produces a pretty screen that does the wrong thing.

1. **Define the purpose** (methodology). One sentence, one primary action.
2. **Architect the information** (IA). Decide what belongs and how it's organized.
3. **Disclose progressively** (PD). Of what belongs, decide what shows now and what waits.
4. **Establish hierarchy** (VH). Rank only what survived onto the screen.

You cannot rank elements before you know which show (3 before 4), cannot decide what shows before you know what belongs (2 before 3), and cannot decide what belongs before you know the screen's job (1 before 2). Hierarchy applied to a kitchen-sink screen just makes the clutter well-organized.

This order holds for every register; only the *targets* shift—in a hub, step 4 ranks destinations; in exploration, it ranks content types over chrome.

---

## Flows (screen-local)

Focal is screen-local on purpose—but navigation and step-count are clutter surfaces too: a five-step flow that should be two, a sidebar of fourteen destinations, a "back" that drops you somewhere unexpected. Audit a flow as a **sequence of single-purpose screens**—apply the methodology to each screen, and to the seams between them: no memory bridge, no redundant steps, one job per step, an obvious path back. That's the boundary. Focal sharpens each screen and the joins between them; it is **not** a whole-app IA or sitemap tool. If the question is "how should the entire product be organized," that is a larger exercise—return to Focal screen by screen once that map exists.

---

## Routing

- **No argument** → explain the methodology and three disciplines briefly, then ask: building a new screen, or reviewing an existing one?
- **`build` (or a description of a screen/flow to design)** → follow **The five moves** below. Pull techniques from [reference/patterns.md](reference/patterns.md).
- **`review` / `critique` / `audit` (or a file, screenshot, or URL to evaluate)** → load and follow [reference/review.md](reference/review.md). It runs the three-discipline audit and produces a scorecard.
- **A question about a specific technique or anti-pattern** → consult [reference/patterns.md](reference/patterns.md).

---

## Build: the five moves

For each screen, in order. Write the answers down—they are the spec.

1. **Name the purpose.** One sentence: *"This screen exists so the user can ___."* No "and." Name the single primary action.
2. **Architect the information.** List what belongs on the screen. Group related items; label them in the user's words; co-locate each decision with its inputs. Anything serving a different intent moves to another screen.
3. **Triage disclosure.** Sort every element into Now / On-demand / Never. Cut the Nevers. Defer the On-demands behind a reveal. Keep the Nows.
4. **Rank what stays.** Assign each surviving element a tier: primary (one), secondary (2–3), ambient (the rest). Spend visual weight accordingly, climbing the hierarchy ladder only as far as needed.
5. **Run the gates.** Before you ship the screen, self-check:
   - [ ] One-sentence purpose, no "and"?
   - [ ] Exactly one primary action?
   - [ ] Content grouped and labeled in the user's words; nothing orphaned; no memory bridge?
   - [ ] ≤4 things to hold at any decision point, and nothing the user needs *now* is hidden behind a reveal?
   - [ ] Passes the squint test (clear #1, #2, grouping)?
   - [ ] Empty / loading / error / full (worst-case) states designed, not afterthoughts?

A screen that passes all six is structurally sound by Focal's standard. Apply visual styling and motion on top of that foundation—it lands far better on a screen that already earns its hierarchy.

**Output—the Screen Spec (use this exact structure).** Every build returns this template verbatim, in this order. Fill the `<…>` slots; keep every fixed label and every gate, even when the answer is one line.

```
**Screen:** <name>—exists so the user can <one purpose, no "and">. Primary action: <the one action>.
**Register:** task | hub | exploration   ·   **Audience:** novice | mixed | expert

## Information
- <element or group>—<why it belongs / how it's grouped>
- Moved off: <element> → <where it goes instead>

## Disclosure
- Now: <shown this visit>
- On-demand: <deferred> → behind <reveal>
- Cut: <removed; nobody needed it>

## Hierarchy
- Primary: <the one>
- Secondary: <2–3>
- Ambient: <the muted rest>

## Gates
- [x] One-sentence purpose, no "and"
- [x] Exactly one primary action
- [x] Grouped + labeled; no orphans; no memory bridge
- [x] ≤4 chunks at any decision point; nothing essential deferred
- [x] Squint test passes
- [x] Empty / loading / error / full (worst-case) states designed
```

Mark each gate `[x]` if it passes, or `[ ]` with a short note if it doesn't.

---

## Voice (when giving feedback)

When you review or justify a Focal decision, write like a senior designer reviewing work they want to be great:

- **Emit the exact output template.** Build and review each have a locked structure—the build template is in the build section below, the review template is in [reference/review.md](reference/review.md). Use it verbatim every time: same sections, same order, same headers, same table columns, same issue-line format. Don't add, remove, reorder, or rename sections; if a section has nothing, keep its header and write "None." Repeatable and scannable is the whole point.
- **Be specific and quantitative.** "There are three primary-weight buttons" beats "too many buttons." Count elements, name the tiers, quote the labels.
- **Be decisive.** "This screen has two purposes"—not "this might feel like it has two purposes."
- **Factual first, then judgment, then the fix.** State what you see, why it hurts the user, what it should be instead.
- **No hedging, no praise padding.** Don't sandwich criticism in empty compliments. If something works, say exactly why.
- **Tie every issue to a discipline.** Each problem names which of the three it breaks, and how that costs the screen its single purpose. That is the whole point of the lens.

---

## Absolute don'ts

Match-and-refuse. If you're about to do one of these, you've broken a discipline—rework it.

- **The kitchen-sink screen.** (IA) A screen that does three jobs is three screens, or one purpose plus deferred secondary paths.
- **Structure that mirrors the data model.** (IA) Organize by user intent, not by your tables.
- **Jargon labels and the memory bridge.** (IA) Name things in the user's words; carry context forward instead of making them remember it.
- **The wall of options.** (PD) Defaults plus a reveal, never N equal choices at once.
- **Burying what the user needs now.** (PD) Price, required fields, consequences, and the primary action are never hidden behind disclosure.
- **Two primary actions on a task screen.** (Methodology / VH) Demote one—unless it's a genuine binary-choice or dual-mode screen, or a hub/exploration surface (see Registers).
- **Hierarchy by color alone.** (VH) Climb the ladder: space and weight first.
- **Decoration outweighing the primary action.** (VH) The hero image must not beat the button.
- **Modal as first thought.** A modal interrupts the screen's one purpose. Exhaust inline and progressive alternatives first.

---

## References

- [reference/review.md](reference/review.md)—the three-discipline audit, the Focal scorecard (0–4 per discipline), severity, and output format.
- [reference/patterns.md](reference/patterns.md)—IA techniques, the progressive-disclosure technique catalog, focus mechanisms and the hierarchy ladder in practice, state care (empty / loading / error / full / first-run / peak-end), and the anti-pattern library with fixes.
- [reference/examples.md](reference/examples.md)—worked examples: a cluttered dashboard reviewed, and a screen built, both in the locked output templates.
