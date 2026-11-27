---
name: avatar-media-verification
description: Verify a generated avatar, portrait, character sheet, or character video by opening the saved file and counting what is actually in it before claiming it is done. Use after any generation, swap, or avatar change; for cell-by-cell character sheet checks against locked specs; for dense sampling of a clip's opening seconds; and for checking that a reframed image survives a circular avatar crop.
---

# Verify avatar and character media

Part of Measured Skills for Muse, by Collin. A measurement record, not a warranty.

## Show the concept before any change

- Generate the concept image first and show it in chat before you change a portrait or an avatar.
- Wait for the user to approve the exact version before you apply it.
- Hold back any earlier version that no longer matches the approved look and say that you are holding it back.
- Flag baked-in text or labels in the concept and ask whether to keep them or make a clean version.

## Open the saved file and count what is in it

- Open the saved image file itself and look at the picture after every generation, swap, or avatar change.
- Count each expected character in the opened file and name any expected character that is missing.
- Treat a list, a picker, a tool result, or a thumbnail as unconfirmed until the opened file shows the same result.
- Check the listing where the avatar appears (for example, a Space listing) separately from the avatar file, because one can be right while the other is wrong.
- Remake the options when none of them contains every expected character, and say that picking a different option would not fix the gap.
- Watch the finished video from start to finish and confirm every expected character appears together in it.

## Sample the opening of a character clip densely

- Check a character clip at 0, 0.5, 1, 1.5 and 2 seconds before you take wider samples across the rest of the clip.
- Compare the character at each opening check for a shift in style, colour, gloss, face shape or proportions, and report any shift even when the character settles later in the clip.
- Do not call the opening clean from sparse samples that straddle the first two seconds, such as 0.5, 6 and 9 seconds alone.
- Report the opening verdict separately from the verdict for the rest of the clip, so a pass after 1 or 2 seconds does not hide a change inside the opening.
- Name the fragile lock for the character in the frame check report and say whether it held at every opening check, not only at the wider samples.

## Verify a character sheet cell by cell

- Write down the locked specs before you open the sheet, naming each fragile lock, each side-locked feature, the scale ratios and heights, and the palette targets.
- Open the sheet and check every cell on its own at a size where its details are readable, never giving a verdict from the whole-sheet thumbnail alone.
- Record a pass or a hold for each named cell and report the sheet as the set of its cell verdicts, so one failing cell is never hidden inside a whole-sheet pass.
- Convert sides out loud in the check, stating the character side and the viewer side for each view, because the character's right is the viewer's left in a front view.
- Compare each side-locked feature against the cited reference of record for that feature and flag any cell where it has swapped sides.
- Check that an artificial or asymmetric feature keeps its own construction in every cell, in every gaze direction and at every blink stage, with natural eye or skin features appearing only on the natural side.
- Hold a cell instead of passing it when the behaviour it shows is not defined yet, and say which definition is missing.
- Measure the colours in the pixels and compare them with any hex values printed on the sheet, treating the printed values as a claim that the measurement can overturn.
- Read every printed label, marker and footer against the locked specs and flag garbled text, wrong left or right markers, and numbers that contradict a locked height or ratio.
- Measure scale figures in pixels against the locked ratio, and prefer an exact composite built from passed figures when generated figures keep missing the ratio.
- Fix a single failing cell as a correction plate that sits beside the sheet, when regenerating the whole sheet would risk the cells that already passed.

## Reframe for the circular crop

- Reframe a wide scene so every expected character sits close to the centre before you offer avatar options.
- Check the reframed image as a tight circle, because the app crops the avatar to a circle.
- Move a character inward or remake the image when the circle would cut that character out.
- Tell the user plainly when a scene cannot survive the crop instead of claiming the wide version will work.

## Report only what you saw

- Report a portrait, avatar, or video as done only after the opened file confirms it.
- Name the file you opened and list the characters you saw in it.
- Own a wrong claim promptly, say exactly what the opened file shows, and offer the concrete remake.
- Stop and ask when the user sends a screenshot that contradicts your last claim, instead of repeating the claim.

## Alternatives for better results

- Use the finished video layout as the reference for the still avatar when the video already shows every character together correctly.
- Offer a close reframed version and a wide scene version when the user wants both the full scene and a crop-safe avatar.
- Ask the user to pick from remade options only after you have opened each option and confirmed it contains every expected character.

## Verification

How this skill's output is checked: the check is the method itself. No portrait, avatar, sheet, or video is reported as done until the saved file has been opened and inspected directly — characters counted in the opened file, sheet cells verdicted one by one at readable size, clip openings sampled at 0, 0.5, 1, 1.5 and 2 seconds, and crop safety judged on the circular crop rather than the wide frame. A tool result, a list, or a thumbnail never substitutes for the opened file, and every report names the file that was opened. If a claim turns out wrong against the opened file, the correction is reported from what the file actually shows.

Status: In regular use in the author's own Muse workspace. Public verifications: 1 — run-001, 2026-11-27 (records/run-001/): verified with findings. The run's artifact verdict was 8 of 9 spec elements present as specified (wing pose deviating); three specificity gaps in this skill's text were recorded in the run's Proof Record, and a revision is owed before verification #2. One verification is a claim with a date on it; two make it a reference.
