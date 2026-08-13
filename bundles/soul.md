# Soul—single-file bundle

This is the complete **Soul** skill as one self-contained document—the spine plus every reference—so you can use it in any AI coding agent, not only Claude Code.

*Synchronized manually from `soul/` source files on the working tree; no commit hash is asserted until commit.*

**How to use it**
- **Claude Code**—you don't need this file; install the `soul/` folder from the repo for `/soul` and on-demand loading. This bundle is for everything else.
- **Codex (CLI)**—append it to your project's `AGENTS.md`, which Codex loads automatically: `cat soul.md >> AGENTS.md`.
- **ChatGPT**—create a Custom GPT and paste this into *Instructions*, or upload it as a *Knowledge* file. A Project works the same way.
- **Cursor / Windsurf / Cline**—add it as a rules file, e.g. `.cursor/rules/soul.md`.

Everything below is the skill, including the full 0–4 / 16 scoring rubrics.

---

---
name: soul
description: Use when a product works but feels like nothing—generic, forgettable, indistinguishable from its competitors. Soul maps the happy path and sorts every beat into three tiers—Expected (stays functional), Elevated (the same moment with more craft—the small delights), and Net-New (an entirely new experience, reserved for the 2–3 biggest moments). Places by reach and memory, splits treatments by frequency so repetition never turns delight into noise, and refuses the traditional dumping grounds (404 pages, easter eggs, error mascots) where delight goes to be unseen. Triggers on boring, bland, generic, soulless, forgettable, delight, personality, charm, whimsy, juice, microinteractions, wow moment, celebration, empty state, success state, first impression, "make it memorable", "feels generic". Not for screen structure (use Focal), flows and navigation (use Compass), retention and activation leaks (use Flywheel), brand identity systems, or marketing pages.
argument-hint: "[build | search] <product, flow, or moment>"
---

# Soul

**Never boring.**

Most products work and feel like nothing. Every screen functional, every flow passable, nothing anyone would describe to a friend. The word people reach for is *soulless*, and the word is a diagnosis: nothing here was authored. The product is the average of its competitors.

**Soul is not a spec—it is what accumulates when specific moments are placed well.** So this skill does not sprinkle. It maps the default path and sorts every beat into one of three tiers—what stays functional, what gets more craft, and the 2–3 moments that get rebuilt entirely.

Three facts decide every placement:

- **People remember the peak and the ending, not the average.** A product with two entirely new moments and quiet craft on everything else is remembered. A product with twelve novelties is exhausting, and nothing in it reads as significant.
- **Reach beats risk.** Delight traditionally goes where failing is cheap—the 404 page, the easter egg—which is exactly where nobody walks. Placement here is chosen by reach × memory: the default path, because that is where everyone is.
- **Repetition kills novelty.** The 50th confetti is noise. A treatment that plays every session must survive its 50th viewing; a treatment that plays once may spend everything.

**The three tiers.** Every beat on the path gets exactly one:

| Tier | What it is | Where it goes | The test |
|---|---|---|---|
| **Expected** | the obvious version, fully functional | beats that must simply work | nothing missing, nothing added |
| **Elevated** | the same moment, executed with more craft | the small things, spread wide—this is how a product stops being boring | nothing new is introduced |
| **Net-New** | an entirely new experience in place of the old one | the 2–3 biggest moments—this is the core work | it could not be mistaken for a competitor, or for the moment it replaced |

---

## When to use

Soul is for a product that already works but reads as anonymous: a functional-but-flat happy path, a success state that stops instead of lands, an ending nobody designed, a personality budget with nowhere to go. Give it a product, a flow, screens, code, or a description.

It is **not** for:
- Single-screen structure, hierarchy, or clutter—that is [Focal](../focal).
- Multi-screen paths and navigation—that is [Compass](../compass).
- Losing users before they reach value—that is [Flywheel](../flywheel). Soul makes a working path memorable; it cannot make a broken path work, and treatments on a broken path read as cosmetic.
- Brand identity systems, logo, illustration style, or marketing pages. Soul places moments inside the product's default path; it does not define the visual language they are executed in.

---

## Map the path first

Every job starts with the happy path: the default flow the primary user actually walks, entry to outcome. Build it from the artifact; where the artifact is silent, ask—the skeleton below is the interview, seven blanks to fill.

```
1. Enters from [source]
2. Sees [first surface or message]
3. Understands [core value or next step]
4. Takes [primary action]
5. System responds with [result]
6. Reaches [successful outcome]
7. Feels [intended emotional state]
```

- **10–12 beats maximum**, expanded from the skeleton. More than 12 means you are mapping edge cases—stop at the default.
- **Tag every beat** with its touchpoint (screen, email, notification, external) and its frequency: `once` (first-run only), `recurring` (weekly-to-monthly rhythm), `every-run` (every session).
- **Beat 7 is a design input, not decoration.** If nobody can say what the user is meant to feel at the end, that absence is the first finding.
- First-run empty states and waits are beats on this path—they are in scope. Error branches are not on this path—see the dumping-grounds rule below.

## Sort every beat

The tiers have owners:

- **Expected** owns the beats that must simply work—load-bearing convention, high stakes, anywhere addition would tax the task. **Expected is a verdict, not a failure**, and the receipt of Expected beats is half the deliverable.
- **Elevated** owns the small things, and it spreads as wide as the ceilings allow. This is the anti-boring tier: the same moments with more craft—copy in the user's words, feedback that names what changed, response that feels instant. Craft survives repetition; novelty does not, which is why Elevated can be distributed and Net-New cannot.
- **Net-New** owns the 2–3 biggest moments, **never more**, and it is the core work: not the old moment done better but an entirely new experience in its place. Peak-end is the reason for the cap—memory keeps peaks and endings and discards the average, so a fourth Net-New does not add memory, it subtracts significance from the first three.

Walk this for every beat, top to bottom, first match wins:

```
Which tier may this beat take?
├── Off the default path ................. none—dumping ground; relocate the budget
├── The floor fails here ................. none yet—hand off first (leak → Flywheel,
│                                          screen → Focal, maze → Compass)
├── Load-bearing convention .............. Expected—muscle memory is the feature
├── High stakes .......................... Expected, or Elevated in a calm register—
│                                          reassurance before feeling; celebration never
├── Every-run ............................ Elevated at most—repetition-proof craft only
└── Otherwise ............................ Elevated; promote to Net-New only if it ranks
                                           in the 2–3 biggest moments (reach × memory)
```

**The frequency split sets each beat's ceiling:**

- `every-run` beats take only repetition-proof treatment—speed, feel, anticipation, useful variation. Jokes, celebration, and novelty decay with repetition; speed does not.
- `once` beats may take one-shot expressive treatment—this is where storytelling spends well.
- `recurring` beats sit between: intensity below first-run, variation so the 30th arrival still reads as alive.

