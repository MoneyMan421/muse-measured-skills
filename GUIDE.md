# Measured Skills for Muse — The Guide

**Every skill here has a dated proof it still works.**

*By Collin. A measurement record, not a warranty.*

> Unofficial community project. Not affiliated with, endorsed by, or
> operated by Meta. "Muse" is Meta's product name, used here only to
> say what these skills are for.

## Who this is for

Anyone who uses skills with Meta's Muse personal agent — or writes
skills for any AI agent — and wants to answer one question about each
skill they rely on: *does this skill still work, and when was that
last checked?*

## The problem

A skill in a catalog is a markdown file someone asserts is good.
Nothing about the file tells you whether its instructions still
produce the right result today, whether anyone has ever run it end
to end against a real artifact, or what it got wrong when they did.
Platforms change, models change, and a skill that worked when it was
written can quietly stop working — drift is silent, and it does not
announce itself.

The usual response is a bigger catalog. This repo makes the opposite
trade: few skills, each one carrying its evidence.

## The system — what a measured skill is

A skill counts as *measured* in this repo when it carries four
things:

1. **A task.** A portable markdown file (`SKILL.md`, the open Agent
   Skills format — YAML frontmatter, then instructions) that says
   what the skill does and when to use it.
2. **An output check.** The skill states, inside its own text, how
   its output gets verified — a measurement, a count, a
   comparison — in numbers, not adjectives.
3. **A dated Proof Record.** Every verification run is published in
   `records/` as a Proof Record (the open format from Open Door
   Standards), stating what was measured, by what method, on what
   date, and what it showed.
4. **A drift / re-verification status.** `STATUS.md` carries every
   skill's public verification count, last verified date, and
   result. Re-verification runs on a cadence: when the Muse
   platform changes, and on a monthly sweep. A skill whose check
   fails is marked failed in the open, not quietly dropped.

The standing rules, copied from the repo:

- Specs in numbers, with tolerances, stated before measuring.
- Measure the deliverable itself — the file, the page, the pixels —
  never a record *about* it.
- Two verifications before a result is called reference-grade; one
  is a claim with a date on it, two make it a reference.
- Failures and inconclusive results are published, not hidden.
- Counts are verified by counting the items, never by adding one to
  the last published figure.

If a skill here has no record yet, its page says so in plain words.
Nothing in the repo is described as verified until a dated record
says it is. That distinction is the product.

### The five seed skills

Each seed skill is adapted from the author's own working Muse
skills, and each carries its check inside its own text:

| Skill | Task | Output check, as the skill states it |
|---|---|---|
| avatar-media-verification | Verify a generated avatar, portrait, character sheet, or character video before claiming it is done | Open the saved file itself and count what is in it; sheet cells verdicted one by one at readable size; a clip's opening sampled at 0, 0.5, 1, 1.5 and 2 seconds; crop safety judged on the circular crop. A tool result, list, or thumbnail never substitutes for the opened file |
| blink-closure-verification | Verify a character's blink and eye closure against numeric specs | Closure fraction measured in pixels at 0%, 50% and 100%; at 100% closure the residual gap is ≤2% of eye width and the lid must not cut into the eyeball; at 50% the lid edge sits at 50% ±5% of the eye's open height; for paired eyes, the sync error between the two eyes at the same frame |
| animation-motion-measurement | Verify generated or procedural animation against numeric motion targets | Frame-by-frame tracking of the actual video at a locked frame rate, the tracker itself verified by an overlay drawn onto the real frames; every test reported as target, measured, verdict |
| delegated-work-checkpointing | Keep delegated, long-running agent work recoverable | One named deliverable file per delegation; before any result is reported, the deliverable is opened and every required section confirmed present, with checkpoint entries covering every piece claimed as done |
| guide-store-publishing | Sequence a guide launch across two or more online stores | A listing counts only after its live product page has been opened and the title, price, visibility, and buy path confirmed from the page itself; a listing in test mode, or with no payout path, is reported as not sellable |

To use a skill with Muse today: open the skill's folder, copy its
`SKILL.md` content into a chat with your Muse, and tell it to
follow the skill for the task at hand.

