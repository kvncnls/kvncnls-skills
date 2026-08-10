# Soul

> **Never boring.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

Soul finds **the 2–3 moments on a product's happy path worth more than functional treatment**—and says what stays standard, on purpose.

Not "add polish everywhere." Placement. A product with two authored moments and ten standard beats is remembered; a product with twelve decorated beats is exhausting.

It's an open-source [Claude Code](https://claude.com/claude-code) skill for making a working product memorable. Where [**Focal**](../focal) sharpens one screen, [**Compass**](../compass) guides one journey, and [**Flywheel**](../flywheel) keeps the people you earned, Soul makes the default path worth describing to a friend.

---

## The idea

Most products work and feel like nothing. The word people reach for is *soulless*, and the word is a diagnosis: nothing was authored—the product is the average of its competitors.

Soul is not a spec. It is what accumulates when specific moments are placed well. Three facts decide every placement:

- **People remember the peak and the ending, not the average.** So you don't elevate everything—you choose.
- **Reach beats risk.** Delight traditionally goes where failing is cheap—the 404 page, the easter egg—which is exactly where nobody walks. Soul refuses the dumping grounds and spends the budget on the default path.
- **Repetition kills novelty.** The 50th confetti is noise. What plays every session gets speed and feel; what plays once may spend everything.

Each chosen moment is designed at three grades:

| Rung | What it is | The test |
|---|---|---|
| **Expected** | the obvious version, fully functional | nothing missing, nothing added—for most beats, the correct final answer |
| **Elevated** | the same moment executed with visible care | nothing new is introduced |
| **Net-New** | the version nobody expects | a screenshot of it could not be mistaken for a competitor |

---

## Install

```bash
git clone https://github.com/kvncnls/kvncnls-skills.git
ln -s "$(pwd)/kvncnls-skills/soul" ~/.claude/skills/soul
```

Prefer a copy, or one project only? `cp -R kvncnls-skills/soul ~/.claude/skills/soul`, or copy the folder into a project's `.claude/skills/`. Restart Claude Code if it was running.

---

## Use

**Search**—soul-searching, mechanized. Point it at a product and it maps the happy path, judges where the expressiveness lives, and returns the moments worth treating.

```
/soul search     ← a product, a flow, screens, or "it feels like every other app"
```

Returns a fixed template: the beat-by-beat path map, a 0–4 score per gate (/16 with a band), the 2–3 moments ranked with a three-rung ladder each, issues tagged P0–P3, and the receipt—which beats stay Expected, and why.

**Build**—design one moment at full depth.

```
/soul build the payment-landed moment
```

Returns a fixed **Moment Spec**: the named feeling, frequency and stakes, why this beat earns the budget, all three rungs, what every rung holds constant, and a gate check. The pick between rungs stays with you.

---

## What's inside

```
soul/
├── SKILL.md              the placement rules, the 7-beat path skeleton, the eligibility tree
├── reference/
│   ├── review.md         the four-gate search (Baseline, Placement, Proportion, Signature) + scorecard
│   ├── moments.md        eight moment archetypes, frequency classes, selection, the dumping grounds
│   ├── treatments.md     the three rungs in depth, the craft levers, repetition-proof design
│   └── examples.md       a worked search + a worked build
├── README.md
└── LICENSE
```

---

## Scope

**Use it for** a product that already works but reads as anonymous: a flat happy path, a success state that stops instead of lands, an ending nobody designed, celebration and personality budgets with nowhere to go.

**Not for:**
- Single-screen structure and clutter—that's [Focal](../focal).
- Multi-screen paths and navigation—that's [Compass](../compass).
- Losing users before they reach value—that's [Flywheel](../flywheel). Soul makes a working path memorable; treatments on a broken path read as cosmetic.
- Brand identity, logo, illustration style, or marketing pages. Soul places moments; it doesn't define the visual language they're executed in.

---

## Quick reference

```
PATH      enters → sees → understands → takes → responds → reaches → feels
          10–12 beats max, each tagged: touchpoint + once | recurring | every-run
PICK      2–3 moments, never more · rank by reach × memory · ties go to the later beat
RUNGS     Expected (the floor) · Elevated (visible care) · Net-New (ship at most one per path)
CEILING   every-run → speed & feel only · high stakes → reassurance before feeling
          once → may spend everything
NEVER     wit at failure · celebration before safety · every-run novelty
          budget in the dumping grounds (404s, easter eggs, error mascots)
```

---

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
