# New Skill: Compass

**Compass** is a Claude Code skill that helps you design and untangle the *flows* of an app, dashboard, or tool—the multi-screen journeys like onboarding, checkout, or setup—so the user is never lost on the way to what they came to do.

Think of it as **wayfinding signage for a journey**. The way good signage in a building answers "where am I, where do I go next, and how do I get back out?" at every junction, Compass asks "at this step, does the user still know where they are and how to escape?"—and tells you which steps to cut, where to add a way back, and what to carry across.

Where its sibling **Focal** sharpens a single screen, Compass guides the path *between* screens. *Focal is within a screen; Compass is between them.*

### The problem it solves

Developers build fast and tend to disregard information architecture, layouts, visual hierarchy and progressive disclosure. What ends up happening is journeys turn into mazes. A checkout balloons to seven steps; the back button wipes everything you typed; a "resume" email link dumps you at step one with an empty cart; a wizard traps you in a modal with no exit. The user gets lost or stranded, and abandons. Compass is a discipline for preventing and fixing that.

### The core idea: Never Lost

At every step of a flow, the user should be able to answer three questions without thinking: **Where am I? How far is left? How do I get back, or out?** The test: name the destination—*"This flow gets the user from \_\_\_ to \_\_\_."* If it needs the word "and," it's two flows wearing one coat.

### How it gets there—three disciplines

1. **Orientation** *(the load-bearing one)*—at every step: position and progress ("Step 2 of 3"), a real Back, and a way out. This is the core "never lost" lever; nothing should ever trap the user.
2. **Path Economy**—the *fewest honest steps* to the destination. Cut redundant screens and merge round-trips—but never shorten the path by hiding a cost or skipping a protection (that's a dark pattern, not economy).
3. **Continuity**—context and state survive the seams between screens. No "remember the code from the last screen," Back never wipes your work, and a deep link lands you *in context* instead of at the start.

### Two ways to use it

- **Build**—describe a flow you want to design, and it hands back a clean **Flow Spec**: the destination, the fewest honest steps, how each step keeps the user oriented, what carries across the seams, and a checklist.
- **Review**—describe an existing flow (or point it at the screens / a prototype), and it scores it 0–4 on each discipline, lists the problems worst-first, and gives you the **top 3 fixes**.

### It's smart about flow types

Not every flow is a straight line, so it adapts:

- a **linear** flow (one path, like checkout or a wizard),
- a **branching** flow (the path forks on a choice),
- a **hub-and-spoke** flow (a dashboard you leave and return to—"back to the hub" is sacred),
- an **open-ended** journey (a feed or search—there's no fixed end, so "how far is left" doesn't apply; it just keeps you from getting lost in the space).

It also adjusts for **who's traveling**—experts want skips and shortcuts; first-timers want guardrails.

### What it deliberately is *not*

It's not about a single screen's layout (that's Focal), and not about colors, fonts, motion, copy, or writing code. It doesn't plan your whole app's sitemap, and it's scoped to apps/dashboards, **not** marketing or landing pages.

**In one sentence:** tell Compass about a flow, and it tells you the fewest honest steps to the destination and how to keep the user oriented at every one—so they never get lost.
