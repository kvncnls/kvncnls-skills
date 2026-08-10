# Compass

> **Never lost.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

Compass is an open-source [Claude Code](https://claude.com/claude-code) skill for designing and reviewing **cross-screen flows**—onboarding, checkout, setup, wizards, dashboards with drill-down, any journey that spans more than one screen. It owns the *path between screens*: navigation, step-count, where "back" goes, state, and entry points.

Where its sibling [**Focal**](../focal) sharpens a single screen, Compass guides the journey across screens. *Focal is within a screen; Compass is between them.*

---

## The idea

A flow is a sequence of screens with a destination. Good cross-screen UX means the user can always answer three questions: **Where am I? How far is left? How do I get back, or out?** The moment they can't, the flow becomes a maze—and people abandon mazes.

```
            ┌──────────────────────────────────────┐
  promise   │              NEVER LOST                │
            └──────────────────────────────────────┘
                  ▲              ▲              ▲
  the means   Orientation   Path Economy   Continuity
              where am I    fewest honest   the seams
              / how out     steps           hold
```

- **Orientation** *(load-bearing)*—at every step: position, progress, and a way back or out.
- **Path Economy**—the fewest *honest* steps to the destination (never shorten by hiding cost).
- **Continuity**—context and state survive the seams between screens.

---

## Install

Compass ships in the [`kvncnls-skills`](https://github.com/kvncnls/kvncnls-skills) collection. To install it for every session:

```bash
git clone https://github.com/kvncnls/kvncnls-skills.git
# Symlink the skill so edits stay in sync:
ln -s "$(pwd)/kvncnls-skills/compass" ~/.claude/skills/compass
```

Prefer an independent copy, or just one project? Use `cp -R kvncnls-skills/compass ~/.claude/skills/compass`, or copy the `compass/` folder into a project's `.claude/skills/` instead. Restart Claude Code if it was already running.

---

## Use

Invoke it with `/compass`, or just describe a flow and let it trigger.

**Build a new flow**

```
/compass build the onboarding flow for a budgeting app
```

Compass walks four moves—name the destination → map the fewest honest steps → signpost every step → join the seams.

It returns a fixed **Flow Spec**:

- **Flow**—one entry-to-destination journey, its type, and audience.
- **Steps**—the ordered path and what can be skipped.
- **Cut**—what was removed or merged, plus protection deliberately retained.
- **Orientation**—position, progress, Back, and exit behavior.
- **Continuity**—what carries forward and survives interruption, plus how entry points land.
- **Gates**—a binary, unscored check of the proposed design.

See the [locked Flow Spec template](./SKILL.md#build-outputthe-flow-spec-use-this-exact-structure).

**Review an existing flow**

```
/compass review     ← describe the flow, or give a set of screens / a prototype
```

It returns a fixed **flow review**:

- **Verdict**—Yes or No for Never Lost, plus the largest break and native `/12` total.
- **Flow, Context, Basis, and Blocker**—what was reviewed, the evidence available, the confirming check, and any critical condition.
- **Scorecard**—Orientation, Path Economy, and Continuity scored `0–4`, followed by the normalized average and final common band.
- **Issues**—P0–P3 findings tagged to the discipline they break, each with a concrete fix.
- **Top 3 moves and Next**—the highest-leverage changes, structural-before-executional sequencing, and any Focal handoff.

See the [locked review template](./reference/review.md#output-formatuse-this-exact-structure) and the collection's [shared audit contract](../README.md#shared-audit-contract).

---

## What's inside

```
compass/
├── SKILL.md              the spine: Never Lost, three disciplines, build workflow
├── reference/
│   ├── review.md         the three-discipline flow audit + scorecard + severity
│   ├── patterns.md       orientation, step-reduction, continuity, flow-type playbooks, anti-patterns
│   └── examples.md       a worked flow review + a worked flow build, in the locked templates
├── README.md
└── LICENSE
```

---

## Scope

**Use it for** cross-screen flows in functional products—apps, tools, dashboards—across mobile, web, and desktop, for everyday or expert users.

**Not for:**
- Single-screen layout and structure—that's [Focal](../focal). Compass assumes each screen is sound and focuses on the joins.
- Marketing or landing pages, where design *is* the product.
- Whole-app sitemaps generated from a spec (deciding *which* screens exist before any flow is drawn).
- Backend or non-UI work.

Compass owns *movement and orientation*. The execution of color, type, motion, and copy is left to your design system, and each individual screen is left to Focal.

---

## Quick reference

```
DESTINATION  "This flow gets the user from ___ to ___."   (one outcome)
STEPS        fewest honest steps · cut waste, never protection
ORIENT       where am I · how far left · a real back + an exit, every step
CARRY        no memory bridge · state survives back/resume · deep links land in context
NEVER        a dead end, a trap, a lost step, or a shortcut that hides cost
```

---

## Contributing

Issues and pull requests welcome. Compass is intentionally tight—three disciplines, one promise. Proposals should sharpen the *between-screens* focus, not broaden it into single-screen design (that's Focal) or whole-app planning.

---

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
