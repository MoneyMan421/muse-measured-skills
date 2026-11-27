# Run 001 — Public verification of avatar-media-verification

- Skill under test: `avatar-media-verification` (published text, MoneyMan421/muse-measured-skills @ 5856c36d)
  - SKILL.md sha256: `03c8aef93a075706fd54afd5f8f02d2fe1c17af0624474093bbff2c86fd90d27`
- Artifact: `~/workspace/avatars/avatar-1795717512128698295-0.webp`
  - sha256: `bd53b63ee938cbe9160a615869dd03bbe3d6ff29975d045351ca448adfafbbe6`
  - Format confirmed: WebP image (RIFF/WebP), real image bytes.
- Method: the skill's own procedure only. Applicable sections for a single still avatar image: "Open the saved file and count what is in it", "Reframe for the circular crop" (supplementary note), "Report only what you saw". The clip-sampling and character-sheet sections do not apply to a single still portrait (noted as not applicable, not skipped silently).

## Locked spec of record (written down before opening the file)

1. Exactly 1 figure (a single character, Mira).
2. Crown and halo BOTH fully inside the frame — nothing cropped at the top.
3. Exactly TWO golden wing pairs, at rest.
4. Hair luminous silver-white, in a braid crown.
5. Facial circuitry under the eyes only; forehead clean.
6. Golden glowing eyes.
7. Slim gold ear cuff with one circuit-blue crystal drop on her RIGHT ear (character's right; in a front view that is the viewer's LEFT — side conversion stated per the skill).
8. The team's merged logo present as a medallion on her chest.
9. Circuit-tree dress.

## Steps

- [x] Read the skill in full; recorded hashes of skill and artifact.
- [ ] Open the saved image file itself and inspect the picture.
- [ ] Count/check each of the 9 elements against the pixels; verdict each individually (present as specified / present but deviating / absent).
- [ ] Write measurements.json; record followability notes on the skill text.

## Measurement — what was done

- Opened the saved file itself with the file reader (1600×1600 WebP; the picture inspected directly, not a thumbnail or tool listing).
- Visual grounding count on the opened file: figures = **1**; distinct golden wings = **4**; halo topmost point at y≈31/1000; crown located on her head.
- Enlarged crops taken from the file's own pixels and read individually: face (circuitry, forehead, eyes, braid), top of frame (halo, orb, crown completeness), viewer's-left ear region, viewer's-right ear region.
- Side conversion, stated out loud per the skill: this is a front view, so **the character's right ear is on the viewer's left**.

## Per-element results (target vs measured vs verdict)

| # | Element | Target | Measured in the opened file | Verdict |
|---|---|---|---|---|
| 1 | Figure count | Exactly 1 figure (Mira) | 1 figure, counted (grounding = 1), single female figure centred; no other character | **present as specified** |
| 2 | Crown & halo in frame | Both fully inside frame, nothing cropped at top | Crown fully visible (gold, blue gems) with rainbow orb seated on top, complete; halo rings complete in top crop, topmost point y≈31/1000 with white margin above halo and orb | **present as specified** |
| 3 | Wing pairs | Exactly TWO golden wing pairs, at rest | Exactly 4 golden wings = 2 pairs (grounding = 4), gold with circuit-blue traces. BUT the upper pair is spread wide and raised to shoulder height, tips reaching the frame edges; the lower pair angles downward. The upper pair is not folded or lowered — the "at rest" qualifier is not met as the pixels show it | **present but deviating** (count and colour exact; pose qualifier not met) |
| 4 | Hair | Luminous silver-white, braid crown | Long luminous silver-white wavy hair; thick braided band of the same hair across the top of the head under the crown (face crop) | **present as specified** |
| 5 | Facial circuitry | Under the eyes only; forehead clean | Fine gold circuit traces on both cheeks directly under the eyes; forehead shows skin and freckles only, no circuitry | **present as specified** |
| 6 | Eyes | Golden glowing eyes | Both eyes golden/amber and visibly glowing | **present as specified** |
| 7 | Ear cuff, right ear | Slim gold ear cuff + one circuit-blue crystal drop on her RIGHT ear | On the viewer's-left ear (her right): gold cuff of linked slim bands wrapping the rim, chain drop ending in exactly one faceted circuit-blue crystal | **present as specified** (see observation A) |
| 8 | Logo medallion | Team's merged logo as a medallion on her chest | Round gold medallion at centre chest bearing an "M" emblem. Medallion present as specified; whether the M device IS the merged logo is not determinable from pixels alone — left to the record-keeper | **present as specified** (identity caveat recorded) |
| 9 | Dress | Circuit-tree dress | Cream-white gown, gold tree-and-root branching motif down torso and skirt interwoven with glowing blue circuit traces | **present as specified** |

