---
name: product-judgement
description: "Use when auditing an existing product, app, or feature across all four Product Judgement scales: screen structure (Focal), multi-screen journeys (Compass), relationship value and retention (Flywheel), and memorable moments (Soul). Run for a holistic app audit, cross-scale critique, or prioritized UX review using a codebase, live product, prototype, Figma/Paper frames, screenshots, or a description. Prefer a codebase because it exposes behavior, state, and lifecycle context. Do not use for a single-screen, single-flow, or single-stage review; invoke the corresponding Skill instead, or for implementation, design-system analysis, visual styling, animation implementation, research, or analytics."
---

# Product Judgement

**Audit the product as a connected system.**

Product Judgement is the orchestration Skill for the four foundational Skills:

- **Focal**—what belongs on a screen, what waits, and what wins attention.
- **Compass**—how a person moves between screens without getting lost.
- **Flywheel**—where momentum drops across the relationship and what earns the next stage.
- **Soul**—which working moments deserve craft and memory.

It is not a fifth design lens and it does not replace the four local methodologies. It runs them against a shared evidence map, keeps their boundaries intact, reconciles their findings, and returns one prioritized audit. Do not invent a fifth score or average the native totals together.

## Use it when

Use Product Judgement when the question is larger than one screen, one flow, one relationship stage, or one expressive moment:

- audit the whole app or a meaningful product area;
- find why a working product feels incoherent, hard to navigate, low-value, or forgettable;
- decide which UX problem to fix first when several Skills identify related issues;
- reconcile screen, journey, relationship, and memory findings into one implementation sequence.

For a narrower question, invoke the local Skill directly. A single dashboard belongs to Focal; an onboarding path belongs to Compass; a first-value or retention problem belongs to Flywheel; a happy-path authorship problem belongs to Soul.

## Evidence and context

Accept a codebase, live product, clickable prototype, Figma or Paper frames, screenshots, or a product description. Also accept the surrounding product context: the PRD (Product Requirements Document), product brief, strategy or goal documents, user research, personas, journey maps, analytics or funnel data, support themes, experiment history, and technical, accessibility, legal, or safety constraints. The artifact tells you what exists; these materials explain why it exists, for whom, and what success means. The more relevant context available, the more specific and defensible the audit. Prefer the codebase when it is available because it can expose routes, components, state transitions, validation, persistence, re-entry behavior, copy, and implementation constraints that frames cannot.

Before auditing, collect or infer the following and label assumptions:

- business goal, product requirements, success criteria, and the outcome that matters;
- primary audience, expertise, situation, and stakes;
- the user's intended first-value event;
- the primary entry points and journeys;
- known constraints, evidence, metrics, or unresolved questions.

Do not stall when context is missing. State the missing context in **Coverage** or **Basis**, use `not shown` for consequential states or lifecycle moments that the evidence does not expose, and name the fastest validating check.

### Figma and Paper

Frames are valid evidence for visible structure, hierarchy, copy, and the transitions they actually show. They are not proof of behavior. When auditing from frames:

1. Point the agent at one frame or component for Focal.
2. Select the ordered set of frames, including branches and meaningful variants, for Compass. Say which frames are in sequence; do not make the agent guess the path order.
3. Include first-run, success, error, empty, loading, permission, interruption, and re-entry frames when they exist.
4. Mark persistence, validation, timing, and unseen lifecycle behavior as `not shown` unless the frames or prototype demonstrate them.

Useful prompts include `/focal audit this dashboard` and `/compass audit this flow`. A holistic pass is `/product-judgement audit this app` with the relevant frames selected.

## Keep the four boundaries clear

Use the failure's location and consequence to assign a primary owner. Several Skills may mention the same symptom, but the holistic audit prints one issue with one owner and any dependencies.

| Question | Primary owner | Keep it out of this Skill |
|---|---|---|
| What belongs here, what waits, and what should draw attention? | **Focal**—the screen-local decision surface | Do not turn it into a navigation, retention, or expressive-treatment fix. |
| Can the user reach the destination, know where they are, and keep their state? | **Compass**—the path and its seams | Do not score local hierarchy or call every extra step a retention problem. |
| Does the relationship earn trust, first value, recognition, return, or advocacy? | **Flywheel**—the stage transition and lifecycle | Do not use it to replace a missing Back affordance, lost route, or screen-level action model. |
| Once the floor holds, what deserves to be remembered? | **Soul**—the authored moment and its frequency | Do not decorate a maze, hide a trust failure, or treat novelty as a retention strategy. |

### The two common overlaps

