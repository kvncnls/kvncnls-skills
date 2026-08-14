# Focal Examples

Two worked examples, captured from real runs of this skill and shown in the locked output templates—one **review**, one **build**. They share a narrative: the review finds a CRM contact screen carrying four jobs, and the build designs one of the task screens it recommends splitting out. These set the bar for length, specificity, and tone; the templates set the shape.

---

## Example 1—Review: a CRM contact detail screen

**Input:** the "Contact detail" screen of a CRM. On it: the contact's name/photo/title; 6 editable fields (email, phone, company, owner, lifecycle stage, lead source); a full activity timeline of 40+ entries; an inline "Log a call" composer; an inline "Send email" composer; a Deals panel with 3 deals; Notes and Files panels; a right rail of 8 "similar contacts"; and 3 top-right buttons all styled identically as filled primary buttons ("Save", "Convert to Deal", "Delete"). Every panel header is the same size and weight.

**Focal's output:**

```
**Verdict:** No · four jobs stacked on one surface, with Delete dressed as a primary button · **3/12**

**Screen:** CRM contact detail—a record home carrying ten co-equal regions and three identical filled primary buttons · register: task-overloaded · audience: mixed
**Flow:** screen-local (Contact detail review)
**State:** full/default plus empty related panels
**Lifecycle:** first visit, recurring review, and first visit after contact creation
**Context:** a rep mid-call or between calls, scanning fast · bar: Linear's issue detail, Stripe's customer record
**Coverage:** full/default state for a returning rep, plus empty Deals/Notes/Files on a newly created contact · gaps: loading, save-in-progress, save error, permission-limited, and destructive-confirmation states not shown
**Basis:** walked from a description · confirm with: open the screen, invoke Delete, and verify the destructive confirmation, autosave, and focus order
**Blocker:** None observed. Delete's actual consequence, reversibility, and confirmation state were not shown; verify them before assigning release-critical severity.

## Scorecard
| Discipline | Score | Why this score | What raises it one point |
|---|---:|---|---|
| Information Architecture | 1/4 | Four independently completable jobs share one surface, plus unrelated panels and a prospecting rail; the rep must sort competing outcomes by eye, which is a major failure of screen intent. | Make Contact detail a routing hub, move the composers to focused task screens, and demote unrelated regions. |
| Progressive Disclosure | 1/4 | Ten top-level regions land open, both composers are resident before selection, and 40+ timeline entries are unfiltered; nothing waits, so first-run and recurring scanning are both overloaded. | Defer composers and secondary regions, cap the timeline, and remove the similar-contacts rail. |
| Visual Hierarchy | 1/4 | Panel headers are visually flat and Delete carries the same filled-primary weight as Save; the screen offers no clear starting point and visually treats a potentially destructive action as routine. | Establish one primary action, visually separate Delete, verify its consequence, and rank the remaining regions with space and weight. |
| **Total** | **3/12 · 1.0/4** | **Broken; exact sum of justified component scores** | Weakest-discipline ceiling applied |

## Issues (most severe first)
- **[P1 · Hierarchy]** **At:** screen: Contact detail action bar · flow: screen-local · state: full/default · lifecycle: returning rep reviewing an existing contact. Save, Convert to Deal, and Delete are styled as identical filled primaries, so the bar has no clear starting point and visually treats a potentially destructive action as routine. The description does not show whether Delete is reversible or confirmed, so P0 would be invented rather than observed. **Fix:** retire Save if autosave is real; keep "Convert to Deal" as the single filled primary; make routine actions secondary; move Delete to a separated overflow action and choose undo, a confirmation, or typed confirmation only after verifying consequence and reversibility.
- **[P1 · IA]** **At:** screen: Contact detail body · flow: screen-local · state: full/default · lifecycle: returning rep scanning during or between calls. Four jobs, one screen—the one-sentence test returns "This screen exists so the user can view a contact *and* edit six fields *and* log a call *and* send an email *and* manage deals, notes, and files." Each outcome can succeed independently, so the sentence exposes competing intents rather than one coherent task. Two of those are full composers sitting open on a record surface, and the six fields render as live inputs with a global Save, which means the screen is permanently in edit mode. A rep who opened it to read a phone number is forced to re-sort several intents by eye. **Fix:** make Contact detail a hub whose organizing intent is *route to the right next action*. Fields become read-only text with per-field inline edit and autosave (no global Save); "Log a call" and "Send email" become their own focused task screens launched from the header.
- **[P1 · IA]** **At:** screen: Activity/Deals/Notes/Files regions · flow: screen-local · state: full/default · lifecycle: recurring account review. The panels mirror the data model—Deals, Notes, Files, and Activity are four peer panels, one per related table, ranked equally because the schema ranks them equally. A rep's actual intent is overwhelmingly "what happened last, and what's the open deal"; Notes and Files are archive lookups. Organizing by table forces the user to re-sort the screen by eye on every visit. **Fix:** reorder by intent—Activity dominant, Deals second in the same column, Notes and Files collapsed into one "Attachments & notes" section.
- **[P1 · Disclosure]** **At:** screen: Contact detail landing viewport · flow: screen-local · state: full/default · lifecycle: every return to an existing contact. Nothing is deferred—ten top-level regions compete at landing, and scored by task rules that is straightforward overload: three *task* surfaces sit resident on the same screen and no element anywhere sits behind a reveal. Every element is "Now" because nobody ran the triage. **Fix:** Now—identity, read-only fields, recent activity, Deals. On-demand—composers behind their header buttons, Notes, Files. Cut—the similar-contacts rail.
- **[P1 · Disclosure]** **At:** screen: Activity timeline · flow: screen-local · state: worst-case full · lifecycle: recurring review of a long-lived contact. The timeline has no ceiling—40+ entries render in full, undifferentiated, with no type filter and no collapse. At the worst realistic case (a two-year customer, 400 entries) this panel is the entire screen and Deals is off-screen. **Fix:** show the 5 most recent grouped by day, with a type filter and "Show 37 more"—the count, so the deferral reads as depth rather than absence.
- **[P1 · Hierarchy]** **At:** screen: Contact detail body · flow: screen-local · state: full/default · lifecycle: first visit by a rep unfamiliar with the record. No visual entry point—every panel header is the same size and weight. Squint at this and you get a list, not a hierarchy: nine equal grey blocks. A first-timer cannot identify the read-first region on an initial scan because nothing is visually primary. **Fix:** climb the ladder with space and weight before color—48–96px between sections against 8–12px within them, one heavier header on Activity, all other headers dropped to a muted label size.
- **[P2 · IA]** **At:** screen: Similar contacts rail · flow: screen-local · state: full/default · lifecycle: returning rep reviewing one known contact. The similar-contacts rail is orphan content—eight contacts occupying a full rail, serving prospecting, an intent nobody arrived on this screen holding. It is here because the data was available, not because a job needed it. **Fix:** cut it; surface similar contacts in search and list views, where the user is actually comparing people.
- **[P2 · Disclosure]** **At:** screen: Deals/Notes/Files regions · flow: screen-local · state: empty · lifecycle: first visit after contact creation. Empty panels hold full weight—Deals, Notes, and Files each render a full-weight header whether they hold three items or zero, so a brand-new contact shows three headers announcing nothing. **Fix:** collapse empty sections to one quiet line with the add action ("No notes yet · Add note").

## Top moves (up to 3)
1. **At:** screen: Contact detail body and action bar · flow: screen-local · state: full/default · lifecycle: returning review · Split the screen: Contact detail becomes a record hub; "Log a call" and "Send email" become focused task screens with clear completion intents; the six fields become read-only text with per-field inline edit and autosave, retiring the global Save.
2. **At:** screen: Contact detail action bar · flow: screen-local · state: full/default · lifecycle: returning review · Rebuild the action bar to one primary: "Convert to Deal" filled, "Log a call" / "Send email" secondary, and Delete separated in overflow with protection proportionate to its verified consequence and reversibility.
3. **At:** screen: Contact detail body · flow: screen-local · state: full/default · lifecycle: recurring review · Rank what remains with space and weight: Activity dominant and capped at 5 with a filter and a "Show N more" count, Deals second, Notes and Files collapsed, similar-contacts rail cut.

## Next
- **Structural** (do first): **At:** screen: Contact detail body · flow: screen-local · state: full/default · lifecycle: returning review · split the two composers onto their own task screens, convert the field block to read-only + inline autosave, re-triage the ten regions, cut the similar-contacts rail, cap and filter the timeline.
- **Executional** (after): **At:** screen: Contact detail body · flow: screen-local · state: full/default · lifecycle: recurring review · the section spacing scale, the muted header treatment, the single accent reserved for the one primary, and the destructive-action confirmation styling.
- **Hand off**: **At:** screen: Contact detail · flow: screen-local · state: full/default · lifecycle: returning review · None—every issue here is within this screen.
```

