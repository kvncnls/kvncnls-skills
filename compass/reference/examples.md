# Compass Examples

Two worked examples showing the quality bar and the locked output templates in use—one **review**, one **build**. They share a narrative: the review flags a maze-like checkout that traps the user, loses their data, and strands returning shoppers; the build redesigns that same flow so the user is never lost. Illustrative, not a real product.

---

## Example 1—Review: a maze-like checkout

**Input (what was handed in):** the checkout flow of a storefront. A 6-step wizard (Cart → Account → Shipping → Billing → Review → Confirm) that opens inside a full-screen modal with no Close. Each step replaces the last; the only Back is the browser's, which wipes everything entered. Shipping cost and taxes appear for the first time on step 5. A "Sign in to continue" wall blocks step 2 for everyone. Returning users who tap the emailed "Resume your order" link land on step 1 with an empty cart. There is no step indicator anywhere.

**Compass's output:**

```
**Verdict:** No · the user is trapped in a modal, loses data on Back, and returning links dump them at step one · **3/12**

**Flow:** Storefront checkout · type: linear · audience: mixed

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Orientation | 1/4 | No step indicator, no in-flow Back, no Close—the modal traps the user |
| Path Economy | 1/4 | 6 steps for a 3-step job; a sign-in wall gates checkout; cost hidden until step 5 |
| Continuity | 1/4 | Back wipes entered data; the "Resume" deep link lands at step 1 with an empty cart |
| **Total** | **3/12** | **broken** |

## Issues (most severe first)
- **[P0 · Orientation]** Trapped modal—the flow opens in a full-screen modal with no Close and no in-flow Back; only the browser Back, which exits the whole modal. The user is trapped: no way out that isn't "lose everything." **Fix:** a real Back on every step and a persistent "Save & exit"—nothing should trap the user in a modal.
- **[P0 · Continuity]** Back wipes data—browser Back wipes every field entered so far; the user re-types shipping and billing from scratch. **Fix:** persist step state so Back returns to the previous step with its data intact. Back is not a reset.
- **[P0 · Continuity]** Resume lands empty—the emailed "Resume your order" link deep-links returning users to step 1 with an empty cart; the order they were resuming is gone. **Fix:** the deep link lands them on the step they left, cart and entered data restored. Honor the entry point.
- **[P1 · Path Economy]** Sign-in wall—a "Sign in to continue" wall blocks step 2 for everyone, including first-time buyers who don't have an account. **Fix:** offer guest checkout; collect the email at shipping and invite account creation *after* the purchase, not as a gate before it.
- **[P1 · Path Economy]** Six steps for three—a job that's honestly three (identify, pay, confirm) is spread across six screens. Account and Billing are separable steps that each demand a full round-trip. **Fix:** merge Account into Shipping (one contact-and-address screen) and Billing into Review (pay where you confirm)—three steps, not six.
- **[P1 · Path Economy]** Cost hidden until step 5—shipping cost and taxes appear for the first time on step 5 (Review), after the user has invested five screens. **Fix:** show the running total from the first step it can be estimated. Surfacing cost early is honest economy; hiding it to shorten the felt path is the dark pattern—the honest-path caveat, not friction reduction.
- **[P2 · Orientation]** No step indicator—nothing tells the user where they are or how far is left. The drop test fails on every screen. **Fix:** a "Step 2 of 3" marker or labeled progress on every step.

## Top 3 moves
1. Free the user—add a real Back and a "Save & exit" to every step, and persist state so Back and resume never lose data.
2. Cut six steps to three honest ones, drop the sign-in wall for guest checkout, and surface the total from the start.
3. Fix the "Resume" deep link to land returning users on the step they left, cart restored—and add a "Step X of 3" indicator throughout.
```

---

## Example 2—Build: the redesigned checkout

**Input:** "Redesign the checkout flow we just reviewed—fewer steps, full orientation, nothing lost."

**Compass's output:**

```
**Flow:** Storefront checkout—gets the user from a full cart to a confirmed order.
**Type:** linear   ·   **Audience:** mixed

## Steps
1. Cart—review items and see the running total (subtotal + estimated shipping/tax) before committing [default: skip if entered from a "Buy now" deep link with one item]
2. Details—contact email + shipping address on one screen; guest by default, "create an account" offered, not required [merged the old Account + Shipping steps]
3. Pay & confirm—payment, final total, and the confirm action on one screen [merged the old Billing + Review steps; order placed here]
(six steps cut to three honest ones; sign-in wall removed—account creation moved to after purchase)

## Orientation
- Position/progress: a "Step 1/2/3 of 3" marker labeled Cart · Details · Pay on every screen; the running total is visible from step 1 forward
- Back + exit: a real Back on steps 2 and 3 that returns to the prior step intact; a persistent "Save & exit" on every step that preserves the cart and drops the user back on the storefront—no trapping modal

## Continuity
- Carries forward: cart contents and running total carry from step 1; email and shipping address carry from step 2 into the step-3 total and confirmation
- Survives: Back returns to the previous step with its fields intact; a refresh or a return tomorrow resumes on the last step reached with the cart and entered data restored—never a reset
- Entry points: the emailed "Resume your order" link lands on the exact step the user left, cart and details restored; a "Buy now" deep link enters at step 2 with the single item already in the cart

## Gates
- [x] One destination, no "and"
- [x] Every step earns its place; nothing protective cut
- [x] Where-am-I + back + exit on every step
- [x] No memory bridge; state survives; deep links land in context
- [x] Drop test passes on every screen
```

---

**Why these two:** the review never just lists problems—it ties every issue to a discipline and ends on three ranked moves. The build never returns prose—it returns the same Flow Spec every time. And the second example resolves the first: "cut six steps to three, free the user, restore the resume link" becomes an actual three-step flow where the user always knows where they are, what's left, and how to get back or out. That is the whole method in motion—never lost, in both directions.

Note the honest-path line running through both: the review's fix for hidden cost is to *surface* the total earlier, and the build shows it from step 1. Shortening the felt path by hiding the price or dropping the sign-in protection would be a dark pattern, not Path Economy. The cuts here remove waste (redundant round-trips, a needless gate), never protection.

Once the path is sound by Compass's standard, design each screen with [Focal](../../focal)—see [review.md](review.md) for the full scorecard method and [patterns.md](patterns.md) for the step-reduction and continuity patterns behind these fixes. The spine is in [../SKILL.md](../SKILL.md).