# kvncnls-skills

A collection of Skills for product design and UI/UX design, by Kevin Canlas. Each one is a self-contained folder of Markdown—no build step, no dependencies—and each also ships as a single file, so they work in Claude Code, Codex, ChatGPT, Cursor, and anything else that reads Markdown.

## Why these exist

Vibe coding made building software fast and easy—describe a feature, watch it appear. But building fast and designing well are different skills, and the second hasn't kept up. I keep seeing the same thing: features stacked on features, screens accumulating widgets, flows sprouting steps, with no one asking whether the app still hangs together.

The first casualties are the quiet disciplines that make software feel effortless—information architecture, visual hierarchy, progressive disclosure, navigation, spatial awareness. They rarely block a release, so they get skipped, and the app ends up technically working but overwhelming to use. It usually breaks in one of four ways:

- **Within a screen**—it does too much. Widgets compete, nothing is clearly primary, everything shows at once.
- **Between screens**—the journey becomes a maze. Too many steps, no sense of where you are, no clean way back.
- **Across the whole visit**—it works, and they still don't come back. Nothing is broken exactly, the product just never made the case for a second visit. The instinct is to go get more people, when the ones you already had were right there.
- **Or nothing breaks at all**—it works, and nobody remembers it. Every screen functional, every flow passable, nothing anyone would describe to a friend.

These skills put that discipline back in the loop, on demand:

- **Focal** keeps a single screen focused—*one screen, one purpose.*
- **Compass** keeps a journey navigable—*never lost.*
- **Flywheel** keeps the value you earned from leaking away—*earn the second visit.*
- **Soul** gives the happy path moments worth remembering—*never boring.*

More will follow, each targeting a craft that speed tends to leave behind.

## One skill, one job

Each skill is deliberately narrow. It addresses one defined design problem, follows one focused workflow, and has a clear boundary.

Focal handles the structure of a screen. Compass handles the structure of a journey. Flywheel handles what happens across the whole relationship. Soul handles the moments that make it memorable. None of them tries to become an all-purpose product design system.

This keeps each skill simple to understand, invoke, test, and improve. It also makes the collection composable: use one skill when that is all the problem requires, or combine several without turning any individual skill into a sprawling set of instructions.


## Skills

| Skill | What it does |
|-------|--------------|
| [**focal**](./focal) | One screen, one purpose. Declutters and structures app/dashboard screens through three disciplines—Information Architecture, Progressive Disclosure, and Visual Hierarchy. Build new screens or review existing ones. |
| [**compass**](./compass) | Never lost. Guides multi-screen flows and navigation through three disciplines—Orientation, Path Economy, and Continuity. Build new flows or review existing ones. Pairs with Focal (single screens). |
| [**flywheel**](./flywheel) | Earn the second visit. Growth and retention: finds where a product loses the users it already earned, across four ordered plays—Trust, Friction, Wins, and Emotion. Diagnose a leak or build a stage. |
| [**soul**](./soul) | Never boring. Delight, placed: sorts every beat of the happy path into three tiers—Expected stays functional, Elevated adds craft to the small things, Net-New rebuilds the 2–3 biggest moments entirely. Search a product or build a moment. |

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
