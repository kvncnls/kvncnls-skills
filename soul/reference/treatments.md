# Treatments—the three tiers

The path sort assigns every beat a **tier**—its verdict. A build designs the **rungs**—the full range for one beat, floor to target—so the caller can land anywhere on it without re-briefing. Same three names, two uses: the tier is where a beat ends up; the rungs are the steps a build lays out getting there.

## Expected—the obvious version

The fully functional execution a competent team ships without thinking hard. Standard pattern, standard copy, standard feedback.

**Expected is real work, not a strawman.** It must be shippable, because the beats that must simply work—load-bearing convention, high stakes, anywhere addition taxes the task—end here as the final answer, on purpose. Getting Expected right is also the precondition for the other tiers: an Elevated treatment of a broken interaction is polish on a defect.

**The test:** nothing missing, nothing added. A user relies on it without noticing it.

Examples of the register: a standard signup form, a clear confirmation toast, a conventional dashboard layout, a plain progress bar, a system-default notification.

## Elevated—the same moment, executed with visible care

Nothing new is introduced. The existing thing, done at a grade users can feel even when they cannot say why: hierarchy sharpened, copy in the user's words, motion that explains, feedback that names what changed, an empty state that starts the work, a wait that shows the work.

**Elevated is the anti-boring tier.** It spreads to every beat whose ceiling allows it—craft survives repetition, so distributing it raises the whole path without exhausting anyone. Concentration is for Net-New; distribution is for craft.

**The test:** describe the treatment in one sentence—if the sentence needs a new noun (a new feature, a new surface, a new mechanic), it is not Elevated, it is Net-New wearing modest clothes.

Examples of the register: the confirmation that states the amount and the running total instead of "Done"; the upload that shows filenames processing instead of a spinner; the form whose labels anticipate the next question; the settle animation that gives a completed payment weight.

**On `every-run` and high-stakes beats, Elevated is also the ceiling**—it raises quality without spending novelty, so it survives repetition and never competes with reassurance.

## Net-New—an entirely new experience

An entirely new experience in place of the old one—not the same moment executed better. Elevated asks how well the moment can be executed; Net-New asks what the moment could be instead. A new mechanic, surface, or artifact that makes the moment itself a reason to talk about the product.

**The test:** it could not be mistaken for a competitor—or for the moment it replaced.

Examples of the register: a live visualization where a table was assumed; a personalized artifact worth keeping (a year-in-review, a printable record, a shareable result card); an interactive demo where static onboarding was assumed; a progress mechanic that accumulates something users check voluntarily.

**Net-New ships only on the 2–3 chosen moments, never more.** It spends surprise, and surprise concentrates—spread thinner, none of it clears the threshold of memorable. (In a build, the Net-New rung still gets designed for any beat whose ceiling allows it—ideation is free; the ration is on shipping.) Two rules keep the tier honest:
- **It must survive its frequency.** A Net-New mechanic on an every-run beat must be useful on the 50th run, not clever on the first. If it is only clever, move it to a `once` or `recurring` beat.
- **It must be worth keeping, not just worth noticing.** The strongest Net-New treatments produce an artifact or capability the user returns to; the weakest produce a reaction and then a chore.

## The levers

What treatments are actually made of. Every lever carries its own failure mode—both columns matter.

| Lever | Used well | The failure mode |
|---|---|---|
| **Speed** | the response so fast it reads as attention; the strongest every-run lever there is | none—speed does not decay, which is why it ranks first |
| **Feel** | weight, physics, and settle that make interaction tactile | motion that delays the action it decorates |
| **Language** | copy in the user's words, at the moment's temperature; the highest-leverage lever per hour spent | charm before clarity; a voice that jokes at tense moments |
| **Anticipation** | the field pre-filled, the next step staged, the default that shows the product was paying attention | guessing wrong confidently; anticipation that removes control |
| **Continuity** | picking up exactly where the user left off, visibly | claiming to know the user better than the relationship supports |
| **Ceremony** | sequence and pacing that give a rare moment weight—reserved for `once` and milestones | ceremony on routine actions; the 12-second animated unboxing of a weekly report |
| **Accumulation** | progress that visibly builds into something owned—streak-free, pressure-free | streaks and guilt; accumulation that punishes absence |

**Sound is opt-in and off by default.** Meaning never depends on it.

## Repetition-proof design

What survives the 50th viewing, in order of durability:

1. **Speed**—never decays. The fastest thing in the category is a signature by itself.
2. **Feel**—physics reads as quality indefinitely; nobody tires of a door that closes well.
3. **Anticipation**—being known stays pleasant as long as it stays accurate.
4. **Useful variation**—content that reflects real state (this week's number, this run's result) is different every time for free.
5. **Cosmetic variation**—a rotating copy pool reads as alive for a while; the pool is always smaller than it looks. Last resort, small doses.

What decays: jokes, confetti, celebration sounds, surprise of any kind, mascot appearances, animated sequences longer than the action they follow. All of these are `once`-class material or cut.

## Proportionality

Feedback intensity matches the size of the moment, and high stakes reorder the sequence:

- **Routine completion**—confirm clearly, offer the next step. No more.
- **Meaningful progress**—name what changed, show the accumulation, restrained motion.
- **Major milestone**—ceremony earned: a designed pause, a summary, an artifact.
- **High-stakes success**—reassurance, records, and control **before** any feeling. The user confirms their money moved safely before anything celebrates. Calm outperforms excitement everywhere the user has something to lose.

Over-celebrating the routine reads as juvenile and burns trust in every future celebration; under-playing the milestone reads as indifference. Both are Proportion failures in the scorecard, and they are the same failure: intensity decided by habit instead of by the moment.

## The accessibility floor

No rung ships below it: treatments honor `prefers-reduced-motion` with a complete non-animated equivalent, meaning never depends on color, motion, or sound alone, focus and keyboard paths survive the treatment, and copy stays legible at the moment's reading pace—a 2-second toast cannot carry a 12-word sentence.
