# Soul—single-file bundle

This is the complete **Soul** skill as one self-contained document—the spine plus every reference—so you can use it in any AI coding agent, not only Claude Code.

*Generated from `soul/` at commit `105a068`. If the repo has moved on, regenerate rather than edit this file: it is a build artifact, not the source.*

**How to use it**
- **Claude Code**—you don't need this file; install the `soul/` folder from the repo for `/soul` and on-demand loading. This bundle is for everything else.
- **Codex (CLI)**—append it to your project's `AGENTS.md`, which Codex loads automatically: `cat soul.md >> AGENTS.md`.
- **ChatGPT**—create a Custom GPT and paste this into *Instructions*, or upload it as a *Knowledge* file. A Project works the same way.
- **Cursor / Windsurf / Cline**—add it as a rules file, e.g. `.cursor/rules/soul.md`.

Everything below is the skill, including the full 0–4 / 16 scoring rubrics.

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
- Single-screen structure, hierarchy, or clutter—that is Focal.
- Multi-screen paths and navigation—that is Compass.
- Losing users before they reach value—that is Flywheel. Soul makes a working path memorable; it cannot make a broken path work, and treatments on a broken path read as cosmetic.
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

**The dumping grounds are refused.** 404 pages, error mascots, easter eggs, release-note bits—the traditional homes of product delight, chosen because failing there is cheap. Cheap failure means no reach: the work is unseen, or seen by a frustrated user at the worst moment. When the sweep finds existing delight in a dumping ground, it relocates the effort to a chosen beat. And an error state frequent enough to be worth delighting is a bug to fix, not a moment to elevate—route it to Flywheel or Focal. One honest edge: a 404 that carries real traffic is not a dumping ground, it is an entry beat—treat it as recovery, one clear path back, no jokes.

Selection heuristics, archetypes, and the full dumping-grounds list live in reference/moments.md.

---

## Routing

- **No argument** → explain the placement idea in three sentences, then ask: search an existing product, or build one moment?
- **`search` / `sweep` / `audit` / `review` / `find` (a product, a flow, screens, or "it feels generic")** → load and follow reference/review.md. It maps the path, scores four gates 0–4 against written rubrics, totals to /16 with a band, tags issues P0–P3, and returns the ranked moments. That file defines the rubrics, the bands, and the severities—all of them, and nowhere else.
- **`build` / `design` / `treat` (one moment)** → confirm the moment sits on the path and is worth the budget (reference/moments.md), read reference/treatments.md, then follow **Build** below.
- **A question about a moment type or a treatment lever** → reference/moments.md or reference/treatments.md.

Before emitting either output, read reference/examples.md. It calibrates length, tone, and what the locked templates look like filled well.

---

## Build: the five moves

1. **Frame it.** The product, the user, the beat, its frequency class, the stakes, and the one feeling this moment should produce—named, not "delight." If you cannot name the feeling, the screen, and the second it happens, you have a brand adjective, not a design target. Stakes are what the user can lose at this beat—money, work, standing, safety. Anything real to lose is high, and high puts reassurance before feeling.
2. **Place it.** Confirm the beat is on the default path and passes the selection bar in reference/moments.md. If the request points at a dumping ground, say so and redirect the budget to the nearest on-path beat.
3. **Ladder it.** Design all three rungs—Expected, Elevated, Net-New—from reference/treatments.md. The Expected rung is real work, not a strawman: it must be shippable, because for most beats it ships.
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

- **Emit the exact output template.** Search and build each have a locked structure—the build template is above, the search template is in reference/review.md. Use it verbatim: same sections, same order, same headers, same table columns. If a section has nothing, keep its header and write "None."
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

- reference/review.md—the search mode: the four-gate audit (Baseline, Placement, Proportion, Signature), 0–4 rubrics, /16 bands, severity, and the locked Moment Map template.
- reference/moments.md—moment archetypes, frequency classes, selection heuristics, the 2–3 rule, and the dumping grounds.
- reference/treatments.md—the three rungs in depth, the craft levers, repetition-proof design, and proportionality.
- reference/examples.md—a worked search and a worked build, in the locked templates.

