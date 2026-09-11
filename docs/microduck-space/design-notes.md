# MicroDuck Space design notes

MicroDuck Space is a structural astronaut transformation of MicroDuck, not a recolor. It keeps the real robot's recognizable identity cues—single camera lens, exposed black actuators, yellow/lavender feet, and the thin nearly closed flat mechanical bill—inside a compact space-explorer silhouette.

## Character brief

- Make the character short, wide, and slightly overstuffed, with an integrated cream/navy helmet ring around the rounded head shell.
- Use a puffy white spacesuit torso, simple circular chest porthole, and compact navy backpack-like shoulder casing.
- Keep stubby arms, close-set boots, and a careful low-gravity balance personality.
- Use a flat sticker-vector treatment: bold dark outlines, cream-white/navy/sky-blue/lavender/warm-yellow color blocks, and restrained cel shading.
- Preserve the original MicroDuck bill as two thin, flat, nearly parallel plates; never turn it into a rounded duck beak or open mouth.

## Animation brief

Generate a Codex v2 atlas with nine standard activity rows and two eight-frame look rows. Ground the motion in the robot construction: short waddles, careful hover jumps, suit compression, head-led gaze changes, mechanical neck bends, and small balance corrections. Keep the boots, hips, lower suit, and chest porthole registered. The 16 look directions run clockwise from `000` up through `090` right, `180` down, and `270` left.

## Generation constraints

Use a flat pure `#00FF00` background for source strips, one complete centered pose per invisible slot, generous padding, and no scenery, shadows, labels, guide marks, detached space effects, or extra props. Extract and register frames deterministically at 192×208, then remove chroma-edge contamination before writing a lossless RGBA WebP atlas.

## Iteration note

The row-10 layout was regenerated with compact uniform height so the down-to-left-to-up-left family fits the shared row-9 registration scale. The final 292.5, 315, and 337.5 poses keep their bill tips on the viewer's left side and form a continuous up-left arc into `000`.
