---
name: soul
description: Use when a product works but feels like nothing—generic, forgettable, indistinguishable from its competitors. Soul maps the happy path, finds the 2–3 moments worth more than functional treatment, and designs each three ways—Expected (the obvious version), Elevated (the same moment executed with visible care), and Net-New (the version nobody expects). Places by reach and memory, keeps most beats deliberately standard, splits treatments by frequency so repetition never turns delight into noise, and refuses the traditional dumping grounds (404 pages, easter eggs, error mascots) where delight goes to be unseen. Triggers on boring, bland, generic, soulless, forgettable, delight, personality, charm, whimsy, juice, microinteractions, wow moment, celebration, empty state, success state, first impression, "make it memorable", "feels generic". Not for screen structure (use Focal), flows and navigation (use Compass), retention and activation leaks (use Flywheel), brand identity systems, or marketing pages.
argument-hint: "[build | search] <product, flow, or moment>"
---

# Soul

**Never boring.**

Most products work and feel like nothing. Every screen functional, every flow passable, nothing anyone would describe to a friend. The word people reach for is *soulless*, and the word is a diagnosis: nothing here was authored. The product is the average of its competitors.

**Soul is not a spec—it is what accumulates when specific moments are placed well.** So this skill does not sprinkle. It maps the default path, finds the 2–3 moments worth more than functional treatment, designs each at three grades, and keeps everything else deliberately standard.

Three facts decide every placement:

- **People remember the peak and the ending, not the average.** A product with two authored moments and ten standard beats is remembered. A product with twelve decorated beats is exhausting, and nothing in it reads as significant.
- **Reach beats risk.** Delight traditionally goes where failing is cheap—the 404 page, the easter egg—which is exactly where nobody walks. Placement here is chosen by reach × memory: the default path, because that is where everyone is.
- **Repetition kills novelty.** The 50th confetti is noise. A treatment that plays every session must survive its 50th viewing; a treatment that plays once may spend everything.

**The three rungs**, applied to each chosen moment:

| Rung | What it is | The test |
|---|---|---|
| **Expected** | the obvious version, fully functional | nothing missing, nothing added—the floor, and for most beats the correct final answer |
| **Elevated** | the same moment executed at a higher grade | nothing new is introduced; the existing thing, done with visible care |
| **Net-New** | the version nobody expects | a screenshot of it could not be mistaken for a competitor |

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

## Choose the moments

**2–3 moments, never more.** Peak-end is the reason: memory keeps the peak and the ending and discards the average, so a fourth treated moment does not add memory, it subtracts significance from the first three. Every other beat gets the verdict **Expected—and Expected is a verdict, not a failure.** The output says which beats stay standard and why; that receipt is half the deliverable.

Walk this for every candidate beat, top to bottom, first match wins:

```
Is this beat eligible for treatment?
├── Off the default path ................. no—dumping ground; relocate the budget
├── The floor fails here ................. no—hand off first (leak → Flywheel,
│                                          screen → Focal, maze → Compass)
├── Load-bearing convention .............. no—Expected; muscle memory is the feature
└── Otherwise ............................ eligible. Frequency and stakes set the ceiling:
      every-run .......................... repetition-proof levers only
      high stakes ........................ reassurance before feeling; celebration never
      once ............................... may spend everything
```

**The frequency split governs what a moment may take:**

- `every-run` beats take only repetition-proof treatment—speed, feel, anticipation, useful variation. Jokes, celebration, and novelty decay with repetition; speed does not.
- `once` beats may take one-shot expressive treatment—this is where storytelling spends well.
- `recurring` beats sit between: intensity below first-run, variation so the 30th arrival still reads as alive.

**The dumping grounds are refused.** 404 pages, error mascots, easter eggs, release-note bits—the traditional homes of product delight, chosen because failing there is cheap. Cheap failure means no reach: the work is unseen, or seen by a frustrated user at the worst moment. When the sweep finds existing delight in a dumping ground, it relocates the effort to a chosen beat. And an error state frequent enough to be worth delighting is a bug to fix, not a moment to elevate—route it to [Flywheel](../flywheel) or [Focal](../focal). One honest edge: a 404 that carries real traffic is not a dumping ground, it is an entry beat—treat it as recovery, one clear path back, no jokes.

Selection heuristics, archetypes, and the full dumping-grounds list live in [reference/moments.md](reference/moments.md).

