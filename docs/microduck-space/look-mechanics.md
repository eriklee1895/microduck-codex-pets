# MicroDuck Space look mechanics

## Natural motion

MicroDuck Space is a short, wide astronaut MicroDuck with a rigid rounded head shell, an integrated helmet ring, a very short articulated neck, a padded suit torso, an attached backpack-like shoulder casing, stubby arms, and planted yellow/lavender boots. The boots, hips, lower torso, and chest porthole form the stable lower-body anchor. The neck actuators lead the gaze, then the helmeted head yaws or pitches in small mechanical increments; the spacesuit makes a restrained counter-settle so the little astronaut looks careful rather than weightless or rubbery.

The single physical camera lens and blue eyelid remain mounted in the face panel and move with the head as one construction. The thin, flat, nearly closed yellow two-plate mechanical bill is rigidly attached to the head's lower edge and follows the head; it must stay shallow and never become a rounded duck beak or open mouth. The helmet ring, backpack casing, chest porthole, joints, arms, and boots remain physically attached. Nothing floats, detaches, or becomes a space-themed overlay.

## Cardinal pose families

- `000` up: boots, hips, and suit torso stay registered; the short neck extends slightly and the helmeted head pitches toward the top edge. The lens and flat bill rise together inside the ring.
- `090` screen-right: the head and face panel yaw toward the viewer's right edge; the bill tip and lens move to the right side of the head center. The backpack casing becomes more visible behind the opposite shoulder while the torso remains planted.
- `180` down: the neck compresses and the helmeted head pitches toward the bottom edge. The flat bill stays shallow and the lens drops beneath the eyelid; the boots and chest porthole remain anchored.
- `270` screen-left: the head and face panel yaw toward the viewer's left edge; the bill tip and lens move to the left side of the head center. The backpack and rear helmet ring remain attached on the opposite side.

Diagonal cells interpolate evenly between these cardinal families. The head, lens, eyelid, and bill carry the main direction signal; the neck and helmet ring follow as a rigid mechanical assembly, while the suit and backpack use only small physically plausible follow-through. Never rotate the whole sprite, slide an iris across a fixed eye white, detach the ring, or turn the porthole into a floating symbol.

## Continuity and motion budget

Keep the boots, hips, lower suit, and chest porthole on a stable baseline. Adjacent 22.5-degree steps should change head yaw/pitch, lens, eyelid, bill angle, and neck bend by similar visual amounts. The `157.5 -> 180` and `337.5 -> 000` joins must preserve helmet scale, bill thickness, backpack attachment, and lower-body registration without a visible snap.
