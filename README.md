# Measured Skills for Muse

**Skills for Meta's Muse personal agent — measured, not just listed.**

Skill catalogs for AI agents count in the thousands now. Almost
none of them can answer a simple question: *does this skill still
work, and when was that last checked?* A skill in a catalog is a
markdown file someone asserts is good. This repo is the opposite
trade — few skills, each one carrying its evidence:

- **A check.** Every skill states how its output gets verified —
  a measurement, a count, a comparison — in numbers, not
  adjectives.
- **A record.** Every verification run is published as a dated
  Proof Record (the open format from
  [Open Door Standards](https://github.com/MoneyMan421/open-door-standards)),
  in `records/`, where anyone can read what was measured, by what
  method, and what it showed.
- **A status.** [STATUS.md](STATUS.md) carries every skill's
  last verified date and result, and gets re-run on a cadence:
  when the Muse platform changes, and on a monthly sweep. A skill
  whose check fails is marked failed in the open, not quietly
  dropped.

If a skill here has no record yet, its page says so in plain
words. Nothing in this repo is described as verified until a
dated record says it is. That distinction is the product.

*By Collin. A measurement record, not a warranty.*

> Unofficial community project. Not affiliated with, endorsed
> by, or operated by Meta. "Muse" is Meta's product name, used
> here only to say what these skills are for.

## Start here — the starter path

New to skills? Work through the seed set in this order; each one
teaches the habit the next one uses.

1. **avatar-media-verification** — never claim a generated image
   or video is right until you have opened the file and counted
   what is actually in it.
2. **blink-closure-verification** — verify a character's blink
   and eye closure against numeric specs, frame by frame.
3. **animation-motion-measurement** — verify generated or
   procedural animation against numeric motion targets by
   measuring frames.
4. **delegated-work-checkpointing** — keep delegated, long-running
   agent work recoverable: named deliverables, written
   checkpoints, verified handoffs.
5. **guide-store-publishing** — sequence a multi-store digital
   guide launch so caps, approval windows and payout states are
   checked before anything is counted as sellable.

## How to use a skill

A skill is a portable markdown file (`SKILL.md`, the open Agent
Skills format — YAML frontmatter, then instructions). To use one
with Muse today, open the skill's folder, copy its `SKILL.md`
content into a chat with your Muse, and tell it to follow the
skill for the task at hand. When Muse gains a native skill
library, these files are already in the right shape to keep
there — the author's own Muse keeps its copies as working
skills, which is where every skill in this repo started.

## The house rules

- Specs in numbers, with tolerances, stated before measuring.
- Measure the deliverable itself — the file, the page, the
  pixels — never a record *about* it.
- Two verifications before a result is called reference-grade;
  one is a claim, two make it a reference.
- Failures and inconclusive results are published, not hidden.
- Counts are verified by counting the items, never by adding
  one to the last published figure.

## Where this sits

This repo is the Muse-user shelf of a larger measured stack:
[Proof Record](https://github.com/MoneyMan421/open-door-standards)
(the record format), [DriftWatch](https://github.com/MoneyMan421/driftwatch)
(the drift checker that re-runs suites against pinned baselines),
and the full Measured Skills pack — the guides-as-skills set for
coding agents, sold on Gumroad — for anyone who wants the deep
versions. The free skills here are complete as they stand; the
paid pack is the larger library, not the missing half of these.

## Status

Seeding. The first five skills are adapted from the author's own
working Muse skills; their first public verification runs are
being scheduled, and STATUS.md will show the dates as they land.
Nothing here is pre-claimed.
