---
name: blink-closure-verification
description: Verify blink and eye closure against numeric specs after any face edit, new blink asset, or character sheet with closed-eye cells. Use when a character's eyes, face proportions, or lid mechanism have changed and closure must be re-measured in pixels at 0%, 50%, and 100% before the edit is called done.
---

# Verify blink and eye closure against numeric specs

Part of Measured Skills for Muse, by Collin. A measurement record, not a warranty.

A blink is a number before it is an impression. This skill keeps the measurement discipline: spec the blink in numbers, measure the actual frames, report target against measured.

## When this skill applies

- Any face edit on a character rig or model — bigger or moved eyes, a face slider change, a proportion revision — invalidates blink keys authored against the old geometry. The face edit is the trigger: re-verify closure in the same pass, before the edited face is called done (sweeps recur on a trigger, not a calendar).
- Any new blink or lid asset: shape keys, a blink cycle in an animation test, a character sheet with closed-eye cells.
- Any character with a device or prosthetic eye, always: a device eye may close by a different mechanism than a flesh lid (for example, an iris-lid sweep), and the sync rule below applies to it.

## Spec the blink in numbers before measuring

- State three closure targets before rendering: 0% (open), 50% (half blink), 100% (closed).
- Express the closure gap RELATIVELY — as a percentage of the eye's own width — never as a bare millimetre figure. A millimetre tolerance without the head's scale attached is an adjective wearing a number's clothes.
- Working tolerances (defaults, adjustable per character): at 100% closure the residual gap is ≤2% of eye width, and the lid must not cut into the eyeball anywhere (overclosure is a fail, worse than a hairline gap). At 50% the lid edge sits at 50% ±5% of the eye's open height.
- Name the fragile lock in the brief before generating: which eye, which lid mechanism (flesh lid over a ball, or a device eye's iris-lid sweep).

## Measure the deliverable, never the record of it

- Measure from the actual frames or the actual sheet cells — extract the frames, locate the lid edge and the eye's open height in pixels, and compute the closure fraction per frame. A panel, a key value, or a prompt claim is a claim until the pixels confirm it.
- Check all three states, not only full closure: a blink that nails 100% and slurs 50% fails the half blink, which is where bad keys actually show.
- For paired eyes, measure BOTH eyes and report the sync error: the difference in closure fraction between the two eyes at the same frame. Example from the author's operation: a character whose device eye is a brass iris-lid and whose other eye is natural — the two blink in sync, same fraction, same frame; halfway is halfway on both sides.
- A device eye keeps its own construction in every gaze state: its housing stays present, with no skin, no sclera, no lashes on the device; its only lid is its own mechanism. The natural eye carries the natural features. Verify per cell on sheets, per frame on clips.

## Repair route when closure fails

- Rebuild or re-derive the closure keys against the EDITED geometry — never hand-nudge the old keys toward the new face and call it fixed.
- After any rebuild, re-measure all three states and the sync error from the new frames. The rebuild is a claim; the re-measurement is the result.
- Record drifts as references to build from: exact numbers, constructive language — but a key that misses its stated tolerance is reported as missing it.

## Report format

- Per test: target, measured, verdict — closure fraction at 0/50/100%, residual gap as % of eye width, overclosure yes/no, sync error for paired eyes.
- Name the file measured (clip, sheet, rig render) and the frame or cell for every number.
- File the result with the asset it verifies, in the same pass — a blink verification that lives only in chat does not exist for the next session.

## Related skills in this repo

- `animation-motion-measurement` — the frame-extraction and tracking method this skill's measurements build on.
- `avatar-media-verification` — confirm the character and eyes are present before measuring them.

## Alternatives for better results

- If an automated checker is ever built for this (measuring lid gap at 0/50/100% automatically), this skill's spec section is its requirements document — hand it over verbatim.
- For a quick look test, a generated blink clip can show the feel; the numbers still come from frame measurement, never from watching.

## Verification

How this skill's output is checked: the check is built into the method. Every blink verdict must trace to frames or sheet cells that were actually extracted and measured in pixels — closure fraction at 0/50/100%, residual gap as a percentage of eye width, overclosure yes/no, and sync error for paired eyes — with the measured file and the frame or cell named for every number. A verdict reported from watching a clip, from a panel value, or from a prompt claim is not a verification under this skill. After any repair, all three states and the sync error are re-measured from the new frames; the re-measurement, not the rebuild, is the result.

Status: In regular use in the author's own Muse workspace. First public verification run: pending — this skill has not yet been re-verified in this repo's cadence, and it will not be described as verified here until a dated Proof Record is published in records/.
