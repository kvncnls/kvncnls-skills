# New Skill: Focal

**Focal** is a Claude Code skill that helps you design and declutter the screens of an app, dashboard, or tool—so each screen does *one job clearly* instead of turning into a crowded mess.

Think of it as an **editor for screens**. The way a good editor asks "what is this paragraph actually saying?" and cuts the rest, Focal asks "what is this screen actually *for*?"—and tells you what to cut, group, hide, or emphasize.

### The problem it solves

Developers build fast and tend to disregard information architecture, layouts, visual hierarchy and progressive disclosure. What ends up happening is screens get crowded over time. A dashboard sprouts ten widgets, a settings page tries to do five things at once, a form asks for everything up front. The user glances, feels overwhelmed, and misses the one thing that mattered. Focal is a discipline for preventing and fixing that.

### The core idea: One Screen, One (Primary) Purpose

Every screen should exist so the user can do **one main thing**. The test: finish the sentence *"This screen exists so the user can \_\_\_."* If you need the word "and," the screen is doing too much.

### How it gets there—three disciplines

1. **Information Architecture**—what belongs on the screen and how it's grouped. (Don't cram two unrelated jobs onto one screen.)
2. **Progressive Disclosure**—show what's needed *now*; tuck the rest behind "more" or "advanced." Keep the choices facing the user at any moment small (~4 things). This is the main anti-clutter lever.
3. **Visual Hierarchy**—make the most important thing visually *loudest*, so the eye instantly knows where to look.

### Two ways to use it

- **Build**—describe a screen you want to design, and it hands back a clean spec: the purpose, what's on the screen, what's hidden, what's most prominent, and a checklist.
- **Review**—paste a screenshot or point it at a screen, and it scores the screen 0–4 on each discipline, lists the problems worst-first, and gives you the **top 3 fixes**.

### It's smart about screen types

Not every screen is a single-task screen, so it adapts:

- a **task** screen (one job, like checkout),
- a **hub** (like a home screen—its job is to *route* you, so many links is fine),
- an **exploration** screen (like a feed—abundance is the point).

It also adjusts for **who's using it**—experts can handle denser screens than first-timers.

### What it deliberately is *not*

It's not about colors, fonts, animation, or writing code—only about *structure and what to show, hide, or emphasize*. And it's scoped to apps/dashboards, **not** marketing or landing pages.

**In one sentence:** tell Focal about a screen, and it tells you what that screen is really for, what to cut, and what to make prominent—so it ends up simple and clear.
