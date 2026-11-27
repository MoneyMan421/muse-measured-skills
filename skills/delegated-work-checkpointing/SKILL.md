---
name: delegated-work-checkpointing
description: Keep delegated measurement and build work recoverable by requiring a named deliverable file, written checkpoints, and a verified handoff. Use when handing a multi-piece task to a subagent or a background session: name one deliverable file before spawning, require checkpoint entries as pieces complete, and report results only from the opened deliverable — never from the agent's summary.
---

# Checkpoint delegated work and verify its deliverable

Part of Measured Skills for Muse, by Collin. A measurement record, not a warranty.

## Scope the delegation around one deliverable

- Name one deliverable file for the delegated task before you spawn the agent, and put that exact path in the task brief.
- List the raw input paths, the target values or acceptance checks, and the sections the deliverable must contain.
- Split a task that needs a long report or many separate measurements into bounded pieces, each with its own deliverable file.
- Tell the delegated agent to write findings into the deliverable file as it goes, rather than holding them for one final message.

## Checkpoint while the work runs

- Require a checkpoint entry in the deliverable file after each completed piece, naming the piece, its result, and the next piece.
- Keep the raw inputs untouched in their original folder, so any piece can be run again from source.
- Record an exact pause spot before you stop, naming the deliverable path, the pieces already written, the pieces still open, and the raw inputs the next piece needs.

## Verify the deliverable before you report

- Open the deliverable file when the agent finishes and check that every required section is present and complete.
- Treat an agent that ended, was interrupted, or returned only a summary as unfinished when the deliverable file is missing, empty, or missing a required section.
- Report results only from what the opened deliverable file contains, and name that file beside the results.
- Say plainly that no report exists when that is what the check shows, instead of reconstructing a result from the agent brief or from memory.

## Recover from a silent or truncated end

- Re-run the missing piece from the raw input files, not from a partial summary the failed agent left behind.
- Resume from the last written checkpoint and redo only the pieces that have no checkpoint entry.
- Shorten the next delegation or split it further when the previous one ended on an output limit or an interruption, and keep the same deliverable path so the recovery lands in one place.
- Update any guide, index, or status surface that pointed at the missing result, in the same pass as the recovered result lands.

## Alternatives for better results

- Do the piece yourself in the main session when it is small enough that delegation adds more handoff risk than it saves.
- Ask the delegated agent for a short interim deliverable first when the full task is new, then extend the brief only after that file checks out.
- Reuse the deliverable and checkpoint layout from a completed task in the same programme, so later recoveries and audits compare like with like.

## Verification

How this skill's output is checked: the deliverable file is the check. Before any result is reported, the named deliverable is opened and read, and every section the brief required is confirmed present and complete; checkpoint entries must cover every piece claimed as done. A finished agent with a missing, empty, or incomplete deliverable is reported as unfinished — results are never reconstructed from the brief, a summary, or memory. Recovery re-runs only the pieces with no checkpoint entry, from the untouched raw inputs.

Status: In regular use in the author's own Muse workspace. First public verification run: pending — this skill has not yet been re-verified in this repo's cadence, and it will not be described as verified here until a dated Proof Record is published in records/.