---

# Soul Search—the happy-path sweep

Map the default path, judge where the product's expressiveness lives, and return the 2–3 moments worth treating. Use when the user asks to search, sweep, audit, review, or find—or hands over a product with "it feels generic," "it's boring," "make it memorable."

## Input modes

- **A product or flow** (screens, a URL, code, a walkthrough)—map the path directly from the artifact. Label findings *observed*.
- **A description** ("a budgeting app where you link accounts and get a weekly summary")—walk the skeleton as an interview, fill the seven blanks, and label findings *walked from a description*. Say plainly which beats are assumed.
- **A symptom** ("nothing about it feels ours")—still map the path first. The symptom picks the emphasis; the map decides the verdict.

## Step 0—Map, then check the floor

Before scoring, establish:

- **The path.** Build the beat table from the skeleton in the Soul spine above—10–12 beats, touchpoint-tagged, frequency-tagged. Don't re-derive the skeleton here.
- **The intended ending feeling.** If nobody can name what the user is meant to feel at beat 7, record "unnamed" in the header—that absence is a finding, and it caps Signature at 2, because a product that has not chosen a feeling cannot have authored one.
- **The floor.** Does the path actually work—reachable outcome, no trust breaks, no maze? If not, the job is not Soul's yet: score Baseline 0–1, make the handoff the first item in **Next**, and keep the moment analysis as "after the path holds." Treatments on a broken path read as cosmetic, and users correctly discount them.
- **Observed or walked?** State which, per the input modes above. Blending them silently turns a heuristic into a false certainty.

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
| 3 | Placed—2–3 chosen moments on the path, the rest deliberately standard |
| 4 | Placed and ranked—the chosen moments are the highest reach × memory beats available, and the receipt shows what was refused |

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

Score each gate 0–4 using its rubric above. Be honest—a 4 is rare by definition.

- **Bands** (the only band list in this skill; look the string up from here): **13–16** authored · **10–12** one moment from memorable · **7–9** functional but forgettable · **0–6** anonymous or exhausting.
- **The Total must equal the four scores summed**, and its band string must be one of the four above, verbatim.
- **Baseline ≤1 makes the handoff the first move, always.** The moments section still gets filled—the analysis is real—but every treatment is sequenced after the path holds, and **Next** leads with the handoff.
- **An unnamed ending feeling caps Signature at 2.** Authorship requires a choice; no choice, no author.
- **A P0 is blocking regardless of total.** Remove it before any new treatment ships. The band still prints; P0 carries the urgency.
- **Expected is a verdict, not a deduction.** A beat kept standard on purpose, with the reason on record, supports Placement 3–4. Sterility is only scored down when it is unchosen—the difference is the receipt.

## Issue severity

| Priority | Meaning |
|----------|---------|
| **P0** | Expressiveness that costs safety, trust, or comprehension (wit at failure, celebration before confirmation, motion blocking the action)—remove now |
| **P1** | The highest reach × memory beat is silent, or the delight budget is spent where nobody walks—the opportunity cost keeping the product anonymous |
| **P2** | Decayed repetition, disproportionate feedback, or inconsistency that dilutes the authored moments—next pass |
| **P3** | Polish—if time permits |

**Ordering (one rule):** sort by priority, P0 first. Within the same priority, path order—earlier beats first, because more people reach them; off-path issues come after on-path issues of the same priority. Never reorder across priorities.

Note the deliberate asymmetry: **issues** are ordered by path position, but **moments** are ranked by reach × memory—which is why an ending can outrank a first impression in the moments list even though it sits later on the path. Memory weights endings; drop-off weights beginnings.

## Output format—use this exact structure

Every search returns this template verbatim, in this order. Don't add, remove, reorder, or rename sections. Fill the `<…>` slots; keep every fixed label. This block is the single source of truth for the emitted shape.

