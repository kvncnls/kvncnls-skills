# Product Judgement

Skills for making better product decisions across the screen, the journey, the relationship, and the memory. The four foundational Skills—Focal, Compass, Flywheel, and Soul—each own a scale; Product Judgement combines them for holistic audits. The Skills are Markdown folders—no build step, no dependencies—and each also ships as a single file, so they work in Claude Code, Codex, ChatGPT, Cursor, and anything else that reads Markdown.

The umbrella is **coherence**: focused within a screen, navigable across a journey, valuable across the relationship, memorable after the experience, and trustworthy throughout.

## Why this collection exists

Vibe coding made implementation fast and easy and made product judgement even easier to skip. Features accumulate, screens grow crowded, flows become mazes, value gets buried, and working products become generic and forgettable. The 'Ship fast, iterate later' mantra has produced AI product slop en masse.

These Skills put product judgement back in the loop. They encode principles, decision trees, failure modes, audit rubrics, exceptions, and fixed outputs for recurring UX problems—helping an AI reason about the experience as a connected system instead of generating one plausible screen at a time.

They complement design systems: design systems standardize how decisions are rendered; these Skills help decide which decisions should be made.

The four foundational Skills each own one scale: Focal sharpens the screen, Compass connects the journey, Flywheel strengthens the relationship, and Soul authors what gets remembered. They stay narrow so they can be combined when a problem crosses scales. **Product Judgement** is the holistic audit that runs all four, keeps their boundaries clear, and turns their findings into one prioritized sequence; it is not a fifth scale or an all-purpose product design system.

## What this repo is not

This is not a design-system analyzer, component library, token validator, visual-regression suite, renderer, prototyping tool, animation library, or implementation framework. It produces product-design judgement, audits, and fixed specifications—not production UI or animation code. Soul can identify where motion or expressive treatment earns its place; other tools implement it.

It is not context-free product wisdom. Because these Skills make product-design decisions, they work best with the context behind the decision: business goals, user intent, audience, constraints, stakes, the existing journey, and the evidence available. The more relevant context you provide, the more specific and useful the output; without it, the result is a hypothesis to validate, not a substitute for product knowledge.

It is not user research, analytics, experimentation, marketing, or product strategy. It can form hypotheses, locate leaks, and name a confirming test or metric, but it does not collect evidence, prove causality, buy attention, set roadmaps, or manufacture product-market fit. It is not a whole-app sitemap or all-purpose UX system, and it does not replace design-system, accessibility, security, legal, or safety reviews.

## Skills

| Skill | What it does | Reach for it when |
|-------|--------------|------------------|
| [**product-judgement**](./product-judgement) | Holistic audit. Runs all 4 Skills below against a shared evidence map, then reconciles their findings into one prioritized fix sequence. | The question spans the app, or several Skills identify related issues and you need to decide what to fix first. |
| [**focal**](./focal) | One screen, one clear intent. Declutters and structures app/dashboard screens through three disciplines—Information Architecture, Progressive Disclosure, and Visual Hierarchy. Its action model adapts to task, hub, and exploration screens. | A screen feels crowded, unclear, or unable to make its organizing intent and action model legible. Use it to decide what belongs, what waits, and what wins attention. |
| [**compass**](./compass) | Never lost. Guides multi-screen flows and navigation through three disciplines—Orientation, Path Economy, and Continuity. Build new flows or review existing ones. Pairs with Focal (single screens). | A task spans screens and users may be lost, facing too many steps, dead ends, Back that resets or loses context, missing progress, or lost state. |
| [**flywheel**](./flywheel) | Earn the second visit. Growth and retention: finds where a product loses the users it already earned, across four ordered plays—Trust, Friction, Wins, and Emotion. Diagnose where value is leaking, or design the experience that earns the next stage of the relationship. | People arrive but do not trust, reach value, recognize value, return, or bring others. Use it to find the earliest relationship leak or design the stage that earns the next step. |
| [**soul**](./soul) | Never boring. Delight, placed: sorts every beat of the happy path into three tiers—Expected stays functional, Elevated adds craft to the small things, Net-New rebuilds the 2–3 biggest moments entirely. Search a product or build a moment. | The happy path works but feels generic, forgettable, or over-designed. Use it to decide which moments stay conventional, gain craft, or become memorable—including where motion earns its place. |

