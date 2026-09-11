# MicroDuck look mechanics

## Natural motion

MicroDuck is a small rigid-shell biped with exposed articulated neck and leg joints. When it looks around, the lower body, hips, and planted feet remain the stable anchor. The neck actuators bend and the rigid head shell yaws or pitches in small mechanical increments. The camera lens and face panel stay physically mounted in the head; they do not become floating googly eyes. The thin, flat two-plate orange bill is a rigid head-mounted part and follows the head shell as one compact flat profile. It stays almost closed in every direction, with only the same narrow seam visible in the canonical base.

The motion should read as a real robot orienting its sensor: neck leads the turn, head shell follows, the flat bill follows with the same rigid attachment, and the lower torso performs only a small counter-settle. Do not rotate the entire sprite, slide a pupil on a fixed eye white, open the bill, or invent a new face layer.

## Cardinal pose families

- `000` up: feet and hips stay planted; the neck extends slightly and the head shell pitches toward the top edge. The flat bill angles upward with the head, with more lower head/neck mechanism visible.
- `090` screen-right: the head shell yaws toward the viewer's right edge; the flat bill tip and front rim clearly cross to the right side of the head center. The neck bends subtly to support the yaw while the feet and hips stay registered.
- `180` down: the neck compresses and the head shell pitches toward the bottom edge. The bill points downward as a thin flat line; upper shell/back surfaces become slightly more visible.
- `270` screen-left: the head shell yaws toward the viewer's left edge; the flat bill tip and front rim clearly cross to the left side of the head center. This is the inverse of `090`, with the same lower-body anchor and no whole-sprite flip.

The diagonal poses interpolate evenly between adjacent cardinal families. The head turn/pitch and neck bend use a small, nearly uniform step for every 22.5 degrees. The bill remains a thin rigid plate attached to the head; it does not widen, gape, detach, or change material. The single physical camera lens stays mounted to the face panel and changes orientation only through the head's yaw/pitch.

## Continuity and motion budget

Keep feet/base and lower torso registration stable across the 16-cell loop. Let head yaw/pitch and neck articulation carry most of the direction signal. No adjacent pair may introduce a larger mouth change, body scale jump, or neck bend than the declared cardinal transition. The wrap transitions `157.5 -> 180` and `337.5 -> 000` must be one normal interpolation step, not a reset to a new pose family.
