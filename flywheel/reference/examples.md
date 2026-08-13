# Flywheel Examples

Two worked examples in the locked output templates—one **diagnosis**, one **relationship-stage design**. They share a narrative: the diagnosis finds a product losing people before first value, and the stage design addresses the leak it names. These set the bar for length, specificity, and tone; the templates set the shape.

---

## Example 1—Diagnose: a team analytics product with a retention complaint

**Input:** *"People sign up and never come back. We think we need better re-engagement emails."* The product turns support tickets into themed insight reports. Signup is email plus a 6-field workspace setup, then a required CSV upload with no sample data, then an empty dashboard reading "No reports yet." First report takes about 4 minutes to generate, and completes with a toast reading "Done." No analytics beyond signup counts.

**Flywheel's output:**

```
**Verdict:** Friction · people never reach a first report, so there is nothing to come back to · **6/16**

**Product:** support-ticket analytics for support and product teams · first value: undefined · stakes: low
**Coverage:** signup, pre-value setup, CSV upload, empty dashboard, report loading/success, and proposed re-engagement · gaps: measured activation cohorts, real returning-user state, lapse timing, and referral/advocacy not shown
**Basis:** walked from a description · confirm with: share of signups that generate a first report, and 4-week retention split by whether they did
**Blocker:** None.

## Scorecard
| Play | Score | Why this score | What raises it one point |
|---|---:|---|---|
| Trust | 3/4 | The outcome is legible and the promise is specific, so the first push is strong; the artifact does not show proof near the promise, which keeps Trust from exemplary. | Put a real report or credible sample beside the promise and verify message match across the highest-traffic entry. |
| Friction | 1/4 | Six setup fields and a required CSV upload block any evidence the product works; the outcome remains technically reachable, but commitment effort is seriously misplaced before first value. | Generate a real report from sample data in one click and defer the six fields until after first value. |
| Wins | 1/4 | Four minutes of work ends in a generic "Done" toast, so the user cannot see what changed or why the result matters; value technically arrives but is largely invisible. | Replace the toast with the report result, what was analyzed, and one next action that extends the win. |
| Emotion | 1/4 | No return-worthy feeling or authored reinforcement is present, and Friction at 1 means the baseline cannot carry expressive treatment yet; the play is absent and sequenced too early. | First make the path reach value reliably, then author a specific reason to prefer returning. |
| **Total** | **6/16 · 1.5/4** | **Broken; exact sum of justified component scores** | Weakest-play ceiling applied |

## Issues (most severe first)
- **[P1 · Friction]** **At:** Workspace setup → CSV upload · state: required configuration with no sample · lifecycle: new signup activating before first value. The setup wall—6 workspace fields and a CSV upload sit before any output. None can be answered well by someone who has not seen a report, and the upload demands data they may not have exported yet. This is commitment friction placed before value. **Fix:** ship a sample dataset that generates a real report in one click; defer all 6 fields until after the first report exists, and infer the workspace name from the email domain.
- **[P1 · Wins]** **At:** Report generation → result · state: success after a 4-minute loading wait · lifecycle: first value for a new signup. The silent power stroke—the product's whole value arrives after a 4-minute wait and is announced by a toast reading "Done." The user is not told what was found, how many tickets were read, or what changed. The single largest win in the product is invisible. **Fix:** replace the toast with the result—themes found, tickets analyzed, the top theme stated in one line—and a next action that extends it.
- **[P1 · Emotion]** **At:** Proposed re-engagement email · state: lapsed before any report exists · lifecycle: attempted return before first value. Re-engagement aimed at people who never got value—the proposed fix emails users who never reached a first report. Mail asking someone to return to a product that never worked for them is pressure substituting for a reason, and it burns the address for the day the product is actually ready. **Fix:** do not build it. Every hour here belongs at Friction until first-report rate moves.
- **[P2 · Trust]** **At:** Acquisition/landing promise · state: first encounter with no product proof · lifecycle: arrival before signup. No evidence near the claim—the promise is specific but nothing on the page shows a real report. **Fix:** put an actual output on the first screen; it does double duty as proof and as comprehension.
- **[P2 · Friction]** **At:** Reports dashboard · state: empty with "No reports yet" · lifecycle: activation before first report. The empty state is a notice—"No reports yet" states a fact and offers no path. **Fix:** make it the activation surface: what will appear here, why it is useful, and one button that runs the sample.

## Fix this first
Friction. Nothing downstream can be evaluated until people reach a first report—the Wins finding is real but affects only the small group that survives setup today, and the Emotion play cannot add mass to a wheel that has not turned once. Re-engagement email is the last thing to build, not the first.

## Next
- **Now**: cut the path to first report to one click on sample data; defer the 6 fields; turn the empty state into the entry point.
- **After it moves**: replace the "Done" toast with the result and a next action, then place the upgrade ask after the second report.
- **Hand off**: the 6-field setup form is a single-screen structure problem once it is repositioned—Focal.
```