## What each Skill returns

The four foundational Skills have two output modes. **Build** proposes a new design as a fixed specification with an unscored gate checklist. **Audit-style modes**—review, diagnose, or search—evaluate an existing artifact with numeric scores, prioritized findings, and a local methodology verdict. Product Judgement is audit-only: it preserves the four native scorecards and adds cross-scale prioritization without inventing a fifth score.

| Skill | Build output | Audit-style output | Local conclusion |
|---|---|---|---|
| [**Product Judgement**](./product-judgement) | — | **Holistic audit**—four native scorecards with evidence-backed component rationales, shared coverage, deduplicated cross-scale findings, and a prioritized list of changes with Screen · Flow · State · Lifecycle locators | Are the four scales coherent, and what should be fixed first? |
| [**Focal**](./focal) | **Screen Spec**—organizing intent, action model, information, disclosure, hierarchy, states, and gates | **Screen review**—three-discipline scorecard with per-discipline rationales, issues, Top 3 moves, and structural/executional next steps, all located by Screen · Flow · State · Lifecycle | Does the screen satisfy **One Screen, One Clear Intent**? |
| [**Compass**](./compass) | **Flow Spec**—destination, steps, cuts, orientation, continuity, and gates | **Flow review**—three-discipline scorecard with per-discipline rationales, issues, Top 3 moves, and structural/executional next steps, all located by Screen · Flow · State · Lifecycle | Is the user **Never Lost**? |
| [**Flywheel**](./flywheel) | **Stage Spec**—first value, leak, design, friction kept, ask placement, and gates | **Diagnosis**—four-play scorecard with per-play rationales, issues, one stage to fix first, and what follows, all located by Screen · Flow · State · Lifecycle | Where does momentum drop first—before engagement, before first value, after value, or after repeat use? |
| [**Soul**](./soul) | **Moment Spec**—feeling, frequency, tier, three rungs, constraints, and gates | **Happy-path sweep**—four-gate scorecard with per-gate rationales, path map, ranked moments, small things, and restraint receipt, all located by Screen · Flow · State · Lifecycle | Is the path authored, anonymous, misplaced, or exhausting? |

For Flywheel, a **leak** is not just churn. It is the first point where momentum drops out of the relationship: people leave without engaging, engage without reaching first value, reach value without returning or converting, or return for a while and then drift away.

## Shared audit contract

Build outputs are proposals, so their gates remain binary and unscored. Audit-style outputs evaluate something that already exists, so every local dimension receives an integer score from `0–4`:

| Score | Meaning |
|---:|---|
| **0 — Broken or harmful** | Fails outright, blocks the dimension's core outcome, inverts the intended behavior, or creates material harm. |
| **1 — Major failure** | Technically possible, but seriously compromised, unreliable, or largely absent. |
| **2 — Partial or inconsistent** | The basic function exists, but a material weakness prevents dependable quality. |
| **3 — Strong** | Deliberate, dependable professional work with only minor gaps—the normal target for good execution. |
| **4 — Exemplary** | Fully realized and unusually strong for its context, realistic states, and constraints. |

The scorecard keeps each foundational Skill's native total—`/12` for Focal and Compass, `/16` for Flywheel and Soul—and also displays `total ÷ dimensions` as a normalized `/4` average rounded to one decimal place. Product Judgement preserves those native totals and does not average them into a misleading collection-wide score.

