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
