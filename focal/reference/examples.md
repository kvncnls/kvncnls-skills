# Focal Examples

Two worked examples showing the quality bar and the locked output templates in use—one **review**, one **build**. They share a narrative: the review flags a cluttered dashboard that's doing three jobs, and the build designs one of the screens it recommends splitting out. Illustrative, not a real product.

---

## Example 1—Review: a cluttered analytics dashboard

**Input (what was handed in):** the "Home" screen of an analytics product. 8 same-size KPI cards, a 14-item ungrouped sidebar, two equally-weighted buttons ("Create report" and "Upgrade"), 6 always-visible filters, a recent-activity feed, a chart, and a "tips" banner.

**Focal's output:**

```
**Verdict:** No—three jobs on one screen (monitor, build a report, upsell). No visual entry point. · 5/12

**Screen:** Analytics product home/overview · register: hub · audience: mixed

## Scorecard
| Discipline | Score | Key finding |
|---|---|---|
| Information Architecture | 1/4 | Monitoring, report-building, and an upsell share one screen—three intents |
| Progressive Disclosure | 2/4 | 8 equal KPIs and 6 filters shown at once; no defaults, nothing deferred |
| Visual Hierarchy | 2/4 | 8 same-size cards + two primary buttons—nothing wins the eye |
| **Total** | **5/12** | **significant rework** |

## Issues (most severe first)
- **[P0 · IA]** Three competing jobs—monitor metrics, build a report, upgrade the plan—collapsed onto one screen. Users scan instead of acting. **Fix:** make this a monitoring hub; route "Create report" to its own screen and move "Upgrade" into the account menu.
- **[P1 · Hierarchy]** Dual primary buttons ("Create report" + "Upgrade") compete at equal weight. **Fix:** a hub needs at most one primary; here, let the most-watched metric be the focal point and demote both buttons.
- **[P1 · Disclosure]** 8 KPI cards at identical weight blow past the ~4-chunk glance budget. **Fix:** surface the 3–4 metrics this audience checks daily; move the rest behind "More metrics."
- **[P2 · Disclosure]** 6 filters always visible. **Fix:** default to the common view (last 7 days); collapse the rest under "Filters."
- **[P2 · IA]** 14-item sidebar, ungrouped. **Fix:** group into 4–5 labeled sections—recognition over scanning.

## Top 3 moves
1. Cut the screen to one job—monitoring—and route report-building and upgrade elsewhere.
2. Promote 3–4 daily metrics to a clear visual lead; defer the rest.
3. Default the filters and group the sidebar into labeled sections.
```

---

## Example 2—Build: the "Create report" screen

**Input:** "Design the Create report screen we just split out of the dashboard."

**Focal's output:**

```
**Screen:** Create report—exists so the user can generate one report from a chosen dataset and date range. Primary action: Generate report.
**Register:** task   ·   **Audience:** mixed

## Information
- Dataset—single select (the one required choice)
- Date range—preset picker, default "Last 30 days"
- Report name—text field, optional, default "Untitled report"
- Generate report—primary button
- Moved off: scheduling, sharing, export format → these belong to a report that already exists (the result screen), not its creation

## Disclosure
- Now: dataset, date range, Generate
- On-demand: advanced filters + grouping → behind "Advanced options" (collapsed)
- Cut: format / recipients / schedule—not needed to create the report

## Hierarchy
- Primary: Generate report
- Secondary: dataset + date range (the two real inputs)
- Ambient: report-name field, "Advanced options" link

## Gates
- [x] One-sentence purpose, no "and"
- [x] Exactly one primary action (Generate)
- [x] Grouped + labeled; no orphans; no memory bridge (dataset chosen where it's used)
- [x] ≤4 chunks at any decision point (name, dataset, range, generate)
- [x] Squint test passes—Generate + the two inputs dominate
- [x] Empty / loading / error / full (worst-case) states designed (no datasets → "Connect a source"; generating → progress; error → inputs preserved; 500-column dataset → range still scannable)
```

---

**Why these two:** the review never just lists problems—it ends on three ranked moves. The build never returns prose—it returns the same Screen Spec every time. And the second example resolves the first: "split Create report onto its own screen" becomes an actual single-purpose screen. That is the whole method in motion—one screen, one purpose, both directions.
