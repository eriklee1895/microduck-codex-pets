# MicroDuck Cloud look mechanics

## Natural motion

MicroDuck Cloud is a short, wide, cloud-cased biped with a rigid head shell, a very short articulated neck, a broad soft-looking belly casing, stubby limbs, and feet close together. The feet, hips, and lower belly are the stable anchor. The neck actuators bend first, then the rounded cloud head yaws or pitches in small mechanical increments. The single physical camera lens and its blue upper eyelid stay mounted to the face panel and move with the head; they are not floating eyes. The thin, flat, nearly closed yellow/orange two-plate bill is rigidly attached to the head's lower edge and follows the head as a shallow line. Cloud puffs remain integrated into the head, belly, shoulder, and limb casings; no loose cloud effect is part of the look motion.

The natural expression is a sleepy little robot trying to look around without losing balance: the head and short neck lead, the wide belly makes a tiny counter-settle, and the stubby legs remain planted. The yellow/lavender feet are body-mounted and do not change identity across directions. Never rotate the whole sprite, slide a pupil across a fixed eye white, open the bill, detach a cloud lobe, or add weather symbols.

## Cardinal pose families

- `000` up: feet, hips, and belly stay registered; the short neck extends slightly and the puffy head pitches toward the top edge. The sleepy lens and thin bill rise together.
- `090` screen-right: the rounded cloud head yaws toward the viewer's right edge; the bill tip and lens cross to the right side of the head center. The short neck bends modestly while the belly remains anchored.
- `180` down: the neck compresses and the head pitches toward the bottom edge. The flat bill stays shallow and points down; the lens sits low beneath the eyelid.
- `270` screen-left: the cloud head yaws toward the viewer's left edge; the bill tip and lens cross to the left side of the head center. The lower body remains stable and the cloud casing does not spin independently.

Diagonal cells interpolate evenly between these families. The puffy head silhouette, sleepy eyelid, thin flat bill, cloud-belly casing, and short limbs keep their proportions. No direction should become a generic round duck, a floating cloud, or a front-facing idle copy.

## Continuity and motion budget

Keep the lower belly, feet, and hips on one stable baseline. Let head yaw/pitch and the short neck carry most of the direction signal, with only small belly/limb counter-settle. Adjacent 22.5-degree steps should use similar visual increments; the `157.5 -> 180` and `337.5 -> 000` joins must not introduce a visible scale pop, bill-thickness change, cloud-lobe jump, or body teleport.