```
**Verdict:** <the state, one phrase> · <the biggest missed or misplaced moment> · **<total>/16**

**Product:** <what it is, for whom> · **Path:** <N> beats, <entry> → <outcome> · **Ends feeling:** <the intended emotion, or "unnamed">
**Basis:** <observed from the artifact | walked from a description> · confirm with: <the fastest check that would settle the biggest claim>

## The path
| # | Beat | Touchpoint | Frequency | Verdict |
|---|---|---|---|---|
| 1 | <enters from…> | <surface> | <once | recurring | every-run> | <Expected | Moment 1 | Moment 2 | Moment 3> |

## Scorecard
| Gate | Score | Key finding |
|---|---|---|
| Baseline | _/4 | <one line> |
| Placement | _/4 | <one line> |
| Proportion | _/4 | <one line> |
| Signature | _/4 | <one line> |
| **Total** | **_/16** | **<band>** |

## The moments (ranked by reach × memory)
### Moment 1—<beat>, <the named feeling>
- Why here: <reach × memory, one line>
- Expected: <one line> · Elevated: <one line> · Net-New: <one line>
- Constraints: <one line>

## Issues (most severe first)
- **[P0 · beat <n>]** <Name>—<observation>. <what it costs>. **Fix:** <fix>.

## Kept Expected, on purpose
<the beats that stay standard, and the strongest reason—load-bearing convention, every-run frequency, high stakes>

## Next
- **Now**: <the first treatment to ship—or the handoff, if the floor failed>
- **After it lands**: <the second moment>
- **Hand off**: <screen structure → Focal; path or navigation → Compass; a leak → Flywheel; "None" if all of it is Soul's>
```

Filling it:
- **The path**—one row per beat, every beat, including the sterile ones. The Verdict column is where restraint becomes visible: most rows read Expected. A beat whose first pass differs from its steady state carries both tags—`every-run (first run: once)`—and the `once` tag is the one a Moment may spend.
- **The moments**—repeat the Moment block for each of the 2–3, ranked. The rung lines are one line each here; a full ladder for the top moment belongs in a follow-up `build`.
- **Issues**—repeat the line once per issue, tagged with the beat number (or `off-path` for dumping-ground finds). If nothing ranks above P3, write "None above P3." under the header and keep the header.
- **Basis**—never claim observation you do not have. "Walked from a description" with the assumed beats named is a stronger answer than borrowed confidence.

---

# Moments—where the budget goes

A moment is a beat on the happy path that deserves more than functional treatment. This file is how you find them, rank them, and refuse the rest.

## The frequency classes

Frequency is destiny for a treatment—it decides what a moment may carry before anything else does.

| Class | What it is | What it may take | Why |
|---|---|---|---|
| `once` | first-run beats: first impression, first success, setup completion | one-shot expressive treatment—storytelling, sequence, ceremony | it plays once, so it may spend everything |
| `recurring` | weekly-to-monthly rhythm: a report ships, an invoice is paid, a milestone lands | mid intensity, with variation—the 30th arrival must still read as alive | familiar enough to expect, rare enough to feel |
| `every-run` | every session: open, navigate, compose, save, send | repetition-proof craft only—speed, feel, anticipation, useful variation | novelty decays with repetition; speed does not |

**The 50th-viewing test:** before treating any beat, say its frequency out loud and imagine the treatment on its 50th appearance. Confetti fails at 3. A 200ms save that used to take 2 seconds never fails.

## The archetypes

Eight places soul is usually won or lost. Skeleton positions refer to the 7-beat map in the Soul spine above.

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

Three boundary notes. *The first success* is the beat where first value lands—Flywheel's term for the event that changes the user's situation; if the product loses people before this beat, that is a leak, and leaks go to Flywheel before treatments. *The return* is expressive treatment on re-entry—whether re-entry restores context at all is Flywheel's continuity question; Soul makes a working return felt, not a broken one work. *The ending* keeps its rank even when it is every-run—a session ending that merely stops is the most common miss on any path—but an every-run ending takes repetition-proof levers only; ceremony belongs to rare endings.

