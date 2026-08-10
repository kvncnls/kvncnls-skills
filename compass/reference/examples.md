# Compass Examples

Two worked examples, captured from real runs of this skill and shown in the locked output templates—one **review**, one **build**. They share a narrative: the review finds a 7-step onboarding wall that traps the user twice over, and the build redesigns that same flow so the user is never lost. These set the bar for length, specificity, and tone; the templates set the shape.

---

## Example 1—Review: a 7-step onboarding wall

**Input:** a team-collaboration app's new-user onboarding, 7 steps: (1) Create account, (2) Verify email—shows "check your email" and dead-ends with no resend and no way back, (3) Choose a plan (free tier present but visually buried, prices shown here for the first time), (4) Invite teammates (required, minimum one), (5) Pick integrations from a grid of 24, (6) Name your first project, (7) a 4-slide feature tour. Only then does the user see the product. No progress indicator. Browser Back restarts at step 1 with all fields empty. The onboarding email's "Continue setup" link always opens step 1.

**Compass's output:**

```
**Verdict:** No · the email-verification screen is a dead end with no resend, no Back, and no way forward · **1/12**

**Flow:** Team-collaboration app new-user onboarding · type: linear · audience: novice
**Context:** a first-timer evaluating the product, patience near zero · bar: Linear's and Notion's first-run
**Basis:** walked from a description · confirm with: walk the prototype through Back, refresh, and the onboarding resume/deep links at every step
**Blocker:** Verification dead end; no exit from the gated wall; buried pricing; Back and resume links reset entered state.

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Orientation | 0/4 | Step 2 is a dead end ("check your email", no resend, no back), and none of the 7 steps has a Cancel or skip—the flow traps the user twice over. |
| Path Economy | 1/4 | 7 steps where 2 are honest, all of them before first value, with prices first shown at step 3 and the free tier visually buried. |
| Continuity | 0/4 | Browser Back restarts at step 1 with every field empty, and the "Continue setup" email link always reopens step 1. |
| **Total** | **1/12 · 0.3/4** | **Broken** |

## Issues (most severe first)
- **[P0 · Orientation]** The verification dead end—step 2 shows "check your email" and stops: no resend, no "change email", no Back, no way forward inside the app. A first-timer whose mail is slow, spam-filtered, or mistyped by one character has exactly one move left, which is closing the tab; the screen can be reached and not left, so it fails the drop test outright and breaks the promise at the earliest possible moment. **Fix:** make step 2 a live screen—a 6-digit code field that auto-advances on paste, "Resend code" on a 30-second countdown, "Change email", a real Back to step 1 with the address intact, and "Finish later" that saves the pending account and mails a resume link.
- **[P0 · Orientation]** No exit from a 7-step wall—there is no Cancel, Close, "Skip for now", or "Save & exit" on any step, and step 4 cannot be skipped and demands a minimum of one teammate invite. A user who wants to see the product before handing over a colleague's email address has no legal move; a wizard with no Cancel is a trap with a polite face, and a required invite makes the trap cost someone else's data. **Fix:** put an escape hatch on every step ("Skip" / "Finish later"), and delete the invite gate—invites become an in-product action prompted when sharing actually matters.
- **[P0 · Path Economy]** The buried price—prices appear for the first time at step 3, after the user has already created an account and verified an email, and the free tier is visually de-emphasized against the paid options. Cost disclosed only after sunk investment, with the free option down-weighted, is a trust break dressed as a conversion tactic; this is a dark pattern, not economy. **Fix:** disclose pricing before or at account creation, with the free tier as a visually equal, pre-selected default and no card required.
- **[P0 · Continuity]** The state-eating Back—pressing browser Back at any step restarts at step 1 with all fields empty. Up to six screens of work vanish on one keystroke, and after it happens once the user distrusts the only retreat they had; a Back that resets is the anti-pattern the safety net is supposed to prevent. **Fix:** make each step a real history entry, persist entered values server-side against the pending signup, and restore every field on Back and on forward.
- **[P0 · Continuity]** The deep link to step one—the onboarding email's "Continue setup" link always opens step 1, so the one channel built to recover an interrupted user resets them instead. A "continue" that starts over is worse than no link, because it promised; every interrupted signup becomes a re-signup. **Fix:** sign a resume token into the link and land the user on the step they left with prior input intact, and make the verification link complete verification and land them in the workspace.
- **[P1 · Orientation]** Hidden progress across all 7 steps—no stepper, no named stages, no count; standing on step 4 the user cannot tell whether one screen is left or six. An unbounded flow reads as endless, and endless is where people quit; combined with the missing signage, the drop test fails on every screen. **Fix:** once the path is cut, carry a milestone stepper with named stages on every remaining gated step ("Step 1 of 2 · Create account"), and never a tally.
- **[P1 · Path Economy]** The setup wall—all 7 steps sit before the user ever sees the product: a plan choice, a forced invite, a 24-tile integration grid, a project name, and a 4-slide tour. Only two are load-bearing (create account, verify email)—this is a 7-step flow that needs 2. Every configuration screen before the first win asks a question the user has no context to answer. **Fix:** cut to account + verify, land the user in a pre-seeded workspace, and move plan, invites, integrations, project naming, and the tour into the product as contextual, dismissible prompts—offer 3 relevant integrations with "Browse all", not a grid of 24.

## Top 3 moves
1. Cut the wall to 2 gated steps—create account, verify email—then put the user in a live, pre-seeded workspace; plan, invites, integrations, project name, and tour all become in-product prompts they can dismiss and return to.
2. Make every step recoverable: a persistent 2-stage stepper, a real Back that preserves state, "Finish later" on both steps, and a verification screen with a code field, resend countdown, and change-email—so no screen can be reached and not left.
3. Fix the seams: persist the pending signup so refresh and return-tomorrow resume in place, and re-point the "Continue setup" and verify links at the step the user actually left instead of step 1.

## Next
- **Structural** (do first): close the verification dead end, add an exit to every step, cut 5 of the 7 steps into in-product prompts, persist pending-signup state across Back and refresh, and re-point both email links at the step the user left.
- **Executional** (after): the stepper's visual weight, the resend countdown's copy, the free-tier's equal visual treatment on the plan disclosure, and the transition between the two gated steps.
- **Hand off**: the plan-disclosure screen's internal layout and the free-vs-paid visual ranking are single-screen problems—Focal's, once the path is cut.
```

