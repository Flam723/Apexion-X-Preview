# TV06+ Fusion design check — 2026-10-18

File: "TV06+" (folder TV TV06Plus-NG_CM). Direct-modeling design, 308 components, 405 occurrences, 329 bodies (32 hidden). No external references, no non-solid bodies, no mesh bodies. Coordinates: X = width, Y = front→back, Z = up (mm).

## Real problems (asymmetric / clearly unintended)
1. **Duplicate rear bed brace** — "Linear_Rod_Bed_Brace_Rear 2-hole" and "Linear_Rod_Bed_Brace_Rear-3Hole" are both visible and occupy the same space (61,352 mm³ overlap). Keep one.
2. **Floating M4 Knurled Nut 1** (Z Assembly) sits at Z≈116–124 near the right-front upright; Nuts 2 and 3 sit at bed level (Z≈−146). Misplaced.
3. **Left Z motor stack is 2 mm higher than right/rear** — Left motor −500.6/−460 vs right & rear −502.6/−462; left mount −437/−420 vs right −439/−422. Result: Left_Lead_Screw overlaps Left_Stepper_Motor (28 mm³); right side is clean. The left mount also cuts into 2020 425FB (20 mm³) and 660FL (10 mm³); the right side doesn't.
4. **Left front Z rod is ~1 mm off its bores** — left rod Y 24.9–32.9 vs right 26.2–34.2. It cuts into Motor_Mount_Left (48 mm³) and Left_Rod_Leadscrew_Upper_Brace (31 mm³); the right rod barely touches (1.5 mm³). The left lead screw has the same ~0.9 mm Y offset.
5. **Rear Z rods pass through solid Motor_Mount_Rear** — 673 mm³ each (≈13 mm of Ø8 rod). Either the bores are missing/undersized or the rods are too long. Cover_x3 on the rear also overlaps the mount (261 mm³).
6. **Right A/B motor mount cuts into rear-right 660 upright** — Upper Right 302 mm³ and Lower Right 55 mm³; the left mounts are clean. Right gantry mount position is off.
7. **Left A/B NEMA17 overlaps Motor_Mount_Lower_Left** (11.5 mm³); the right side doesn't.
8. **Drag chain hits the rear bed braces** (7–8 mm³), and the rear/right lead screws touch the bed braces (2–3.5 mm³). Check clearance at the brace holes.
9. **Idler bearing insert, left vs right** — 78 mm³ into the left idler body vs 18 mm³ on the right. Inserts aren't positioned the same way on each side.

## Probably modeling artifacts (worth a look, likely fine)
- Hot Bed Plate vs Heater, 9,038 mm³: the heater pad is modeled inside the plate.
- Toolhead parts (PRODUCT_NAME_1..5, RapidoHF_Mount, WristWatch_BMG_Mount) overlap Carriage_Mount (up to 1,305 mm³). Old toolhead geometry is stacked in the same place.
- XY_Joint upper/lower overlap each other and the 2020 X extrusion (67–103 mm³). Same on both sides, so probably the joints interlock or press-fit into the slot by design.
- Idler bodies into 495LTM/RTM (63 mm³ each, symmetric): probably slot keys.
- Fasteners into printed parts (16–19 mm³): screws modeled without holes. Normal.
- Spacer_x6 / Cover_x3 overlaps under the front Z motors (75–88 mm³).
- Frame 495RB and 495TR start at Y 8.6 instead of 9.0, so they overlap the front uprights by 0.4 mm. 425FB bottom is at −450.1.

## Housekeeping
- Hidden leftovers: Z_Bed_Right_Hardware(Mirror) and GE5C(Mirror) inside Z_Bed_Left; hidden SideDiffuser bodies in 3 side skirts; one hidden rubber foot in FootAssembly v5 (3); hidden Z_Cable_Anchor and chain-screw hardware.
- 68 empty/container components, and heavily suffixed copies ("corner_clip_4mm (2) (3) (1) (2) (4) (1) (2) (1)"). Consider renaming or consolidating.
- Several occurrence bounding boxes reach far outside the printer (OpenGrid to X −1691/Y 2240, Z_Cable_Anchor, Skirts). That points to stray sketch or construction geometry in those components.
- Interference couldn't be computed for the Frame group as a whole (Fusion returned no result). Frame-vs-gantry/Z was checked pair by pair instead. Panels/skirts weren't checked for interference.
