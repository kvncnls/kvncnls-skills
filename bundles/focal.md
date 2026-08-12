# Focal—single-file bundle

This is the complete **Focal** skill as one self-contained document—the spine plus every reference—so you can use it in any AI coding agent, not only Claude Code.

*Synchronized manually from `focal/` source files on the working tree; no commit hash is asserted until commit.*

**How to use it**
- **Claude Code**—you don't need this file; install the `focal/` folder from the repo for `/focal` and on-demand loading. This bundle is for everything else.
- **Codex (CLI)**—append it to your project's `AGENTS.md`, which Codex loads automatically: `cat focal.md >> AGENTS.md`.
- **ChatGPT**—create a Custom GPT and paste this into *Instructions*, or upload it as a *Knowledge* file. A Project works the same way.
- **Cursor / Windsurf / Cline**—add it as a rules file, e.g. `.cursor/rules/focal.md`.

Everything below is the skill, including the full 0–4 / 12 scoring rubrics.

---

---
name: focal
description: Use when designing, reviewing, or decluttering a functional product, app, dashboard, or tool screen on any platform for novice or expert users. Focal is the screen-local structure-and-attention lens—it decides what belongs, what waits, and what wins attention through Information Architecture, Progressive Disclosure, and Visual Hierarchy. Its methodology is One Screen, One Clear Intent—not one action per screen. It classifies the register (task, hub, exploration), chooses the matching action model, accommodates inherent binary-choice or dual-mode sets, and adjusts density for expertise. Triggers on clutter, "too much on screen", "simplify this screen", "what's the primary action", one screen one purpose, one clear intent, IA, dashboard, admin, onboarding, or settings. Not for multi-screen flows or navigation (use Compass), visual styling, motion, research, code, marketing/landing pages, backend, or non-UI work.
argument-hint: "[build | review] <screen, file, or description>"
---

# Focal

**One screen, one clear intent.**

Good UX guides attention. People don't read a screen, they orient on it—scanning for where they are, what matters, and what to do next. Every screen, the moment it appears, has to answer three questions: *Where am I? What matters here? What do I do?* The faster and more certainly it answers, the better it works—whether it's a phone app glanced at one-handed or a dashboard an expert lives in all day. Only the pace and the density change.

Focal's answer is a single methodology: **every screen needs one clear organizing intent.** That does not mean one action, one content block, or one possible user goal. A task screen usually has one primary action; a hub can offer many destinations; an exploration surface can foreground many items. What stays singular is the screen's center of gravity—the reason its content and actions belong together.

Simple, clean UX is not a style. It is the visible result of a screen making that organizing intent legible instead of forcing the user to sort competing intents by eye.

Three disciplines, treated as top priorities, are how you earn that outcome:

- **Information Architecture**—what belongs on the screen, and how it's organized.
- **Visual Hierarchy**—what wins attention once it's there.
- **Progressive Disclosure**—what's shown now, and what waits.

```
                 ┌────────────────────────────────────────────┐
   the outcome   │         ONE SCREEN, ONE CLEAR INTENT         │
                 └────────────────────────────────────────────┘
                        ▲              ▲               ▲
   the means     Information      Progressive       Visual
                 Architecture     Disclosure        Hierarchy
                 what belongs     what shows now     what wins
```

Get all three right and the screen settles around one clear intent on its own. Miss any one and that intent blurs. **Progressive Disclosure is the load-bearing discipline**—a screen with the right structure and clear hierarchy decays the instant you let complexity pile on, so weight it the most.

---

## When to use

Focal is for **functional interfaces**—the screens of an app, product, or tool, on any platform (mobile, web, desktop, tablet), for any user (first-timer or expert). Onboarding, feeds, home screens, settings, dashboards, admin panels, checkout, editors, consoles. If a person is on the screen trying to *do* something, Focal applies.

It is **not** for:
- Marketing pages, landing pages, campaigns—design there is persuasion and narrative, not task completion, so the clear-intent test and working-memory limit bend too far to guide you.
- Backend, infra, or non-UI work.