### Copy this for your own skills

The pattern lifts out of this repo unchanged:

1. Write the skill so it **states its own check** — what gets
   measured or counted, against what target, with what tolerance.
2. When you run it, **write the spec of record down before you
   look at the output** — the targets first, the artifact second.
3. **Publish the run** as a dated record: the artifact's identity
   (a hash, where the format supports it), the method, the
   per-element results, and the verdict — including the failures.
4. **Keep a status page**: one line per skill — verification
   count, last verified date, result — updated in the same pass
   as the record itself.
5. **Re-run on a trigger and on a cadence**, and let a failed
   check show as failed.

## The worked example — verification run 001

The first public verification run in this repo measured the skill
`avatar-media-verification` against a real artifact: the author's
active Muse avatar. It ran on **2026-11-27**, following the skill's
own procedure, and its Proof Record
(`MMS-001-AVATAR-MEDIA-VERIFICATION-2026-11-27`, Proof Record
format version 0.3.0) is published in `records/run-001/` alongside
the run log and the machine-readable measurements.

**What was pinned before measuring.** The skill text under test
was the published `SKILL.md` (repo commit 5856c36d; file sha256
`03c8aef93a075706fd54afd5f8f02d2fe1c17af0624474093bbff2c86fd90d27`).
The artifact was a WebP image, 1600×1600 (sha256
`bd53b63ee938cbe9160a615869dd03bbe3d6ff29975d045351ca448adfafbbe6`).
The spec of record — 9 elements, written down before the file was
opened — required, among other things: exactly 1 figure; crown and
halo both fully inside the frame; exactly two golden wing pairs,
at rest; a slim gold ear cuff with one circuit-blue crystal drop
on the character's right ear.

**How it was measured.** The saved file itself was opened and
inspected directly — not a thumbnail, not a tool listing. Figures
and wings were counted with visual grounding on the opened file;
details were checked in enlarged crops taken from the file's own
pixels (face, top of frame, both ear regions). The side conversion
was stated out loud, as the skill requires: in this front view,
the character's right is the viewer's left.

**The result, as measured on 2026-11-27:**

- **8 of 9 elements present as specified; 1 present but deviating;
  0 absent.**
- Figure count: 1, counted. Crown and halo: complete in frame,
  the halo's topmost point at y≈31/1000 of frame height, with
  white margin above.
- **The deviation — `wing_pairs`, described exactly:** exactly 4
  golden wings were counted, so the count (2 pairs) and the
  colour (gold, with circuit-blue traces) were exact. But the
  upper pair was spread wide and raised to shoulder height, with
  tips reaching the left and right frame edges; the lower pair
  angled downward. The upper pair was not folded or lowered, so
  the spec's "at rest" qualifier was not met as the pixels showed
  it. In the Proof Record this element is scored a fail against
  the target "Exactly TWO golden wing pairs, at rest."
- Two observations were recorded outside the spec's claims: a
  second, matching blue crystal drop hangs at the character's
  left ear (no cuff there), which the spec neither claims nor
  forbids; and the upper wing tips reach the frame edges, where
  the spec's no-crop requirement covers crown and halo only.
- One caveat was recorded with the medallion element: a round
  gold medallion bearing an "M" emblem is present at centre
  chest as specified, but whether the M device *is* the team's
  merged logo is not determinable from pixels alone.

**The followability verdict.** The skill could be followed as
written — its core discipline (open the file itself, count in the
opened file, name the file, report only what was seen) was
followed exactly and produced the verdict above. But the run
recorded the skill text itself as **insufficiently specific for
spec-conformance verification of a single still avatar**, with
3 gaps:

1. **No still-portrait spec-check procedure.** The skill's
   portrait guidance is "open the file and count what is in it,"
   surrounded by workflow sections. The per-element verdict
   taxonomy used in the run (present as specified / present but
   deviating / absent) came from the run brief, not the skill.
2. **The side-conversion rule is buried in the sheet section.**
   "Convert sides out loud" appears only under character-sheet
   checks; checking a right-ear feature on a portrait required
   importing the rule across sections.
