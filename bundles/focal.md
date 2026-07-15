# Focal—single-file bundle

This is the complete **Focal** skill as one self-contained document—the spine plus every reference—so you can use it in any AI coding agent, not only Claude Code.

**How to use it**
- **Claude Code**—you don't need this file; install the `focal/` folder from the repo for `/focal` and on-demand loading. This bundle is for everything else.
- **Codex (CLI)**—append it to your project's `AGENTS.md`, which Codex loads automatically: `cat focal.md >> AGENTS.md`.
- **ChatGPT**—create a Custom GPT and paste this into *Instructions*, or upload it as a *Knowledge* file. A Project works the same way.
- **Cursor / Windsurf / Cline**—add it as a rules file, e.g. `.cursor/rules/focal.md`.

Everything below is the skill.

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
  - *On-demand*—needed by some users sometimes. Defer it behind a reveal (see reference/patterns.md).
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
- **`build` (or a description of a screen/flow to design)** → follow **The five moves** below. Pull techniques from reference/patterns.md.
- **`review` / `critique` / `audit` (or a file, screenshot, or URL to evaluate)** → load and follow reference/review.md. It runs the three-discipline audit and produces a scorecard.
- **A question about a specific technique or anti-pattern** → consult reference/patterns.md.

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

- **Emit the exact output template.** Build and review each have a locked structure—the build template is in the build section below, the review template is in reference/review.md. Use it verbatim every time: same sections, same order, same headers, same table columns, same issue-line format. Don't add, remove, reorder, or rename sections; if a section has nothing, keep its header and write "None." Repeatable and scannable is the whole point.
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

- reference/review.md—the three-discipline audit, the Focal scorecard (0–4 per discipline), severity, and output format.
- reference/patterns.md—IA techniques, the progressive-disclosure technique catalog, focus mechanisms and the hierarchy ladder in practice, state care (empty / loading / error / full / first-run / peak-end), and the anti-pattern library with fixes.
- reference/examples.md—worked examples: a cluttered dashboard reviewed, and a screen built, both in the locked output templates.


---

# Focal Review—the three-discipline audit

Evaluate a screen (or flow) against the three disciplines and the overarching methodology, then return a scorecard with prioritized, concrete fixes. Use when the user asks to review, critique, audit, or "what's wrong with" any functional product, app, or tool screen.

## Input modes

- **Screenshot / image**—read it, critique what you see. The common mode for design review.
- **File path (JSX/TSX/HTML/Vue/Svelte)**—read it, mentally render the layout, critique structure and prescribed styles. You can't see pixels, so qualify visual claims.
- **Live URL**—if browser automation is available, open the page; otherwise fetch markup. Per-flow review: audit 3–5 representative screens.

## Step 0—Notice, frame, and name the purpose

Before judging, *notice*. Most people glance; a reviewer sees. Count the elements. Name the colors. Identify the type sizes. Read the labels verbatim. The specificity of your observation is the ceiling on the quality of your critique.

Then frame, in one or two sentences each:
- **What is this?** App type, screen purpose, target user.
- **What's the user's state?** Anxious, rushed, casual, distracted, one-handed? A checkout under time pressure demands different care than a Sunday-morning feed scroll. Name it; the critique must respect it.
- **What's the bar?** Every product category has an invisible standard set by its best-in-class tool. A notes screen is judged against Apple Notes and Bear; a dashboard against Linear, Stripe, and Vercel; a checkout against Stripe and Shop Pay. Ask: *what would the best-in-class product in this category do here?*
- **The register.** Classify it: **task** (completing one job), **hub** (choosing where to go), or **exploration** (browsing for its own sake). This sets how the gates should be read—see *Adjust for register* below. If you can't tell, it's likely a task screen overloaded into a hub.
- **The methodology lens.** State the screen's *apparent* single purpose in one sentence (for a hub, that purpose is *routing*; for exploration, *browsing a kind of content*), and name what *appears* to be the primary action. On a task screen, if the sentence needs an "and," or you can't find one primary action, the screen has already failed its overarching purpose, and the gates below will show why.