## Selection—the bar a moment must clear

Rank candidates by **reach × memory**: how many users hit this beat, times how likely the beat is to be what they remember. Peak-end weights the scale—the emotional peak and the ending hold memory far beyond their share of the path, which is why the ending can outrank the first impression even though fewer people arrive there. **When two candidates tie, take the later one**—peak-end weights endings, so the later beat holds more memory per user who reaches it.

Then interrogate the shortlist:

1. Where would a generic execution actively hurt—cost trust, cost the story users tell?
2. What is public-facing—screenshotted, demoed, shared, judged by people who are not users yet?
3. Where does the user's effort peak? High effort is high emotional energy; treatment there converts strain into momentum.
4. Which beat carries the product's one distinctive claim? That beat is where Net-New belongs, if anywhere.
5. What would marketing show? If nothing on the path is showable, that is the finding.

**Take the top 2–3. Never more.** The fourth treated moment does not add memory; it subtracts significance from the first three. Everything below the line gets the verdict **Expected**, recorded with its reason—the receipt is what separates restraint from neglect.

**Reasons a beat stays Expected** (any one suffices):
- **Load-bearing convention**—checkout, save, undo, back. Muscle memory is the feature; novelty there costs comprehension and pays nothing.
- **Every-run frequency with no repetition-proof lever available**—if speed and feel are already at ceiling, standard is correct.
- **High stakes, calm already present**—money movement, health data, and irreversible actions want reassurance and records before anything else. Where the calm, clear version already exists, standard is the treatment; where it does not, calm *is* the treatment (see proportionality in treatments.md). Trustworthy restraint is an emotional choice, not the absence of one.
- **Below the line**—a fine candidate that lost to a better one. Two is a budget, not a quota.

## The dumping grounds

The canonical list. These are where delight traditionally goes—chosen because failing there is cheap, which is exactly the problem: cheap failure means no reach, and no reach means the work is unseen or seen by a frustrated user at the worst possible moment.

- **404 and error pages**—reached by accident, read in annoyance.
- **Error mascots and cheerful failure copy**—wit at the moment the user is most tense reads as mockery.
- **Easter eggs and hidden games**—found by almost nobody, by definition off every path.
- **Release notes bits**—read by a rounding error of the user base.
- **Splash-screen and loading-copy jokes on every-run loads**—novelty on repeat decays into noise; if the wait is real, show the work instead.

**The two moves when the sweep finds delight in a dumping ground:**
1. **Relocate the effort.** The craft is real; the placement is wrong. Name the on-path beat that deserves it.
2. **Fix the frequency, not the feeling.** An error state frequent enough to be worth delighting is a bug to fix, not a moment to elevate—route it to Flywheel (a leak) or Focal (a screen).

One honest edge: a 404 that carries real traffic—dead links shared socially, a renamed content library—is not a dumping ground. It is an entry beat for those users. Treat it as recovery: state what happened, one clear path to the likely destination, zero jokes. The rule was never "404s don't matter"; it was "placement follows reach."

---

# Treatments—the three rungs

Every chosen moment gets designed at three grades. The ladder is the deliverable: it separates what the moment needs from what it could carry, and it gives the caller a real choice instead of a single take-it-or-leave-it design.

## Expected—the obvious version

The fully functional execution a competent team ships without thinking hard. Standard pattern, standard copy, standard feedback.

**Expected is real work, not a strawman.** It must be shippable, because for most beats it ships—9 or 10 of 12 beats on a well-run path end here, on purpose. Getting Expected right is also the precondition for the other rungs: an Elevated treatment of a broken interaction is polish on a defect.

**The test:** nothing missing, nothing added. A user relies on it without noticing it.

Examples of the register: a standard signup form, a clear confirmation toast, a conventional dashboard layout, a plain progress bar, a system-default notification.