**The dumping grounds are refused.** 404 pages, error mascots, easter eggs, release-note bits—the traditional homes of product delight, chosen because failing there is cheap. Cheap failure means no reach: the work is unseen, or seen by a frustrated user at the worst moment. When the sweep finds existing delight in a dumping ground, it relocates the effort to a chosen beat. And an error state frequent enough to be worth delighting is a bug to fix, not a moment to elevate—route it to [Flywheel](../flywheel) or [Focal](../focal). One honest edge: a 404 that carries real traffic is not a dumping ground, it is an entry beat—treat it as recovery, one clear path back, no jokes.

Selection heuristics, archetypes, and the full dumping-grounds list live in [reference/moments.md](reference/moments.md).

---

## Routing

- **No argument** → explain the placement idea in three sentences, then ask: search an existing product, or build one moment?
- **`search` / `sweep` / `audit` / `review` / `find` (a product, a flow, screens, or "it feels generic")** → load and follow [reference/review.md](reference/review.md). It maps the path, assigns every beat a tier, scores four gates 0–4 against written rubrics, requires an evidence-based rationale and next-point change for every score, totals to /16, displays a normalized /4 average and common quality band with a weakest-gate ceiling, tags issues P0–P3, and anchors every issue and suggested moment to the exact **Screen · Flow · State · Lifecycle** locator before returning the ranked Net-New moments plus the small things worth elevating. That file defines the rubrics, scoring contract, bands, severities, and audit locator—all of them, and nowhere else.
- **`build` / `design` / `treat` (one beat)** → run the beat through the sort tree above; its tier is the build's **Target**. Read [reference/treatments.md](reference/treatments.md)—plus [reference/moments.md](reference/moments.md) when the target is Net-New, to confirm it clears the selection bar—then follow **Build** below.
- **A question about a moment type or a treatment lever** → [reference/moments.md](reference/moments.md) or [reference/treatments.md](reference/treatments.md).

Before emitting either output, read [reference/examples.md](reference/examples.md). It calibrates length, tone, and what the locked templates look like filled well.

---

## Build: the five moves

1. **Frame it.** The product, the user, the beat, its frequency class, the stakes, and the one feeling this moment should produce—named, not "delight." If you cannot name the feeling, the screen, and the second it happens, you have a brand adjective, not a design target. Stakes are what the user can lose at this beat—money, work, standing, safety. Anything real to lose is high, and high puts reassurance before feeling.
2. **Place it.** Run the beat through the sort tree—its tier is the spec's **Target**. A Net-New target must also clear the selection bar in [reference/moments.md](reference/moments.md); an Elevated target has no bar to clear, only its ceiling to respect. If the request points at a dumping ground, say so and redirect the budget to the nearest on-path beat.
3. **Ladder it.** The path sort names the target tier; the spec still designs the full range from [reference/treatments.md](reference/treatments.md)—Expected as the floor, then Elevated, then Net-New—because rungs below the target are the interim ships and the caller may land there. A rung above the beat's ceiling is written as unavailable, with the reason. The Expected rung is real work, not a strawman: it must be shippable.
4. **Guard it.** No rung may tax speed, comprehension, or the primary action. High-stakes moments get reassurance before feeling. Every-run moments get only what survives repetition.
5. **Run the gates.** Self-check against the **`## Gates`** block of the Moment Spec below—that block is the canonical list. Mark `[x]` only what the spec satisfies; leave `[ ]` with a one-line reason for any it does not.

**Output—the Moment Spec (use this exact structure).** Every build returns this template verbatim, in this order. Fill the `<…>` slots; keep every fixed label.

```
**Moment:** <the beat>—for <who>, on <the first pass | every pass | the nth pass>.
**Feeling:** <one named emotion> · **Frequency:** <once | recurring | every-run> · **Stakes:** <low | medium | high> · **Target:** <Elevated | Net-New>

## Why this moment
- On the path: <where it sits, and who reaches it>
- Worth the budget: <reach × memory—first impression, effort peak, first success, milestone, the ending>
- Today: <what the moment does now—observed from the artifact, or assumed>

## The rungs
- **Expected:** <the floor—the obvious version, fully functional, shippable as-is>
- **Elevated:** <the same moment with more craft—nothing new introduced; the interim ship when the target is Net-New>
- **Net-New:** <an entirely new experience in place of the old one—or "unavailable at this beat's ceiling," with the reason>

## Held constant
- <what no rung may damage—speed, comprehension, the primary action, reversibility>
- <the convention kept, if this beat is muscle-memory>

## Constraints for the pick
- <brand, technical, accessibility, and context limits every rung already respects>

## Gates
- [ ] On the default path—reached without hunting
- [ ] One feeling, named—"soul" and "delight" appear nowhere as specs
- [ ] Survives its frequency—repetition-proof if every-run
- [ ] Proportionate to the moment's magnitude
- [ ] Speed, comprehension, and the primary action untouched
- [ ] Honest without motion and without sound
```

**The pick between rungs is the caller's.** The target names the tier the sort assigned; rungs below it are interim ships, and landing on one is a product decision that belongs to the human. Recommend only when asked.

---

## Voice (when giving feedback)

- **Emit the exact output template.** Search and build each have a locked structure—the build template is above, the search template is in [reference/review.md](reference/review.md). Use it verbatim: same sections, same order, same headers, same table columns. If a section has nothing, keep its header and write "None."
- **Template precedence.** The template is the complete contract for what gets emitted. If any instruction in this skill asks for something the template has no slot for, put it in the nearest slot that fits, or leave it out—never invent a section. A gap like that is a bug in this skill: name it in one line after the output so it can be fixed.
- **Name the feeling, every time.** "Delight," "personality," "magic," and "soul" never appear as specifications. The feeling, the beat, and the second it happens—or it is not a design decision yet.
- **Separate observed from assumed.** Findings read off the artifact and findings inferred from a description carry different weight; the Basis line says which is which.
- **Be specific and quantitative.** "The paid notification says 'Done' and nothing else" beats "the success state is underwhelming." Quote the copy, count the beats, name the second.
- **Locate every issue.** Name the exact beat or touchpoint, rendered app state, and lifecycle occurrence where the treatment—or restraint—belongs.
- **Your output is a spec, not a performance.** Zero wit is the default register; one placed line is the ceiling, and never at anyone's expense.

---

## Absolute don'ts

Match-and-refuse. Each of these is expressiveness spending trust it did not earn.

