# Soul Search—the readiness check and three-gate happy-path sweep

Map the working happy path, decide where expressive treatment belongs, and return a restrained set of opportunities. Use when the user asks to search, sweep, audit, review, or find the soul in a product that feels generic, forgettable, over-decorated, or inconsistently authored.

## Input modes

- **A product or flow description**—reconstruct the default path and label every assumed beat. Walked evidence is valid when it is named as such; borrowed confidence is not.
- **Screens, Figma/Paper frames, or a prototype**—read the visible beats and their order. Include first-use, repeat-use, success, failure, interruption, and re-entry states when available. A frame does not prove timing, persistence, or repetition.
- **A live product or codebase**—walk the default path, trigger the real success state, repeat frequent beats, inspect reduced-motion behavior, and test failure for restraint. The codebase can expose lifecycle and frequency behavior that static frames cannot.

## Step 0—Map the path and check readiness

Build the happy path with the seven-part skeleton in [SKILL.md](../SKILL.md), then expand only where a beat changes understanding, action, system response, or feeling. Tag each beat with its touchpoint and frequency. State the intended ending feeling; `unnamed` is a finding, not permission to invent brand personality.

Then run Readiness before choosing treatment:

- **Ready**—the primary user can reach the outcome with enough clarity, stability, trust, and control that expressive work will not cover a defect.
- **Deferred**—a screen, path, or relationship failure materially prevents the outcome or makes treatment cosmetic. Name the owner: Focal for the screen, Compass for the path, Flywheel for the relationship stage.

Readiness is deliberately **unscored**. The other Skills already score structural and lifecycle quality; scoring it again would double-penalize the same failure. A Deferred result still records observed treatment problems and future candidates, but **Next** starts with the handoff. If the broken path makes Placement, Proportion, or Signature impossible to evaluate, mark that gate `N/E—not evaluable until readiness holds` and do not calculate a `/12` total.

Error branches are not Net-New candidates, but they are evidence for restraint. Check whether failure copy, motion, and personality preserve clarity and dignity; do not turn the error itself into a delight opportunity.

## Locate every finding

Before scoring or suggesting a change, build a four-part implementation locator. Every issue, Moment, small thing, Next item, and handoff carries it:

1. **Screen**—the exact beat, touchpoint, message, or control.
2. **Flow**—the named happy path or transition.
3. **State**—the rendered or system condition: first-use, empty, loading, success, failure, re-entry, and so on.
4. **Lifecycle**—the occurrence: first run, every run, recurring milestone, first value, return, lapse, or recovery.

Use the narrowest defensible locator. `Payment notification · invoice-to-payment · successful settlement · recurring value realization` is actionable; `the ending` is not. If any field is not evidenced, write `not shown` and name the fastest validating check in Coverage or Basis.

## The three scored gates

### Gate 1—Placement *(where does expressiveness belong?)*

- List every deliberate expressive touch and every meaningful beat kept Expected.
- Check whether treatment follows reach × memory rather than low implementation risk.
- Check the selection bar, frequency and stakes constraints, and load-bearing conventions before promoting any beat. Treat Elevated as the default ceiling for every-run or high-stakes beats, with Net-New allowed only when durable utility, reassurance, records, or control justify the exception.
- Treat zero Net-New moments as valid when the restraint receipt explains why no beat earns a rebuild.

| Score | Criteria |
|---|---|
| 0 | Backwards or harmful—expressiveness concentrates in dumping grounds, obstructs the path, or exploits failure while consequential beats are neglected |
| 1 | Unauthored—no deliberate treatment decisions and no evidence that Expected restraint was chosen |
| 2 | Partial—some on-path craft exists, but placement is scattered, inherited, or unsupported by a clear restraint receipt |
| 3 | Deliberate—every meaningful beat has a defensible tier; Elevated craft is distributed where useful; zero to three Net-New moments are chosen only when justified |
| 4 | Exemplary—treatment and restraint are ranked against the strongest available candidates, alternatives were explicitly refused, and each choice is unusually effective for its context |

### Gate 2—Proportion *(does intensity fit frequency, magnitude, and stakes?)*

- Does an every-run beat use repetition-proof craft rather than novelty that decays?
- Does intensity match the size of the moment?
- On high-stakes actions, do reassurance, records, and control precede feeling?
- Does the ending receive enough weight without turning routine completion into ceremony?

