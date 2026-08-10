# Moments—where the budget goes

A moment is a beat on the happy path that earns the Net-New tier—an entirely new experience, not a better version of the old one. This file is how you find the 2–3, rank them, and sort everything else into Elevated or Expected.

## The frequency classes

Frequency is destiny for a treatment—it decides what a moment may carry before anything else does.

| Class | What it is | What it may take | Why |
|---|---|---|---|
| `once` | first-run beats: first impression, first success, setup completion | one-shot expressive treatment—storytelling, sequence, ceremony | it plays once, so it may spend everything |
| `recurring` | weekly-to-monthly rhythm: a report ships, an invoice is paid, a milestone lands | mid intensity, with variation—the 30th arrival must still read as alive | familiar enough to expect, rare enough to feel |
| `every-run` | every session: open, navigate, compose, save, send | repetition-proof craft only—speed, feel, anticipation, useful variation | novelty decays with repetition; speed does not |

**The 50th-viewing test:** before treating any beat, say its frequency out loud and imagine the treatment on its 50th appearance. Confetti fails at 3. A 200ms save that used to take 2 seconds never fails.

## The archetypes

Eight places soul is usually won or lost. Skeleton positions refer to the 7-beat map in [SKILL.md](../SKILL.md).

| Archetype | Skeleton position | Frequency | Candidate feelings | What usually goes wrong |
|---|---|---|---|---|
| **The first impression** | beats 1–2 | once | curiosity, recognition, relief | generic welcome copy; a form where an experience should be |
| **The first success** | beats 5–6, first pass | once | capability, pride | the product's biggest moment announced by a toast |
| **The wait** | beat 5, when work takes >1s | varies | anticipation, confidence | a spinner where evidence of work should be |
| **The effort peak** | beat 4 at its hardest | varies | momentum, control | the hardest step is also the most sterile |
| **The ending** | beat 6 | varies | completion, relief, pride | it stops instead of landing—the most neglected surface in most products |
| **The milestone** | recurring passes | recurring | progress, accumulation | either silent, or identical the 40th time |
| **The handoff** | the artifact that leaves the product | recurring | pride to the sender, sense to the receiver | an export nobody would show anyone |
| **The return** | re-entry after absence | recurring | continuity, being known | a cold start where a "welcome back" state should be |

Three boundary notes. *The first success* is the beat where first value lands—Flywheel's term for the event that changes the user's situation; if the product loses people before this beat, that is a leak, and leaks go to [Flywheel](../flywheel) before treatments. *The return* is expressive treatment on re-entry—whether re-entry restores context at all is Flywheel's continuity question; Soul makes a working return felt, not a broken one work. *The ending* keeps its rank even when it is every-run—a session ending that merely stops is the most common miss on any path—but an every-run ending takes repetition-proof levers only; ceremony belongs to rare endings.

## Selection—the bar a moment must clear

Rank candidates by **reach × memory**: how many users hit this beat, times how likely the beat is to be what they remember. Peak-end weights the scale—the emotional peak and the ending hold memory far beyond their share of the path, which is why the ending can outrank the first impression even though fewer people arrive there. **When two candidates tie, take the later one**—peak-end weights endings, so the later beat holds more memory per user who reaches it.

Then interrogate the shortlist:

1. Where would a generic execution actively hurt—cost trust, cost the story users tell?
2. What is public-facing—screenshotted, demoed, shared, judged by people who are not users yet?
3. Where does the user's effort peak? High effort is high emotional energy; treatment there converts strain into momentum.
4. Which beats carry the product's distinctive claims? Those are the strongest Net-New candidates.
5. What would marketing show? If nothing on the path is showable, that is the finding.

**Take the top 2–3 as Net-New. Never more.** The fourth rebuilt moment does not add memory; it subtracts significance from the first three. Everything below the line takes **Elevated** where its ceiling allows craft that pays, and **Expected** otherwise—recorded either way, because the receipt is what separates restraint from neglect.

**Reasons a beat stays Expected** (any one suffices):
- **Load-bearing convention**—checkout, save, undo, back. Muscle memory is the feature; novelty there costs comprehension and pays nothing.
- **Every-run frequency with no repetition-proof lever available**—if speed and feel are already at ceiling, standard is correct.
- **High stakes, calm already present**—money movement, health data, and irreversible actions want reassurance and records before anything else. Where the calm, clear version already exists, standard is the treatment; where it does not, calm *is* the treatment (see proportionality in [treatments.md](treatments.md)). Trustworthy restraint is an emotional choice, not the absence of one.
- **Below the line**—a fine Net-New candidate that lost to a better one; it takes Elevated craft instead, and loses nothing but the rebuild. Two is a budget, not a quota.

## The dumping grounds

The canonical list. These are where delight traditionally goes—chosen because failing there is cheap, which is exactly the problem: cheap failure means no reach, and no reach means the work is unseen or seen by a frustrated user at the worst possible moment.

- **404 and error pages**—reached by accident, read in annoyance.
- **Error mascots and cheerful failure copy**—wit at the moment the user is most tense reads as mockery.
- **Easter eggs and hidden games**—found by almost nobody, by definition off every path.
- **Release notes bits**—read by a rounding error of the user base.
- **Splash-screen and loading-copy jokes on every-run loads**—novelty on repeat decays into noise; if the wait is real, show the work instead.

**The two moves when the sweep finds delight in a dumping ground:**
1. **Relocate the effort.** The craft is real; the placement is wrong. Name the on-path beat that deserves it.
2. **Fix the frequency, not the feeling.** An error state frequent enough to be worth delighting is a bug to fix, not a moment to elevate—route it to [Flywheel](../flywheel) (a leak) or [Focal](../focal) (a screen).

One honest edge: a 404 that carries real traffic—dead links shared socially, a renamed content library—is not a dumping ground. It is an entry beat for those users. Treat it as recovery: state what happened, one clear path to the likely destination, zero jokes. The rule was never "404s don't matter"; it was "placement follows reach."
