# kvncnls-skills

A collection of [Claude Code](https://claude.com/claude-code) skills for product design, by Kevin Canlas. Each skill is a self-contained folder of Markdown—no build step, no dependencies.

## Why these exist

Vibe coding made building software fast and easy—describe a feature, watch it appear. But building fast and designing well are different skills, and the second hasn't kept up. I keep seeing the same thing: features stacked on features, screens accumulating widgets, flows sprouting steps, with no one asking whether the app still hangs together.

The first casualties are the quiet disciplines that make software feel effortless—information architecture, visual hierarchy, progressive disclosure, navigation, spatial awareness. They rarely block a release, so they get skipped, and the app ends up technically working but overwhelming to use. It usually breaks in one of two ways:

- **Within a screen**—it does too much. Widgets compete, nothing is clearly primary, everything shows at once.
- **Between screens**—the journey becomes a maze. Too many steps, no sense of where you are, no clean way back.

These first two skills put that discipline back in the loop, on demand:

- **Focal** keeps a single screen focused—*one screen, one purpose.*
- **Compass** keeps a journey navigable—*never lost.*

More will follow, each targeting a craft that speed tends to leave behind.

## Skills

| Skill | What it does |
|-------|--------------|
| [**focal**](./focal) | One screen, one purpose. Declutters and structures app/dashboard screens through three disciplines—Information Architecture, Progressive Disclosure, and Visual Hierarchy. Build new screens or review existing ones. |
| [**compass**](./compass) | Never lost. Guides multi-screen flows and navigation through three disciplines—Orientation, Path Economy, and Continuity. Build new flows or review existing ones. Pairs with Focal (single screens). |

## Install a skill

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

## License

[MIT](./LICENSE) © 2026 Kevin Canlas.