| Score | Criteria |
|---|---|
| 0 | Inverted or harmful—celebration precedes safety on a high-stakes action, or heavy novelty repeatedly obstructs a core task |
| 1 | Uniform—one intensity is applied everywhere, so routine and milestone beats carry the same emotional weight |
| 2 | Mostly fit with a material mismatch—one decayed repeat, misplaced ceremony, or underplayed consequential ending |
| 3 | Fit—frequent beats are repetition-proof, rare beats may carry greater expression, and intensity follows magnitude and stakes |
| 4 | Exemplary—variation, pacing, and restraint remain unusually effective across first use, repetition, reduced-motion behavior, and the ending |

### Gate 3—Signature *(is any authorship worth remembering?)*

- Name the product-specific moment, interaction quality, or quiet pattern a user could describe.
- Cover the logo: does the experience retain a coherent point of view without depending on novelty or decoration?
- Check whether authorship survives both success and failure through clarity, restraint, and consistent character.
- Do not require Net-New. A distinctive, repetition-proof Elevated pattern or exceptional quiet baseline can carry signature.

| Score | Criteria |
|---|---|
| 0 | Anti-signature—the memorable thing is an interruption, dark pattern, mockery at failure, or exhausting repeated treatment |
| 1 | Anonymous—no product-specific authorship is visible in the evaluated path |
| 2 | Coherent surface, weak memory—the experience has care or style but nothing yet forms a describable product-specific pattern |
| 3 | Authored—at least one product-specific moment or quiet pattern is useful, coherent, and describable without taxing the task |
| 4 | Exemplary—a coherent authored point of view survives success, failure, repetition, accessibility constraints, and multiple path beats without becoming noise |

## Scoring rules

Every evaluated gate uses the same integer anchors:

| Score | Canonical label | Shared meaning |
|---:|---|---|
| **0** | **Broken or harmful** | The gate fails outright, inverts its intended behavior, or creates material harm. |
| **1** | **Major failure** | The gate is seriously compromised, unreliable, or largely absent. Substantial correction is required. |
| **2** | **Partial or inconsistent** | The basic quality exists, but a material weakness prevents dependable execution. |
| **3** | **Strong** | Deliberate, dependable, context-appropriate professional work with only minor gaps. This is the normal target. |
| **4** | **Exemplary—above and beyond** | Fully realized and unusually effective for the context, realistic states, and constraints. This is intentionally uncommon, not the normal target. |

Score each gate holistically against its local rubric. Do not use hidden sub-scores, checklist subtraction, averaging, half-points, or a Net-New count as a proxy for quality. A `4` explains what is unusually effective; a restrained `3` can be better product judgment than an over-authored `4` attempt.

A score without an explanation is invalid. Every row uses **evidence → consequence → rubric anchor → next-point change**. A `2` names what works and the material weakness; a `3` names the remaining minor gap; a `4` says why the gate is above and beyond and uses `None—already exemplary` for the next point. `N/E` is permitted only when Deferred readiness makes the gate genuinely unevaluable; it is not a low score.

When all three gates are evaluated, keep the native total: `total = Placement + Proportion + Signature`. Calculate `average = total / 3`, round to one decimal, and apply:

| Band | Average rule | Native total |
|---|---:|---:|
| **Broken** | `average <= 1.5` | `0–4 / 12` |
| **Significant rework** | `1.5 < average < 2.5` | `5–7 / 12` |
| **Solid** | `2.5 <= average < 3.5` | `8–10 / 12` |
| **Excellent** | `average >= 3.5` | `11–12 / 12` |

Cap the displayed band by the weakest evaluated gate: `0` caps at Broken, `1` at Significant rework, `2` at Solid, and `3–4` adds no ceiling. If any gate is `N/E`, report no total, average, or common band.

Readiness, gate score, final band, issue severity, blocker, and authored-state verdict remain separate. A Deferred readiness result is not itself P0. Assign severity from consequence, reach, and recoverability; a methodology preference is never automatically release-critical.

## Issue severity

| Priority | Meaning |
|---|---|
| **P0 — Critical** | Blocks the core outcome; destroys work or state; causes or risks material harm; hides material cost, consequence, permission, or risk; removes informed choice; or uses coercive manipulation. Fix before release. |
| **P1 — Major** | Materially damages comprehension, trust, value realization, return, or the experience's authorship for a meaningful share of users. Fix before release. |
| **P2 — Moderate** | Creates real friction, dilution, misplaced treatment, or missed value with a viable recovery, workaround, or limited scope. Fix in the next planned pass. |
| **P3 — Minor** | Low-impact craft, consistency, or polish. Fix when time permits. |

## Output format—use this exact structure

Every search returns this template in this order. Repeat Moment and small-thing lines only as warranted; fixed sections remain present even when their content is `None.`