- **Wit at failure or loss.** The joke at the worst moment reads as mockery. Personality is tested at failure, and it passes the test by restraint.
- **Celebration before confirmation on high-stakes actions.** Confetti before "your money arrived safely" reads as a casino. Reassurance, records, and control come first; feeling comes after.
- **Motion that taxes the task.** Any animation that delays the primary action or comprehension converts delight into friction. Respect reduced-motion preferences without exception.
- **Every-run novelty.** A joke on a beat users hit daily is noise by week two. If the beat is every-run, the treatment is speed, feel, or anticipation—nothing that depends on surprise.
- **The dumping grounds.** Delight placed by low risk instead of reach. If the path is sterile and the 404 has an easter egg, the budget is upside down.
- **Charm covering confusion.** A mascot in front of an unclear flow is a bandage on a structural problem—fix the structure first (Focal or Flywheel), then decide if the moment deserves treatment.
- **Breaking load-bearing convention.** Checkout, save, undo, back—muscle-memory beats rely on the Expected. Novelty there costs comprehension and pays back nothing.
- **"Make it delightful" as a requirement.** Refuse the adjective; extract the moment. Which beat, for whom, feeling what? Then work.
- **Manufactured intimacy.** Personalization the relationship has not earned—first-name warmth from a product used twice, references to sensitive data, false friendship.
- **Decorating a broken path.** If users cannot reliably reach the outcome, hand off before treating anything—a leak is Flywheel's, a screen is Focal's, a maze is Compass's.

---

## References

- [reference/review.md](reference/review.md)—the search mode: the four-gate audit (Baseline, Placement, Proportion, Signature), 0–4 rubrics, /16 bands, severity, and the locked Moment Map template.
- [reference/moments.md](reference/moments.md)—moment archetypes, frequency classes, selection heuristics, the 2–3 rule, and the dumping grounds.
- [reference/treatments.md](reference/treatments.md)—the three tiers in depth, the rungs a build lays out, the craft levers, repetition-proof design, and proportionality.
- [reference/examples.md](reference/examples.md)—a worked search and a worked build, in the locked templates.

---

# Soul Search—the happy-path sweep

Map the default path, sort every beat into a tier, and return the 2–3 Net-New moments plus the small things worth elevating. Use when the user asks to search, sweep, audit, review, or find—or hands over a product with "it feels generic," "it's boring," "make it memorable."

## Input modes

- **A product or flow** (screens, a URL, code, a walkthrough)—map the path directly from the artifact. Label findings *observed*.
- **A description** ("a budgeting app where you link accounts and get a weekly summary")—walk the skeleton as an interview, fill the seven blanks, and label findings *walked from a description*. Say plainly which beats are assumed.
- **A symptom** ("nothing about it feels ours")—still map the path first. The symptom picks the emphasis; the map decides the verdict.

## Step 0—Map, then check the floor

Before scoring, establish:

- **The path.** Build the beat table from the skeleton in [SKILL.md](../SKILL.md)—10–12 beats, touchpoint-tagged, frequency-tagged. Don't re-derive the skeleton here.
- **The intended ending feeling.** If nobody can name what the user is meant to feel at beat 7, record "unnamed" in the header—that absence is a finding, and it caps Signature at 2, because a product that has not chosen a feeling cannot have authored one.
- **The floor.** Does the path actually work—reachable outcome, no trust breaks, no maze? If not, the job is not Soul's yet: score Baseline 0–1, make the handoff the first item in **Next**, and keep the moment analysis as "after the path holds." Treatments on a broken path read as cosmetic, and users correctly discount them.
- **The state and lifecycle coverage.** For each observed beat, distinguish the rendered state from its occurrence: first run, steady-state repeat, re-entry, milestone, failure, or recovery. Frequency is cadence, not lifecycle; `recurring` alone does not say whether this is the first success or the fiftieth.
- **Observed or walked?** State which, per the input modes above. Blending them silently turns a heuristic into a false certainty.

## Locate every finding

Before scoring or suggesting a change, build a four-part implementation locator. Every issue, Moment, small thing, Next item, and handoff must carry the same locator:

1. **Screen**—the exact beat, touchpoint, screen, message, or control.
2. **Flow**—the named happy path or transition that contains the beat.
3. **State**—the rendered or system condition: default, empty, loading, error, success, notification, and so on.
4. **Lifecycle**—the occurrence in the experience: first run, first success, steady-state repeat, re-entry, milestone, failure, or recovery.

Use concrete moments. `Payment screen → confirmation · payment flow · success notification · first payment received` is actionable; `the happy path` is not. If any locator field is not evidenced, write `not shown` and name the fastest validating trigger in **Coverage** or **Basis**—do not invent it.

## The four gates

Score all four, even when one is obviously the problem—the reader needs to see whether the failure is absence (nothing placed), misplacement (placed where nobody walks), or excess (placed everywhere).

### Gate 1—Baseline *(does the path hold?)*

- Can the primary user get from entry to outcome without confusion, delay, or doubt?
- Is the pace itself a quality signal—fast, stable, immediate acknowledgment?
- Would quiet craft read as intentional here, or would it sit on top of jank?

| Score | Criteria |
|-------|----------|
| 0 | Broken—users cannot reliably reach the outcome, or trust fails on the way; hand off before any treatment |
| 1 | Reachable but taxed—slow, unstable, or confusing enough that expressive treatment would read as cosmetic |
| 2 | Sound but bare—it works; nothing about the execution signals that anyone cared |
| 3 | Quiet quality—fast, stable, comprehensible; the baseline itself reads as intentional |
| 4 | The baseline is the signature—speed and clarity so far above category norm that they are what users describe |

### Gate 2—Placement *(where does the expressiveness live?)*

- List every deliberate expressive touch in the product. How many sit on the default path?
- Is anything living in a dumping ground—404 humor, error mascots, easter eggs—while path beats stay sterile?
- Were the treated beats chosen, or accumulated?

| Score | Criteria |
|-------|----------|
| 0 | Backwards—expressiveness lives in dumping grounds while the path is sterile |
| 1 | Sterile—no deliberately designed moment anywhere on the path |
| 2 | Scattered—touches exist on-path, but nobody chose them; density without placement |
| 3 | Placed—Net-New concentrated on 2–3 chosen moments, craft on the small things, the rest deliberately standard |
| 4 | Placed and ranked—the Net-New moments are the highest reach × memory beats available, and the receipt shows what was refused |

### Gate 3—Proportion *(does intensity fit frequency and magnitude?)*

- Walk each treated beat: does an every-run beat carry novelty that decays, or repetition-proof craft?
- Does feedback intensity match the size of the moment—and on high-stakes actions, does reassurance come before feeling?
- Do the endings outweigh the middles?

| Score | Criteria |
|-------|----------|
| 0 | Inverted—celebration at high stakes before safety is confirmed, or heavy novelty on every-run beats |
| 1 | Uniform—one intensity everywhere, so nothing reads as significant |
| 2 | Mostly fit, one leak—a decayed repeat, or one clearly under-played milestone |
| 3 | Fit—every-run beats repetition-proof, rare beats carrying the expressiveness, intensity matching magnitude |
| 4 | Tuned—variation keeps repeated beats alive without exhausting anyone, and the ending is the strongest beat on the path |

