# kvncnls-skills

A collection of [Claude Code](https://claude.com/claude-code) skills for product design and ui/ux design, by Kevin Canlas. Each skill is a self-contained folder of Markdown—no build step, no dependencies. The intent behind each Skill is to complete one job instead of turning them into "everything Skills". This makes it clearer and simpler to use.

## Why these exist

Vibe coding made building software fast and easy—describe a feature, watch it appear. But building fast and designing well are different skills, and the second hasn't kept up. I keep seeing the same thing: features stacked on features, screens accumulating widgets, flows sprouting steps, with no one asking whether the app still hangs together.

The first casualties are the quiet disciplines that make software feel effortless—information architecture, visual hierarchy, progressive disclosure, navigation, spatial awareness. They rarely block a release, so they get skipped, and the app ends up technically working but overwhelming to use. It usually breaks in one of two ways:

- **Within a screen**—it does too much. Widgets compete, nothing is clearly primary, everything shows at once.
- **Between screens**—the journey becomes a maze. Too many steps, no sense of where you are, no clean way back.

These first two skills put that discipline back in the loop, on demand:

- **Focal** keeps a single screen focused—*one screen, one purpose.*
- **Compass** keeps a journey navigable—*never lost.*

More will follow, each targeting a craft that speed tends to leave behind.

## One skill, one job

Each skill is deliberately narrow. It addresses one defined design problem, follows one focused workflow, and has a clear boundary.

Focal handles the structure of a screen. Compass handles the structure of a journey. Neither tries to become an all-purpose product design system.

This keeps each skill simple to understand, invoke, test, and improve. It also makes the collection composable: use one skill when that is all the problem requires, or combine several without turning any individual skill into a sprawling set of instructions.


## Skills

| Skill | What it does |
|-------|--------------|
| [**focal**](./focal) | One screen, one purpose. Declutters and structures app/dashboard screens through three disciplines—Information Architecture, Progressive Disclosure, and Visual Hierarchy. Build new screens or review existing ones. |
| [**compass**](./compass) | Never lost. Guides multi-screen flows and navigation through three disciplines—Orientation, Path Economy, and Continuity. Build new flows or review existing ones. Pairs with Focal (single screens). |

## Install (Claude Code)

Clone the collection, then point Claude Code at the skill you want (here, `focal`):

```bash
git clone https://github.com/kvncnls/kvncnls-skills.git
# Symlink so it's available in every session and edits stay in sync:
ln -s "$(pwd)/kvncnls-skills/focal" ~/.claude/skills/focal
```

Prefer an independent copy, or scope it to one project?

```bash
cp -R kvncnls-skills/focal ~/.claude/skills/focal     # independent copy, all projects
cp -R kvncnls-skills/focal <project>/.claude/skills/  # one project only
```

Restart Claude Code, then the skill's slash command (e.g. `/focal`) is available. Each skill's own `README.md` has its full usage.

## Using these outside Claude Code

The skills are plain Markdown, so they work in any AI coding agent, not only Claude Code. Each skill has a single-file **bundle** in [`bundles/`](./bundles)—the spine plus every reference in one document—for tools that can't load a multi-file skill folder.

- **Codex (CLI)**—append a bundle to your project's `AGENTS.md`, which Codex loads automatically: `cat bundles/focal.md >> AGENTS.md`.
- **ChatGPT**—create a Custom GPT and paste a bundle into *Instructions*, or upload it as a *Knowledge* file. A ChatGPT Project works the same way (add it to the project's files).
- **Cursor / Windsurf / Cline**—drop a bundle in as a rules file, e.g. `cp bundles/focal.md .cursor/rules/focal.md`.

The bundle is self-contained—no folder structure or slash command needed. On Claude Code, ignore the bundle and install the skill folder above for on-demand loading and `/focal`.

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