```markdown
**Verdict:** <authored | anonymous | misplaced | exhausting | deferred> · <the biggest missed or misplaced decision> · **<total/12 | N/E>**

**Product:** <what it is, for whom> · **Path:** <N> beats, <entry> → <outcome> · **Ends feeling:** <named state or `unnamed`>
**Readiness:** <Ready | Deferred> · <why, plus owner when Deferred>
**Screen:** <exact touchpoint(s) or `not shown`>
**Flow:** <named happy path or transition(s) or `not shown`>
**State:** <exact rendered or system state(s) reviewed>
**Lifecycle:** <exact occurrence(s) reviewed>
**Coverage:** <app states and lifecycle occurrences actually reviewed> · gaps: <material states or occurrences not shown, or `none`>
**Basis:** <observed from a screenshot or artifact | inferred from code | tested in a prototype or live product | walked from a description | measured from product data> · confirm with: <fastest validating check>
**Blocker:** <None. | concise blocker reason>

## The path
| # | Beat | Touchpoint | Frequency | Verdict |
|---|---|---|---|---|
| 1 | <enters from…> | <surface> | <once | recurring | every-run> | <Expected | Elevated | Net-New (Moment 1)> |

## Scorecard
| Gate | Score | Why this score | What raises it one point |
|---|---:|---|---|
| Placement | <_/4 or N/E> | <evidence → consequence → rubric anchor> | <change, `None—already exemplary`, or N/E reason> |
| Proportion | <_/4 or N/E> | <evidence → consequence → rubric anchor> | <change, `None—already exemplary`, or N/E reason> |
| Signature | <_/4 or N/E> | <evidence → consequence → rubric anchor> | <change, `None—already exemplary`, or N/E reason> |
| **Total** | **<_/12 · _._/4 | N/E>** | **<band and exact sum | no total until readiness exposes all gates>** | <weakest-gate ceiling or N/E> |

## The moments (Net-New, up to 3, ranked by reach × memory)
### Moment 1—<beat>, <named feeling>
- **At:** screen: <exact beat/touchpoint> · flow: <named happy path or transition> · state: <exact app state> · lifecycle: <exact occurrence>
- Why here: <reach × memory and why this beat clears its ceiling>
- Expected: <one line> · Elevated: <one line> · Net-New: <one line>
- Constraints: <one line>

## The small things (Elevated)
- **At:** screen: <exact beat/touchpoint> · flow: <named happy path or transition> · state: <exact app state> · lifecycle: <exact occurrence> · Beat <n>—<craft touch>

## Issues (most severe first)
- **[P0–P3 · beat <n> | off-path restraint]** **At:** screen: <exact beat/touchpoint> · flow: <named path or transition> · state: <exact app state> · lifecycle: <exact occurrence>. <Name>—<observation and consequence>. **Fix:** <fix>.

## Kept Expected, on purpose
<beats kept standard and the strongest reason—convention, frequency, stakes, already-sufficient craft>

## Next
- **Now**: **At:** screen: <exact beat/touchpoint> · flow: <named path or transition> · state: <exact app state> · lifecycle: <exact occurrence> · <first treatment—or required readiness handoff>
- **After it lands**: **At:** screen: <exact beat/touchpoint or `not shown`> · flow: <named path or transition or `not shown`> · state: <exact app state or `not shown`> · lifecycle: <exact occurrence or `not shown`> · <next justified treatment, or `None`>
- **Hand off**: **At:** screen: <exact beat/touchpoint or `not shown`> · flow: <named path or transition or `not shown`> · state: <exact app state or `not shown`> · lifecycle: <exact occurrence or `not shown`> · <screen structure → Focal; path/navigation → Compass; relationship leak → Flywheel; `None` if ready>
```

Filling it:

- **The path**—one row per consequential default-path beat, including Expected beats. A beat whose first pass differs from steady state carries both frequency tags.
- **The moments**—emit zero to three. If none clears the bar, keep the header and write `None—no beat currently earns Net-New; see Kept Expected.` Never create filler to satisfy a count.
- **The small things**—emit only craft the beat's ceiling allows. Write `None.` when no Elevated treatment is warranted.
- **Readiness and N/E**—Deferred does not automatically erase Soul findings. Use `N/E` only when the structural failure genuinely prevents a gate from being evaluated; otherwise score observed treatment and sequence it after the handoff.
- **Coverage and Basis**—name only states and occurrences actually observed or walked. Use `not shown` and the fastest validating check instead of awarding credit or inventing failure.
- **Issues and suggestions**—every issue, Moment, small thing, Next item, and handoff receives a complete **Screen · Flow · State · Lifecycle** locator. If nothing ranks above P3, write `None above P3.` under Issues.