---

## Routing

- **No argument** → explain the placement idea in three sentences, then ask: search an existing product, or build one moment?
- **`search` / `sweep` / `audit` / `review` / `find` (a product, a flow, screens, or "it feels generic")** → load and follow [reference/review.md](reference/review.md). It maps the path, scores four gates 0–4 against written rubrics, totals to /16 with a band, tags issues P0–P3, and returns the ranked moments. That file defines the rubrics, the bands, and the severities—all of them, and nowhere else.
- **`build` / `design` / `treat` (one moment)** → confirm the moment sits on the path and is worth the budget ([reference/moments.md](reference/moments.md)), read [reference/treatments.md](reference/treatments.md), then follow **Build** below.
- **A question about a moment type or a treatment lever** → [reference/moments.md](reference/moments.md) or [reference/treatments.md](reference/treatments.md).

Before emitting either output, read [reference/examples.md](reference/examples.md). It calibrates length, tone, and what the locked templates look like filled well.

---

## Build: the five moves

1. **Frame it.** The product, the user, the beat, its frequency class, the stakes, and the one feeling this moment should produce—named, not "delight." If you cannot name the feeling, the screen, and the second it happens, you have a brand adjective, not a design target. Stakes are what the user can lose at this beat—money, work, standing, safety. Anything real to lose is high, and high puts reassurance before feeling.
2. **Place it.** Confirm the beat is on the default path and passes the selection bar in [reference/moments.md](reference/moments.md). If the request points at a dumping ground, say so and redirect the budget to the nearest on-path beat.
3. **Ladder it.** Design all three rungs—Expected, Elevated, Net-New—from [reference/treatments.md](reference/treatments.md). The Expected rung is real work, not a strawman: it must be shippable, because for most beats it ships.
4. **Guard it.** No rung may tax speed, comprehension, or the primary action. High-stakes moments get reassurance before feeling. Every-run moments get only what survives repetition.
5. **Run the gates.** Self-check against the **`## Gates`** block of the Moment Spec below—that block is the canonical list. Mark `[x]` only what the spec satisfies; leave `[ ]` with a one-line reason for any it does not.

**Output—the Moment Spec (use this exact structure).** Every build returns this template verbatim, in this order. Fill the `<…>` slots; keep every fixed label.

```
**Moment:** <the beat>—for <who>, on the <first | every | nth> pass.
**Feeling:** <one named emotion> · **Frequency:** <once | recurring | every-run> · **Stakes:** <low | medium | high>

## Why this moment
- On the path: <where it sits, and who reaches it>
- Worth the budget: <reach × memory—first impression, effort peak, first success, milestone, the ending>
- Today: <what the moment does now—observed from the artifact, or assumed>

## The rungs
- **Expected:** <the obvious version, fully functional—shippable as-is>
- **Elevated:** <the same moment at a higher grade—nothing new introduced>
- **Net-New:** <the version nobody expects—different, not merely more>

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

**The pick between rungs is the caller's.** Soul defines the opportunity and builds the ladder; choosing a rung is a product decision that belongs to the human. Recommend only when asked.

---

## Voice (when giving feedback)

- **Emit the exact output template.** Search and build each have a locked structure—the build template is above, the search template is in [reference/review.md](reference/review.md). Use it verbatim: same sections, same order, same headers, same table columns. If a section has nothing, keep its header and write "None."
- **Template precedence.** The template is the complete contract for what gets emitted. If any instruction in this skill asks for something the template has no slot for, put it in the nearest slot that fits, or leave it out—never invent a section. A gap like that is a bug in this skill: name it in one line after the output so it can be fixed.
- **Name the feeling, every time.** "Delight," "personality," "magic," and "soul" never appear as specifications. The feeling, the beat, and the second it happens—or it is not a design decision yet.
- **Separate observed from assumed.** Findings read off the artifact and findings inferred from a description carry different weight; the Basis line says which is which.
- **Be specific and quantitative.** "The paid notification says 'Done' and nothing else" beats "the success state is underwhelming." Quote the copy, count the beats, name the second.
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
- [reference/treatments.md](reference/treatments.md)—the three rungs in depth, the craft levers, repetition-proof design, and proportionality.
- [reference/examples.md](reference/examples.md)—a worked search and a worked build, in the locked templates.