---

## Example 2—Build: the "Log a call" screen

**Input:** "Build the Log a call screen we just split out of the contact record."

**Focal's output:**

```
**Screen:** Log a call—organized around recording what happened on a call the user just made. **Action model:** one primary: Log call.
**Register:** task   ·   **Audience:** mixed

## Information
- Call context strip (contact name, photo, number dialed, timestamp, prefilled)—co-locates the decision with its inputs so the rep never has to remember who they called or when; read-only, no fields to re-enter.
- Outcome selector: Connected / Voicemail / No answer / Wrong number—the one fact every logged call must carry. Four options, inside the working-memory budget, so it needs no grouping.
- Duration—prefilled from the dialer, editable. Sits beside Outcome because the two are read together as one "what happened" chunk.
- Notes—the reason the rep is on this screen thirty seconds after hanging up. Given the most vertical space of anything on the screen.
- "Schedule follow-up" toggle—the most common next step after a connected call, and the thing the rep will otherwise forget by end of day, so it lives here rather than on a separate task screen.
- "Add to deal (3)"—one quiet control, with the count, because a call that moves a deal must be attributable to it.
- Last call line ("Last call: Jul 2, voicemail")—one ambient line, so the rep knows whether this is a first attempt or a fifth without leaving for the timeline.
- Moved off: the six editable contact fields → Contact detail hub, edited in place per field with autosave.
- Moved off: the full 40+ activity timeline → Contact detail hub, capped and filtered; only the single last-call line survives here.
- Moved off: Send email composer → its own compose screen, launched from the Contact detail header.
- Moved off: Deals, Notes, and Files panels → Contact detail hub; this screen reaches Deals only through "Add to deal (3)".
- Moved off: the 8 similar contacts → search and list views, where comparing people is the actual job.

## Disclosure
- Now: call context strip, Outcome (4 options), Duration, Notes, last-call line, "Log call". Busiest decision point holds 4 chunks—context, outcome, duration, notes.
- On-demand: follow-up date and task title → behind the "Schedule follow-up" toggle (contextual reveal—the fields only matter after the rep says yes).
- On-demand: deal association picker → behind "Add to deal (3)", with the count shown so the deferral reads as depth, not absence.
- On-demand: call recording and transcript → behind a "Recording" link in the context strip, present for the rare dispute, absent from the fast path.
- Cut: lifecycle stage and lead source editors—a call log is not where a rep re-classifies a contact, and offering it invites a wrong edit under time pressure.
- Cut: the similar-contacts rail. Nobody logging a call needs eight other people.
- Cut: a cancel-confirmation dialog. Nothing here is destructive; discard is a link.

## Hierarchy
- Primary: "Log call"—the only filled button on the screen, bottom-right in the form's resolution zone, isolated by more whitespace than anything else.
- Secondary: the Outcome selector (four large segmented targets, autofocused on load so the eye starts there), the Notes field (largest area, quiet-bordered), Duration.
- Ambient: the call context strip and last-call line (muted, read-only), "Schedule follow-up", "Add to deal (3)", "Recording", and "Discard" as a plain text link. Space and weight carry the whole ranking; the single accent color is spent only on "Log call".

## States
- Empty: a first-ever call shows "First call with Ana" in place of the last-call line.
- Loading: context strip skeletons while the dialer record resolves; the form is interactive immediately.
- Error: a save failure keeps every keystroke and names the cause inline at the source—"Couldn't reach the server—your notes are saved locally, retry."
- Full (worst case): 900-character notes scroll inside the field without pushing "Log call" off-screen; a 40-character company name truncates in the strip rather than wrapping to three lines.

## Gates
- [x] One-sentence organizing intent; no unrelated second outcome
- [x] Action model matches the register; any co-equal actions are inherent to the same intent
- [x] Grouped + labeled; no orphans; no memory bridge
- [x] Decision load fits the audience and stakes; nothing essential deferred
- [x] One element or region is materially heaviest and expresses the action model; any primary action reads as actionable
- [x] Every applicable state above designed; each `N/A` is justified
```

---

**Why these two:** the review never just lists problems—it ties every issue to a discipline, ends on a short ranked set of real moves, and sorts the work structural-before-executional. The build never returns prose—it returns the same Screen Spec every time. And the second resolves the first: "split the composers onto their own task screens" becomes a screen with one coherent completion intent and an action model that fits. That is the method in motion, in both directions.

Note the disclosure discipline doing the real work in the build: seven things were cut or deferred, and the busiest decision point holds four chunks. Note also what was *not* deferred—nothing the rep needs in order to log the call sits behind a reveal. Deferral is not burial.