3. **Qualitative terms are untestable as written.** "At rest,"
   "slim" and "luminous" carry no definitions or pass tests in
   the skill. The wing deviation rests on the plain meaning of
   "at rest" and is flagged for the record-keeper's ruling for
   exactly this reason.

The Proof Record's own verdict line states the outcome as
**VERIFIED WITH FINDINGS**, and records that a revision of the
skill is owed before verification #2. The Proof Record body
hash is
`299fc0d8b492d66b649400058b72a7784a92eff1065b507c7fed503fcc5bda38`.

## How to run a verification yourself, step by step

This is the procedure run 001 followed, generalised from the
repo's method so you can run it on any skill — yours or one from
this repo:

1. **Pin the skill text.** Record which version you are testing
   (a commit, a file hash) so the verdict attaches to an exact
   text, not a moving target.
2. **Write the spec of record first.** List every element or
   target the output must meet, in numbers with tolerances,
   *before* you open the artifact.
3. **Identify the artifact exactly.** Name the file; record its
   format, dimensions, and hash where you can.
4. **Open the deliverable itself.** Inspect the file, the page,
   the pixels — never a thumbnail, a listing, or a summary of it.
5. **Count and measure in the opened artifact.** Count the items
   themselves; check details at a size where they are readable.
6. **Convert sides out loud** for any side-dependent element:
   state the view, and which side of the subject is which side
   of the frame, before you verdict it.
7. **Verdict element by element.** For each spec element:
   present as specified, present but deviating (deviation
   described exactly), or absent. No blanket "looks fine."
8. **Record observations outside the spec.** Anything the
   artifact shows that the spec neither claims nor forbids gets
   written down, so the record is complete, not tidy.
9. **Judge the skill text as well as the artifact.** Note every
   place the skill was impossible, contradictory, or too vague
   to test against — undefined terms are findings, not shame.
10. **Publish the record, dated, whatever it shows.** Update the
    status page in the same pass. A failing element is an entry,
    not a veto on publishing.

## Failure modes — and what this system does not claim

- **One run is not reliability.** Run 001's own Proof Record
  states its limitation plainly: one artifact, one run, one day
  verifies that the skill produced a correct verdict on *this*
  artifact; it does not establish the skill's reliability across
  artifacts. Under the repo's rule, a second verification is
  required before the skill is reference-grade — and as of this
  guide, that second verification has not run.
- **A verdict can turn on an undefined term.** The wing-pose
  failure in run 001 rests on the plain meaning of "at rest,"
  which the spec leaves undefined. The system records the basis
  and flags it for a ruling; it does not pretend the term was
  precise.
- **Pixels have limits.** Some claims are not determinable from
  the artifact alone — run 001 could confirm a medallion's
  presence, position and form, but not whether its emblem is the
  team's merged logo. The record says so instead of guessing.
- **A followable skill can still be an insufficient one.** Run
  001's skill passed its core discipline and still carried
  3 recorded specificity gaps. "Verified with findings" is a
  real outcome here, not a euphemism for passed.
- **No record means not verified.** Four of the five seed skills
  are in the author's daily use and have no public verification
  record yet. Daily use is not verification, and this repo does
  not describe them as verified.
- **This is a measurement record, not a warranty.** A dated
  record says what was measured, by what method, on that date.
  It does not promise the skill will produce the same result
  tomorrow, on a different artifact, or in different hands.

## Status, stated plainly

As of 2026-11-27, per the repo's own `STATUS.md`:

- **5 seed skills** are published: avatar-media-verification,
  blink-closure-verification, animation-motion-measurement,
  delegated-work-checkpointing, guide-store-publishing. All five
  are in the author's daily use.
- **1 public verification run is published:** run 001,
  avatar-media-verification, 2026-11-27 — verified with
  findings (artifact 8/9 elements as specified; 3 skill-text
  gaps recorded).
- **4 skills have 0 public verifications — pending:**
  blink-closure-verification, animation-motion-measurement,
  delegated-work-checkpointing, guide-store-publishing. In the
  numbering of the runs still owed, these are runs 002–005.
- No skill in the repo is yet reference-grade: that takes two
  verifications, and the highest count any skill carries today
  is 1.