### Gate 4—Signature *(would you know it without the logo?)*

- Name one moment a user would describe to a friend. Is there one?
- Cover the logo: does anything—copy voice, motion character, a specific interaction—identify the product?
- Is the expressiveness coherent, or a pile of borrowed patterns?

| Score | Criteria |
|-------|----------|
| 0 | Anti-signature—the memorable thing is an annoyance, an interruption, or a dark pattern |
| 1 | Anonymous—swap the logo for a competitor's and nobody notices |
| 2 | A style, not a moment—consistent surface, nothing anyone would describe |
| 3 | One authored moment users could describe to a friend |
| 4 | Recognizable without the logo—the moments cohere into a personality that survives success and failure |

## Scoring rules

Every gate uses the same integer anchors:

| Score | Canonical label | Shared meaning |
|---:|---|---|
| **0** | **Broken or harmful** | The dimension fails outright, blocks its core outcome, actively inverts the intended behavior, or creates material harm. |
| **1** | **Major failure** | The outcome may remain technically possible, but the dimension is seriously compromised, unreliable, or largely absent. Substantial correction is required. |
| **2** | **Partial or inconsistent** | The basic function exists, with a material weakness, missing decision, or inconsistency that prevents dependable quality. |
| **3** | **Strong** | Deliberate, dependable, context-appropriate professional work with only minor gaps. This is the normal target for good execution. |
| **4** | **Exemplary** | Fully realized and unusually strong for the relevant context, including realistic states and constraints, with no material gaps. |

Score each gate holistically against its local rubric. Read all checks and evidence, choose the anchor that best describes the gate overall, apply explicit prerequisite caps, and let one severe material failure determine the score when the rubric warrants it. Do not use hidden sub-scores, checklist subtraction, averaging, or half-points. A 4 is exemplary for the gate being scored; Signature may legitimately require recognizable authorship because distinctiveness is what that gate measures.

### Score rationale—required

A score without an explanation is invalid. Fill every scorecard row with the same chain: **evidence → consequence → rubric anchor → next-point change**. State what was observed, inferred, tested, walked, or measured; what it costs the path's authorship or usability; why that evidence earns the integer under the local rubric and stops there; and the smallest concrete change that would raise it one point. A `2` must say what works and name the material weakness; a `3` must name the remaining gap; a `4` must explain why the gate is exemplary and say `None—already exemplary` in the next-point field. If the evidence does not expose a state or lifecycle occurrence, say `not shown` in Coverage/Basis and name the validating check—do not award credit or invent failure.

Keep the native total: `total = Baseline + Placement + Proportion + Signature`. Calculate `average = total / 4`, display it rounded to one decimal place, and apply this shared algorithm:

| Band | Average rule | Native total |
|---|---:|---:|
| **Broken** | `average <= 1.5` | `0–6 / 16` |
| **Significant rework** | `1.5 < average < 2.5` | `7–9 / 16` |
| **Solid** | `2.5 <= average < 3.5` | `10–13 / 16` |
| **Excellent** | `average >= 3.5` | `14–16 / 16` |

Then cap the band by the weakest gate: a minimum of `0` allows only **Broken**, `1` allows at most **Significant rework**, `2` allows at most **Solid**, and `3–4` adds no ceiling. Use the lower-quality result of the average band and this ceiling. The total must equal the exact sum of the four scores.

- **Baseline ≤1 makes the handoff the first move, always.** The moments section still gets filled—the analysis is real—but every treatment is sequenced after the path holds, and **Next** leads with the handoff.
- **An unnamed ending feeling caps Signature at 2.** Authorship requires a choice; no choice, no author.
- **A P0 is a critical blocker regardless of total.** Name it in **Blocker** and remove it before any new treatment ships. Do not mechanically force the affected gate to 0; score it using its rubric.
- **Expected is a verdict, not a deduction.** A beat kept standard on purpose, with the reason on record, supports Placement 3–4. Sterility is only scored down when it is unchosen—the difference is the receipt.

Dimension score, overall quality band, issue severity, critical blocker, and the authored-state verdict are separate. A score of 0 does not automatically imply P0, and a P0 does not automatically rewrite a score to 0. Baseline prerequisite behavior remains a local sequencing and handoff rule, not a universal severity label.

## Issue severity

| Priority | Meaning |
|----------|---------|
| **P0 — Critical** | Blocks the core outcome; traps the user; destroys work or state; causes or risks material harm; hides material cost, consequence, permission, or risk; removes informed choice; or uses coercive manipulation. Fix before release. |
| **P1 — Major** | Materially damages comprehension, completion, orientation, trust, value realization, or return for a meaningful share of users. Fix before release. |
| **P2 — Moderate** | Creates real friction, confusion, dilution, or missed value with a viable recovery, workaround, or limited scope. Fix in the next planned pass. |
| **P3 — Minor** | Low-impact craft, consistency, or polish. Fix when time permits. |

Assign severity from consequence, reach, and recoverability. A methodology rule violation is not automatically P0.

**Ordering (one rule):** sort by priority, P0 first. Within the same priority, path order—earlier beats first, because more people reach them; off-path issues come after on-path issues of the same priority. Never reorder across priorities.

Note the deliberate asymmetry: **issues** are ordered by path position, but **moments** are ranked by reach × memory—which is why an ending can outrank a first impression in the moments list even though it sits later on the path. Memory weights endings; drop-off weights beginnings.

## Output format—use this exact structure

Every search returns this template verbatim, in this order. Don't add, remove, reorder, or rename sections. Fill the `<…>` slots; keep every fixed label. This block is the single source of truth for the emitted shape.

