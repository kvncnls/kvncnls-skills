# Behavioral contracts

[`behavioral-contracts.yml`](./behavioral-contracts.yml) contains representative prompts and evidence conditions that guard the collection’s decision boundaries. Each fixture states behavior an agent should produce and behavior it must reject.

These are contract fixtures, not snapshot prose. A human or an agent-evaluation harness can run each scenario against the named Skill and judge the result semantically. The repository verifier checks that every fixture has evidence, expected behavior, and rejected behavior, while static assertions guard the corresponding source instructions.

The fixtures concentrate on regressions that simple link or frontmatter checks cannot catch:

- contextual Focal density instead of a hard item quota;
- finite and open-ended Compass journeys;
- platform-appropriate retreat behavior;
- targeted versus full Flywheel scoring;
- Soul restraint, Readiness, and zero-Net-New outcomes;
- cross-scale deduplication in Product Judgement;
- the intentionally uncommon `4/4` threshold.
