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
- **`search` / `sweep` / `audit` / `review` / `find` (a product, a flow, screens, or "it feels generic")** → load and follow [reference/review.md](reference/review.md). It maps the path, assigns every beat a tier, scores four gates 0–4 against written rubrics, totals to /16, displays a normalized /4 average and common quality band with a weakest-gate ceiling, tags issues P0–P3, anchors every issue to the exact beat, app state, and lifecycle occurrence, and returns the ranked Net-New moments plus the small things worth elevating. That file defines the rubrics, scoring contract, bands, severities, and audit locator—all of them, and nowhere else.
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