```
**Verdict:** <the state, one phrase> · <the biggest missed or misplaced moment> · **<total>/16**

**Product:** <what it is, for whom> · **Path:** <N> beats, <entry> → <outcome> · **Ends feeling:** <the intended emotion, or "unnamed">
**Screen:** <exact touchpoint(s) or `not shown`>
**Flow:** <named happy path or transition(s) or `not shown`>
**State:** <exact rendered or system state(s) reviewed>
**Lifecycle:** <exact occurrence(s) reviewed>
**Coverage:** <app states and lifecycle occurrences actually reviewed> · gaps: <material states or occurrences not shown or triggered, or "none">
**Basis:** <observed from a screenshot or artifact | inferred from code | tested in a prototype or live product | walked from a description | measured from product data> · confirm with: <the fastest validating check>
**Blocker:** <None. | concise blocker reason>

## The path
| # | Beat | Touchpoint | Frequency | Verdict |
|---|---|---|---|---|
| 1 | <enters from…> | <surface> | <once | recurring | every-run> | <Expected | Elevated | Net-New (Moment 1)> |

## Scorecard
| Gate | Score | Why this score | What raises it one point |
|---|---:|---|---|
| Baseline | _/4 | <evidence → consequence → rubric anchor> | <smallest concrete change, or `None—already exemplary`> |
| Placement | _/4 | <evidence → consequence → rubric anchor> | <smallest concrete change, or `None—already exemplary`> |
| Proportion | _/4 | <evidence → consequence → rubric anchor> | <smallest concrete change, or `None—already exemplary`> |
| Signature | _/4 | <evidence → consequence → rubric anchor> | <smallest concrete change, or `None—already exemplary`> |
| **Total** | **_/16 · _._/4** | **<band; exact sum of justified component scores>** | <weakest-gate ceiling applied> |

## The moments (Net-New, ranked by reach × memory)
### Moment 1—<beat>, <the named feeling>
- **At:** screen: <exact beat/touchpoint> · flow: <named happy path or transition> · state: <exact app state> · lifecycle: <exact occurrence>
- Why here: <reach × memory, one line>
- Expected: <one line> · Elevated: <one line> · Net-New: <one line>
- Constraints: <one line>

## The small things (Elevated)
- **At:** screen: <exact beat/touchpoint> · flow: <named happy path or transition> · state: <exact app state> · lifecycle: <exact occurrence> · Beat <n>—<the craft touch, one line>

## Issues (most severe first)
- **[P0 · beat <n>]** **At:** screen: <exact beat/touchpoint> · flow: <named happy path or transition> · state: <exact app state> · lifecycle: <exact occurrence>. <Name>—<observation>. <what it costs>. **Fix:** <fix>.

## Kept Expected, on purpose
<the beats that stay standard, and the strongest reason—load-bearing convention, every-run frequency, high stakes>

## Next
- **Now**: **At:** screen: <exact beat/touchpoint> · flow: <named happy path or transition> · state: <exact app state> · lifecycle: <exact occurrence> · <the first treatment to ship—or the handoff, if the floor failed>
- **After it lands**: **At:** screen: <exact beat/touchpoint> · flow: <named happy path or transition> · state: <exact app state> · lifecycle: <exact occurrence> · <the second moment>
- **Hand off**: **At:** screen: <exact beat/touchpoint or `not shown`> · flow: <named happy path or transition or `not shown`> · state: <exact app state or `not shown`> · lifecycle: <exact occurrence or `not shown`> · <screen structure → Focal; path or navigation → Compass; a leak → Flywheel; "None" if all of it is Soul's>
```

Filling it:
- **The path**—one row per beat, every beat, including the sterile ones. The Verdict column is where restraint becomes visible: most rows read Expected. A beat whose first pass differs from its steady state carries both tags—`every-run (first run: once)`—and the `once` tag is the one a Moment may spend.
- **The moments**—repeat the Moment block for each of the 2–3 Net-New moments, ranked. The rung lines show the floor-to-target range in one line each; a full ladder belongs in a follow-up `build`.
- **The small things**—one line per Elevated touch, only craft the beat's ceiling allows: on every-run beats that is speed, feel, anticipation, or useful variation. Write "None." if the ceilings leave nothing.
- **Coverage**—name only states and lifecycle occurrences actually observed or walked. Use `gaps` for material variants such as first run, repeated use, re-entry, failure, recovery, or the real success trigger that were not shown.
- **Issues and suggestions**—repeat the line once per issue, and give every issue, Moment, small thing, Next item, and handoff a complete **screen · flow · state · lifecycle** locator. Keep the `At` locator precise enough to trigger the same moment and see the same state. If nothing ranks above P3, write "None above P3." under the header and keep the header.
- **Basis**—never claim observation you do not have. "Walked from a description" with the assumed beats named is a stronger answer than borrowed confidence.

---

# Moments—where the budget goes

A moment is a beat on the happy path that earns the Net-New tier—an entirely new experience, not a better version of the old one. This file is how you find the 2–3, rank them, and sort everything else into Elevated or Expected.

## The frequency classes

Frequency is destiny for a treatment—it decides what a moment may carry before anything else does.

| Class | What it is | What it may take | Why |
|---|---|---|---|
| `once` | first-run beats: first impression, first success, setup completion | one-shot expressive treatment—storytelling, sequence, ceremony | it plays once, so it may spend everything |
| `recurring` | weekly-to-monthly rhythm: a report ships, an invoice is paid, a milestone lands | mid intensity, with variation—the 30th arrival must still read as alive | familiar enough to expect, rare enough to feel |
| `every-run` | every session: open, navigate, compose, save, send | repetition-proof craft only—speed, feel, anticipation, useful variation | novelty decays with repetition; speed does not |

**The 50th-viewing test:** before treating any beat, say its frequency out loud and imagine the treatment on its 50th appearance. Confetti fails at 3. A 200ms save that used to take 2 seconds never fails.

## The archetypes

Eight places soul is usually won or lost. Skeleton positions refer to the 7-beat map in [SKILL.md](../SKILL.md).

| Archetype | Skeleton position | Frequency | Candidate feelings | What usually goes wrong |
|---|---|---|---|---|
| **The first impression** | beats 1–2 | once | curiosity, recognition, relief | generic welcome copy; a form where an experience should be |
| **The first success** | beats 5–6, first pass | once | capability, pride | the product's biggest moment announced by a toast |
| **The wait** | beat 5, when work takes >1s | varies | anticipation, confidence | a spinner where evidence of work should be |
| **The effort peak** | beat 4 at its hardest | varies | momentum, control | the hardest step is also the most sterile |
| **The ending** | beat 6 | varies | completion, relief, pride | it stops instead of landing—the most neglected surface in most products |
| **The milestone** | recurring passes | recurring | progress, accumulation | either silent, or identical the 40th time |
| **The handoff** | the artifact that leaves the product | recurring | pride to the sender, sense to the receiver | an export nobody would show anyone |
| **The return** | re-entry after absence | recurring | continuity, being known | a cold start where a "welcome back" state should be |

Three boundary notes. *The first success* is the beat where first value lands—Flywheel's term for the event that changes the user's situation; if the product loses people before this beat, that is a leak, and leaks go to [Flywheel](../flywheel) before treatments. *The return* is expressive treatment on re-entry—whether re-entry restores context at all is Flywheel's continuity question; Soul makes a working return felt, not a broken one work. *The ending* keeps its rank even when it is every-run—a session ending that merely stops is the most common miss on any path—but an every-run ending takes repetition-proof levers only; ceremony belongs to rare endings.

## Selection—the bar a moment must clear

Rank candidates by **reach × memory**: how many users hit this beat, times how likely the beat is to be what they remember. Peak-end weights the scale—the emotional peak and the ending hold memory far beyond their share of the path, which is why the ending can outrank the first impression even though fewer people arrive there. **When two candidates tie, take the later one**—peak-end weights endings, so the later beat holds more memory per user who reaches it.

