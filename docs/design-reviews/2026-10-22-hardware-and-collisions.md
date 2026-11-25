# TV06+ fixed — collision recheck + hardware added (2026-10-22)

Saved as a new version of "TV06+ fixed". Follows [2026-10-18-tv06plus-fixes](2026-10-18-tv06plus-fixes.md) and [2026-10-19-screw-list](../build/2026-10-19-screw-list.md).

## Collision sweep
The sweep covered all 295 bodies, including the panels, skirts and electronics that weren't checked before.

### Fixed
- **Duplicate extrusion:** a second copy of "2020 Frame 660FL" was nested inside Top_Panel and fully overlapped the real one. Deleted.
- **Front-right skirt corner:** this group was shifted (+0.5 X, +0.37 Y) and has been moved to mirror the front-left. It covers Side_Skirt:2, CenterCap:1, Foot (2) and its FootAccent, FrontSkirt:1, Diffuser:2, the HDMI mount and the HDMI housing. This also cleared the right Z motor hitting the front skirt.
- **Rear-left skirt:** Side_Skirt:3, CenterCap (1) and Component416 were 0.2 mm outboard. Moved.
- **Foot:3** was offset 0.13/0.07/0.18 mm. Realigned.
- **Foot accents:** three of them sat 0.91 mm up inside their feet. Moved flush.
- **Rear fan skirt** was 0.09 mm into its neighbours. Centred.
- **Right upper rod brace** was 0.1 mm into the frame. Mirrored from the left.
- **Door (Clacky) panel** went 11 mm into the bottom rail and could only go 6 mm. Trimmed 5.3 mm off the bottom edge.
- **Bottom_Inner_Panel:** the rear Z mount cutout was widened.
- **Bottom_Panel_Electronics:** the front-right foot accent cutout was widened.

### Still open (design decisions)
- **X rail offset:** the MGN12 X rail holes are 5 mm off the X-extrusion slot centre (Z 44.5 vs 39.5), so the rail screws hit solid aluminium.
- **IEC module:** the C14 module intersects the rear skirt wall (2,300 mm³).
- **Rear fans:** both fans intersect the Rear_Cnter-Fans duct.
- **HDMI mount:** about 17 mm wider than the front-skirt gap on each side.
- **Midspan clips:** their pockets are 1 mm shallower than the corner clips, so the panels overlap every midspan clip by 1 mm.
- **Door corners:** the blind-joint screw heads touch the door panel corners.
- **Right front skirt:** the M2 self-tapping screw heads touch the right Z stepper.
- **Blind-joint access holes:** only modeled at a few heights on the vertical extrusions.
- **Earlier flags still apply:**
  - Z motor and A/B motor screw lengths
  - holes that miss their T-slots (hinges, latch, XY joints)
  - the bed plate has no tapped holes
  - the electronics panel has no holes for the OpenGrid tiles

## Hardware added
499 parts in a new top-level component, "Printer Hardware (generated)". The Dragon Burner toolhead is excluded.

| Part | Qty |
|---|---|
| Screws (from the hole analysis) | 243 |
| M5x10 BHCS frame blind joints (frame, door frame, bed tee) | 33 |
| M3x8 SHCS + T-nut on the MGN12 X rail | 11 |
| T-nuts | 133 |
| M3 heat-set inserts | 59 |
| Hex and nyloc nuts | 20 |

- **Z motor screws:** modeled as M3x40. That's still only about 1.4 mm of thread; the fix is still needed.
- **Accuracy:** the hardware is simplified geometry (cylinders and hex prisms). Expect small overlaps where threads engage.
