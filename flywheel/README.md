# Flywheel

> **Earn the second visit.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

Flywheel finds **where a product loses people who already showed up**, and tells you the one thing to fix.

Not "how do we get more users." You already got them. Where did they go?

It's an open-source [Claude Code](https://claude.com/claude-code) skill for the **growth and retention** side of design. Where [**Focal**](../focal) sharpens one screen and [**Compass**](../compass) guides one journey, Flywheel works across the whole relationship—first encounter, activation, value, return.

---

## The idea

A product's journey is usually drawn as a funnel. But the last stage—people who return and bring others—feeds the first. The chain closes. It is not a funnel, it is a wheel.

Four properties of a real flywheel decide everything: it is hardest to start, every push adds to what is stored, its mass keeps it turning between pushes, and friction steals what is stored.

| Play | The part of the wheel | What you're checking | What the user is asking |
|---|---|---|---|
| **1. Trust** | the first push | Do they believe this is worth a minute? | *Is this relevant, credible, worth continuing?* |
| **2. Friction** | drag on the bearing | Can they get to the good part? | *Can I reach value without getting lost or exposed?* |
| **3. Wins** | the power stroke | Do they notice the good part happened? | *Did this improve my situation, and what now?* |
| **4. Emotion** | the mass | Do they want to come back? | *How did that feel, and do I prefer it?* |

The order is not a preference. If people don't trust you, nothing downstream matters. If they can't reach the good part, it doesn't matter how good it is. **You cannot add mass to a wheel that never started turning.**

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

Returns a fixed template: the leaking stage, a 0–4 score per play (/16 with a normalized /4 average and common quality band), P0–P3 issues, the one stage to fix first, and what becomes worth doing after it moves.

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

**Use it for** what attention becomes: onboarding, activation, empty states, success states, upgrade and referral moments, re-entry, win visibility. The wheel closes, so the moments that earn word of mouth count too.

**Not for:**
- Single-screen structure—that's [Focal](../focal).
- Multi-screen paths and getting lost—that's [Compass](../compass).
- **Buying** attention: paid channels, budget, bidding, SEO, campaign copy. Flywheel designs what attention meets when it arrives, and what makes people bring more of it. Earned acquisition is in scope; paid is not.
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