| Common band | Average | `/12` total | `/16` total |
|---|---:|---:|---:|
| **Broken** | `≤ 1.5` | `0–4` | `0–6` |
| **Significant rework** | `> 1.5` and `< 2.5` | `5–7` | `7–9` |
| **Solid** | `≥ 2.5` and `< 3.5` | `8–10` | `10–13` |
| **Excellent** | `≥ 3.5` | `11–12` | `14–16` |

The weakest dimension then caps the final displayed band: a lowest score of `0` caps it at **Broken**, `1` at **Significant rework**, `2` at **Solid**, and `3–4` adds no ceiling. This prevents a high total from hiding one failed dimension.

### Scores must explain themselves

A score without an explanation is invalid. Every scorecard row must show the chain **evidence → consequence → rubric anchor → next-point change**:

- **Evidence**—what was observed, inferred, tested, walked, or measured, anchored to the relevant surface or transition, app state, and lifecycle moment.
- **Consequence**—what that condition costs the user or product in the Skill's terms.
- **Rubric anchor**—why the evidence earns this integer and what keeps it from the next higher integer. A `2` says what works and names the material weakness; a `3` names the remaining gap; a `4` explains why the dimension is exemplary.
- **Next-point change**—the smallest concrete change that would raise the score by one point; a `4` says `None—already exemplary.`

Do not award credit for behavior the artifact does not expose, and do not turn an unseen state into a failure without a rubric basis. Mark it `not shown` in Coverage/Basis and name the validating check. The total is the exact sum of the justified component scores; never derive component scores from the total.

`Focal 7/12` is therefore incomplete. A valid result must show something like: `Information Architecture 2/4`—the screen groups the core content but leaves two independent jobs resident, so the user still sorts competing outcomes; split or demote one job to reach 3. `Progressive Disclosure 2/4`—the primary facts are visible but secondary history loads at full depth; cap the default and defer the rest to reach 3. `Visual Hierarchy 3/4`—the primary action wins, with one secondary region still too loud; quiet that region to reach 4. Then, and only then, report **7/12 · 2.3/4 · Significant rework**.

Five concepts remain separate in every audit:

- **Dimension score**—quality within one Skill-specific discipline, play, or gate.
- **Final quality band**—the lower of the average-derived band and weakest-dimension ceiling.
- **Issue severity**—P0 Critical, P1 Major, P2 Moderate, or P3 Minor, assigned from consequence, reach, and recoverability.
- **Blocker**—an explicit release-critical condition; every P0 is a blocker, but a blocker does not automatically force a score to `0`.
- **Local verdict**—the Skill's own north-star conclusion, evaluated independently from the common band.

Every audit declares **Coverage** with a four-part implementation locator: **Screen** (the exact UI surface), **Flow** (the named journey or transition, or `screen-local`), **State** (the exact rendered or system condition), and **Lifecycle** (the exact user/product moment). Every issue, Top 3 move, Next item, handoff, and Product Judgement priority change carries the same four fields, so the reader can open the right place and reproduce how and when the condition occurs. Here, lifecycle means the user's journey or relationship with the product (first run, pre-value activation, recurring use, interruption/resume, re-entry, lapse), not a software release phase. Never use only `the dashboard` or `onboarding`; if a field is not evidenced, write `not shown` and name the validating check instead of inventing behavior.

Every audit also states its evidence **Basis** and the fastest test, behavior, or metric that would confirm its most consequential uncertain claim.

## How to use

Designers and developers can use these Skills from a codebase, Figma, Paper, a clickable prototype, screenshots, or a product description. Point the LLM at the artifact and name the scale you want it to inspect.

### From Figma or Paper

Point at one frame when using Focal:

```text
/focal audit this dashboard
```

For Compass, select the screens in order—including branches and important variants—and say which frames form the flow:

```text
/compass audit this flow
```

You can also ask Flywheel to inspect the relationship represented by the frames, or Soul to sweep the happy path:

