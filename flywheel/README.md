# Flywheel

> **Earn the second visit.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

Flywheel is an open-source [Claude Code](https://claude.com/claude-code) skill for the **growth and retention** side of design. It finds where a product loses the people it already earned, then applies the play that fixes that stage.

Where [**Focal**](../focal) sharpens one screen and [**Compass**](../compass) guides one journey, Flywheel works across the whole relationship—first encounter, activation, value, return.

---

## The idea

A product's journey is usually drawn as a funnel. But the last stage—people who return and bring others—feeds the first. The chain closes. It is not a funnel, it is a wheel.

Four properties of a real flywheel decide everything: it is hardest to start, every push adds to what is stored, its mass keeps it turning between pushes, and friction steals what is stored.

| Play | The part of the wheel | The question |
|---|---|---|
| **1. Trust** | the first push | Is this relevant, credible, worth continuing? |
| **2. Friction** | drag on the bearing | Can I reach value without getting lost or exposed? |
| **3. Wins** | the power stroke | Did this improve my situation, and what now? |
| **4. Emotion** | the mass | How did that feel, and do I prefer it? |

The order is not a preference. **You cannot add mass to a wheel that never started turning.**

---

## Install

```bash
git clone https://github.com/kvncnls/kvncnls-skills.git
ln -s "$(pwd)/kvncnls-skills/flywheel" ~/.claude/skills/flywheel
```

Prefer a copy, or one project only? `cp -R kvncnls-skills/flywheel ~/.claude/skills/flywheel`, or copy the folder into a project's `.claude/skills/`. Restart Claude Code if it was running.

---

## Use

**Diagnose**—find the leak and what to fix first.

```
/flywheel diagnose     ← a product, a stage, or a symptom like "nobody comes back"
```

Returns a fixed template: the leaking stage, a 0–4 score per play (/16 with a band), P0–P3 issues, the one stage to fix first, and what becomes worth doing after it moves.

**Build**—design one stage with its play.

```
/flywheel build the first-run experience for a budgeting app
```

Returns a fixed **Stage Spec**: first value, the leak, the design, the friction deliberately kept, where any ask lands, and a gate check.

---

## What's inside

```
flywheel/
├── SKILL.md              the wheel, the diagnosis tree, the build workflow
├── reference/
│   ├── trust.md          the trust stack, message match, performance, accessibility
│   ├── friction.md       the six-type friction taxonomy, activation, first value
│   ├── wins.md           win map, making value visible, timing asks
│   ├── emotion.md        the arc, baseline vs peaks, endings and re-entry
│   ├── review.md         the four-play audit + scorecard + severity
│   └── examples.md       a worked diagnosis + a worked build
├── README.md
└── LICENSE
```

---

## Scope

**Use it for** the yield on attention you already have: onboarding, activation, empty states, success states, upgrade and referral moments, re-entry, win visibility.

**Not for:**
- Single-screen structure—that's [Focal](../focal).
- Multi-screen paths and getting lost—that's [Compass](../compass).
- Paid acquisition, channels, or marketing copy. Flywheel improves what happens *after* attention arrives.
- Analytics instrumentation, research protocols, or experiment statistics.

Flywheel cannot manufacture product-market fit. It stops a valuable product from hiding its value behind uncertainty, effort, silence, or forgettability.

---

## Quick reference

```
DIAGNOSE  leave without engaging → Trust · never reach value → Friction
          reach value, don't return → Wins · return, then drift → Emotion
EARLIEST  two stages leaking? fix the earlier one—loss compounds downstream
FRICTION  remove accidental & cognitive · keep protective & productive
ASKS      after the value they extend, and declining is free
NEVER     hide cost, permission, risk, or reversibility to increase action
```

---

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