## Elevated—the same moment, executed with visible care

Nothing new is introduced. The existing thing, done at a grade users can feel even when they cannot say why: hierarchy sharpened, copy in the user's words, motion that explains, feedback that names what changed, an empty state that starts the work, a wait that shows the work.

**The test:** describe the treatment in one sentence—if the sentence needs a new noun (a new feature, a new surface, a new mechanic), it is not Elevated, it is Net-New wearing modest clothes.

Examples of the register: the confirmation that states the amount and the running total instead of "Done"; the upload that shows filenames processing instead of a spinner; the form whose labels anticipate the next question; the settle animation that gives a completed payment weight.

**Elevated is the default recommendation register for `every-run` and high-stakes beats**—it raises quality without spending novelty, so it survives repetition and never competes with reassurance.

## Net-New—the version nobody expects

Meaningfully different, not merely more. A new mechanic, surface, or artifact that makes the moment itself a reason to talk about the product.

**The test:** a screenshot of it could not be mistaken for a competitor.

Examples of the register: a live visualization where a table was assumed; a personalized artifact worth keeping (a year-in-review, a printable record, a shareable result card); an interactive demo where static onboarding was assumed; a progress mechanic that accumulates something users check voluntarily.

**Every moment gets a Net-New rung on its ladder—ideation is free. Shipping is rationed:** at most one Net-New treatment per path, placed on the beat that carries the product's distinctive claim, because Net-New spends surprise and surprise does not split. Two rules keep the rung honest:
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
**Basis:** observed from the artifact · confirm with: trigger a real payment and read the actual notification—the claim the verdict rests on

## The path
| # | Beat | Touchpoint | Frequency | Verdict |
|---|---|---|---|---|
| 1 | Enters from bookmark | web app | every-run | Expected |
| 2 | Sees dashboard—outstanding and recent | screen | every-run (first run: once) | Moment 3 (first run) |
| 3 | Understands who owes what | screen | every-run | Expected |
| 4 | Composes invoice—client, items, due date | screen | recurring | Expected |
| 5 | Sends—confirmation appears | screen | recurring | Moment 2 |
| 6 | Payment lands—notification | push/email | recurring | Moment 1 |
| 7 | Sees dashboard updated—paid, month total | screen | recurring | Expected |

## Scorecard
| Gate | Score | Key finding |
|---|---|---|
| Baseline | 3/4 | Fast and clear—the path holds, so treatment will read as intentional rather than cosmetic. |
| Placement | 2/4 | Touches exist on-path (send confetti) but nobody chose them, and the best-crafted work in the product is a 404 minigame. |
| Proportion | 1/4 | Intensity is decided by habit—confetti on the routine send, silence at the payoff. Nothing tracks magnitude. |
| Signature | 1/4 | Swap the logo and nobody notices. The mascot is a stock personality, and the ending feeling is unchosen. |
| **Total** | **7/16** | **functional but forgettable** |

## The moments (ranked by reach × memory)
### Moment 1—Payment lands (beat 6), relief
- Why here: the entire point of invoicing, reached by every paying client, and it is the peak and near-ending of the path—currently rendered as "Invoice #1042 was paid."
- Expected: notification names client, invoice, and amount · Elevated: amount-first copy, a paid-receipt block, the outstanding total visibly settling to its new value · Net-New: a Paid ledger—a year-view that fills with each payment and exports clean at tax time
- Constraints: money moment—records and amounts precede any feeling; no sound.

### Moment 2—Send (beat 5), confidence
- Why here: the effort peak, and the anxiety is "does it look professional to my client"—the confirmation answers a different question than the one being asked.
- Expected: "Sent to client@" with timestamp · Elevated: preview exactly as the client sees it, then a delivered state · Net-New: a client-facing invoice page polished enough to be the freelancer's storefront
- Constraints: nothing may delay the send action itself.