Then interrogate the shortlist:

1. Where would a generic execution actively hurt—cost trust, cost the story users tell?
2. What is public-facing—screenshotted, demoed, shared, judged by people who are not users yet?
3. Where does the user's effort peak? High effort is high emotional energy; treatment there converts strain into momentum.
4. Which beats carry the product's distinctive claims? Those are the strongest Net-New candidates.
5. What would marketing show? If nothing on the path is showable, that is the finding.

**Take the top 2–3 as Net-New. Never more.** The fourth rebuilt moment does not add memory; it subtracts significance from the first three. Everything below the line takes **Elevated** where its ceiling allows craft that pays, and **Expected** otherwise—recorded either way, because the receipt is what separates restraint from neglect.

**Reasons a beat stays Expected** (any one suffices):
- **Load-bearing convention**—checkout, save, undo, back. Muscle memory is the feature; novelty there costs comprehension and pays nothing.
- **Every-run frequency with no repetition-proof lever available**—if speed and feel are already at ceiling, standard is correct.
- **High stakes, calm already present**—money movement, health data, and irreversible actions want reassurance and records before anything else. Where the calm, clear version already exists, standard is the treatment; where it does not, calm *is* the treatment (see proportionality in [treatments.md](treatments.md)). Trustworthy restraint is an emotional choice, not the absence of one.
- **Below the line**—a fine Net-New candidate that lost to a better one; it takes Elevated craft instead, and loses nothing but the rebuild. Two is a budget, not a quota.

## The dumping grounds

The canonical list. These are where delight traditionally goes—chosen because failing there is cheap, which is exactly the problem: cheap failure means no reach, and no reach means the work is unseen or seen by a frustrated user at the worst possible moment.

- **404 and error pages**—reached by accident, read in annoyance.
- **Error mascots and cheerful failure copy**—wit at the moment the user is most tense reads as mockery.
- **Easter eggs and hidden games**—found by almost nobody, by definition off every path.
- **Release notes bits**—read by a rounding error of the user base.
- **Splash-screen and loading-copy jokes on every-run loads**—novelty on repeat decays into noise; if the wait is real, show the work instead.

**The two moves when the sweep finds delight in a dumping ground:**
1. **Relocate the effort.** The craft is real; the placement is wrong. Name the on-path beat that deserves it.
2. **Fix the frequency, not the feeling.** An error state frequent enough to be worth delighting is a bug to fix, not a moment to elevate—route it to [Flywheel](../flywheel) (a leak) or [Focal](../focal) (a screen).

One honest edge: a 404 that carries real traffic—dead links shared socially, a renamed content library—is not a dumping ground. It is an entry beat for those users. Treat it as recovery: state what happened, one clear path to the likely destination, zero jokes. The rule was never "404s don't matter"; it was "placement follows reach."

---

# Treatments—the three tiers

The path sort assigns every beat a **tier**—its verdict. A build designs the **rungs**—the full range for one beat, floor to target—so the caller can land anywhere on it without re-briefing. Same three names, two uses: the tier is where a beat ends up; the rungs are the steps a build lays out getting there.

## Expected—the obvious version

The fully functional execution a competent team ships without thinking hard. Standard pattern, standard copy, standard feedback.

**Expected is real work, not a strawman.** It must be shippable, because the beats that must simply work—load-bearing convention, high stakes, anywhere addition taxes the task—end here as the final answer, on purpose. Getting Expected right is also the precondition for the other tiers: an Elevated treatment of a broken interaction is polish on a defect.

**The test:** nothing missing, nothing added. A user relies on it without noticing it.

Examples of the register: a standard signup form, a clear confirmation toast, a conventional dashboard layout, a plain progress bar, a system-default notification.

## Elevated—the same moment, executed with visible care

Nothing new is introduced. The existing thing, done at a grade users can feel even when they cannot say why: hierarchy sharpened, copy in the user's words, motion that explains, feedback that names what changed, an empty state that starts the work, a wait that shows the work.

**Elevated is the anti-boring tier.** It spreads to every beat whose ceiling allows it—craft survives repetition, so distributing it raises the whole path without exhausting anyone. Concentration is for Net-New; distribution is for craft.

**The test:** describe the treatment in one sentence—if the sentence needs a new noun (a new feature, a new surface, a new mechanic), it is not Elevated, it is Net-New wearing modest clothes.

Examples of the register: the confirmation that states the amount and the running total instead of "Done"; the upload that shows filenames processing instead of a spinner; the form whose labels anticipate the next question; the settle animation that gives a completed payment weight.

**On `every-run` and high-stakes beats, Elevated is also the ceiling**—it raises quality without spending novelty, so it survives repetition and never competes with reassurance.

## Net-New—an entirely new experience

An entirely new experience in place of the old one—not the same moment executed better. Elevated asks how well the moment can be executed; Net-New asks what the moment could be instead. A new mechanic, surface, or artifact that makes the moment itself a reason to talk about the product.

**The test:** it could not be mistaken for a competitor—or for the moment it replaced.

Examples of the register: a live visualization where a table was assumed; a personalized artifact worth keeping (a year-in-review, a printable record, a shareable result card); an interactive demo where static onboarding was assumed; a progress mechanic that accumulates something users check voluntarily.

**Net-New ships only on the 2–3 chosen moments, never more.** It spends surprise, and surprise concentrates—spread thinner, none of it clears the threshold of memorable. (In a build, the Net-New rung still gets designed for any beat whose ceiling allows it—ideation is free; the ration is on shipping.) Two rules keep the tier honest:
- **It must survive its frequency.** A Net-New mechanic on an every-run beat must be useful on the 50th run, not clever on the first. If it is only clever, move it to a `once` or `recurring` beat.
- **It must be worth keeping, not just worth noticing.** The strongest Net-New treatments produce an artifact or capability the user returns to; the weakest produce a reaction and then a chore.

## The levers

What treatments are actually made of. Every lever carries its own failure mode—both columns matter.

| Lever | Used well | The failure mode |
|---|---|---|
| **Speed** | the response so fast it reads as attention; the strongest every-run lever there is | none—speed does not decay, which is why it ranks first |
| **Feel** | weight, physics, and settle that make interaction tactile | motion that delays the action it decorates |
| **Language** | copy in the user's words, at the moment's temperature; the highest-leverage lever per hour spent | charm before clarity; a voice that jokes at tense moments |
| **Anticipation** | the field pre-filled, the next step staged, the default that shows the product was paying attention | guessing wrong confidently; anticipation that removes control |
| **Continuity** | picking up exactly where the user left off, visibly | claiming to know the user better than the relationship supports |
| **Ceremony** | sequence and pacing that give a rare moment weight—reserved for `once` and milestones | ceremony on routine actions; the 12-second animated unboxing of a weekly report |
| **Accumulation** | progress that visibly builds into something owned—streak-free, pressure-free | streaks and guilt; accumulation that punishes absence |

