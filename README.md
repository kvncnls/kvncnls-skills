# kvncnls-skills

A collection of Skills for product design and UI/UX design, by Kevin Canlas. Each one is a self-contained folder of Markdown—no build step, no dependencies—and each also ships as a single file, so they work in Claude Code, Codex, ChatGPT, Cursor, and anything else that reads Markdown.

**A system for product judgment across four scales of experience: the screen, the journey, the relationship, and the memory.**

The umbrella is **coherence**: focused within a screen, navigable across a journey, valuable across the relationship, memorable after the experience, and trustworthy throughout.

## Why these exist

Vibe coding made building software fast and easy—describe a feature, watch it appear. But building fast and designing well are different skills, and the second hasn't kept up. I keep seeing the same pattern: features stacked on features, screens accumulating widgets, flows sprouting steps, value buried behind setup, and meaningful moments flattened into generic UI. No one stops to ask whether the app still hangs together, earns a second visit, or gives anyone something worth remembering.

The first casualties are the quiet judgments that make software feel coherent: what belongs, what waits, what deserves attention, how state survives, whether value becomes visible, and where craft earns its place. They rarely block a release, so they get skipped. The product still works, but it breaks at one of four scales:

- **The screen**—it does too much. Widgets compete, nothing is clearly primary, everything shows at once.
- **The journey**—the path becomes a maze. Too many steps, no sense of where you are, no clean way back.
- **The relationship**—people arrive, but value is buried, delayed, or delivered silently, so the product never earns a second visit.
- **The memory**—everything works and nothing stays with you. Every screen functional, every flow passable, nothing anyone would describe to a friend.

Across all four, trust is the floor: no coherent experience hides material consequence, destroys work, removes informed choice, or uses craft to cover a broken path.

These Skills put that judgment back in the loop, on demand:

- **Focal** gives a screen one clear center of gravity—*one screen, one clear intent.*
- **Compass** keeps a journey navigable—*never lost.*
- **Flywheel** keeps the value you earned from leaking away—*earn the second visit.*
- **Soul** gives the happy path moments worth remembering—*never boring.*

More will follow, each targeting a craft that speed tends to leave behind.

## One skill, one job

Each Skill is deliberately scoped around one design lens and a north-star outcome. Each supports a focused build workflow and a separate audit-style workflow, with handoffs for adjacent problems.

Focal decides what belongs on one screen and what wins attention. Compass designs the path between screens so users stay oriented and state survives the seams. Flywheel finds the earliest leak that keeps arrival from becoming value—or value from earning a second visit. Soul decides where a working happy path should stay conventional, gain craft, or become memorable.

Their boundaries are working boundaries, not walls. This keeps the collection composable: use one lens when it is enough, combine several when the problem crosses scales, and never turn any one Skill into an all-purpose product design system.

## Product judgment, encoded

These Skills encode product-design judgment: principles, decision trees, failure modes, review rubrics, exceptions, and fixed outputs for recurring UX problems. Their purpose is to help an AI reason about the experience as a connected system instead of generating one plausible screen at a time.

They operate on actual UX decisions: what belongs on a screen, what should wait, which action deserves attention, how a user knows where they are, whether state survives between steps, where a product loses people, whether users recognize that value happened, and which moments deserve deeper authorship.

They complement rather than replace conventional design systems. Traditional systems help teams render decisions consistently through components, tokens, patterns, and documentation. AI-native design systems also need a judgment layer that governs which decisions should be made: what belongs, what waits, what protects the user, which stage is leaking, and where expressive treatment earns its place. That is the layer this collection explores.

## What this repo is not

This is not a design-system analyzer, component library, token validator, or visual-regression suite. It does not judge whether components are consistent or tell you how to organize tokens. It sits above those systems and helps decide what the experience should do: what belongs, what waits, where value leaks, and where craft earns its place.

It is not a renderer, prototyping tool, animation library, or implementation framework. The Skills produce judgment, audits, and fixed specifications—not production UI or animation code. Soul can identify which moments deserve motion, what that motion should communicate, and when restraint is better; design and engineering tools still implement it.

It is not user research, analytics, experimentation, marketing, or product strategy. It can form hypotheses, locate leaks, and name the fastest validating test or metric, but it does not interview users, instrument events, prove causality, buy attention, set the roadmap, or manufacture product-market fit.

It is not a whole-app sitemap or an all-purpose UX system. Focal works within a screen, Compass between screens, Flywheel across relationship stages, and Soul across memorable moments. They complement design systems and formal accessibility, security, legal, and safety reviews; they do not replace them.

## Skills

| Skill | What it does | Reach for it when |
|-------|--------------|------------------|
| [**focal**](./focal) | One screen, one clear intent. Declutters and structures app/dashboard screens through three disciplines—Information Architecture, Progressive Disclosure, and Visual Hierarchy. Its action model adapts to task, hub, and exploration screens. | A screen feels crowded, unclear, or unable to make its organizing intent and action model legible. Use it to decide what belongs, what waits, and what wins attention. |
| [**compass**](./compass) | Never lost. Guides multi-screen flows and navigation through three disciplines—Orientation, Path Economy, and Continuity. Build new flows or review existing ones. Pairs with Focal (single screens). | A task spans screens and users may be lost, facing too many steps, dead ends, Back that resets or loses context, missing progress, or lost state. |
| [**flywheel**](./flywheel) | Earn the second visit. Growth and retention: finds where a product loses the users it already earned, across four ordered plays—Trust, Friction, Wins, and Emotion. Diagnose where value is leaking, or design the experience that earns the next stage of the relationship. | People arrive but do not trust, reach value, recognize value, return, or bring others. Use it to find the earliest relationship leak or design the stage that earns the next step. |
| [**soul**](./soul) | Never boring. Delight, placed: sorts every beat of the happy path into three tiers—Expected stays functional, Elevated adds craft to the small things, Net-New rebuilds the 2–3 biggest moments entirely. Search a product or build a moment. | The happy path works but feels generic, forgettable, or over-designed. Use it to decide which moments stay conventional, gain craft, or become memorable—including where motion earns its place. |

