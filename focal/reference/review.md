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

- **Structural**—wrong job, screens to split or merge, content to regroup or relabel, disclosure to re-triage. These change what the screen *is*. Resolve them first with the five-move build workflow in [SKILL.md](../SKILL.md).
- **Executional**—visual weight, color, type, spacing, motion, transitions. These change how the screen *looks*. Apply them in your own design system once the structure is sound.

Always fix structural before executional: polishing a screen with the wrong purpose only organizes the clutter. Re-run the audit after fixes to watch the score climb.