**Sound is opt-in and off by default.** Meaning never depends on it.

## Repetition-proof design

What survives the 50th viewing, in order of durability:

1. **Speed**—never decays. The fastest thing in the category is a signature by itself.
2. **Feel**—physics reads as quality indefinitely; nobody tires of a door that closes well.
3. **Anticipation**—being known stays pleasant as long as it stays accurate.
4. **Useful variation**—content that reflects real state (this week's number, this run's result) is different every time for free.
5. **Cosmetic variation**—a rotating copy pool reads as alive for a while; the pool is always smaller than it looks. Last resort, small doses.

What decays: jokes, confetti, celebration sounds, surprise of any kind, mascot appearances, animated sequences longer than the action they follow. All of these are `once`-class material or cut.

## Proportionality

Feedback intensity matches the size of the moment, and high stakes reorder the sequence:

- **Routine completion**—confirm clearly, offer the next step. No more.
- **Meaningful progress**—name what changed, show the accumulation, restrained motion.
- **Major milestone**—ceremony earned: a designed pause, a summary, an artifact.
- **High-stakes success**—reassurance, records, and control **before** any feeling. The user confirms their money moved safely before anything celebrates. Calm outperforms excitement everywhere the user has something to lose.

Over-celebrating the routine reads as juvenile and burns trust in every future celebration; under-playing the milestone reads as indifference. Both are Proportion failures in the scorecard, and they are the same failure: intensity decided by habit instead of by the moment.

## The accessibility floor

No rung ships below it: treatments honor `prefers-reduced-motion` with a complete non-animated equivalent, meaning never depends on color, motion, or sound alone, focus and keyboard paths survive the treatment, and copy stays legible at the moment's reading pace—a 2-second toast cannot carry a 12-word sentence.

---

# Soul Examples

Two worked examples in the locked templates—one **search**, one **build**. They share a narrative: the search finds an invoicing product spending its personality budget in all the wrong places, and the build treats the moment the search ranked first. These set the bar for length, specificity, and tone; the templates set the shape.

---

## Example 1—Search: an invoicing tool that "feels generic"

**Input:** *"Users say the product feels like every other invoicing app. Make it more delightful?"* Screenshots and a walkthrough: freelancers compose and send invoices, clients pay, payments land as OS-default notifications. The product has a mascot that appears on error dialogs saying "Whoops! Gremlins!", confetti on every invoice send, and a hidden breakout game on the 404 page that the team is proud of.

**Soul's output:**

```
**Verdict:** functional but forgettable · the product's biggest moment—getting paid—is a system-default notification · **7/16**

**Product:** invoicing for freelancers · **Path:** 7 beats, bookmark → payment landed · **Ends feeling:** unnamed—relief is the obvious candidate, and nobody has chosen it
**Screen:** dashboard, invoice composer, payment notification, and 404
**Flow:** invoice-to-payment
**State:** recurring default, invoice-send success, payment success notification, failed-send error, and invalid-route recovery
**Lifecycle:** first run, recurring use, first value, re-entry, and accidental off-path visit
**Coverage:** recurring default path, first-run dashboard, invoice-send success, payment success notification, failed-send error, and 404 · gaps: payment failure, notifications disabled, re-entry after lapse, and later milestones not triggered
**Basis:** observed from a screenshot or artifact · confirm with: trigger a real payment and read the actual notification—the claim the verdict rests on
**Blocker:** The mascot jokes through a failed send, risking trust and material financial harm while the invoice's delivery state is uncertain.

## The path
| # | Beat | Touchpoint | Frequency | Verdict |
|---|---|---|---|---|
| 1 | Enters from bookmark | web app | every-run | Expected |
| 2 | Sees dashboard—outstanding and recent | screen | every-run (first run: once) | Net-New (Moment 3, first run) |
| 3 | Understands who owes what | screen | every-run | Elevated |
| 4 | Composes invoice—client, items, due date | screen | recurring | Expected |
| 5 | Sends—confirmation appears | screen | recurring | Net-New (Moment 2) |
| 6 | Payment lands—notification | push/email | recurring | Net-New (Moment 1) |
| 7 | Sees dashboard updated—paid, month total | screen | recurring | Elevated |

## Scorecard
| Gate | Score | Why this score | What raises it one point |
|---|---:|---|---|
| Baseline | 3/4 | The default path is fast, clear, and reachable, so expressive treatment will not read as a cover for broken UX; the evidence does not show a signature-level baseline, which keeps it at Strong. | Make the payment confirmation equally fast, clear, and dependable across the actual notification and re-entry states. |
| Placement | 2/4 | Confetti exists on the path but is unchosen, while the strongest craft lives on a 404; expressive effort is present but materially misplaced away from the moments most people remember. | Move the budget to two or three chosen path beats, especially payment and the ending. |
| Proportion | 1/4 | Confetti fires on a routine send while the payment peak is silent; intensity ignores frequency and magnitude, so repetition becomes noise and the payoff becomes flat. | Remove recurring confetti, then tune treatment intensity to beat frequency and consequence. |
| Signature | 1/4 | Swap the logo and the product is indistinguishable; the mascot is generic and the ending feeling is unnamed, so no authored moment identifies the product. | Choose the ending feeling and build one distinctive payment or completion moment around it. |
| **Total** | **7/16 · 1.8/4** | **Significant rework; exact sum of justified component scores** | Weakest-gate ceiling applied |

## The moments (Net-New, ranked by reach × memory)
### Moment 1—Payment lands (beat 6), relief
- **At:** screen: payment notification and dashboard · flow: invoice-to-payment · state: successful payment · lifecycle: first and recurring value realization
- Why here: the entire point of invoicing, reached by every paying client, and it is the peak and near-ending of the path—currently rendered as "Invoice #1042 was paid."
- Expected: notification names client, invoice, and amount · Elevated: amount-first copy, a paid-receipt block, the outstanding total visibly settling to its new value · Net-New: a Paid ledger—a year-view that fills with each payment and exports clean at tax time
- Constraints: money moment—records and amounts precede any feeling; no sound.

### Moment 2—Send (beat 5), confidence
- **At:** screen: invoice send confirmation · flow: invoice-to-payment · state: successful send · lifecycle: recurring invoice creation
- Why here: the effort peak, and the anxiety is "does it look professional to my client"—the confirmation answers a different question than the one being asked.
- Expected: "Sent to client@" with timestamp · Elevated: preview exactly as the client sees it, then a delivered state · Net-New: a client-facing invoice page polished enough to be the freelancer's storefront
- Constraints: nothing may delay the send action itself.

### Moment 3—First-run dashboard (beat 2, first pass), possibility
- **At:** screen: first-run dashboard · flow: invoice-to-payment · state: empty state · lifecycle: first run
- Why here: the first impression, every user, exactly once—a `once` beat that can carry expressive treatment the recurring beats cannot.
- Expected: "No invoices yet" plus a button · Elevated: an empty state that starts the work—a sample invoice and "your first takes 2 minutes" · Net-New: composing the first invoice is the onboarding; the form is the tour
- Constraints: one primary action; the sample must be deletable in one tap.

## The small things (Elevated)
- **At:** screen: dashboard outstanding summary · flow: invoice-to-payment · state: populated recurring state · lifecycle: recurring use · Beat 3—say it in the freelancer's words: "Who owes you: $4,200 across 3 invoices" instead of "Outstanding: $4,200."
- **At:** screen: updated dashboard · flow: invoice-to-payment · state: payment-settled state · lifecycle: post-payment re-entry · Beat 7—paid rows settle to the bottom with a quiet check; the outstanding total counts down to its new value, and reduced motion gets the delta in text.

## Issues (most severe first)
- **[P0 · off-path]** **At:** screen: Invoice send · flow: invoice-to-payment · state: failed-send error · lifecycle: recurring invoice creation. Wit at failure—the mascot grins through a failed send with "Whoops! Gremlins!" A freelancer whose invoice did not reach a client is losing money while the product jokes. **Fix:** plain error—what happened, whether the invoice is safe, what to do next. If failed sends are frequent, that is a leak for Flywheel, not copy for Soul.
- **[P1 · beat 6]** **At:** screen: Payment landed notification · flow: invoice-to-payment · state: successful payment · lifecycle: first and recurring value realization. The silent payoff—the product's peak moment is an OS-default notification, indistinguishable from a calendar reminder. **Fix:** treat as Moment 1; the Elevated rung alone changes what users remember this product doing.
- **[P1 · off-path]** **At:** screen: 404 page · flow: invoice-to-payment · state: invalid-route recovery · lifecycle: accidental off-path visit. The misdirected budget—the 404 minigame is the most-crafted surface in the product, reached by accident, in annoyance. **Fix:** relocate the craft to Moment 2 or 3; the game itself is cut, not polished.
- **[P2 · beat 5]** **At:** screen: Invoice send confirmation · flow: invoice-to-payment · state: successful send with confetti · lifecycle: steady-state recurring use after novelty has decayed. Decayed repetition—confetti on every send was charming once and is wallpaper by week two, and it spends celebration the payoff never gets. **Fix:** replace with a sent-state that survives repetition—preview, delivered check, done.

## Kept Expected, on purpose
Beats 1 and 4 stay standard. Beat 4 is load-bearing convention—a weekly form freelancers fill from muscle memory, where novelty costs speed. Beat 1 is an every-run entry whose only honest lever is pace, and pace is already at ceiling (Baseline 3).

## Next
- **Now**: **At:** screen: payment notification and dashboard · flow: invoice-to-payment · state: successful payment · lifecycle: first and recurring value realization · the small things and Moment 1's Elevated interim—amount-first notification, receipt block, the settling total—ship while the Net-New ledger is scoped.
- **After it lands**: **At:** screen: Paid ledger and first-run dashboard · flow: invoice-to-payment · state: payment-settled and empty states · lifecycle: first value and first run · Moment 1's Net-New ledger, then Moment 3—the only `once` beat on the path, currently spending nothing.
- **Hand off**: **At:** screen: invoice send error branch · flow: invoice-to-payment · state: failed-send error · lifecycle: recurring invoice creation · None. (If failed sends turn out to be frequent, route the error branch to Flywheel as a leak.)
```

