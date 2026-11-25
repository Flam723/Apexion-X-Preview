# TV06+ fixes — 2026-10-18

Saved as a new file **"TV06+ fixed"** in TV TV06Plus-NG_CM. The original "TV06+" is unchanged. Companion to [2026-10-18-tv06plus-design-check](2026-10-18-tv06plus-design-check.md).

## Changed
- **Left front Z stack mirrored to the right side** (about X = −167.5 mm):
  - Left stepper: +2.09 X, +0.42 Y, −2.0 Z
  - Left motor mount: −0.11 X, +0.52 Y, −2.0 Z
  - Spacer_x6 (3) and (1)(2): +1.99 X, +0.52 Y, −2.0 Z
  - Cover_x3 (2): −0.11 X, +0.52 Y, −2.0 Z
  - Front_Linear_Rod_Left: −0.11 X, +1.32 Y
  - Left_Lead_Screw: −0.11 X, +0.87 Y
  - Linear_Rod_Bed_Brace_Left: +0.39 X
  - Result: the lead-screw/motor clash and the mount/frame clash are gone. Rod-in-mount is now 1.5 mm³, the same as the right side.
- **Rear Z rods** moved −0.3 X, −0.2 Y to center them on the Ø8.3 bores in Motor_Mount_Rear. Bottom ends shortened 13 mm (−450 → −437, the bore floor), so the rods are now 429.3 mm long. The mount interference is gone (was 673 mm³ each).
- **Right A/B motor mounts** (upper and lower) moved −1.0 Y so they sit flush on the rear-right upright like the left ones. The frame clash is gone (was 302 and 55 mm³).
- **Right upper A/B mount:** the XY rod pocket was 1 mm shallower than the left mount's. The floor was offset 1 mm deeper (Y 476 → 477) to match. **This changes the printed part. Re-export its STL.**
- **Left idler bearing insert** moved +0.73 X, −0.99 Y to mirror the right one. Overlap is now 17.8 mm³, same as the right (was 77.8).
- **Deleted:** the duplicate "Linear_Rod_Bed_Brace_Rear 2-hole" (kept the 3-hole version, which takes the drag-chain end), and the hidden Z_Bed_Right_Hardware(Mirror) and GE5C(Mirror) inside Z_Bed_Left.

## Report corrections
- M4 Knurled Nut 1 was not misplaced. Its nut body sits under the front-right bed screw; the odd position came from a stale occurrence bounding box.
- 2020 Frame 495RB/495TR are not too long. The 0.37 mm bump is the modeled tap cone in the end hole.

## Left as is (by design, symmetric, or modeling artifacts)
- Drag chain link touching the rear 3-hole brace (7 mm³).
- Lead screws through the bed-brace nut holes (2–3.5 mm³, the same on all three).
- Front A/B NEMA bosses in the lower mounts (11.5 mm³, now both sides).
- Heater modeled inside the bed plate.
- Old toolhead parts stacked inside Carriage_Mount.
- XY joint and idler-slot overlaps (symmetric).
- Fasteners modeled without holes.
- Hidden skirt diffusers, foot and cable-anchor hardware (kept as optional parts).
- Suffixed component names and stray sketch geometry.
- Panels and skirts were not interference-checked.