---

## Example 2—Build: the redesigned first run

**Input:** "Redesign the onboarding flow we just reviewed—fewest honest steps, nothing lost, no dead ends."

**Compass's output:**

```
**Flow:** Team-collaboration app first run—gets the user from a signup click to their first real action inside a live workspace.
**Type:** linear   ·   **Audience:** novice

## Steps
1. Create account—email + password or SSO, with plan tiers stated in plain view ("Free forever · Pro $X/user/month—start free, switch anytime"), free pre-selected, no card. [skip: none—this is the entry]
2. Verify email—a 6-digit code field that auto-advances on paste, plus a magic link in the same mail; "Resend code" on a 30s countdown, "Change email", Back to step 1, "Finish later". [skip: the magic link completes this step from the inbox, so a user who clicks it never types anything]
3. Workspace—the product itself, live: a workspace named from the email domain, one pre-seeded project, and the first real action (post, task, doc) available immediately. [skip: workspace and project names are inferred and renamed inline, which removes the old naming step]

## Cut
- Merged: the plan step (old 3) → folded into step 1 as plain-view disclosure, so price is stated before any investment rather than after two screens.
- Merged: the project-name step (old 6) → inference from the email domain plus inline rename inside step 3.
- Removed: the required teammate invite (old 4)—a gate that cost a third party's data to pass; it becomes an in-product prompt at the moment sharing matters.
- Removed: the 24-tile integration grid (old 5)—replaced by a contextual "3 suggested · Browse all" prompt inside the workspace, asked when the user has context to answer.
- Removed: the 4-slide feature tour (old 7)—replaced by a dismissible 3-item checklist that survives dismissal and stays reachable.
- Kept as protection: email verification—it protects the account and the address is needed for recovery, so it is not waste. Price disclosure moved *earlier*, never hidden to shorten the felt path.

## Orientation
- Position/progress: both gated steps carry a two-stage milestone stepper with named stages—"Step 1 of 2 · Create account", "Step 2 of 2 · Verify email"—so the end is visible from the first screen. On arrival, the product's own nav is the position signal: workspace name as the active anchor, plus a "Get started" card reading "1 of 3 done" that honors progress rather than gating it.
- Back + exit: step 1 has "Back to site"; step 2 has a real Back to step 1 with the email still filled, plus "Finish later" which saves the pending account and mails a resume link. Step 2 can never dead-end—resend, change email, paste code, Back, and exit are all live on it. Inside the workspace every deferred prompt is dismissible and permanently reachable: Invite in the header, Integrations in the sidebar, and the checklist collapses rather than disappearing.

## Continuity
- Carries forward: the address typed on step 1 is shown verbatim on step 2 ("We sent a code to kevin@acme.com") with a change link, so no code or address is carried in the user's head; the email domain becomes the suggested workspace name on step 3; the plan chosen on step 1 carries to billing and is never re-asked.
- Survives: Back restores every field on both steps; a refresh, a closed tab, or a return tomorrow resumes on the last step reached with prior input intact, because the pending signup is persisted server-side rather than held in the page; the workspace checklist state persists per user, so a dismissed prompt stays dismissed and a half-done item stays half-done.
- Entry points: the "Continue setup" email link carries a signed resume token and opens the exact step the user left, never step 1; the verification magic link completes verification and lands the user in the workspace; a teammate's invite link lands the invitee on that workspace's join screen and, after account creation, inside that workspace rather than a fresh empty one.

## Gates
- [x] One destination, no "and"
- [x] Every step earns its place; nothing protective cut
- [x] Where-am-I + back + exit on every step
- [x] No memory bridge; state survives; deep links land in context
- [x] Drop test passes on every screen
```

---

**Why these two:** the review never just lists problems—it ties every issue to a discipline, ends on three ranked moves, and sorts the work structural-before-executional. The build never returns prose—it returns the same Flow Spec every time. And the second resolves the first: "cut the wall to 2 gated steps and make every one recoverable" becomes an actual three-screen flow where the user always knows where they are, what's left, and how to get back or out.

Note the honest-path line running through both: the review's fix for the buried price is to disclose it *earlier*, and the build states it on step 1. Shortening the felt path by hiding cost, or dropping verification to save a screen, would be a dark pattern rather than Path Economy—which is why `## Cut` names what was kept as protection alongside what was removed as waste.