---

## Example 2—Build: the payment moment

**Input:** "Design the payment-landed moment the search ranked first."

**Soul's output:**

```
**Moment:** Payment lands—for a freelancer, on every pass.
**Feeling:** relief · **Frequency:** recurring · **Stakes:** medium · **Target:** Net-New

## Why this moment
- On the path: beat 6, reached by every client who pays—which is every successful use of the product.
- Worth the budget: it is the payoff the whole path exists for, and peak-end says this beat holds more memory than the six before it combined.
- Today: an OS-default notification—"Invoice #1042 was paid."—and a dashboard that shows the change only after a manual refresh. Observed from the artifact.

## The rungs
- **Expected:** notification carries client, invoice number, and amount; the dashboard row flips to Paid on next load. Shippable as-is.
- **Elevated:** the interim ship—the notification leads with what matters: "$1,850 from Meridian Co · Invoice #1042 paid." Opening it lands on the invoice with a paid-receipt block: date, method, a record that exists somewhere. The outstanding total settles to its new value with one 400ms count-down; reduced motion gets the delta in text—"Outstanding: $4,200 → $2,350."
- **Net-New:** the Paid ledger—every payment lands as a row in a year-view that visibly fills, month totals accumulate, and at tax time it exports clean. Relief gains a place to compound into evidence of a working business. Useful on the 400th payment, not merely clever on the first.

## Held constant
- The notification is complete in text alone—no motion, sound, or color required to know you were paid, and it survives OS truncation at 60 characters.
- Records reachable in one tap from the notification, at every rung.
- Nothing celebrates before the amount is stated—money moments put reassurance before feeling.

## Constraints for the pick
- No sound at any rung. No confetti at any rung—recurring frequency plus money rules it out twice.
- Notifications appear on shared and locked screens; amount-first copy is the point, so a "hide amounts" preference ships alongside whichever rung is chosen.

## Gates
- [x] On the default path—reached without hunting
- [x] One feeling, named—"soul" and "delight" appear nowhere as specs
- [x] Survives its frequency—accuracy and accumulation, nothing that depends on surprise
- [x] Proportionate to the moment's magnitude
- [x] Speed, comprehension, and the primary action untouched
- [x] Honest without motion and without sound
```

---

**Why these two:** the search refuses the question as asked. The user said "make it more delightful" and the answer is that delight is already there—in a 404 game and a failure mascot—and the job is relocation, not addition. The verdict names a misplacement, not an absence. Note the tiers doing the restraint: three Net-New moments concentrated where reach × memory peaks, two small things elevated because their ceilings allow only craft, and two beats standard with reasons on record. The build then shows the full range on one moment—Expected floor, Elevated interim, Net-New target—so the caller can land anywhere on the ladder, and proportionality at a money moment: relief is built from records, amounts, and one restrained settle. Celebration never appears, because the frequency is recurring and the subject is money, and either alone would rule it out.

Note what never appears: confetti at any tier, the mascot polished rather than cut, or a fourth Net-New. And the first-run empty state is the only place one-shot expressive treatment is even considered, because it is the only `once` beat on the path.