### Moment 3—First-run dashboard (beat 2, first pass), possibility
- Why here: the first impression, every user, exactly once—a `once` beat that can carry expressive treatment the recurring beats cannot.
- Expected: "No invoices yet" plus a button · Elevated: an empty state that starts the work—a sample invoice and "your first takes 2 minutes" · Net-New: composing the first invoice is the onboarding; the form is the tour
- Constraints: one primary action; the sample must be deletable in one tap.

## Issues (most severe first)
- **[P0 · off-path]** Wit at failure—the mascot grins through a failed send with "Whoops! Gremlins!" A freelancer whose invoice did not reach a client is losing money while the product jokes. **Fix:** plain error—what happened, whether the invoice is safe, what to do next. If failed sends are frequent, that is a leak for Flywheel, not copy for Soul.
- **[P1 · beat 6]** The silent payoff—the product's peak moment is an OS-default notification, indistinguishable from a calendar reminder. **Fix:** treat as Moment 1; the Elevated rung alone changes what users remember this product doing.
- **[P1 · off-path]** The misdirected budget—the 404 minigame is the most-crafted surface in the product, reached by accident, in annoyance. **Fix:** relocate the craft to Moment 2 or 3; the game itself is cut, not polished.
- **[P2 · beat 5]** Decayed repetition—confetti on every send was charming once and is wallpaper by week two, and it spends celebration the payoff never gets. **Fix:** replace with a sent-state that survives repetition—preview, delivered check, done.

## Kept Expected, on purpose
Beats 1, 3, 4, and 7 stay standard. Beat 4 is load-bearing convention—a weekly form freelancers fill from muscle memory, where novelty costs speed. Beats 1, 3, and 7 are every-run beats whose only honest lever is pace, and pace is already at ceiling (Baseline 3).

## Next
- **Now**: Moment 1, Elevated rung—amount-first notification, receipt block, the settling total.
- **After it lands**: Moment 3—the first-run empty state, since it is the only `once` beat on the path and currently spends nothing.
- **Hand off**: None. (If failed sends turn out to be frequent, route the error branch to Flywheel as a leak.)
```

---

## Example 2—Build: the payment moment

**Input:** "Design the payment-landed moment the search ranked first."

**Soul's output:**

```
**Moment:** Payment lands—for a freelancer, on every pass.
**Feeling:** relief · **Frequency:** recurring · **Stakes:** medium

## Why this moment
- On the path: beat 6, reached by every client who pays—which is every successful use of the product.
- Worth the budget: it is the payoff the whole path exists for, and peak-end says this beat holds more memory than the six before it combined.
- Today: an OS-default notification—"Invoice #1042 was paid."—and a dashboard that shows the change only after a manual refresh. Observed from the artifact.

## The rungs
- **Expected:** notification carries client, invoice number, and amount; the dashboard row flips to Paid on next load. Shippable as-is.
- **Elevated:** the notification leads with what matters—"$1,850 from Meridian Co · Invoice #1042 paid." Opening it lands on the invoice with a paid-receipt block: date, method, a record that exists somewhere. The outstanding total settles to its new value with one 400ms count-down; reduced motion gets the delta in text—"Outstanding: $4,200 → $2,350."
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

**Why these two:** the search refuses the question as asked. The user said "make it more delightful" and the answer is that delight is already there—in a 404 game and a failure mascot—and the job is relocation, not addition. The verdict names a misplacement, not an absence. Note the P0 is copy, not structure: the cheapest fix in the report is also the most urgent, which is common. The build then shows proportionality at a money moment: relief is built from records, amounts, and one restrained settle—celebration never appears, because the frequency is recurring and the subject is money, and either alone would rule it out.

Note the receipt doing its work: four of seven beats stay Expected with reasons on record, the Net-New rung appears exactly once across all three moments at full depth (the ledger—the one beat carrying the product's distinctive claim), and the first-run empty state is the only place one-shot expressive treatment is even considered, because it is the only `once` beat on the path.