## Adjust for register

Read the gates through the register you classified in Step 0. The disciplines still apply; their targets move. Scoring a hub or feed by task-screen rules produces false failures.

- **Task** (default): score exactly as the gates describe.
- **Hub** (home, profile, settings index, app root, dashboard overview, admin index): the purpose is *routing*. Do **not** penalize many destinations under Gate 2—the ≤4 limit binds *per group and per row*, not on the total. Score IA on whether destinations are grouped and labeled, VH on whether the most-likely next step wins. A hub flattened to one action scores *worse*, not better.
- **Exploration** (feeds, browse/discover, search results, grids, data tables, log viewers): abundance is the point. Do **not** penalize many items under Gate 2—the ≤4 limit binds *per item* (each row's or card's facts), not on the item count. Score VH on whether one content type dominates and chrome recedes; a single "primary action" is not expected.
- **Audience:** weigh expertise. The working-memory budget is ~4 *chunks*, and experts read dense displays as a few learned groups. Don't score a pro tool's dense panel as overload if its users chunk it; do score a novice or first-run screen strictly. Density is a function of who's reading it.

The relocation still bites: a settings *row* or feed *card* that crams 8+ unfamiliar facts fails Gate 2 even though the screen's total item count is fine. And a screen you can't classify is usually a task screen overloaded into a hub—score it as a task screen and flag the overload under Gate 1.

## The three gates

Run each gate in turn, in the order the disciplines apply. Each produces a 0–4 score and the specific findings behind it.

### Gate 1—Information Architecture

*What belongs on this screen, and how is it organized?*