## Claims & sources

Every quantitative claim in this guide, and the source it
traces to. Source paths are relative to the repo
(`records/run-001/` files are the run-001 evidence set).

| # | Claim | Value | Source |
|---|---|---|---|
| 1 | Seed skills published | 5 | README.md; STATUS.md |
| 2 | Skills in the author's daily use | 5 of 5 | STATUS.md |
| 3 | Public verification runs published | 1 (run 001) | STATUS.md; records/run-001/proof-record.json |
| 4 | Skills with public verifications pending | 4 | STATUS.md |
| 5 | Runs still owed (numbering) | 002–005 | STATUS.md (4 skills at 0 public verifications, pending) |
| 6 | Run 001 date | 2026-11-27 | records/run-001/proof-record.json (`measured_at`); records/run-001/RUN-LOG.md |
| 7 | Proof Record format version | 0.3.0 | records/run-001/proof-record.json (`standard.version`) |
| 8 | Run 001 record ID | MMS-001-AVATAR-MEDIA-VERIFICATION-2026-11-27 | records/run-001/proof-record.json (`record_id`) |
| 9 | Published skill source commit | 5856c36d | records/run-001/RUN-LOG.md; records/run-001/proof-record.json (`subject.version`) |
| 10 | Skill file sha256 | 03c8aef93a075706fd54afd5f8f02d2fe1c17af0624474093bbff2c86fd90d27 | records/run-001/RUN-LOG.md; records/run-001/measurements.json |
| 11 | Artifact format and dimensions | WebP, 1600×1600 | records/run-001/measurements.json (`artifact.format`); records/run-001/RUN-LOG.md |
| 12 | Artifact sha256 | bd53b63ee938cbe9160a615869dd03bbe3d6ff29975d045351ca448adfafbbe6 | records/run-001/measurements.json; records/run-001/RUN-LOG.md |
| 13 | Spec elements in run 001's spec of record | 9 | records/run-001/RUN-LOG.md (locked spec of record) |
| 14 | Elements present as specified | 8 of 9 | records/run-001/measurements.json (`overall_outcome`); records/run-001/proof-record.json (`verdict`) |
| 15 | Elements present but deviating | 1 (wing_pairs) | records/run-001/measurements.json; records/run-001/RUN-LOG.md |
| 16 | Elements absent | 0 | records/run-001/RUN-LOG.md (overall outcome) |
| 17 | Figures counted in the artifact | 1 | records/run-001/measurements.json (figure_count) |
| 18 | Golden wings counted | 4 = 2 pairs | records/run-001/measurements.json (wing_pairs); records/run-001/RUN-LOG.md |
| 19 | Halo topmost point | y≈31/1000 of frame height | records/run-001/RUN-LOG.md; records/run-001/proof-record.json (crown_and_halo_fully_in_frame) |
| 20 | Observations recorded outside the spec | 2 | records/run-001/RUN-LOG.md; records/run-001/measurements.json (`observations_outside_spec`) |
| 21 | Skill-text specificity gaps recorded | 3 | records/run-001/proof-record.json (`verdict.deficits`); records/run-001/RUN-LOG.md (followability notes) |
| 22 | Proof Record body sha256 | 299fc0d8b492d66b649400058b72a7784a92eff1065b507c7fed503fcc5bda38 | records/run-001/proof-record.json (`body_sha256`) |
| 23 | Verifications required for reference-grade | 2 (one is a claim) | README.md (house rules); STATUS.md |
| 24 | Re-verification cadence | On Muse platform changes, plus a monthly sweep | STATUS.md |
| 25 | Clip-opening sample points (avatar-media-verification) | 0, 0.5, 1, 1.5, 2 seconds | skills/avatar-media-verification/SKILL.md |
| 26 | Blink residual-gap tolerance at 100% closure | ≤2% of eye width | skills/blink-closure-verification/SKILL.md |
| 27 | Blink lid-edge tolerance at 50% closure | 50% ±5% of the eye's open height | skills/blink-closure-verification/SKILL.md |

*By Collin. A measurement record, not a warranty.*