## What each Skill returns

Every Skill has two output modes. **Build** proposes a new design as a fixed specification with an unscored gate checklist. **Audit-style modes**—review, diagnose, or search—evaluate an existing artifact with numeric scores, prioritized findings, and a local methodology verdict.

| Skill | Build output | Audit-style output | Local conclusion |
|---|---|---|---|
| [**Focal**](./focal) | **Screen Spec**—organizing intent, action model, information, disclosure, hierarchy, states, and gates | **Screen review**—three-discipline scorecard, issues, Top 3 moves, and structural/executional next steps | Does the screen satisfy **One Screen, One Clear Intent**? |
| [**Compass**](./compass) | **Flow Spec**—destination, steps, cuts, orientation, continuity, and gates | **Flow review**—three-discipline scorecard, issues, Top 3 moves, and structural/executional next steps | Is the user **Never Lost**? |
| [**Flywheel**](./flywheel) | **Stage Spec**—first value, leak, design, friction kept, ask placement, and gates | **Diagnosis**—four-play scorecard, issues, one stage to fix first, and what follows | Where does momentum drop first—before engagement, before first value, after value, or after repeat use? |
| [**Soul**](./soul) | **Moment Spec**—feeling, frequency, tier, three rungs, constraints, and gates | **Happy-path sweep**—path map, four-gate scorecard, ranked moments, small things, and restraint receipt | Is the path authored, anonymous, misplaced, or exhausting? |

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

The scorecard keeps each Skill's native total—`/12` for Focal and Compass, `/16` for Flywheel and Soul—and also displays `total ÷ dimensions` as a normalized `/4` average rounded to one decimal place.

| Common band | Average | `/12` total | `/16` total |
|---|---:|---:|---:|
| **Broken** | `≤ 1.5` | `0–4` | `0–6` |
| **Significant rework** | `> 1.5` and `< 2.5` | `5–7` | `7–9` |
| **Solid** | `≥ 2.5` and `< 3.5` | `8–10` | `10–13` |
| **Excellent** | `≥ 3.5` | `11–12` | `14–16` |

The weakest dimension then caps the final displayed band: a lowest score of `0` caps it at **Broken**, `1` at **Significant rework**, `2` at **Solid**, and `3–4` adds no ceiling. This prevents a high total from hiding one failed dimension.

Five concepts remain separate in every audit:

- **Dimension score**—quality within one Skill-specific discipline, play, or gate.
- **Final quality band**—the lower of the average-derived band and weakest-dimension ceiling.
- **Issue severity**—P0 Critical, P1 Major, P2 Moderate, or P3 Minor, assigned from consequence, reach, and recoverability.
- **Blocker**—an explicit release-critical condition; every P0 is a blocker, but a blocker does not automatically force a score to `0`.
- **Local verdict**—the Skill's own north-star conclusion, evaluated independently from the common band.

Every audit declares **Coverage**: the app states and lifecycle moments actually reviewed, plus material gaps. Every issue then carries an implementation locator—**surface or transition · state · lifecycle**—so the reader can open the right place and reproduce the condition directly. Here, lifecycle means the user's journey or relationship with the product (first run, pre-value activation, recurring use, interruption/resume, re-entry, lapse), not a software release phase. If the evidence does not expose a consequential state, the audit says `not shown` and names the validating check instead of inventing behavior.

Every audit also states its evidence **Basis** and the fastest test, behavior, or metric that would confirm its most consequential uncertain claim.

## Install

Each skill comes in two shapes. The **folder** (`focal/`) loads its references on demand and gives you a slash command. The **bundle** ([`bundles/focal.md`](./bundles)) is the same skill flattened into one file—spine, references, rubrics, and templates—for tools that can't load a multi-file folder. Start by cloning:

```bash
git clone https://github.com/kvncnls/kvncnls-skills.git
```

**Claude Code**—install the folder. Symlink to keep edits in sync:

```bash
ln -s "$(pwd)/kvncnls-skills/focal" ~/.claude/skills/focal
```

Prefer an independent copy, or scope it to one project?

```bash
cp -R kvncnls-skills/focal ~/.claude/skills/focal     # independent copy, all projects
cp -R kvncnls-skills/focal <project>/.claude/skills/  # one project only
```

Restart Claude Code and `/focal` is available.

**Codex**—append a bundle to your project's `AGENTS.md`, which Codex loads automatically:

```bash
cat kvncnls-skills/bundles/focal.md >> AGENTS.md
```

**ChatGPT**—create a Custom GPT and paste a bundle into *Instructions*, or upload it as a *Knowledge* file. A Project works the same way: add it to the project's files.

**Cursor / Windsurf / Cline**—drop a bundle in as a rules file:

```bash
cp kvncnls-skills/bundles/focal.md .cursor/rules/focal.md
```

Swap `focal` for whichever skill you want. Each skill's own `README.md` has its full usage, and the bundles are build artifacts—regenerate rather than edit them.

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