- Apply the **one-sentence test** to the actual content: write *"This screen exists so the user can ___."* If you need "and," IA has put two jobs on one screen.
- Count the **primary-weight actions** the structure implies. More than one means more than one purpose.
- Check **grouping and labeling**: are related things together? Are labels in the user's words or in system jargon?
- Check for the **memory bridge**: does any decision require a fact only shown on an earlier screen?
- Check for **orphan content** and **data-model-shaped structure** (organized for the database, not the user's intent).

| Score | Criteria |
|-------|----------|
| 0 | No discernible job—a dumping ground of unrelated content |
| 1 | Multiple competing jobs; structure mirrors the data model; jargon labels |
| 2 | One job identifiable but a second muddies it; weak grouping or a memory bridge |
| 3 | Clear single job, sensible grouping and labels, minor structural noise |
| 4 | One unmistakable job; everything on screen earns its place; plain labels; nothing orphaned |

### Gate 2—Progressive Disclosure *(load-bearing)*

*Of what belongs, is the right amount shown now?*

- At the busiest decision point, **count items in working memory**. ≤4 good, 5–7 borderline, 8+ overload.
- Check the **disclosure triage**: is anything shown that should be deferred (rare options, advanced settings)? Is anything deferred that should be shown *now* (price, required fields, consequences, the primary action)?
- Check that deferral signals **what's hidden** (a count, a clear "More") rather than reading as absence.

| Score | Criteria |
|-------|----------|
| 0 | Everything dumped at once (severe overload), or essential info buried |
| 1 | Wall of options; or a dark-pattern reveal hiding price / required field / consequence |
| 2 | Some layering, but a key decision point exceeds working memory |
| 3 | Mostly well-layered; one or two things shown or deferred wrongly |
| 4 | Each step holds ≤4; complexity revealed exactly when needed; nothing essential hidden |

Because this discipline is load-bearing, treat a score of ≤1 caused by **burying an essential** as a blocking issue regardless of the total.

### Gate 3—Visual Hierarchy

*Does weight match importance?*

- Run the **squint test** on the screenshot (or describe the weight order from the code). Name #1, #2, and the groupings.
- Run the **3-second test**: would a first-timer name the most important element in 3 seconds?
- Check **weight vs. importance**: does anything decorative outweigh the primary action? Is there a single visual entry point (the focusing mechanism)? Count distinct type sizes/weights—deliberate scale, or noise?

| Score | Criteria |
|-------|----------|
| 0 | Flat—everything equal weight, no ranking survives a squint |
| 1 | Weak or inverted hierarchy; decoration beats function; no entry point |
| 2 | Hierarchy present but muddy; some elements miscalibrated |
| 3 | Clear hierarchy, weight mostly matches importance |
| 4 | Effortless ranking; the heaviest thing is the most important thing |

## The scorecard

Present scores as a table. Be honest—a 4 means genuinely excellent, not "fine."

| Discipline | Score | Key finding |
|------------|-------|-------------|
| 1—Information Architecture | ?/4 | [specific finding] |
| 2—Progressive Disclosure | ?/4 | [specific finding] |
| 3—Visual Hierarchy | ?/4 | [specific finding] |
| **Total** | **?/12** | **[band]** |

**Bands:** 11–12 ship it · 8–10 solid, fix the weak discipline · 5–7 significant rework before users are happy · 0–4 the screen does not work yet.

**The verdict—One Screen, One Purpose.** This becomes the **Verdict** line at the very top of the output (see Output format): does this screen serve a single primary purpose, yes or no? The total measures how close it gets; the verdict states whether it arrives. A screen can score moderately and still fail the verdict if IA put two jobs on it.

## Issues and severity

List the issues found, ordered by severity, not by discipline. Tag each:

| Priority | Meaning |
|----------|---------|
| **P0** | Blocks the task or breaks trust (essential info hidden, no primary action, two purposes)—fix now |
| **P1** | Causes real confusion or overload—fix before release |
| **P2** | Annoyance with a workaround—next pass |
| **P3** | Polish—if time permits |

Order issues by *type* of harm, most severe first: **structural** (IA—wrong job or mental model) → **behavioral** (PD—flow, disclosure, overload) → **visual** (VH—weight, spacing, type). A structural flaw outranks a visual one.

For each issue:
> **[P?] [Discipline] Name**—what you see (factual, specific, counted). Why it hurts *this* user in *this* state, and how it costs the screen its single purpose. The concrete fix.

## Output format—use this exact structure

Every review returns this template verbatim, in this order. Same sections, same headers, same table columns, same issue-line format. Don't add, remove, reorder, or rename sections. Fill the `<…>` slots; keep each fixed label.

```
**Verdict:** <single purpose—yes or no> · <the one biggest problem, one phrase> · **<total>/12**

**Screen:** <what it is> · register: <task | hub | exploration> · audience: <novice | mixed | expert>

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Information Architecture | _/4 | <one line> |
| Progressive Disclosure | _/4 | <one line> |
| Visual Hierarchy | _/4 | <one line> |
| **Total** | **_/12** | **<band>** |

## Issues (most severe first)
- **[P0 · IA]** <Name>—<observation>. <impact>. **Fix:** <fix>.
- **[P1 · Disclosure]** <Name>—<observation>. <impact>. **Fix:** <fix>.
(if nothing above P3, write "None above P3." and keep this header)

## Top 3 moves
1. <highest-leverage change>
2. <next>
3. <next>
```

Bands: **11–12** ship it · **8–10** solid, fix the weak discipline · **5–7** significant rework · **0–4** doesn't work yet. Tag issues with the abbreviations **IA / Disclosure / Hierarchy**.

## Next steps

Close by sorting the fixes into two buckets and ordering the work:

- **Structural**—wrong job, screens to split or merge, content to regroup or relabel, disclosure to re-triage. These change what the screen *is*. Resolve them first with the five-move build workflow in SKILL.md.
- **Executional**—visual weight, color, type, spacing, motion, transitions. These change how the screen *looks*. Apply them in your own design system once the structure is sound.

Always fix structural before executional: polishing a screen with the wrong purpose only organizes the clutter. Re-run the audit after fixes to watch the score climb.


---

# Focal Patterns—techniques and anti-patterns

The working catalog behind the three disciplines. Pull from here when building or when prescribing a fix in a review. Ordered the way the disciplines apply: Information Architecture → Progressive Disclosure → Visual Hierarchy.

---

## Information Architecture (Discipline 1)

How to decide what belongs on a screen and organize it so a single job is possible.

- **The screen inventory.** List every element a screen wants to hold. For each, ask: *does this serve the one job?* If it serves a different intent, it belongs on a different screen. This is the fastest way to find a kitchen-sink screen.
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

*The ≤4 working-memory budget below is the task-screen default. On hub and exploration screens it relocates rather than disappears—per row on a hub, per card on a feed. See **Registers** in SKILL.md.*

| Technique | Use when | Example |
|-----------|----------|---------|
| **Smart defaults + Advanced** | Most users want the common choice; a few need control | "Send now" with a collapsed "Schedule / options" |
| **Accordion / expander** | Several independent sections, user needs one at a time | FAQ, settings groups, order details |
| **Stepper / wizard** | A task has natural sequential stages | Checkout, multi-part signup, setup |
| **Drill-down (master → detail)** | A list where each item has depth | Inbox → message, feed → post |
| **Contextual reveal** | A field/control only matters after a prior choice | "Other" → free-text box; "Ship to address" → address form |
| **Overflow / "more" menu** | One or two primary actions, a tail of rare ones | "⋯" menu, kebab on a card |
| **Peek + expand** | Content is scannable truncated, occasionally read in full | "Show more" on long text, truncated comments |
| **Tooltip / inline hint** | Help is needed rarely and contextually | "?" next to an unfamiliar term |

**Choosing well:**
- Defer the *rare*, surface the *common*. The split is by frequency of need, never by your convenience.
- Show the **count** when you hide things ("12 more"), so deferral doesn't read as absence.
- One layer of disclosure is a path; three nested layers is a maze. If users must expand to expand to expand, the screen has the wrong architecture (Discipline 1).
- A stepper must show **where the user is and how far is left**—but frame it as achievable milestones ("Step 1 of 3"), not a demoralizing tally ("3 of 47 done").

**Never defer:** the price, required fields, destructive consequences, error states, or the primary action. Deferral is for reducing choice overload, never for hiding what the user needs to act or to trust the screen.

---

## Focus mechanisms (Discipline 3)

How to give a screen a single visual entry point so the eye knows where to start—the visual expression of the one purpose.

- **Size and weight differential.** Make the primary element materially larger or heavier than its neighbors. A ≥1.25 step between tiers reads as intentional; smaller reads as accidental.
- **Isolation by space.** Surround the primary element with more whitespace than anything else. The eye goes to what's alone.
- **Position.** Above the fold, in the reading-flow landing zone (top-left start, bottom-right resolution for LTR). On mobile, primary actions sit where the thumb rests (the bottom third); on pointer-driven desktop, in the natural resolution zone of the layout (often bottom-right of a form or panel).
- **Singular color.** Exactly one saturated accent on the screen, reserved for the primary action. The moment a second element shares it, focus splits.
- **Suppress the rest.** Often the fastest way to create a focal point is not to amplify the hero but to *quiet everything else*—mute secondary text, recede chrome, drop ambient elements to low contrast.

**Test:** cover the primary element with your thumb. If the screen now feels purposeless, the focus mechanism is working.

---

## The hierarchy ladder in practice (Discipline 3)

Climb only as far as you need. Each rung is louder than the last.

1. **Space.** Proximity groups; distance separates; generous margin elevates. Most hierarchy problems are solved here, for free. Tight gaps within a group (8–12px), generous gaps between groups (48–96px).
2. **Weight.** Font weight and contrast. A bold label against regular body, or full-contrast text against muted, ranks without changing size or hue.
3. **Size.** Type scale and element scale. Keep a real scale (≥1.25 ratio between steps); three deliberate sizes beat six arbitrary ones.
4. **Color.** The loudest, last rung. A single accent for the one thing that matters most. Color as *the* hierarchy tool (rather than reinforcement) is fragile—it fails for colorblind users and in dark/light inversion.

**Rule:** if space and weight already rank the screen, don't add size and color on top. Redundant emphasis flattens hierarchy as surely as no emphasis.

---

## State care

Products live or die on the states most teams treat as afterthoughts. Each is a Focal surface in its own right—it has a purpose, an architecture, and a disclosure budget.

- **Full (worst-case) state.** The biggest clutter trap in data UIs: a screen designed against 3 tidy demo rows becomes chaos at 300—with the longest label, the most items, max-digit numbers, the deepest nesting. Design and review every screen against its *worst realistic data*, not the mock. A layout that only holds together when nearly empty isn't done. (This is why dashboards drift into clutter: they were composed empty.)

- **Empty state.** Not a void—the first-run teacher. One sentence of what this becomes, one primary action to get there. Empty states are the highest-leverage onboarding you have.
- **Loading.** Always communicate system status. Skeletons over spinners for content; optimistic UI for actions the user just took. Never a blank screen with no signal.
- **Error.** Plain language, name the actual problem, offer the fix, preserve the user's work. "Email is missing an @" beats "Invalid input." Place it at the source, not in a banner far away.
- **First run.** Teach through action, not a wall of coach marks. Defer everything not needed for the first success (Discipline 2). The fastest path to one real win beats a tour.
- **Peak-end.** Users remember the most intense moment and the ending. Make sure the peak (the payoff, the "sent!", the result) is celebrated, and the experience ends on a high—not on a dead-end screen. Reassure at anxiety spikes (payment, delete, irreversible commits) with progress, confirmation, and undo.

---

## Anti-pattern library

Each entry: the tell, the discipline it breaks, the fix.

- **The kitchen-sink screen**—one screen tries to do three jobs. *(IA, P1)* Split by intent, or keep one purpose and route the others to secondary paths.
- **The data-model screen**—structure mirrors the database, not the user's goal. *(IA, P1)* Reorganize around intent; group what's used together.
- **The jargon label**—sections and actions named in system terms. *(IA, P2)* Rename in the user's words; test labels blind.
- **The memory bridge**—step 3 needs a fact only shown on step 1. *(IA, PD, P1)* Carry the context forward, or co-locate the decision with its inputs.
- **The wall of options**—8+ equal choices at one decision point. *(PD, P2)* Defaults + reveal; recommend one; group the rest.
- **The everything-up-front form**—onboarding asks for all data immediately. *(PD, P2)* Ask only what's needed for the first success; defer the rest to when it's relevant.
- **The premature settings dump**—advanced options shown before anyone needs them. *(PD, P3)* Collapse behind "Advanced"; smart-default the common case.
- **The buried essential**—price, required field, or consequence hidden behind a tap. *(PD, P0)* Surface it. This is a dark pattern, not disclosure.
- **Dual primary CTAs**—two equally-weighted buttons competing. *(VH, P1)* One primary, the other demoted to secondary or a link.
- **The hero that eats the button**—a giant image/illustration outweighs the primary action. *(VH, P2)* Cut the decoration's weight; the action wins.
- **The rainbow screen**—color used decoratively everywhere, so it can't signal hierarchy. *(VH, P2)* Reserve one accent for the primary action; mute the rest.
- **The flat list pretending to be a hierarchy**—every row identical weight. *(VH, P2)* Differentiate the lead item, or add grouping by space.
- **The modal reflex**—interrupting the screen's purpose with a dialog for something that could be inline. *(VH, P2)* Exhaust inline and progressive alternatives first.
- **The icon-only mystery nav**—unlabeled icons forcing recall. *(IA, P2)* Add labels; recognition beats recall.

---

## Quick reference card

```
PURPOSE    "This screen exists so the user can ___."   (no "and")
ACTION     one primary action, period
IA         everything on screen serves that one job · group related · label plainly
DISCLOSE   every element → Now / On-demand / Never · ≤4 at any decision point
HIERARCHY  1 primary · 2–3 secondary · rest ambient · space → weight → size → color
NEVER      hide price, required fields, consequences, or the primary action
```

*Defaults for a task screen. On a hub the ≤4 binds per row; on an exploration surface, per item.*


---

# Focal Examples

Two worked examples showing the quality bar and the locked output templates in use—one **review**, one **build**. They share a narrative: the review flags a cluttered dashboard that's doing three jobs, and the build designs one of the screens it recommends splitting out. Illustrative, not a real product.

---

## Example 1—Review: a cluttered analytics dashboard

**Input (what was handed in):** the "Home" screen of an analytics product. 8 same-size KPI cards, a 14-item ungrouped sidebar, two equally-weighted buttons ("Create report" and "Upgrade"), 6 always-visible filters, a recent-activity feed, a chart, and a "tips" banner.

**Focal's output:**

```
**Verdict:** No—three jobs on one screen (monitor, build a report, upsell). No visual entry point. · 5/12

**Screen:** Analytics product home/overview · register: hub · audience: mixed

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Information Architecture | 1/4 | Monitoring, report-building, and an upsell share one screen—three intents |
| Progressive Disclosure | 2/4 | 8 equal KPIs and 6 filters shown at once; no defaults, nothing deferred |
| Visual Hierarchy | 2/4 | 8 same-size cards + two primary buttons—nothing wins the eye |
| **Total** | **5/12** | **significant rework** |

## Issues (most severe first)
- **[P0 · IA]** Three competing jobs—monitor metrics, build a report, upgrade the plan—collapsed onto one screen. Users scan instead of acting. **Fix:** make this a monitoring hub; route "Create report" to its own screen and move "Upgrade" into the account menu.
- **[P1 · Hierarchy]** Dual primary buttons ("Create report" + "Upgrade") compete at equal weight. **Fix:** a hub needs at most one primary; here, let the most-watched metric be the focal point and demote both buttons.
- **[P1 · Disclosure]** 8 KPI cards at identical weight blow past the ~4-chunk glance budget. **Fix:** surface the 3–4 metrics this audience checks daily; move the rest behind "More metrics."
- **[P2 · Disclosure]** 6 filters always visible. **Fix:** default to the common view (last 7 days); collapse the rest under "Filters."
- **[P2 · IA]** 14-item sidebar, ungrouped. **Fix:** group into 4–5 labeled sections—recognition over scanning.

## Top 3 moves
1. Cut the screen to one job—monitoring—and route report-building and upgrade elsewhere.
2. Promote 3–4 daily metrics to a clear visual lead; defer the rest.
3. Default the filters and group the sidebar into labeled sections.
```

---

## Example 2—Build: the "Create report" screen

**Input:** "Design the Create report screen we just split out of the dashboard."

**Focal's output:**

```
**Screen:** Create report—exists so the user can generate one report from a chosen dataset and date range. Primary action: Generate report.
**Register:** task   ·   **Audience:** mixed

## Information
- Dataset—single select (the one required choice)
- Date range—preset picker, default "Last 30 days"
- Report name—text field, optional, default "Untitled report"
- Generate report—primary button
- Moved off: scheduling, sharing, export format → these belong to a report that already exists (the result screen), not its creation

## Disclosure
- Now: dataset, date range, Generate
- On-demand: advanced filters + grouping → behind "Advanced options" (collapsed)
- Cut: format / recipients / schedule—not needed to create the report

## Hierarchy
- Primary: Generate report
- Secondary: dataset + date range (the two real inputs)
- Ambient: report-name field, "Advanced options" link

## Gates
- [x] One-sentence purpose, no "and"
- [x] Exactly one primary action (Generate)
- [x] Grouped + labeled; no orphans; no memory bridge (dataset chosen where it's used)
- [x] ≤4 chunks at any decision point (name, dataset, range, generate)
- [x] Squint test passes—Generate + the two inputs dominate
- [x] Empty / loading / error / full (worst-case) states designed (no datasets → "Connect a source"; generating → progress; error → inputs preserved; 500-column dataset → range still scannable)
```

---

**Why these two:** the review never just lists problems—it ends on three ranked moves. The build never returns prose—it returns the same Screen Spec every time. And the second example resolves the first: "split Create report onto its own screen" becomes an actual single-purpose screen. That is the whole method in motion—one screen, one purpose, both directions.
