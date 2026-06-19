# Focal Patterns—techniques and anti-patterns

The working catalog behind the three disciplines. Pull from here when building or when prescribing a fix in a review. Ordered the way the disciplines apply: Information Architecture → Progressive Disclosure → Visual Hierarchy.

---

## Information Architecture (Discipline 1)

How to decide what belongs on a screen and organize it so a single job is possible.

- **The screen inventory.** List every element a screen wants to hold. For each, ask: *does this serve the one job?* If it serves a different intent, it belongs on a different screen. This is the fastest way to find a kitchen-sink screen.
- **Split by intent, not content type.** "Account" is not one screen because the data lives in one table—it's profile, security, billing, and notifications, each a separate intent. Split where the user's goal changes, not where your schema does.
- **Group by relatedness.** Things used together live together. Proximity is the strongest, cheapest grouping signal—closer than a border, closer than a shared background. Reach for dividers and containers only when space alone isn't enough.
- **Label in the user's words.** Sections, nav, and actions named in language the user already owns. "Trips" not "Itinerary records." Test a label by asking whether a first-timer would pick it blind.
- **Co-locate the decision and its inputs.** Everything needed to make a choice is present where the choice is made. If step 3 needs a number from step 1, show it on step 3. Never make the user hold it in their head.
- **Merge round-trips; split overload.** Two screens that each do half a job and bounce the user back and forth should be one. One screen juggling three jobs should be three.
- **Keep navigation shallow and oriented.** ≤5 top-level destinations; group the rest. The user should always know where they are (active state, breadcrumb, title) and how to get back.

**Test:** read only the screen's labels and groupings, ignoring the visuals. Can a stranger tell what the screen is for and what they'd do here? If not, the architecture is unclear before any pixel is styled.

---

## Progressive-disclosure technique catalog (Discipline 2—load-bearing)

Match the technique to *why* the content is deferred.

*The ≤4 working-memory budget below is the task-screen default. On hub and exploration screens it relocates rather than disappears—per row on a hub, per card on a feed. See **Registers** in [SKILL.md](../SKILL.md).*

| Technique | Use when | Example |
|-----------|----------|---------|
| **Smart defaults + Advanced** | Most users want the common choice; a few need control | "Send now" with a collapsed "Schedule / options" |
| **Accordion / expander** | Several independent sections, user needs one at a time | FAQ, settings groups, order details |
| **Stepper / wizard** | A task has natural sequential stages | Checkout, multi-part signup, setup |
| **Drill-down (master → detail)** | A list where each item has depth | Inbox → message, feed → post |
| **Contextual reveal** | A field/control only matters after a prior choice | "Other" → free-text box; "Ship to address" → address form |
| **Overflow / "more" menu** | One or two primary actions, a tail of rare ones | "⋯" menu, kebab on a card |
| **Peek + expand** | Content is scannable truncated, occasionally read in full | "Show more" on long text, truncated comments |
| **Tooltip / inline hint** | Help is needed rarely and contextually | "?" next to an unfamiliar term |

**Choosing well:**
- Defer the *rare*, surface the *common*. The split is by frequency of need, never by your convenience.
- Show the **count** when you hide things ("12 more"), so deferral doesn't read as absence.
- One layer of disclosure is a path; three nested layers is a maze. If users must expand to expand to expand, the screen has the wrong architecture (Discipline 1).
- A stepper must show **where the user is and how far is left**—but frame it as achievable milestones ("Step 1 of 3"), not a demoralizing tally ("3 of 47 done").

**Never defer:** the price, required fields, destructive consequences, error states, or the primary action. Deferral is for reducing choice overload, never for hiding what the user needs to act or to trust the screen.

---

## Focus mechanisms (Discipline 3)

How to give a screen a single visual entry point so the eye knows where to start—the visual expression of the one purpose.

- **Size and weight differential.** Make the primary element materially larger or heavier than its neighbors. A ≥1.25 step between tiers reads as intentional; smaller reads as accidental.
- **Isolation by space.** Surround the primary element with more whitespace than anything else. The eye goes to what's alone.
- **Position.** Above the fold, in the reading-flow landing zone (top-left start, bottom-right resolution for LTR). On mobile, primary actions sit where the thumb rests (the bottom third); on pointer-driven desktop, in the natural resolution zone of the layout (often bottom-right of a form or panel).
- **Singular color.** Exactly one saturated accent on the screen, reserved for the primary action. The moment a second element shares it, focus splits.
- **Suppress the rest.** Often the fastest way to create a focal point is not to amplify the hero but to *quiet everything else*—mute secondary text, recede chrome, drop ambient elements to low contrast.

**Test:** cover the primary element with your thumb. If the screen now feels purposeless, the focus mechanism is working.

---

## The hierarchy ladder in practice (Discipline 3)