**Compass vs Flywheel.** Compass asks whether the route is understandable, economical, reversible, and stateful: *Where do I go? What is next? How do I get back?* Flywheel asks whether the effort and uncertainty on that route earn the next relationship stage: *Why should I continue? Is this too much work or exposure before value?* A hidden step, dead end, or lost state is Compass. A coherent but over-demanding setup, premature ask, or effort that delays first value is Flywheel. Use both when both conditions are present; make the path defect the primary owner when it blocks access to the stage.

**Flywheel vs Soul.** Flywheel owns whether value lands, is recognized, and creates a reason to return. Soul owns how a working moment is authored, placed, and made memorable. If people do not return because they never reached or recognized value, fix Flywheel. If value lands and the path holds but the experience is anonymous, use Soul. Soul may identify motion or expressive treatment that strengthens a Flywheel win or emotion, but it must wait behind trust, comprehension, accessibility, and path integrity.

Focal has the same boundary rule: a confusing action surface is Focal; a misleading product promise or missing evidence across the relationship is Flywheel; a broken transition is Compass. Do not let a local symptom acquire the wrong owner just because it appears on a screen.

## The audit workflow

Run the four local methodologies in this order. This is the evidence order, not an automatic fix order.

### 1. Frame the audit and map coverage

Establish the product, audience, stakes, first value, business goal, and evidence basis. Build a compact map with four views:

- **Screens**—entry, first decision, first value, repeat use, re-entry, high-stakes actions, and failure or recovery states.
- **Journeys**—the primary entry-to-outcome flows, branches, deep links, Back behavior, interruption, and resume behavior.
- **Relationship**—arrival, trust, activation before value, first value, return, lapse, re-engagement, and advocacy.
- **Memory**—the default happy path, its beats, frequency, ending, and any moments already carrying expressive treatment.

Use the same implementation locator throughout: **surface or transition · exact app state · lifecycle moment**. Keep rendered state separate from occurrence. For example, `Import screen · validation error · first-run activation` is precise; `onboarding` is not.

### 2. Run Focal on the decision surfaces

Load [Focal](../focal/SKILL.md) and its [review contract](../focal/reference/review.md). Review the screens that carry the primary decisions or expose the largest relationship stages. Include representative variants rather than pretending one screenshot proves every state. Preserve Focal's native `/12` score and **One Screen, One Clear Intent** verdict.

Record which screen issue is local and which one is actually a path, lifecycle, or memory issue for the later reconciliation.

### 3. Run Compass on the primary journeys

Load [Compass](../compass/SKILL.md) and its [review contract](../compass/reference/review.md). Review the primary journeys as ordered paths, including the seams where state, context, or entry points can fail. Preserve Compass's native `/12` score and **Never Lost** verdict.

Do not use Compass to rescore every screen. Use Focal for local structure and Compass for the route between those surfaces.

### 4. Run Flywheel across the relationship

Load [Flywheel](../flywheel/SKILL.md) and its [review contract](../flywheel/reference/review.md). Name first value before diagnosing. Score all four plays—Trust, Friction, Wins, and Emotion—then identify the earliest leaking stage, not merely the largest downstream symptom. Preserve Flywheel's native `/16` score and diagnosis.

Use the Compass map as evidence for the route, but keep the question separate: Compass explains whether the user can traverse the path; Flywheel explains whether the path earns the next relationship stage.

### 5. Run Soul after checking the floor

Load [Soul](../soul/SKILL.md) and its [review contract](../soul/reference/review.md). Sweep the default happy path, assign frequency and state to each beat, and preserve Soul's native `/16` score and authored-state verdict.

If Focal, Compass, or Flywheel finds a broken floor, still record the Soul findings, but sequence expressive treatment after the structural or lifecycle repair. Do not use delight to cover confusion, a maze, a trust break, or invisible value.

### 6. Reconcile without flattening the Skills

Create one issue ledger from the four native reports:

1. Deduplicate findings that describe the same condition.
2. Assign one primary owner using the boundary rules above.
3. Keep the exact surface or transition, state, and lifecycle locator.
4. Record dependencies, such as `Soul after Compass` or `Flywheel after Focal`.
5. Preserve every local score and verdict; do not average unlike totals into a false Product Judgement score.
6. Separate observed, inferred, walked, tested, and measured claims.

Set the priority changes by dependency and consequence. Rank concrete implementation changes, not just findings or Skill owners:

1. Stop material harm, coercion, hidden cost, permission, or safety failures.
2. Repair the earliest blocker on the route to first value—often trust or path integrity.
3. Fix screen-local decision surfaces that keep the user from acting or understanding.
4. Make delivered value visible and earn the next relationship stage.
5. Spend Soul's expressive budget only after the path, value, and trust floor holds.

This order can change when evidence shows a different upstream dependency. Do not force every product through the same backlog.

