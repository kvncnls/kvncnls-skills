# Soul Search—the happy-path sweep

Map the default path, judge where the product's expressiveness lives, and return the 2–3 moments worth treating. Use when the user asks to search, sweep, audit, review, or find—or hands over a product with "it feels generic," "it's boring," "make it memorable."

## Input modes

- **A product or flow** (screens, a URL, code, a walkthrough)—map the path directly from the artifact. Label findings *observed*.
- **A description** ("a budgeting app where you link accounts and get a weekly summary")—walk the skeleton as an interview, fill the seven blanks, and label findings *walked from a description*. Say plainly which beats are assumed.
- **A symptom** ("nothing about it feels ours")—still map the path first. The symptom picks the emphasis; the map decides the verdict.

## Step 0—Map, then check the floor

Before scoring, establish:

- **The path.** Build the beat table from the skeleton in [SKILL.md](../SKILL.md)—10–12 beats, touchpoint-tagged, frequency-tagged. Don't re-derive the skeleton here.
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
