# Focal

> **One screen, one (primary) purpose.**

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

Focal is an open-source [Claude Code](https://claude.com/claude-code) skill for designing and reviewing **the UX of functional product screens**—apps, tools, and dashboards across mobile, web, and desktop. It is a lens, not a renderer: it decides what belongs on a screen and how it's ranked, so every screen lands on a single, clear purpose.

People don't read a screen, they orient on it—scanning for where they are, what matters, and what to do next. Every screen has to answer *Where am I? What matters here? What do I do?*—whether it's a phone app glanced at one-handed or a dashboard an expert lives in all day. Focal exists to make those answers obvious.

---

## The idea

Simple, clean UX is not a style. It is the visible result of every screen knowing its one job. Focal makes three disciplines the top priority, all culminating in one methodology.

```
                 ┌────────────────────────────────────────────┐
   the outcome   │      ONE SCREEN, ONE (PRIMARY) PURPOSE       │
                 └────────────────────────────────────────────┘
                        ▲              ▲               ▲
   the means     Information      Progressive       Visual
                 Architecture     Disclosure        Hierarchy
                 what belongs     what shows now     what wins
```

- **Information Architecture**—what belongs on the screen, and how it's organized.
- **Progressive Disclosure** *(load-bearing)*—what's shown now, and what waits. At most ~4 things at any decision point on a task screen.
- **Visual Hierarchy**—what wins attention; the heaviest element is the most important one.

Get all three right and the screen settles onto its single purpose on its own. Miss any one and the purpose blurs.

**It adapts to the screen type.** The rules above describe a *task* screen—one job to finish. Two other screen types bend them: a **hub** (home, profile, settings index) exists to *route*, so many destinations is correct, not clutter; an **exploration** surface (feeds, search, grids) exists for *browsing*, so abundance is the point. The working-memory limit doesn't vanish on these—it relocates (per row on a hub, per card on a feed). Focal classifies the register before it judges the screen.

---

## Install

Focal is a standard Claude Code Agent Skill—a folder of Markdown, no build step or dependencies. It ships in the [`kvncnls-skills`](https://github.com/kvncnls/kvncnls-skills) collection. To install it for every session:

```bash
git clone https://github.com/kvncnls/kvncnls-skills.git
# Symlink the skill so edits stay in sync:
ln -s "$(pwd)/kvncnls-skills/focal" ~/.claude/skills/focal
```

Prefer an independent copy, or just one project? Use `cp -R kvncnls-skills/focal ~/.claude/skills/focal`, or copy the `focal/` folder into a project's `.claude/skills/` instead. Restart Claude Code if it was already running.

---

## Use

Invoke it explicitly with `/focal`, or just describe a screen and let it trigger.

**Build a new screen**

```
/focal build a checkout screen for a food-delivery app
```

Focal walks the five moves: name the purpose and single primary action → architect the information → triage disclosure (Now / On-demand / Never) → rank what stays → run the gates. It returns a **fixed Screen Spec**—the same template every time: a one-line screen summary, then Information, Disclosure, Hierarchy, and a six-gate check.

**Review an existing screen**

```
/focal review     ← then paste a screenshot, point at a component file, or give a URL
```

Focal returns the same fixed template every time: a one-line verdict, a 0–4 scorecard (/12 total), prioritized P0–P3 issues (each tied to the discipline it breaks, with the fix), and the top 3 moves.

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

Focal owns *structure and attention*. The execution of color, typography, spacing, and motion is left to your own design system and tooling—visual polish lands far better on a screen that already knows its one job.

---

## Quick reference

```
PURPOSE    "This screen exists so the user can ___."   (no "and")
ACTION     one primary action, period
IA         everything on screen serves that one job · group related · label plainly
DISCLOSE   every element → Now / On-demand / Never · ≤4 at any decision point
HIERARCHY  1 primary · 2–3 secondary · rest ambient · space → weight → size → color
NEVER      hide price, required fields, consequences, or the primary action
```

*Defaults for a task screen. On a hub the ≤4 binds per row; on an exploration surface, per item.*

---

## Contributing

Issues and pull requests welcome. Focal is intentionally tight—three disciplines, one methodology. Proposals should sharpen that focus, not broaden the scope. If a change adds a new topic area (visual craft, motion, code), it probably belongs in a separate skill.

---

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