Climb only as far as you need. Each rung is louder than the last.

1. **Space.** Proximity groups; distance separates; generous margin elevates. Most hierarchy problems are solved here, for free. Tight gaps within a group (8–12px), generous gaps between groups (48–96px).
2. **Weight.** Font weight and contrast. A bold label against regular body, or full-contrast text against muted, ranks without changing size or hue.
3. **Size.** Type scale and element scale. Keep a real scale (≥1.25 ratio between steps); three deliberate sizes beat six arbitrary ones.
4. **Color.** The loudest, last rung. A single accent for the one thing that matters most. Color as *the* hierarchy tool (rather than reinforcement) is fragile—it fails for colorblind users and in dark/light inversion.

**Rule:** if space and weight already rank the screen, don't add size and color on top. Redundant emphasis flattens hierarchy as surely as no emphasis.

---

## State care

Products live or die on the states most teams treat as afterthoughts. Each is a Focal surface in its own right—it has a purpose, an architecture, and a disclosure budget.

- **Full (worst-case) state.** The biggest clutter trap in data UIs: a screen designed against 3 tidy demo rows becomes chaos at 300—with the longest label, the most items, max-digit numbers, the deepest nesting. Design and review every screen against its *worst realistic data*, not the mock. A layout that only holds together when nearly empty isn't done. (This is why dashboards drift into clutter: they were composed empty.)

- **Empty state.** Not a void—the first-run teacher. One sentence of what this becomes, one primary action to get there. Empty states are the highest-leverage onboarding you have.
- **Loading.** Always communicate system status. Skeletons over spinners for content; optimistic UI for actions the user just took. Never a blank screen with no signal.
- **Error.** Plain language, name the actual problem, offer the fix, preserve the user's work. "Email is missing an @" beats "Invalid input." Place it at the source, not in a banner far away.
- **First run.** Teach through action, not a wall of coach marks. Defer everything not needed for the first success (Discipline 2). The fastest path to one real win beats a tour.
- **Peak-end.** Users remember the most intense moment and the ending. Make sure the peak (the payoff, the "sent!", the result) is celebrated, and the experience ends on a high—not on a dead-end screen. Reassure at anxiety spikes (payment, delete, irreversible commits) with progress, confirmation, and undo.

---

## Anti-pattern library

Each entry: the tell, the discipline it breaks, the fix.

- **The kitchen-sink screen**—one screen tries to do three jobs. *(IA, P1)* Split by intent, or keep one purpose and route the others to secondary paths.
- **The data-model screen**—structure mirrors the database, not the user's goal. *(IA, P1)* Reorganize around intent; group what's used together.
- **The jargon label**—sections and actions named in system terms. *(IA, P2)* Rename in the user's words; test labels blind.
- **The memory bridge**—step 3 needs a fact only shown on step 1. *(IA, PD, P1)* Carry the context forward, or co-locate the decision with its inputs.
- **The wall of options**—8+ equal choices at one decision point. *(PD, P2)* Defaults + reveal; recommend one; group the rest.
- **The everything-up-front form**—onboarding asks for all data immediately. *(PD, P2)* Ask only what's needed for the first success; defer the rest to when it's relevant.
- **The premature settings dump**—advanced options shown before anyone needs them. *(PD, P3)* Collapse behind "Advanced"; smart-default the common case.
- **The buried essential**—price, required field, or consequence hidden behind a tap. *(PD, P0)* Surface it. This is a dark pattern, not disclosure.
- **Dual primary CTAs**—two equally-weighted buttons competing. *(VH, P1)* One primary, the other demoted to secondary or a link.
- **The hero that eats the button**—a giant image/illustration outweighs the primary action. *(VH, P2)* Cut the decoration's weight; the action wins.
- **The rainbow screen**—color used decoratively everywhere, so it can't signal hierarchy. *(VH, P2)* Reserve one accent for the primary action; mute the rest.
- **The flat list pretending to be a hierarchy**—every row identical weight. *(VH, P2)* Differentiate the lead item, or add grouping by space.
- **The modal reflex**—interrupting the screen's purpose with a dialog for something that could be inline. *(VH, P2)* Exhaust inline and progressive alternatives first.
- **The icon-only mystery nav**—unlabeled icons forcing recall. *(IA, P2)* Add labels; recognition beats recall.

---

## Quick reference card

```
PURPOSE    "This screen exists so the user can ___."   (no "and")
ACTION     one primary action, period
IA         everything on screen serves that one job · group related · label plainly
DISCLOSE   every element → Now / On-demand / Never · ≤4 at any decision point
HIERARCHY  1 primary · 2–3 secondary · rest ambient · space → weight → size → color
NEVER      hide price, required fields, consequences, or the primary action
```

*Defaults for a task screen. On a hub the ≤4 binds per row; on an exploration surface, per item.*