```text
/flywheel audit this onboarding flow
/soul audit the happy path
```

Frames show visible structure and selected transitions well, but they do not prove persistence, validation, timing, or lifecycle behavior. Include loading, empty, error, success, permission, interruption, and re-entry states when they exist; otherwise the audit will mark them `not shown`.

### From the codebase (recommended)

The codebase usually contains more context than Figma or Paper: routes, state transitions, persistence, validation, copy, error handling, and the actual lifecycle of the product. Run the Skills from the project so the LLM can inspect that context:

```text
/focal audit the dashboard
/compass audit the onboarding flow
/flywheel audit the onboarding flow
/soul audit the happy path
```

When the question spans the app, use the holistic Skill:

```text
/product-judgement audit the app
```

Product Judgement runs all four foundational Skills, keeps their ownership distinct, and returns the native scorecards plus a deduplicated issue ledger, a prioritized list of changes with dependencies, and a validation plan. It does not add another lens: Focal owns the screen, Compass the path, Flywheel the relationship, and Soul the memory.

Give the Skills the surrounding product context as well. Attach or point the LLM at the PRD (Product Requirements Document), product brief, strategy or goal documents, user research, personas, journey maps, analytics or funnel data, support themes, experiment history, and technical, accessibility, legal, or safety constraints. The more relevant context you provide, the better the Skills can judge whether a design serves a real user, goal, and constraint instead of only reacting to what is visible. When context is missing, the Skills state their assumptions instead of presenting them as facts.

## Install

### Any supported agent

Install all five Skills—including the holistic audit—with the [Skills CLI](https://skills.sh/docs/cli):

```bash
npx skills add kvncnls/product-judgement --all
```

Or install the collection globally for Claude Code, Codex, and Cursor:

```bash
npx skills add kvncnls/product-judgement --skill '*' -g -a claude-code -a codex -a cursor -y
```

Install one foundational Skill by name:

```bash
npx skills add kvncnls/product-judgement --skill focal
```

Product Judgement uses the four foundational Skills, so install the full set with the command above when you want `/product-judgement`.

### Manual installation

Each skill comes in two shapes. The **folder** (`focal/`) loads its references on demand and gives you a slash command. The **bundle** ([`bundles/focal.md`](./bundles)) is the same skill flattened into one file—spine, references, rubrics, and templates—for tools that can't load a multi-file folder. Start by cloning:

```bash
git clone https://github.com/kvncnls/product-judgement.git
```

**Claude Code**—install the folder. Symlink to keep edits in sync:

```bash
ln -s "$(pwd)/product-judgement/focal" ~/.claude/skills/focal
```

Prefer an independent copy, or scope it to one project?

```bash
cp -R product-judgement/focal ~/.claude/skills/focal     # independent copy, all projects
cp -R product-judgement/focal <project>/.claude/skills/  # one project only
```

Restart Claude Code and `/focal` is available.

**Codex**—append a bundle to your project's `AGENTS.md`, which Codex loads automatically:

```bash
cat product-judgement/bundles/focal.md >> AGENTS.md
```

**ChatGPT**—create a Custom GPT and paste a bundle into *Instructions*, or upload it as a *Knowledge* file. A Project works the same way: add it to the project's files.

**Cursor / Windsurf / Cline**—drop a bundle in as a rules file:

```bash
cp product-judgement/bundles/focal.md .cursor/rules/focal.md
```

Swap `focal` for whichever foundational Skill you want. The root README and each foundational Skill's own `README.md` have full usage details, and the bundles are build artifacts—regenerate rather than edit them. Product Judgement's orchestration instructions live in its `SKILL.md` and bundle.

For a holistic `/product-judgement` audit in a single-file environment, load the `product-judgement` bundle together with the Focal, Compass, Flywheel, and Soul bundles. The holistic Skill needs all four local methodologies to produce its native scorecards and cross-scale fix order.

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
