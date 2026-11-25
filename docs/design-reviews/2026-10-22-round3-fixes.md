# TV06+ fixed — round 3 fixes (2026-10-22)

Saved as a new version of "TV06+ fixed". Resolves the "Still open" list in [2026-10-22-hardware-and-collisions](2026-10-22-hardware-and-collisions.md). The screw list spreadsheet was updated to match.

## Done
- **X rail:** the MGN12 rail, carriage and Dragon Burner moved −5 mm Z onto the X-extrusion slot centre (Z 39.5). The 11 rail screws now land in the slot. **The toolhead and nozzle are 5 mm lower, so check belt alignment and re-home Z.**
- **Z motor spacers:** Spacer_x6 is 30 → 28 mm (6 off). The motors and lead screws were raised 2 mm. M3x40 now gets about 3.4 mm of motor thread.
- **Blind joints:** Ø7.35 access holes are cut at all 33 joints. The door-panel corners are notched Ø10.5 around the 4 door-frame heads.
- **IEC inlet:** fixed by the designer.
- **Rear fans:** the duct is cut to fit both fans.
- **HDMI mount:** the real overlap was 0.57 mm (X 179.04–179.61), not 17 mm. The mount is trimmed to the front skirt.
- **Midspan clips:** all 7 are cut to their panels.
- **Right front skirt M2s:** 4 are M2x6 BHCS. 2 still touched the motor, so they are M2x6 FHCS in new countersinks. All clear the motor now.
- **A/B motors:** moved −1 mm Y to line up with the mount holes. The motor-to-lower-mount overlap dropped from 11.5 to 0.17 mm³.
  - The screws are **M3x30 SHCS**, 3 per motor.
  - The Ø6 counterbores in both upper mounts were deepened 1.8 mm (2.8 → 4.6 mm, floor Z 51.3 → 49.5). The head sits 1.6 mm below the face.
  - M3x30 now gets 5.0 mm of thread in the 5.46 mm motor hole, 0.46 mm clear of the bottom. There's about 8–10 mm of mount under the floor.
  - **Re-export both upper mount STLs.**
- **Hinges and latch:** the holes moved 0.1 mm in the printed parts onto the slot centres (Y −23.8 door frame, −1.0 uprights). The parts themselves didn't move, so the pins stay coaxial.
  - Left hinges: M3x8 SHCS. The old M3x12s bottomed in the slot.
  - Hinge_Top/Bottom: M3x22, plus M3x25 with a washer in the deeper-seated holes.
  - Latch: 2 M3x8 + T-nut were added (they were missing).
  - Panel_Clip pivot: M3x25 → M3x12 into a Ø2.5 pilot in the latch key.
  - The T-nuts are re-seated under the slot lip. They had been modeled ~8 mm deep in the extrusion core.
- **XY joints:** rechecked. The M5s are already centred on the top slot (Y 451.0), so the earlier flag was a false alarm. The left nylocs were re-seated under the lower joint.
- **Bed plate:** 14 M3 tap holes (Ø2.5, 4 mm blind) under the carriage screws. The M3x12 BHCS get ~3 mm of thread.
- **Electronics panel and OpenGrid tiles:**
  - Panel: 12 Ø3.4 holes with a 90° (45° per side) countersink on the underside.
  - Tiles: mount holes bored to Ø4.0 with M3 heat-set inserts.
  - Screws: M3x8 FHCS from below. The nuts were removed.

## Still open
- **Heater pad:** 10 of the 14 bed-carriage screws pass through the modeled silicone heater pad. Order a pad with cut-outs or check the outline.
- **Panel_Clip pivot:** only ~2.5 mm of plastic thread.
- **Hinge_Top/Bottom:** a 0.25 mm³ touch with the door frame. Cosmetic.

## Totals (screw list)
- 314 screws: 267 high confidence, 47 to check.
- Nuts and inserts:
  - T-nuts: 76 M3, 18 M4, 38 M5
  - 76 M3 heat-set inserts, plus 22 spare insert holes
  - M5 nuts: 4 hex, 4 nyloc
  - 2 M3 washers
  - No M3 hex nuts are needed now.