## Holistic output

Run all four local audits first, then return this wrapper. Keep the local reports available in working notes; print their full locked templates only when the user asks for the detailed passes. The **Priority changes** section is required: each item must name the owner, exact surface or transition, app state, lifecycle moment, concrete change, reason for its rank, and dependency.

```markdown
**Verdict:** <coherent | needs structural work | needs lifecycle work | needs authorship> · <one biggest cross-scale issue>

**Product:** <what it is, for whom> · goal: <business or user outcome> · first value: <event, or "undefined"> · stakes: <low | medium | high>
**Coverage:** <screens, journeys, relationship stages, states, and lifecycle moments reviewed> · gaps: <material gaps, or "none">
**Basis:** <observed from a screenshot or artifact | inferred from code | tested in a prototype or live product | walked from a description | measured from product data> · confirm with: <fastest validating check>
**Blocker:** <None. | concise blocker reason>

## Four-scale scorecard
| Skill | Native verdict | Score | Primary finding |
|---|---|---:|---|
| Focal | <Clear Intent verdict> | _/12 · _._/4 | <one line> |
| Compass | <Never Lost verdict> | _/12 · _._/4 | <one line> |
| Flywheel | <earliest leaking stage> | _/16 · _._/4 | <one line> |
| Soul | <authored-state verdict> | _/16 · _._/4 | <one line> |

## Cross-scale findings
- **[P0–P3 · <Focal | Compass | Flywheel | Soul>]** **At:** <surface or transition> · state: <exact app state> · lifecycle: <exact lifecycle moment>. <Name>—<observation and cost>. **Fix:** <specific change>. **Depends on:** <owner or "none">.

## Priority changes
1. **Priority 1 · <P0–P3> · Now — <primary owner and stage>** · **At:** <surface or transition> · state: <exact app state> · lifecycle: <exact lifecycle moment>. **Change:** <the concrete implementation change>. **Why now:** <the consequence and upstream reason>. **Depends on:** <owner or "none">.
2. **Priority 2 · <P0–P3> · Next — <primary owner>** · **At:** <surface or transition> · state: <exact app state> · lifecycle: <exact lifecycle moment>. **Change:** <the change unlocked by Now>. **Why now:** <the consequence and dependency>. **Depends on:** <owner or "none">.
3. **Priority 3 · <P0–P3> · Then — <primary owner>** · **At:** <surface or transition> · state: <exact app state> · lifecycle: <exact lifecycle moment>. **Change:** <the change that makes value, return, or comprehension stronger>. **Why now:** <the consequence and dependency>. **Depends on:** <owner or "none">.
4. **Priority 4 · <P0–P3> · After the floor holds — Soul** · **At:** <surface or transition> · state: <exact app state> · lifecycle: <exact lifecycle moment>. **Change:** <the one or two moments worth authoring, or "None yet."> **Why now:** <why expressive treatment is ready—or not ready>. **Depends on:** <owner or "none">.

## Handoffs and validation
- **Focal:** <screen(s) to review or rebuild, with state and lifecycle>.
- **Compass:** <journey or seam to review or rebuild, with state and lifecycle>.
- **Flywheel:** <stage and first-value or return check to validate>.
- **Soul:** <moment to author only after its dependency holds>.
- **Validation:** <fastest behavior, user test, or metric for the highest-consequence claim>.
```

Never emit a vague location such as `the onboarding` or `the dashboard` when a screen, transition, state, and lifecycle moment can be named. If the evidence cannot support that precision, say `not shown` and name what would expose it.

## Routing

- **No argument** → explain that this is the whole-app audit and ask for the product, codebase, prototype, or selected frames plus the primary goal.
- **`audit` / `review` / `critique`** → run the full workflow above. Treat `audit` as the default command.
- **A single-screen request** → hand off to `/focal` and do not run the other three unless the user asks for a holistic pass.
- **A single-flow request** → hand off to `/compass`; add `/flywheel` only when the question includes activation, value, return, or a relationship leak.
- **A single moment or expressive-treatment request** → hand off to `/soul`, after checking whether the floor is sound.
- **A build request** → use the relevant local build Skill; Product Judgement is an audit and reconciliation layer, not a replacement for the Screen, Flow, Stage, or Moment Specs.

## Source files

Read the sibling Skill spines and their review contracts when running the local passes:

- [Focal](../focal/SKILL.md) · [review](../focal/reference/review.md)
- [Compass](../compass/SKILL.md) · [review](../compass/reference/review.md)
- [Flywheel](../flywheel/SKILL.md) · [review](../flywheel/reference/review.md)
- [Soul](../soul/SKILL.md) · [review](../soul/reference/review.md)
