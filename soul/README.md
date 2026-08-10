# Soul

> **Never boring.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

Soul sorts every beat of a product's happy path into **three tiers**—what stays functional, what gets more craft, and the 2–3 moments that get rebuilt entirely.

Not "add polish everywhere." Placement. A product with two authored moments and ten standard beats is remembered; a product with twelve decorated beats is exhausting.

It's an open-source [Claude Code](https://claude.com/claude-code) skill for making a working product memorable. Where [**Focal**](../focal) sharpens one screen, [**Compass**](../compass) guides one journey, and [**Flywheel**](../flywheel) keeps the people you earned, Soul makes the default path worth describing to a friend.

---

## The idea

Most products work and feel like nothing. The word people reach for is *soulless*, and the word is a diagnosis: nothing was authored—the product is the average of its competitors.

Soul is not a spec. It is what accumulates when specific moments are placed well. Three facts decide every placement:

- **People remember the peak and the ending, not the average.** So the biggest swings concentrate on 2–3 moments; the everyday beats get craft, not confetti.
- **Reach beats risk.** Delight traditionally goes where failing is cheap—the 404 page, the easter egg—which is exactly where nobody walks. Soul refuses the dumping grounds and spends the budget on the default path.
- **Repetition kills novelty.** The 50th confetti is noise. What plays every session gets speed and feel; what plays once may spend everything.

Every beat on the path gets exactly one of three tiers:

| Tier | What it is | Where it goes |
|---|---|---|
| **Expected** | the obvious version, fully functional | beats that must simply work |
| **Elevated** | the same moment, executed with more craft | the small things, spread wide—how a product stops being boring |
| **Net-New** | an entirely new experience in place of the old one | the 2–3 biggest moments—the core work |

---

## Install

```bash
git clone https://github.com/kvncnls/kvncnls-skills.git
ln -s "$(pwd)/kvncnls-skills/soul" ~/.claude/skills/soul
```

Prefer a copy, or one project only? `cp -R kvncnls-skills/soul ~/.claude/skills/soul`, or copy the folder into a project's `.claude/skills/`. Restart Claude Code if it was running.

---

## Use

**Search**—soul-searching, mechanized. Point it at a product and it maps the happy path, sorts every beat into a tier, and returns the Net-New moments plus the small things worth elevating.

```
/soul search     ← a product, a flow, screens, or "it feels like every other app"
```

Returns a fixed template: the beat-by-beat path map with a tier per beat, a 0–4 score per gate (/16 with a normalized /4 average and common quality band), the 2–3 Net-New moments ranked, the small things worth elevating, issues tagged P0–P3, and the receipt—which beats stay Expected, and why.

**Build**—design one moment at full depth.

```
/soul build the payment-landed moment
```

Returns a fixed **Moment Spec**: the named feeling, frequency, stakes, and target tier; why this beat earns the budget; all three rungs from floor to target; what every rung holds constant; and a gate check. The pick between rungs stays with you.

---

## What's inside

```
soul/
├── SKILL.md              the placement rules, the 7-beat path skeleton, the eligibility tree
├── reference/
│   ├── review.md         the four-gate search (Baseline, Placement, Proportion, Signature) + scorecard
│   ├── moments.md        eight moment archetypes, frequency classes, selection, the dumping grounds
│   ├── treatments.md     the three tiers in depth, the craft levers, repetition-proof design
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
PICK      2–3 Net-New moments, never more · rank by reach × memory · ties go to the later beat
TIERS     Expected (must simply work) · Elevated (craft the small things) · Net-New (rebuild the biggest)
CEILING   every-run → speed & feel only · high stakes → reassurance before feeling
          once → may spend everything
NEVER     wit at failure · celebration before safety · every-run novelty
          budget in the dumping grounds (404s, easter eggs, error mascots)
```

---

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