---

## Example 2—Stage design: the first-report stage

**Input:** "Design the first-report experience the diagnosis called for."

**Flywheel's output:**

```
**Stage:** First report—the friction play, for a support lead evaluating the product in their first session.
**First value:** a themed report generated from real tickets, read and understood   ·   **Stakes:** low

## The leak
- Today: 6 workspace fields and a required CSV upload stand between signup and any output, and the empty state offers no path. Nobody sees a report without exporting data first.
- Confirm with: share of signups generating a first report within 24 hours, and 4-week retention split on that event.

## The design
- Signup asks for email only. The workspace name is inferred from the domain and shown as editable text, not a field to fill.
- The first screen after signup is a live report built from a sample support dataset, already generated—not an invitation to generate one. The user reads an actual output before doing any work.
- One primary action: "Run this on your tickets." It opens the upload, now framed as replacing sample data with real data, which is a different and easier decision than uploading into a void.
- The 4-minute generation shows what it is doing—tickets read, themes forming—rather than an indeterminate spinner, because a wait the user can see is a wait they will sit through.
- Completion states the result: themes found, tickets analyzed, the top theme in one sentence, and the report itself. No toast.
- The 6 workspace fields move behind a "Workspace settings" link, prefilled with safe defaults, reachable but never blocking.

## Friction kept
- The upload step itself. It is procedural, not accidental—the product cannot analyze tickets it does not have—and it now sits after the user has seen what the analysis produces, where it reads as worth doing.
- Naming the report before saving it. Productive friction: a named report is one the user returns to and finds again, and the cost is a few seconds against a durable gain.

## The ask
- Ask: None on this stage.
- Lands after: n/a—the first upgrade ask belongs after the *second* report, when the user has evidence the product works repeatedly rather than once.
- Declining costs them: nothing.

## Gates
- [x] First value named as an outcome, not setup
- [x] The leak is stated with evidence, and the confirming metric is named
- [x] Every required step has a purpose the user could be told
- [x] Protective and productive friction preserved
- [x] Any ask lands after the value it extends, and declining is free
- [x] Nothing here hides cost, consequence, permission, or reversibility
```

---

**Why these two:** the diagnosis refuses the question it was asked. The user came for re-engagement email and the honest answer is that there is nothing to re-engage *to*—which is what "fix this first" exists to say. Note that the re-engagement finding is a P1, not a P0: it is a misdirected investment, not a dark pattern, and P0 is reserved for the ethical floor so that it keeps its meaning. The relationship-stage design then resolves it: the sample report inverts the whole stage, because a user who has already seen an output is making a completely different decision when asked to upload.

Note what stayed. Two frictions were preserved and named—the upload and the report name—because this play is not about removing effort, it is about making the remaining effort obviously worth it. And note what was refused: no ask on the stage at all, because nothing has happened twice yet.
