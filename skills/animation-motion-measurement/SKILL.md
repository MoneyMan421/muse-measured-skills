---
name: animation-motion-measurement
description: Verify generated or procedural animation against numeric motion targets by measuring frames, not by watching. Use when a speed, period, fall time, squash value, or turn count must be checked against a stated target at a locked frame rate, and when a procedural render is needed to prove a guide's numbers are reachable before spending a generated video test on them.
---

# Measure animation motion from frames

Part of Measured Skills for Muse, by Collin. A measurement record, not a warranty.

## Lock the frame rate and targets before you test

- Write down each target as a per-second value before you generate or render anything.
- Lock one frame rate for the guide and the test, and state it in every report.
- Rescale any per-frame value to the locked rate before you compare it with a measurement.
- Treat a number from a panel, a counter, or a prompt as a claim until the frames confirm it.

## Measure the frames instead of eyeballing the motion

- Extract every frame from the test video and track the moving feature frame by frame, for example with Python, numpy, and PIL colour segmentation.
- Verify the tracker by drawing it onto the actual frames, and report a number only when the overlay shows the tracker on the right object.
- Record the measured value beside the target value for each test and give a pass or fail verdict per test.
- Save the measurement file with the method, the frame rate, the tracker check, and the measured-against-target values.
- Do not report a speed, a period, a fall time, a squash value, or a turn count from watching the video or from reading an on-screen counter.
- Treat an on-screen counter as unconfirmed when it advances irregularly instead of once per cycle.

## Render numbers procedurally and treat generated video as a look test

- Render a numbers test procedurally from the guide formulas when the claim is a number.
- Use generated video only as a look test for appearance and general movement.
- Do not use tempo compensation by asking for double the speed: in observed test rounds it overshot rotation while other motions stayed at the same tempo.
- Keep the procedural result and the generated video result in separate reports, so a look test never stands in for a numbers test.

## Report measured against target

- Report each test as target, measured, and verdict in plain text.
- Name the video file and the measurement file you used for every reported number.
- Say plainly when a test has no measurable motion in the tracked signal, instead of assigning a value from the prompt.
- Own a wrong earlier claim by naming the measured value that replaced it and offering the procedural remake.

## Alternatives for better results

- Use the procedural render first to confirm the guide numbers are reachable before you spend a generated video test on them.
- Use `avatar-media-verification` (in this repo) to confirm every expected character appears, and this skill to confirm the motion numbers.
- Ask the user to choose the procedural route when a numeric target matters, and keep generated video for look only.
- Reuse the measurement script and frame extracts across rounds, so later rounds compare against the same tracker and the same frame rate.

## Verification

How this skill's output is checked: every reported number must come from frame-by-frame tracking of the actual video, with the tracker itself verified by an overlay drawn onto the real frames — never from watching the video, from a prompt, or from an on-screen counter. Each test is reported as target, measured, verdict, at the locked frame rate, naming the video file and the measurement file; the measurement file (method, frame rate, tracker check, measured against target) is saved with the result. A test whose tracked signal shows no measurable motion is reported as having none, not assigned a value.

Status: In regular use in the author's own Muse workspace. First public verification run: pending — this skill has not yet been re-verified in this repo's cadence, and it will not be described as verified here until a dated Proof Record is published in records/.
