# Focal

> **One screen, one clear intent.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

Focal is an open-source [Claude Code](https://claude.com/claude-code) skill for designing and reviewing **the UX of functional product screens**—apps, tools, and dashboards across mobile, web, and desktop. It is a lens, not a renderer: it decides what belongs on a screen and how it's ranked, so every screen has one legible organizing intent.

That does **not** mean one action, one content block, or one possible user goal. A task screen usually has one primary action. A hub can offer many destinations. An exploration surface can foreground many items. Focal asks whether those things share a clear center of gravity and whether the action model fits the kind of screen.

People don't read a screen, they orient on it—scanning for where they are, what matters, and what to do next. Every screen has to answer *Where am I? What matters here? What do I do?*—whether it's a phone app glanced at one-handed or a dashboard an expert lives in all day. Focal exists to make those answers obvious.

---

## The idea

Simple, clean UX is not a style. It is the visible result of every screen making its organizing intent clear. Focal makes three disciplines the top priority, all culminating in one methodology.

```
                 ┌────────────────────────────────────────────┐
   the outcome   │         ONE SCREEN, ONE CLEAR INTENT         │
                 └────────────────────────────────────────────┘
                        ▲              ▲               ▲
   the means     Information      Progressive       Visual
                 Architecture     Disclosure        Hierarchy
                 what belongs     what shows now     what wins
```

- **Information Architecture**—what belongs on the screen, and how it's organized.
- **Progressive Disclosure** *(load-bearing)*—what's shown now, and what waits. At most ~4 things at any decision point on a task screen.
- **Visual Hierarchy**—what wins attention; the heaviest element or region should match the action model.

Get all three right and the screen settles around one clear intent on its own. Miss any one and that intent blurs.

Focal treats the screen as a **decision surface**, not just a container. It minimizes decisions without withholding useful evidence, infers recognizable input before asking users to classify it, keeps decision-critical context beside the action, and makes consequences legible through summaries, comparisons, previews, or visualizations when raw values are not enough. It can prescribe what the interface should make clear; it does not implement parsers, chart systems, or visual styling.

**It adapts to the screen type.** The default is a *task* screen—one coherent job, usually one primary action. A genuine binary choice or inseparable dual mode can keep co-equal actions. A **hub** (home, profile, settings index) exists to *route*, so many ranked destinations are correct, not clutter. An **exploration** surface (feeds, search, grids) exists for *browsing*, so content leads and abundance is the point. The working-memory limit doesn't vanish on these—it relocates (per row on a hub, per card on a feed). Focal classifies the register before it judges the screen.

---

## Install

Focal is a standard Claude Code Agent Skill—a folder of Markdown, no build step or dependencies. It ships in the [**Product Judgement**](https://github.com/kvncnls/product-judgement) collection. To install it with the Skills CLI:

```bash
npx skills add kvncnls/product-judgement --skill focal
```

To install it manually for every session:

```bash
git clone https://github.com/kvncnls/product-judgement.git
# Symlink the skill so edits stay in sync:
ln -s "$(pwd)/product-judgement/focal" ~/.claude/skills/focal
```

Prefer an independent copy, or just one project? Use `cp -R product-judgement/focal ~/.claude/skills/focal`, or copy the `focal/` folder into a project's `.claude/skills/` instead. Restart Claude Code if it was already running.

---

## Use

Invoke it explicitly with `/focal`, or just describe a screen and let it trigger.

**Build a new screen**

```
/focal build a checkout screen for a food-delivery app
```

Focal walks the five moves: name the organizing intent and register-aware action model → architect the information → triage disclosure (Now / On-demand / Never) → rank what stays → run the gates.

It returns a fixed **Screen Spec**:

- **Screen**—one clear organizing intent and the action model that fits its register.
- **Information**—what stays, moves, merges, or leaves.
- **Disclosure**—what appears Now, On-demand, or Never.
- **Hierarchy**—the intended attention order and focusing mechanism.
- **States**—empty, loading, error, and worst-case full behavior.
- **Gates**—a binary, unscored check of the proposed design.

See the [locked Screen Spec template](./SKILL.md#build-the-five-moves).

**Review an existing screen**

```
/focal review     ← then paste a screenshot, point at a component file, or give a URL
```

It returns a fixed **screen review**:

- **Verdict**—Yes or No for One Screen, One Clear Intent, plus the largest problem and native `/12` total.
- **Screen, Context, Coverage, Basis, and Blocker**—what was reviewed, the user's situation, which app states and lifecycle moments were inspected, material gaps, the confirming check, and any critical condition.
- **Scorecard**—Information Architecture, Progressive Disclosure, and Visual Hierarchy scored `0–4`, with evidence-backed rationales and the smallest change that would raise each score one point, followed by the normalized average and final common band.
- **Issues**—P0–P3 findings tagged to the discipline they break, each anchored to the exact **Screen · Flow · State · Lifecycle** locator with a concrete fix.
- **Top 3 moves and Next**—the highest-leverage changes, structural-before-executional sequencing, and any Compass or Flywheel handoff.

See the [locked review template](./reference/review.md#output-formatuse-this-exact-structure) and the collection's [shared audit contract](../README.md#shared-audit-contract).

---

## What's inside

```
focal/
├── SKILL.md              the spine: methodology, three disciplines, build workflow
├── reference/
│   ├── review.md         the three-discipline audit + scorecard + severity
│   ├── patterns.md       IA techniques, disclosure catalog, hierarchy ladder, anti-patterns
│   └── examples.md       a worked review + a worked build, in the locked templates
├── README.md
└── LICENSE
```

---

## Scope

**Use it for** functional interfaces—app, product, and tool screens across mobile, web, desktop, and tablet, for everyday or expert users: onboarding, feeds, home screens, settings, dashboards, admin panels, checkout, editors, consoles. Anywhere someone is trying to get something done. Density-heavy expert tools are in scope too—Focal adapts via the screen's register and the user's expertise (experts read dense displays as a few familiar chunks).

**Not for:**
- Marketing or landing pages, where design *is* the product and the job is persuasion, not task completion.
- Backend or non-UI work.

Focal owns *structure and attention*. The execution of color, typography, spacing, and motion is left to your own design system and tooling—visual polish lands far better on a screen whose center of gravity is already clear.

For a whole-app audit that combines this screen pass with journey, relationship, and memory reviews, use [**Product Judgement**](../product-judgement).

For a complete multi-screen journey, use Compass to map the path and Flywheel to diagnose where activation, value recognition, or return loses momentum. Focal keeps each screen inside that journey understandable and actionable.

---

## Quick reference

```
INTENT     "This screen exists so the user can ___."   (no unrelated second outcome)
ACTION     task: one primary usually · hub: ranked routes · exploration: content leads
IA         everything supports the organizing intent · group related · label plainly
DISCLOSE   every element → Now / On-demand / Never · ≤4 at any decision point
DECIDE     minimize choices · infer before asking · context at the decision · consequence visible
HIERARCHY  1 dominant element/region · 2–3 secondary · rest ambient
           space → weight → size → color
NEVER      hide price, required fields, consequences, or controls needed now
```

*A task can preserve an inherent binary choice or inseparable dual mode. On a hub the ≤4 binds per row; on an exploration surface, per item.*

---

## Contributing

Issues and pull requests welcome. Focal is intentionally tight—three disciplines, one methodology. Proposals should sharpen that focus, not broaden the scope. If a change adds a new topic area (visual craft, motion, code), it probably belongs in a separate skill.

---

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