## Deviations and observations — named exactly

- **DEVIATION (element 3):** the upper wing pair is spread wide and raised, not at rest. Count (2 pairs), colour (gold) and circuitry match; the pose qualifier does not, on the plain meaning of "at rest". The skill defines no pose test — see followability notes.
- **Observation A (element 7):** a second, matching blue crystal drop hangs at the character's LEFT ear (viewer's right), where no cuff is visible. The spec of record claims the cuff + one drop on the right ear and neither claims nor forbids a left-ear drop; recorded so the record-keeper can rule on it.
- **Observation B:** the upper wing tips reach the left/right frame edges. The spec's no-crop requirement covers crown and halo only; noted, not verdicted.

## Skill sections not applied, with reasons

- Clip-opening sampling (0–2 s): artifact is a still image — not applicable.
- Character-sheet cell checks: artifact is a single portrait, not a sheet — not applicable. (Its side-conversion rule was imported for element 7; see followability notes.)
- Circular-crop reframe: governs reframing before offering avatar options, not verification of an existing avatar file — not applied.
- "Check the listing where the avatar appears": no listing check was in this run's brief — noted, not performed.

## Followability notes on the skill text

Followed as written, exactly: open the saved file itself; count in the opened file; name the file; report only what was seen. No applicable instruction was impossible, contradictory, or wrong.

Where the skill was insufficient for this run:

1. **No still-portrait spec-check procedure exists in the skill.** Its portrait guidance is "open the file and count what is in it," surrounded by workflow sections (concept approval, sheets, clips, crop). The per-element verdict taxonomy used here (present as specified / present but deviating / absent) came from the run brief, not the skill. A verifier holding only the skill would know to look and count, but would have no prescribed way to structure a conformance verdict against a written spec.
2. **The side-conversion rule is buried in the sheet section.** "Convert sides out loud" appears only under character-sheet checks. The portrait path never mentions sides; checking a right-ear feature on a portrait required importing the rule across sections.
3. **Qualitative terms are untestable as written.** "At rest," "slim," "luminous" carry no definitions or pass tests in the skill, and the skill neither sanctions nor forbids plain-language judgement on them. The element-3 deviation rests on plain meaning and is flagged for the record-keeper's ruling for exactly this reason.

**Followability verdict:** the skill CAN be followed as written — its core discipline was followed exactly and produced this report — but it is **insufficiently specific for spec-conformance verification of a single still avatar**: the run succeeded because the brief supplied the spec and the verdict taxonomy the skill lacks. Whether "followable but insufficient" counts as a verification pass for the skill is the record-keeper's call; both halves of that finding are stated here so the call is made on the full evidence.

## Overall outcome

**8 of 9 elements present as specified; 1 present but deviating (wings — pose qualifier); 0 absent.** Two observations recorded outside the spec's claims (left-ear drop; wing tips at frame edges). Machine-readable results: `measurements.json` in this folder.

- [x] Open the saved image file itself and inspect the picture.
- [x] Count/check each of the 9 elements against the pixels; verdict each individually.
- [x] Write measurements.json; record followability notes on the skill text.
