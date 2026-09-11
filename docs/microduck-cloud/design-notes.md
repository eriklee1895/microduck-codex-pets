# MicroDuck Cloud design notes

MicroDuck Cloud is the first deliberately transformed MicroDuck theme in the archive. The design keeps the real robot's identity cues—single camera lens, exposed black actuators, yellow/lavender feet, and the thin nearly closed flat mechanical bill—but makes the silhouette shorter, wider, and cloud-integrated for a Codex pet.

## Character brief

- Make the head oversized and puffy, with cloud lobes integrated into the shell.
- Use a very short neck, broad rounded belly, stubby limbs, and close-set feet.
- Keep the expression sleepy and a little unbalanced, as if a tiny robot is trying to stay planted while looking around.
- Use a flat-vector mascot treatment: bold dark outlines, cream/sky-blue/lavender color blocks, and restrained cel shading.
- Keep the original MicroDuck bill recognizable: two thin, flat, nearly parallel plates; never turn it into a rounded duck beak.

## Animation brief

Generate a Codex v2 atlas with nine standard activity rows and two eight-frame look rows. Ground the motion in the hardware: short waddles, soft compression, small head-led gaze changes, mechanical neck bends, and subtle balance corrections. Keep the lower belly, hips, and feet registered. The 16 look directions are clockwise from `000` up through `090` right, `180` down, and `270` left; the diagonals should interpolate rather than become independent character redraws.

## Generation constraints

Use a flat pure `#00FF00` background for source strips, one complete centered pose per invisible slot, generous padding, and no scenery, shadows, labels, guide marks, detached cloud effects, or extra props. Extract and register frames deterministically at 192×208, then remove chroma-edge contamination before writing a lossless RGBA WebP atlas.

## Iteration note

The final look-row repair explicitly constrained `292.5`, `315`, and `337.5` to remain on the viewer's left/up-left arc. In those poses the bill tip stays to the viewer's left of its hinge while the blue rear panel stays on the right/back side. This preserves a readable clockwise loop and the flat-bill identity at pet size.