Dense, expert tools (dashboards, IDEs, trading terminals) **are** in scope—high density is right when the audience can read it. The methodology bends for them, never breaks, through two modifiers covered below: the screen's **register** and the user's **expertise** (experts read dense displays as a few familiar chunks; first-timers can't).

**Scope.** Focal is a *lens* for structure and attention—*what belongs on a screen and how it's ranked*—not a full visual-design system. It tells you the screen's organizing intent, the action model appropriate to its register, its information structure, and its hierarchy. The execution of color, typography, spacing, and motion is left to your own design system and tooling. Get the methodology right first: visual polish lands far better on a screen whose center of gravity is already clear.

---

## The methodology—One Screen, One Clear Intent

The north star. Every screen earns its place by making one organizing intent legible. An **organizing intent** is the reason this screen exists in the product—not a demand that only one action, destination, or item can appear.

- **The one-sentence test.** Finish this sentence: *"This screen exists so the user can ______."* If "and" joins two outcomes that can succeed independently, the screen has competing intents. Split them, or demote one to a secondary path. Do not fail a coherent task merely because its natural name contains "and"—*review and approve this invoice* is one intent when review is necessary to approval.
- **The register-aware action model.** Do not force one CTA onto every screen. A task screen usually gives one action primary weight. A hub ranks several destinations. An exploration surface lets a coherent field of content lead. Binary-choice screens (Accept / Decline) and genuine dual-mode screens (a map's browse + search) may carry an inherent co-equal set. Multiple primary-weight actions are a failure only when they compete for different outcomes or leave the screen without a clear center of gravity.
- **Why this is the whole game.** People need to understand what kind of place they are in before they can use it. A screen with one legible organizing intent feels coherent; a screen hedging across three independent outcomes feels like work. The three disciplines below are the three ways that intent becomes clear—or gets lost.

---

## The three disciplines

These describe the **task screen**—the default screen type, where the user is completing a single job. Hub and exploration screens bend them; see **Registers**, below.

### 1. Information Architecture—what belongs, and how it's organized

A screen is a unit of intent. IA decides which content and actions belong on it, how they're grouped and labeled, and where the screen sits in the larger flow. Get this wrong and no amount of hierarchy or polish can rescue the screen—it is organizing the wrong things.

- **One organizing intent per screen.** Supporting actions can coexist when they advance the same intent. If an action or content region serves an independently completable outcome, move it, defer it, or make the screen's routing role explicit. Split by *intent*, not by content type or by your data model.
- **Group by relatedness.** Things used together live together. Proximity is the cheapest, strongest signal that two elements belong to the same idea.
- **Label in the user's words.** Navigation, sections, and actions named in plain language the user already owns—never system or domain jargon. Recognition beats recall.
- **Co-locate a decision and its inputs.** Everything needed to make a choice is present where the choice is made. Never force the user to remember a fact from a previous screen (the "memory bridge").
- **Merge needless round-trips; split overloaded screens.** Two screens that each do half of one intent should be one. One screen carrying three independent intents should be split or reframed as an explicit hub.
- **Orientation.** The user always knows where they are and how to get back. Findability is structure, not decoration.

> **Fails:** the kitchen-sink screen (three jobs at once); structure that mirrors the database instead of the user's intent; orphan content with no clear home; jargon labels; the memory bridge across screens.

### 2. Progressive Disclosure—show now, defer the rest *(load-bearing)*

Reveal complexity only when the user needs it. Working memory is the hard constraint, not screen real estate. This is the discipline that *keeps* a screen's organizing intent legible over time.

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
- **No disclosure without a signifier.** Every deferred thing needs a perceptible cue that it exists—a chevron, a labeled "More options," a tab, a count. Deferral hides *complexity*; it must never hide *existence*. Name the cue when you defer, not just the fact of deferring: "advanced filters, behind an 'Advanced' toggle," not "advanced filters, deferred." Content behind a cue nobody perceives is content you cut—and you cut it without deciding to, which is the one form of cutting this skill does not allow. **A cue qualifies only if it is present in the screen's default state, without hover or gesture.** A function reachable only by swipe or long-press is the named worst case: if the only way to discover it is to be told about it, it is hidden, not deferred.
- **The disclosure trap (read this).** Progressive disclosure is *deferral, not burial*. Hiding the primary action, the price, a required field, or a consequence behind a tap is a dark pattern, not disclosure. Never defer what the user needs *now* to act or to trust the screen. Disclosure reduces *choice overload*, never *honesty*.

> **Fails:** the wall of options; an onboarding form that asks everything up front; settings exposed before they're relevant; the primary action or price buried behind a reveal; a reveal with no cue that anything is behind it.

### 3. Visual Hierarchy—what wins attention

Once the right things are on the screen and the rest deferred, rank what remains. Importance is communicated by visual weight: the heaviest element or region is the most important one—always, with no exceptions you did not choose deliberately for the register.

- **The squint test.** Blur your eyes (or the screenshot). Can you still tell what's #1, what's #2, and how things group? If everything has the same weight, you have a list, not a hierarchy.
- **The 3-second test.** A first-time user should be able to name the most important thing on screen within ~3 seconds.
- **Weight must match importance.** The most common hierarchy bug: decoration (a hero image, an illustration, a giant logo) outweighs the action model's dominant element or region. Visual weight is a budget—spend it on what the user came to do.
- **The focusing mechanism.** One element or region must be the visual entry point that says *start here*. On a task screen that is usually the primary action or the content needed before it; on a hub it can be the leading destination or group; in exploration it is the content field itself. If the eye bounces between unrelated, equally weighted regions, the organizing intent is not being expressed.
- **Weight ranks; it does not permit.** Hierarchy answers *what should I do*; it does not answer *what can I do*. A heading can be the heaviest thing on screen and still be inert. So where the primary is an action, it has to carry a signifier that reads as actionable inside the same ~3 seconds: a traced boundary (fill, border, or elevation), a platform-native control convention (an iOS bar button), or an icon plus label inside a tap target. Bare text at any weight, with no convention behind it, ranks without permitting—say which of these the primary is using. A screen can pass the squint test and still leave the user unsure they are allowed to touch anything.
- **No false signifiers.** A shadowed card that doesn't open, underlined text that isn't a link, a chevron that leads nowhere—these spend attention the screen budgeted for real actions, because the eye reads them exactly like real controls. They also cost trust the first time someone taps one and nothing happens. Count them as clutter, not decoration.
- **The hierarchy ladder.** Use the *fewest* dimensions that achieve clear ranking, in this order: **space → weight → size → color.** Reach for color last; it is the loudest and easiest to overuse.
- **The shape of a good screen:** one dominant element or region, two to three secondary tiers, everything else ambient. The dominant thing must match the register's action model. When every element is loud, none is.

> **Fails:** hierarchy carried by color alone; the "visual noise floor" where everything has equal weight; decoration outweighing function; six type sizes that read as one; a dominant action that ranks first but doesn't read as actionable; inert elements dressed as controls.

---

## Registers—when the rules shift

The disciplines above assume the **task screen**: the default, and the most common. Two other screen types are legitimate, and applying task rules to them is a mistake—it flattens screens that are *supposed* to hold many things. Identify the register first; it changes how the clear intent is expressed, which action model fits, and where the disciplines bind.

**Classify with this tree.** Walk it top to bottom and take the first match. Answer about what the user came to *do*, not about how the screen currently looks—a cluttered screen is not automatically a hub.

```
Did the user come here to complete one specific job?
├── Yes → TASK
└── No
    ├── Is this screen's own job to send them somewhere else?
    │   └── Yes → HUB
    └── Did they come to browse content, with no particular endpoint?
        ├── Yes → EXPLORATION
        └── Neither is clearly true
            └── TASK, overloaded into a hub. Score it as a task screen
                and flag the overload under Information Architecture.
```

Two ties worth naming, because they recur:
- **A record or detail screen** (a contact, an issue, an order) is a **hub** when its job is to show state and route you onward, and a **task** screen when it exists to be edited. If it tries to be both at once, that is the overloaded case—the tree's last branch.
- **Search results** are **exploration** when the user is scanning to discover, and a **task** screen when they are finding one known item to act on.

- **Task**—the user is completing a specific job. *Default; everything above applies as written.* One completion intent, usually one primary action, ≤4 chunks at a decision point. An inherent binary choice or inseparable dual mode can be co-equal without creating a second intent. (Checkout, compose, a signup step, a settings detail, any form.)
- **Hub**—the user is choosing where to go. The organizing intent *is routing*; many destinations is correct, not clutter. (Home screen, profile, settings index, account screen, app root.)
- **Exploration**—the user is browsing for its own sake. Abundance is the point; the goal is dwell and discovery, not a fast exit. (Feeds, discover/browse tabs, search results, a photo or product grid.)

The methodology still holds—*one screen, one clear intent*—but its expression changes by register, and the working-memory limit **relocates** rather than disappears:

| | Task | Hub | Exploration |
|---|---|---|---|
| **Organizing intent** | complete one coherent job | route among related destinations | browse one coherent content space |
| **Action model** | one primary action usually wins; name any inherent co-equal set | rank destinations; let the likely next route lead | content leads; controls support continued discovery |
| **Where ≤4 binds** | the whole decision point | per group / per row (not the total destination count) | per item (each card holds ≤4 facts), not the item count |
| **Hierarchy** | one dominant action or read-first region | one destination or group leads; routes remain comparable | one content type dominates; chrome recedes |

Note that ≤4 never vanishes—it moves. A settings index with 9 rows is fine (hub); a settings *row* cramming 9 facts is not. A feed with 200 posts is fine (exploration); a feed *card* with 9 competing elements is not.

The trap runs both ways: flattening a hub or feed down to a single action (now it does its job badly), **or** letting a task screen sprawl into an accidental hub because you skipped the one-sentence test. When you can't tell which register you're in, you're usually looking at a task screen wearing too many hats—split it or deliberately reframe it as routing.

---

## How they combine—order of operations

Apply them in this order. Skipping ahead produces a pretty screen that does the wrong thing.

1. **Define the intent and action model** (methodology). One sentence; then choose the model that fits the register.
2. **Architect the information** (IA). Decide what belongs and how it's organized.
3. **Disclose progressively** (PD). Of what belongs, decide what shows now and what waits.
4. **Establish hierarchy** (VH). Rank only what survived onto the screen.

You cannot rank elements before you know which show (3 before 4), cannot decide what shows before you know what belongs (2 before 3), and cannot decide what belongs before you know the screen's organizing intent (1 before 2). Hierarchy applied to a kitchen-sink screen just makes the clutter well-organized.

This order holds for every register; only the *targets* shift—in a hub, step 4 ranks destinations; in exploration, it ranks content types over chrome.

---

## Flows—hand off to Compass

Focal is screen-local on purpose. A flow is a *sequence* of screens with clear organizing intents, so apply Focal to each screen in one—but the path *between* them belongs to **Compass**, the sibling skill for cross-screen flows. Focal is *within* a screen; Compass is *between* them.

Route it:
- **Focal's**—a screen that does too much, buries what matters, uses the wrong action model, or ranks the wrong thing loudest.
- **Compass's**—too many steps, a dead end, a trapped modal, a Back that wipes work, a deep link that dumps the user at step one, or a user who can't tell where they are in the journey.

Neither is a whole-app IA or sitemap tool. If the question is "how should the entire product be organized," that is a larger exercise—return to Focal screen by screen, and Compass flow by flow, once that map exists.

---

## Routing

- **No argument** → explain the methodology and three disciplines briefly, then ask: building a new screen, or reviewing an existing one?
- **`build` (or a description of a screen to design)** → follow **The five moves** below. Pull techniques from [reference/patterns.md](reference/patterns.md).
- **A multi-screen flow, journey, or navigation question** → that is Compass's, not Focal's. Say so and hand off (see **Flows**, above).
- **`review` / `critique` / `audit` (or a file, screenshot, or URL to evaluate)** → load and follow [reference/review.md](reference/review.md). It scores each discipline 0–4 against a written rubric, totals to /12, displays a normalized /4 average and common quality band with a weakest-dimension ceiling, tags issues P0–P3, anchors every issue to the exact screen region, app state, and lifecycle moment, and closes on a Clear-Intent verdict. That file defines the rubrics, scoring contract, bands, severities, and audit locator—all of them, and nowhere else.
- **A question about a specific technique or anti-pattern** → consult [reference/patterns.md](reference/patterns.md).

Before emitting either output, read [reference/examples.md](reference/examples.md). It is the calibration for length, tone, and how the locked templates look when filled well—the templates define the shape, the examples set the bar.

---

## Build: the five moves

For each screen, in order. Write the answers down—they are the spec.

1. **Name the intent and action model.** One sentence: *"This screen exists so the user can ___."* Reject an "and" only when it joins independently completable outcomes. Classify the register, then name one primary action, an inherent co-equal set, ranked routes, or the content field that leads.
2. **Architect the information.** List what belongs on the screen. Group related items; label them in the user's words; co-locate each decision with its inputs. Anything serving a different intent moves to another screen.
3. **Triage disclosure.** Sort every element into Now / On-demand / Never. Cut the Nevers. Defer the On-demands behind a reveal. Keep the Nows.
4. **Rank what stays.** Assign each surviving element or region a tier: dominant (one), secondary (2–3), ambient (the rest). Make the dominant tier express the register's action model, climbing the hierarchy ladder only as far as needed.
5. **Run the gates.** Self-check against the six gates in the **`## Gates`** block of the Screen Spec template below. That block is the single canonical list—read them there, and emit them there. Never restate them in your own words.

A screen that passes all six is structurally sound by Focal's standard. Apply visual styling and motion on top of that foundation—it lands far better on a screen that already earns its hierarchy.

**Output—the Screen Spec (use this exact structure).** Every build returns this template verbatim, in this order. Fill the `<…>` slots; keep every fixed label and every gate, even when the answer is one line.

```
**Screen:** <name>—organized around <one clear intent; no unrelated second outcome>. **Action model:** <one primary | inherent co-equal set | ranked routes | content-led>: <name the action, set, routes, or content field>.
**Register:** task | hub | exploration | task-overloaded   ·   **Audience:** novice | mixed | expert

## Information
- <element or group>—<why it belongs / how it's grouped>
- Moved off: <element> → <where it goes instead>

## Disclosure
- Now: <shown this visit>
- On-demand: <deferred> → behind <reveal>
- Cut: <removed; nobody needed it>

## Hierarchy
- Primary: <the one element or region that is the visual entry point—the task action, read-first content, leading hub route/group, or exploration content field; when it is an action, name what makes it read as actionable>
- Secondary: <2–3>
- Ambient: <the muted rest>

## States
- Empty: <what the screen says and offers with no data>
- Loading: <skeleton or optimistic; never a blank>
- Error: <plain-language message, at the source, work preserved>
- Full (worst case): <how it holds at max realistic data—longest label, most rows>

## Gates
- [ ] One-sentence organizing intent; no unrelated second outcome
- [ ] Action model matches the register; any co-equal actions are inherent to the same intent
- [ ] Grouped + labeled; no orphans; no memory bridge
- [ ] ≤4 chunks at any decision point; nothing essential deferred
- [ ] One element or region is materially heaviest and expresses the action model; any primary action reads as actionable
- [ ] All four states above designed
```

Filling it:
- **Repeat any labeled bullet as many times as the screen needs**—`Moved off`, `On-demand`, and `Cut` usually take several lines each. Repeating a label is not adding a section.
- **`<reveal>` means the perceptible cue, not the mechanism.** "Behind an 'Advanced' toggle" and "behind a chevron on the row" are answers; "behind a modal" and "deferred" are not, because neither tells the reader what the user would see that says anything is there.
- **Gates ship unchecked.** Mark `[x]` only for gates the spec actually satisfies; leave `[ ]` with a short reason (one clause) for any it doesn't. Never check a gate the spec does not satisfy—but a spec that genuinely satisfies all six should show all six checked.
- **`Cut` covers removed and replaced.** If a control was needed but has to become a different, safer control, put it under `Cut` and name the replacement—"uncapped refund field → hard-capped to the order total." Cutting an unsafe affordance is not the same as deciding nobody needed it.
- If a labeled bullet has nothing, keep the label and write "None."

Gate 5 is deliberately worded for spec time: it asks whether the spec *assigns* one element or region decisive weight, matches that weight to the action model, and names what makes any primary action read as actionable—all of which a spec can answer. The squint test itself needs a render—run it once the screen exists, and treat a failure there as a review finding, not a build gate.

---

## Voice (when giving feedback)

When you review or justify a Focal decision, write like a senior designer reviewing work they want to be great:

- **Emit the exact output template.** Build and review each have a locked structure—the build template is in the build section above, the review template is in [reference/review.md](reference/review.md). Use it verbatim every time: same sections, same order, same headers, same table columns, same issue-line format. Don't add, remove, reorder, or rename sections; if a section has nothing, keep its header and write "None." Repeatable and scannable is the whole point.
- **Template precedence.** The template is the complete contract for what gets emitted. If any instruction in this skill asks you to produce something the template has no slot for, put it in the nearest slot that fits, or leave it out—never invent a section. A gap like that is a bug in this skill, not a judgment call: name it in one line after the output so it can be fixed. Analysis the template has no room for is still worth doing; it informs the scores even when it isn't printed.
- **Be specific and quantitative.** "There are three primary-weight buttons" beats "too many buttons." Count elements, name the tiers, quote the labels.
- **Be decisive.** "This screen carries two independent intents"—not "this might feel unfocused."
- **Factual first, then judgment, then the fix.** State what you see, why it hurts the user, what it should be instead.
- **No hedging, no praise padding.** Don't sandwich criticism in empty compliments. If something works, say exactly why.
- **Tie every issue to a discipline.** Each problem names which of the three it breaks, and how that obscures the screen's organizing intent. That is the whole point of the lens.
- **Locate every issue.** Name the exact screen or region, rendered app state, and user lifecycle moment where the change belongs. Never make the implementer infer when the finding applies.

---

## Absolute don'ts

Match-and-refuse. If you're about to do one of these, you've broken a discipline—rework it.

- **The kitchen-sink screen.** (IA) A screen carrying three independent intents is three screens, or an explicit hub with focused task paths.
- **Structure that mirrors the data model.** (IA) Organize by user intent, not by your tables.
- **Jargon labels and the memory bridge.** (IA) Name things in the user's words; carry context forward instead of making them remember it.
- **The wall of options.** (PD) Defaults plus a reveal, never N equal choices at once.
- **Burying what the user needs now.** (PD) Price, required fields, consequences, and controls required by the action model are never hidden behind disclosure.
- **Competing primary actions on a task screen.** (Methodology / VH) Demote one when they pursue independent outcomes. Preserve an inherent binary-choice or dual-mode set, and never apply this task rule to a hub or exploration surface (see Registers).
- **A reveal with no cue.** (PD) If nothing on screen says something is there, it isn't deferred—it's cut by accident. Gesture-only functions are the worst case.
- **False signifiers.** (VH) Inert things dressed as controls. A shadowed card that doesn't open, underlined text that isn't a link. They spend the attention budget and cost trust on the first tap.
- **Hierarchy by color alone.** (VH) Climb the ladder: space and weight first.
- **Decoration outweighing the action model.** (VH) The hero image must not beat the task action, leading hub route, or exploration content field.
- **Modal as first thought.** (VH) A modal interrupts the screen's organizing intent. Exhaust inline and progressive alternatives first.

---

## References

- [reference/review.md](reference/review.md)—the three-discipline audit, the Focal scorecard (0–4 per discipline), severity, and output format.
- [reference/patterns.md](reference/patterns.md)—IA techniques, the progressive-disclosure technique catalog, focus mechanisms and the hierarchy ladder in practice, state care (empty / loading / error / full / first-run / peak-end), and the anti-pattern library with fixes.
- [reference/examples.md](reference/examples.md)—worked examples: a cluttered dashboard reviewed, and a screen built, both in the locked output templates.

---

# Focal Review—the three-discipline audit

Evaluate a screen against the three disciplines and the overarching methodology, then return a scorecard with prioritized, concrete fixes. Use when the user asks to review, critique, audit, or "what's wrong with" any functional product, app, or tool screen.

## Input modes

- **Screenshot / image**—read it, critique what you see. The common mode for design review.
- **File path (JSX/TSX/HTML/Vue/Svelte)**—read it, mentally render the layout, critique structure and prescribed styles. You can't see pixels, so qualify visual claims.
- **Live URL**—if browser automation is available, open the page; otherwise fetch markup. If the request names several screens, return one complete scorecard per screen, and say plainly that the path between them is Compass's.
- **A description**—walk the stated screen and its states, label findings as walked from a description, and name the fastest interaction or artifact check that would confirm the consequential claims.

## Step 0—Notice, frame, and name the intent

Before judging, *notice*. Most people glance; a reviewer sees. Count the elements. Name the colors. Identify the type sizes. Read the labels verbatim. The specificity of your observation is the ceiling on the quality of your critique.

Then frame, in one or two sentences each:
- **What is this?** App type, screen purpose, target user.
- **What's the user's state?** Anxious, rushed, casual, distracted, one-handed? A checkout under time pressure demands different care than a Sunday-morning feed scroll. Name it; the critique must respect it.
- **Which app state and lifecycle moment is this?** Name the rendered state—default/full, loading, empty, error, success, expanded, permission-denied—and when it occurs—first run, setup, recurring use, re-entry, or post-action. If the artifact shows several variants, inventory them. If it does not, mark material states `not shown` rather than assuming them.
- **What's the bar?** Every product category has an invisible standard set by its best-in-class tool. A notes screen is judged against Apple Notes and Bear; a dashboard against Linear, Stripe, and Vercel; a checkout against Stripe and Shop Pay. Ask: *what would the best-in-class product in this category do here?*
- **The register.** Classify it by walking the decision tree in **Registers** in [SKILL.md](../SKILL.md)—take the first match, and don't re-derive the categories here. This sets how the gates should be read; see *Adjust for register* below.
- **The methodology lens.** State the screen's apparent **organizing intent** in one sentence, then name its apparent **action model**: one primary action, an inherent co-equal set, ranked routes, or content-led exploration. On a task screen, an "and" fails only when it joins independently completable outcomes; multiple primary-weight actions fail only when they compete rather than form an inherent binary or dual-mode set. For a hub, the intent is *routing*; for exploration, *browsing one coherent content space*.

## Locate every finding

Every issue must carry an implementation locator that answers **where**, **in what state**, and **when**:

- **Surface**—the exact screen plus region or control.
- **State**—the rendered UI or system condition, not the user's emotion.
- **Lifecycle**—the moment in use or relationship: first run, setup, recurring use, re-entry, post-action, or another specific moment.

Use product labels and concrete conditions. `Contact detail · empty state · first visit after contact creation` is actionable; `CRM screen` is not. List only reviewed variants under **Coverage**. Put material unobserved variants under `gaps`, and name the fastest validating check in **Basis** instead of inventing behavior.

## Adjust for register

Read the gates through the register you classified in Step 0. The disciplines still apply; their targets move. Scoring a hub or feed by task-screen rules produces false failures.

- **Task**: score exactly as the gates describe.
- **Hub**: the organizing intent is *routing*. Do **not** penalize many destinations under Gate 1 or Gate 2—the ≤4 limit binds *per group and per row*, not on the total. Score IA on whether destinations form a coherent, grouped space, and VH on whether the likely next route or leading group is easy to find. A hub flattened to one action scores *worse*, not better.
- **Exploration**: abundance is the point. Do **not** penalize many items under Gate 1 or Gate 2—the ≤4 limit binds *per item* (each row's or card's facts), not on the item count. Score VH on whether one coherent content field dominates and chrome recedes; a single primary action is not expected.
- **Task-overloaded**: score by task rules and flag the overload as the leading Gate 1 issue.
- **Audience:** weigh expertise. The working-memory budget is ~4 *chunks*, and experts read dense displays as a few learned groups. Don't score a pro tool's dense panel as overload if its users chunk it; do score a novice or first-run screen strictly. Density is a function of who's reading it.

**A region can carry its own register.** A data table or log inside a task screen is an exploration *region*: score the screen by its own register, and apply the relocated per-row budget to that region rather than counting its rows against the screen's decision point. Say which region you scored separately. The relocation still bites either way—a settings *row* or feed *card* cramming 8+ unfamiliar facts fails Gate 2 even when the screen's total item count is fine.

## The three gates

Run each gate in turn, in the order the disciplines apply. Each produces a 0–4 score and the specific findings behind it.

### Gate 1—Information Architecture

*What belongs on this screen, and how is it organized?*

- Apply the **one-sentence test** to the actual content: write *"This screen exists so the user can ___."* If "and" joins independently completable outcomes, IA has put competing intents on one screen. A phrase such as *review and approve this invoice* can remain one coherent intent when the first action is necessary to the second.
- Identify the **action model** and test it against the register. On a task screen, multiple primary-weight actions usually signal competing intents unless they form an inherent binary or dual-mode set. On a hub, ranked routes are expected; in exploration, the content field leads.
- Check **grouping and labeling**: are related things together? Are labels in the user's words or in system jargon?
- Check for the **memory bridge**: does any decision require a fact only shown on an earlier screen?
- Check for **orphan content** and **data-model-shaped structure** (organized for the database, not the user's intent).

| Score | Criteria |
|-------|----------|
| 0 | No discernible organizing intent—a dumping ground of unrelated content |
| 1 | Multiple competing intents; structure mirrors the data model; jargon labels |
| 2 | One intent is identifiable but an independent outcome muddies it; weak grouping or a memory bridge |
| 3 | Clear organizing intent, suitable action model, sensible grouping and labels, minor structural noise |
| 4 | Unmistakable organizing intent; every element supports it; action model fits the register; plain labels; nothing orphaned |

### Gate 2—Progressive Disclosure *(load-bearing)*

*Of what belongs, is the right amount shown now?*

- At the busiest decision point, **count items in working memory**. ≤4 good, 5–7 borderline, 8+ overload.
- Check the **disclosure triage**: is anything shown that should be deferred (rare options, advanced settings)? Is anything deferred that should be shown *now* (price, required fields, consequences, the task's primary action, or a control required by the register's action model)?
- Check that deferral signals **what's hidden** (a count, a clear "More") rather than reading as absence. Name the cue for each deferred thing; if you cannot find one, the content is hidden rather than deferred. A function reachable only by an uncued gesture is the worst case.

| Score | Criteria |
|-------|----------|
| 0 | Fundamentally broken—severe overload blocks the core task, or essential information is concealed in a way that removes informed choice or creates material harm |
| 1 | Major failure—a wall of options or a dark-pattern reveal hides price, a required field, or a consequence, but the core task remains technically possible |
| 2 | Some layering, but a key decision point exceeds working memory; or content deferred behind no perceptible cue |
| 3 | Mostly well-layered; one or two things shown or deferred wrongly |
| 4 | Each step holds ≤4; complexity revealed exactly when needed; nothing essential hidden |

Because this discipline is load-bearing, record a score of ≤1 caused by **burying an essential** as a blocker regardless of the total. Severity still follows consequence, reach, and recoverability; do not force the dimension to 0 unless its rubric supports 0.

### Gate 3—Visual Hierarchy

*Does weight match importance?*

- Run the **squint test** on the screenshot (or describe the weight order from the code). Name #1, #2, and the groupings.
- Run the **3-second test**: would a first-timer name the most important element in 3 seconds?
- Check **weight vs. importance**: does anything decorative outweigh the action model's dominant element or region? Is there a clear visual entry point (the focusing mechanism)? Count distinct type sizes/weights—deliberate scale, or noise?
- Check **rank vs. actionability** separately. Ranking first is not the same as reading as actionable: when the dominant element is an action, name what says it can be acted on. Then count **false signifiers** (patterns.md, The false signifier).

| Score | Criteria |
|-------|----------|
| 0 | Flat—everything equal weight, no ranking survives a squint |
| 1 | Weak or inverted hierarchy; decoration beats function; no entry point; false signifiers competing with real controls |
| 2 | Hierarchy present but muddy; some elements miscalibrated; or a dominant action ranks first but carries nothing that reads as actionable |
| 3 | Clear hierarchy, weight mostly matches importance |
| 4 | Effortless ranking; the dominant element or region is the right one for the action model |

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

Keep the native total: `total = Information Architecture + Progressive Disclosure + Visual Hierarchy`. Calculate `average = total / 3`, display it rounded to one decimal place, and apply this shared algorithm:

| Band | Average rule | Native total |
|---|---:|---:|
| **Broken** | `average <= 1.5` | `0–4 / 12` |
| **Significant rework** | `1.5 < average < 2.5` | `5–7 / 12` |
| **Solid** | `2.5 <= average < 3.5` | `8–10 / 12` |
| **Excellent** | `average >= 3.5` | `11–12 / 12` |

Then cap the band by the weakest discipline: a minimum of `0` allows only **Broken**, `1` allows at most **Significant rework**, `2` allows at most **Solid**, and `3–4` adds no ceiling. Use the lower-quality result of the average band and this ceiling. The total must equal the exact sum of the three scores.

Dimension score, overall quality band, issue severity, critical blocker, and the **One Screen, One Clear Intent** verdict are separate. The verdict remains Yes or No: a screen can be Solid and still receive No if its organizing intent or action model is structurally unresolved. Every P0 is a blocker, but a blocker does not automatically rewrite a score to 0; a score of 0 does not automatically imply P0. Non-P0 methodology blockers remain in local caps, sequencing, and handoffs.

## Issue severity

| Priority | Meaning |
|----------|---------|
| **P0 — Critical** | Blocks the core outcome; traps the user; destroys work or state; causes or risks material harm; hides material cost, consequence, permission, or risk; removes informed choice; or uses coercive manipulation. Fix before release. |
| **P1 — Major** | Materially damages comprehension, completion, orientation, trust, value realization, or return for a meaningful share of users. Fix before release. |
| **P2 — Moderate** | Creates real friction, confusion, dilution, or missed value with a viable recovery, workaround, or limited scope. Fix in the next planned pass. |
| **P3 — Minor** | Low-impact craft, consistency, or polish. Fix when time permits. |

Assign severity from consequence, reach, and recoverability. A methodology rule violation is not automatically P0.

**Ordering (one rule):** sort by priority, P0 first. Within the same priority, break ties by type of harm—**structural** (IA: wrong job or mental model) outranks **behavioral** (PD: disclosure, overload) outranks **visual** (VH: weight, spacing, type). Never reorder across priorities; a P0 Hierarchy issue outranks a P1 IA issue.

## Output format—use this exact structure

Every review returns this template verbatim, in this order. Don't add, remove, reorder, or rename sections. Fill the `<…>` slots; keep every fixed label. This block is the single source of truth for the emitted shape—the issue line, the table columns, and the section list exist only here.

```
**Verdict:** <clear intent—yes or no> · <the one biggest problem, one phrase> · **<total>/12**

**Screen:** <what it is> · register: <task | hub | exploration | task-overloaded> · audience: <novice | mixed | expert>
**Context:** <the user's state in a few words> · bar: <the best-in-class comparator you judged against>
**Coverage:** <app states and lifecycle moments actually reviewed> · gaps: <material states not shown or tested, or "none">
**Basis:** <observed from a screenshot or artifact | inferred from code | tested in a prototype or live product | walked from a description | measured from product data> · confirm with: <the fastest validating check>
**Blocker:** <None. | concise blocker reason>

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Information Architecture | _/4 | <one line> |
| Progressive Disclosure | _/4 | <one line> |
| Visual Hierarchy | _/4 | <one line> |
| **Total** | **_/12 · _._/4** | **<band>** |

## Issues (most severe first)
- **[P0 · IA]** **At:** <screen/region> · state: <exact state> · lifecycle: <exact moment>. <Name>—<observation>. <impact>. **Fix:** <fix>.
- **[P1 · Disclosure]** **At:** <screen/region> · state: <exact state> · lifecycle: <exact moment>. <Name>—<observation>. <impact>. **Fix:** <fix>.

## Top 3 moves
1. <highest-leverage change>
2. <next>
3. <next>

## Next
- **Structural** (do first): <what changes what the screen *is*—split or merge, regroup, relabel, re-triage>
- **Executional** (after): <what changes how it *looks*—weight, color, type, spacing, motion>
- **Hand off**: <anything that is not this screen's problem—cross-screen path issues go to Compass; "None" if all of it is Focal's>
```

Filling it:
- **Coverage**—name only states and lifecycle moments the evidence actually exposes. Use `gaps` for consequential variants such as loading, error, first-run, re-entry, or worst-case data that were not shown or tested.
- **Issues**—repeat the issue line once per issue, tagged **IA / Disclosure / Hierarchy**. Keep the `At` locator specific enough that a designer or engineer can open the right surface and reproduce the state without rereading the diagnosis. `<observation>` may run two or three sentences when you are being specific and quantitative; the rest stay tight. If nothing ranks above P3, write "None above P3." under the header and keep the header.
- **Next**—structural before executional, always: polishing a screen with an unresolved organizing intent only organizes the clutter. Resolve structural items with the five-move build workflow in [SKILL.md](../SKILL.md). Single-screen work is Focal's; if the real problem is the path between screens, say so and hand off to Compass.
- Re-run the audit after fixes to watch the score climb.

---

# Focal Patterns—techniques and anti-patterns

The working catalog behind the three disciplines. Pull from here when building or when prescribing a fix in a review. Ordered the way the disciplines apply: Information Architecture → Progressive Disclosure → Visual Hierarchy.

---

## Information Architecture (Discipline 1)

How to decide what belongs on a screen and organize it around one clear intent.

- **The screen inventory.** List every element a screen wants to hold. For each, ask: *does this support the organizing intent?* If it serves an independently completable outcome, move it, defer it, or make the screen an explicit hub. This is the fastest way to find an accidental kitchen-sink screen.
- **Split by intent, not content type.** "Account" is not one screen because the data lives in one table—it's profile, security, billing, and notifications, each a separate intent. Split where the user's goal changes, not where your schema does.
- **Group by relatedness.** Things used together live together. Proximity is the strongest, cheapest grouping signal—closer than a border, closer than a shared background. Reach for dividers and containers only when space alone isn't enough.
- **Label in the user's words.** Sections, nav, and actions named in language the user already owns. "Trips" not "Itinerary records." Test a label by asking whether a first-timer would pick it blind.
- **Co-locate the decision and its inputs.** Everything needed to make a choice is present where the choice is made. If step 3 needs a number from step 1, show it on step 3. Never make the user hold it in their head.
- **Merge round-trips; split overload.** Two screens that each do half a job and bounce the user back and forth should be one. One screen juggling three jobs should be three.
- **Keep navigation shallow and oriented.** ≤5 top-level destinations; group the rest. The user should always know where they are (active state, breadcrumb, title) and how to get back.

**Test:** read only the screen's labels and groupings, ignoring the visuals. Can a stranger tell what the screen is for and what they'd do here? If not, the architecture is unclear before any pixel is styled.

---

## Progressive-disclosure technique catalog (Discipline 2—load-bearing)

Match the technique to *why* the content is deferred.

*The ≤4 working-memory budget below is the task-screen default. On hub and exploration screens it relocates rather than disappears—per row on a hub, per card on a feed. See **Registers** in [SKILL.md](../SKILL.md).*

| Technique | Use when | Example |
|-----------|----------|---------|
| **Smart defaults + Advanced** | Most users want the common choice; a few need control | "Send now" with a collapsed "Schedule / options" |
| **Accordion / expander** | Several independent sections, user needs one at a time | FAQ, settings groups, order details |
| **Stepper / wizard** | A task has natural sequential stages | Checkout, multi-part signup, setup |
| **Drill-down (master → detail)** | A list where each item has depth | Inbox → message, feed → post |
| **Contextual reveal** | A field/control only matters after a prior choice | "Other" → free-text box; "Ship to address" → address form |
| **Overflow / "more" menu** | A dominant action or small inherent set, plus a tail of rare actions | "⋯" menu, kebab on a card |
| **Peek + expand** | Content is scannable truncated, occasionally read in full | "Show more" on long text, truncated comments |
| **Tooltip / inline hint** | Help is needed rarely and contextually | "?" next to an unfamiliar term |

**Choosing well:**
- Defer the *rare*, surface the *common*. The split is by frequency of need, never by your convenience.
- **Every deferral needs a signifier**—the perceptible cue that says something is there, present in the screen's default state without hover or gesture. The table above pairs each technique with its cue: an accordion has its chevron, an overflow menu its "⋯", a peek its "Show more", a stepper its position marker. Choosing a technique means committing to its cue; a technique whose cue you cannot name is not deferral, it is disappearance. When the deferred thing is a countable set, make the cue a count ("12 more") rather than a bare "More", so deferral reads as depth and not absence. Gestures (swipe, long-press) carry no inherent cue, so they need a visible partner control on the screen itself—never use one as the only path to a function.
- One layer of disclosure is a path; three nested layers is a maze. If users must expand to expand to expand, the screen has the wrong architecture (Discipline 1).
- A stepper must show **where the user is and how far is left**—but frame it as achievable milestones ("Step 1 of 3"), not a demoralizing tally ("3 of 47 done").

**Never defer:** the price, required fields, destructive consequences, error states, or controls needed to use the screen's action model now. Deferral is for reducing choice overload, never for hiding what the user needs to act or to trust the screen.

---

## Focus mechanisms (Discipline 3)

How to give a screen a clear visual entry point so the eye knows where to start—the visual expression of its organizing intent and action model.

- **Size and weight differential.** Make the primary element materially larger or heavier than its neighbors. A ≥1.25 step between tiers reads as intentional; smaller reads as accidental.
- **Isolation by space.** Surround the primary element with more whitespace than anything else. The eye goes to what's alone.
- **Position.** Above the fold, in the reading-flow landing zone (top-left start, bottom-right resolution for LTR). On mobile, primary actions sit where the thumb rests (the bottom third); on pointer-driven desktop, in the natural resolution zone of the layout (often bottom-right of a form or panel).
- **Disciplined color.** On a task screen, reserve the strongest accent for the primary action or inherent co-equal set. On hubs and exploration surfaces, repeated link or interaction color can support a family of comparable routes; keep one region or content type visually dominant through space and weight.
- **Suppress the rest.** Often the fastest way to create a focal point is not to amplify the hero but to *quiet everything else*—mute secondary text, recede chrome, drop ambient elements to low contrast.

**Test:** squint at the screen and name where the eye starts. It should land on the task's dominant action or read-first content, the hub's leading route or group, or the exploration surface's content field. If unrelated regions tie for first, the focus mechanism has failed.

---

## The hierarchy ladder in practice (Discipline 3)

Climb only as far as you need. Each rung is louder than the last.

1. **Space.** Proximity groups; distance separates; generous margin elevates. Most hierarchy problems are solved here, for free. Tight gaps within a group (8–12px), generous gaps between groups (48–96px).
2. **Weight.** Font weight and contrast. A bold label against regular body, or full-contrast text against muted, ranks without changing size or hue.
3. **Size.** Type scale and element scale. Keep a real scale (≥1.25 ratio between steps); three deliberate sizes beat six arbitrary ones.
4. **Color.** The loudest, last rung. On task screens, reserve the strongest accent for the dominant action or inherent set. On hubs and exploration surfaces, use interaction color consistently across comparable controls while space and weight preserve a dominant region. Color as *the* hierarchy tool (rather than reinforcement) is fragile—it fails for colorblind users and in dark/light inversion.

**Rule:** if space and weight already rank the screen, don't add size and color on top. Redundant emphasis flattens hierarchy as surely as no emphasis.

---

## State care

Products live or die on the states most teams treat as afterthoughts. Each is a Focal surface in its own right—it has an organizing intent, an architecture, and a disclosure budget.

- **Full (worst-case) state.** The biggest clutter trap in data UIs: a screen designed against 3 tidy demo rows becomes chaos at 300—with the longest label, the most items, max-digit numbers, the deepest nesting. Design and review every screen against its *worst realistic data*, not the mock. A layout that only holds together when nearly empty isn't done. (This is why dashboards drift into clutter: they were composed empty.)

- **Empty state.** Not a void—the first-run teacher. One sentence of what this becomes, one primary action to get there. Empty states are the highest-leverage onboarding you have.
- **Loading.** Always communicate system status. Skeletons over spinners for content; optimistic UI for actions the user just took. Never a blank screen with no signal.
- **Error.** Plain language, name the actual problem, offer the fix, preserve the user's work. "Email is missing an @" beats "Invalid input." Place it at the source, not in a banner far away.
- **First run.** Teach through action, not a wall of coach marks. Defer everything not needed for the first success (Discipline 2). The fastest path to one real win beats a tour.
- **Peak-end.** Users remember the most intense moment and the ending. Make sure the peak (the payoff, the "sent!", the result) is celebrated, and the experience ends on a high—not on a dead-end screen. Reassure at anxiety spikes (payment, delete, irreversible commits) with progress, confirmation, and undo.

---

## Anti-pattern library

Each entry: the tell, the discipline it breaks, the fix. Severity is assigned in [review.md](review.md), not here—one authority, so a finding can't carry two priorities.

- **The kitchen-sink screen**—one screen carries several independent intents without declaring itself a hub. *(IA)* Split by intent, or explicitly organize it as routing with focused task paths.
- **The data-model screen**—structure mirrors the database, not the user's goal. *(IA)* Reorganize around intent; group what's used together.
- **The jargon label**—sections and actions named in system terms. *(IA)* Rename in the user's words; test labels blind.
- **The memory bridge**—step 3 needs a fact only shown on step 1. *(IA, PD)* Carry the context forward, or co-locate the decision with its inputs.
- **The wall of options**—8+ equal choices at one decision point. *(PD)* Defaults + reveal; recommend one; group the rest.
- **The everything-up-front form**—onboarding asks for all data immediately. *(PD)* Ask only what's needed for the first success; defer the rest to when it's relevant.
- **The premature settings dump**—advanced options shown before anyone needs them. *(PD)* Collapse behind "Advanced"; smart-default the common case.
- **The buried essential**—price, required field, or consequence hidden behind a tap. *(PD)* Surface it. This is a dark pattern, not disclosure.
- **Competing primary CTAs**—two equally weighted task actions pursue independent outcomes. *(VH)* Demote or move one. Preserve a genuine binary choice or inseparable dual-mode set, and do not apply this task rule to ranked hub routes or content-led exploration.
- **The hero that eats the button**—a giant image/illustration outweighs the primary action. *(VH)* Cut the decoration's weight; the action wins.
- **The rainbow screen**—color used decoratively everywhere, so it can't signal hierarchy. *(VH)* Reserve the strongest accent for the dominant task action or use one consistent interaction color across comparable hub/exploration controls; mute the rest.
- **The flat list pretending to be a hierarchy**—every row identical weight. *(VH)* Differentiate the lead item, or add grouping by space.
- **The invisible reveal**—content deferred behind nothing the user can perceive. *(PD)* Name the cue, or bring the content back. A gesture-only function is this at its worst.
- **The false signifier**—an element that looks interactive and isn't: a shadowed card that doesn't open, underlined text that isn't a link, a chevron that leads nowhere. *(VH)* Give it a control's shape or take the shape away; the ambiguous middle costs a tap and some trust.
- **Nothing reads as actionable**—the primary action carries no control signifier at all, regardless of where it ranks, so the user can see what matters and still not know they may act on it. *(VH)* Give it a traced boundary, a platform-native control convention, or an icon-plus-label tap target.
- **The modal reflex**—interrupting the screen's organizing intent with a dialog for something that could be inline. *(VH)* Exhaust inline and progressive alternatives first.
- **The icon-only mystery nav**—unlabeled icons forcing recall. *(IA)* Add labels; recognition beats recall.

---

## Quick reference card

```
INTENT     "This screen exists so the user can ___."   (no unrelated second outcome)
ACTION     task: one primary usually · hub: ranked routes · exploration: content leads
IA         everything supports the organizing intent · group related · label plainly
DISCLOSE   every element → Now / On-demand / Never · ≤4 at any decision point
           name the signifier for each deferral
HIERARCHY  1 dominant element/region · 2–3 secondary · rest ambient
           space → weight → size → color
NEVER      hide price, required fields, consequences, or controls needed now
```

*A task can preserve an inherent binary choice or inseparable dual mode. On a hub the ≤4 binds per row; on an exploration surface, per item.*

---

# Focal Examples

Two worked examples, captured from real runs of this skill and shown in the locked output templates—one **review**, one **build**. They share a narrative: the review finds a CRM contact screen carrying four jobs, and the build designs one of the task screens it recommends splitting out. These set the bar for length, specificity, and tone; the templates set the shape.

---

## Example 1—Review: a CRM contact detail screen

**Input:** the "Contact detail" screen of a CRM. On it: the contact's name/photo/title; 6 editable fields (email, phone, company, owner, lifecycle stage, lead source); a full activity timeline of 40+ entries; an inline "Log a call" composer; an inline "Send email" composer; a Deals panel with 3 deals; Notes and Files panels; a right rail of 8 "similar contacts"; and 3 top-right buttons all styled identically as filled primary buttons ("Save", "Convert to Deal", "Delete"). Every panel header is the same size and weight.

**Focal's output:**

```
**Verdict:** No · four jobs stacked on one surface, with Delete dressed as a primary button · **3/12**

**Screen:** CRM contact detail—a record home carrying ten co-equal regions and three identical filled primary buttons · register: task-overloaded · audience: mixed
**Context:** a rep mid-call or between calls, scanning fast · bar: Linear's issue detail, Stripe's customer record
**Coverage:** full/default state for a returning rep, plus empty Deals/Notes/Files on a newly created contact · gaps: loading, save-in-progress, save error, permission-limited, and destructive-confirmation states not shown
**Basis:** walked from a description · confirm with: open the screen, invoke Delete, and verify the destructive confirmation, autosave, and focus order
**Blocker:** Delete is presented as a filled primary beside routine actions, creating a material risk of accidental record destruction.

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Information Architecture | 1/4 | Four jobs on one screen: view the record, edit six fields, log a call, send an email—plus three related-record panels and a prospecting rail that serve a different intent entirely. |
| Progressive Disclosure | 1/4 | Zero deferral anywhere: ten top-level regions at landing, both composers open before the rep has chosen to compose, 40+ timeline entries unfiltered. |
| Visual Hierarchy | 1/4 | Below the identity header the screen is flat—every panel header identical in size and weight—and the ranking that does exist is inverted: Delete carries the same primary weight as Save. |
| **Total** | **3/12 · 1.0/4** | **Broken** |

## Issues (most severe first)
- **[P0 · Hierarchy]** **At:** Contact detail action bar · state: full/default · lifecycle: returning rep reviewing an existing contact. Three filled primaries, one destructive—Save, Convert to Deal, and Delete are styled identically. On this task-overloaded action bar, three competing primaries means no primary: nothing says where to start, and an irreversible action wears the exact affordance of the safest one, sitting adjacent to it. This is the one issue on the screen that can destroy a customer record on a mis-click. **Fix:** with autosave, Save disappears. Keep "Convert to Deal" as the single filled primary; "Log a call" and "Send email" become secondary; Delete moves into an overflow "⋯" menu behind a typed confirmation.
- **[P1 · IA]** **At:** Contact detail body · state: full/default · lifecycle: returning rep scanning during or between calls. Four jobs, one screen—the one-sentence test returns "This screen exists so the user can view a contact *and* edit six fields *and* log a call *and* send an email *and* manage deals, notes, and files." Each outcome can succeed independently, so the sentence exposes competing intents rather than one coherent task. Two of those are full composers sitting open on a record surface, and the six fields render as live inputs with a global Save, which means the screen is permanently in edit mode. A rep who opened it to read a phone number is forced to re-sort several intents by eye. **Fix:** make Contact detail a hub whose organizing intent is *route to the right next action*. Fields become read-only text with per-field inline edit and autosave (no global Save); "Log a call" and "Send email" become their own focused task screens launched from the header.
- **[P1 · IA]** **At:** Activity/Deals/Notes/Files regions · state: full/default · lifecycle: recurring account review. The panels mirror the data model—Deals, Notes, Files, and Activity are four peer panels, one per related table, ranked equally because the schema ranks them equally. A rep's actual intent is overwhelmingly "what happened last, and what's the open deal"; Notes and Files are archive lookups. Organizing by table forces the user to re-sort the screen by eye on every visit. **Fix:** reorder by intent—Activity dominant, Deals second in the same column, Notes and Files collapsed into one "Attachments & notes" section.
- **[P1 · Disclosure]** **At:** Contact detail landing viewport · state: full/default · lifecycle: every return to an existing contact. Nothing is deferred—ten top-level regions compete at landing, and scored by task rules that is straightforward overload: three *task* surfaces sit resident on the same screen and no element anywhere sits behind a reveal. Every element is "Now" because nobody ran the triage. **Fix:** Now—identity, read-only fields, recent activity, Deals. On-demand—composers behind their header buttons, Notes, Files. Cut—the similar-contacts rail.
- **[P1 · Disclosure]** **At:** Activity timeline · state: worst-case full · lifecycle: recurring review of a long-lived contact. The timeline has no ceiling—40+ entries render in full, undifferentiated, with no type filter and no collapse. At the worst realistic case (a two-year customer, 400 entries) this panel is the entire screen and Deals is off-screen. **Fix:** show the 5 most recent grouped by day, with a type filter and "Show 37 more"—the count, so the deferral reads as depth rather than absence.
- **[P1 · Hierarchy]** **At:** Contact detail body · state: full/default · lifecycle: first visit by a rep unfamiliar with the record. No visual entry point—every panel header is the same size and weight. Squint at this and you get a list, not a hierarchy: nine equal grey blocks. A first-timer cannot name the most important thing in three seconds because nothing is the most important thing. **Fix:** climb the ladder with space and weight before color—48–96px between sections against 8–12px within them, one heavier header on Activity, all other headers dropped to a muted label size.
- **[P2 · IA]** **At:** Similar contacts rail · state: full/default · lifecycle: returning rep reviewing one known contact. The similar-contacts rail is orphan content—eight contacts occupying a full rail, serving prospecting, an intent nobody arrived on this screen holding. It is here because the data was available, not because a job needed it. **Fix:** cut it; surface similar contacts in search and list views, where the user is actually comparing people.
- **[P2 · Disclosure]** **At:** Deals/Notes/Files regions · state: empty · lifecycle: first visit after contact creation. Empty panels hold full weight—Deals, Notes, and Files each render a full-weight header whether they hold three items or zero, so a brand-new contact shows three headers announcing nothing. **Fix:** collapse empty sections to one quiet line with the add action ("No notes yet · Add note").

## Top 3 moves
1. Split the screen: Contact detail becomes a record hub; "Log a call" and "Send email" become focused task screens with clear completion intents; the six fields become read-only text with per-field inline edit and autosave, retiring the global Save.
2. Rebuild the action bar to one primary: "Convert to Deal" filled, "Log a call" / "Send email" secondary, Delete in an overflow menu behind typed confirmation.
3. Rank what remains with space and weight: Activity dominant and capped at 5 with a filter and a "Show N more" count, Deals second, Notes and Files collapsed, similar-contacts rail cut.

## Next
- **Structural** (do first): split the two composers onto their own task screens, convert the field block to read-only + inline autosave, re-triage the ten regions, cut the similar-contacts rail, cap and filter the timeline.
- **Executional** (after): the section spacing scale, the muted header treatment, the single accent reserved for the one primary, and the destructive-action confirmation styling.
- **Hand off**: None—every issue here is within this screen.
```

---

## Example 2—Build: the "Log a call" screen

**Input:** "Build the Log a call screen we just split out of the contact record."

**Focal's output:**

```
**Screen:** Log a call—organized around recording what happened on a call the user just made. **Action model:** one primary: Log call.
**Register:** task   ·   **Audience:** mixed

## Information
- Call context strip (contact name, photo, number dialed, timestamp, prefilled)—co-locates the decision with its inputs so the rep never has to remember who they called or when; read-only, no fields to re-enter.
- Outcome selector: Connected / Voicemail / No answer / Wrong number—the one fact every logged call must carry. Four options, inside the working-memory budget, so it needs no grouping.
- Duration—prefilled from the dialer, editable. Sits beside Outcome because the two are read together as one "what happened" chunk.
- Notes—the reason the rep is on this screen thirty seconds after hanging up. Given the most vertical space of anything on the screen.
- "Schedule follow-up" toggle—the most common next step after a connected call, and the thing the rep will otherwise forget by end of day, so it lives here rather than on a separate task screen.
- "Add to deal (3)"—one quiet control, with the count, because a call that moves a deal must be attributable to it.
- Last call line ("Last call: Jul 2, voicemail")—one ambient line, so the rep knows whether this is a first attempt or a fifth without leaving for the timeline.
- Moved off: the six editable contact fields → Contact detail hub, edited in place per field with autosave.
- Moved off: the full 40+ activity timeline → Contact detail hub, capped and filtered; only the single last-call line survives here.
- Moved off: Send email composer → its own compose screen, launched from the Contact detail header.
- Moved off: Deals, Notes, and Files panels → Contact detail hub; this screen reaches Deals only through "Add to deal (3)".
- Moved off: the 8 similar contacts → search and list views, where comparing people is the actual job.

## Disclosure
- Now: call context strip, Outcome (4 options), Duration, Notes, last-call line, "Log call". Busiest decision point holds 4 chunks—context, outcome, duration, notes.
- On-demand: follow-up date and task title → behind the "Schedule follow-up" toggle (contextual reveal—the fields only matter after the rep says yes).
- On-demand: deal association picker → behind "Add to deal (3)", with the count shown so the deferral reads as depth, not absence.
- On-demand: call recording and transcript → behind a "Recording" link in the context strip, present for the rare dispute, absent from the fast path.
- Cut: lifecycle stage and lead source editors—a call log is not where a rep re-classifies a contact, and offering it invites a wrong edit under time pressure.
- Cut: the similar-contacts rail. Nobody logging a call needs eight other people.
- Cut: a cancel-confirmation dialog. Nothing here is destructive; discard is a link.

## Hierarchy
- Primary: "Log call"—the only filled button on the screen, bottom-right in the form's resolution zone, isolated by more whitespace than anything else.
- Secondary: the Outcome selector (four large segmented targets, autofocused on load so the eye starts there), the Notes field (largest area, quiet-bordered), Duration.
- Ambient: the call context strip and last-call line (muted, read-only), "Schedule follow-up", "Add to deal (3)", "Recording", and "Discard" as a plain text link. Space and weight carry the whole ranking; the single accent color is spent only on "Log call".

## States
- Empty: a first-ever call shows "First call with Ana" in place of the last-call line.
- Loading: context strip skeletons while the dialer record resolves; the form is interactive immediately.
- Error: a save failure keeps every keystroke and names the cause inline at the source—"Couldn't reach the server—your notes are saved locally, retry."
- Full (worst case): 900-character notes scroll inside the field without pushing "Log call" off-screen; a 40-character company name truncates in the strip rather than wrapping to three lines.

## Gates
- [x] One-sentence organizing intent; no unrelated second outcome
- [x] Action model matches the register; any co-equal actions are inherent to the same intent
- [x] Grouped + labeled; no orphans; no memory bridge
- [x] ≤4 chunks at any decision point; nothing essential deferred
- [x] One element or region is materially heaviest and expresses the action model; any primary action reads as actionable
- [x] All four states above designed
```

---

**Why these two:** the review never just lists problems—it ties every issue to a discipline, ends on three ranked moves, and sorts the work structural-before-executional. The build never returns prose—it returns the same Screen Spec every time. And the second resolves the first: "split the composers onto their own task screens" becomes a screen with one coherent completion intent and an action model that fits. That is the method in motion, in both directions.

Note the disclosure discipline doing the real work in the build: seven things were cut or deferred, and the busiest decision point holds four chunks. Note also what was *not* deferred—nothing the rep needs in order to log the call sits behind a reveal. Deferral is not burial.
