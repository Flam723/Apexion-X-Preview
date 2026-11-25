# TV06+ fixed — BFI symmetrical front idlers (2026-10-22/23)

**Status: adopted.**
- **One print per side:** each front idler body is now the TV06+ idler mount merged with a BFI housing (design decision: merge each idler with its mount into one print).
- **Versions:**
  - v14: before the BFI work.
  - v15: first mock-up.
  - v16/v17: right side matched to the left.
  - v18: the housing merged into each mount.
- **Background:** the earlier thin restacked carrier was rejected because the walls were too thin for belt tension in a heated chamber.

## Source
- The "BFI Symmetric" STEP from [Beefy Front Idlers for Trident](https://github.com/clee/VoronBFI).
- **Parts:** VT and V2.4 symmetrical housings; carriers in M5, M3 and BHCS versions; fronts with and without logo.
- **Carrier:** 14 × 15 × 49 mm, one part for both sides. The 10 mm bearing gap sits 5 mm below centre, so flipping it gives the two belt levels 10 mm apart.
  - Same 5 × 18 pin and 2 × F695 + shim stack.
  - Clamp holes 37 mm apart.

## Final parts (printed)
| Part | Qty | Notes |
|---|---|---|
| Front idler body + BFI housing, Left (Idler_Body_Left) | 1 | TV06+ mount + BFI VT symmetrical housing (extrusion clamp removed: the two straps around the 2020, cut at X+21). One solid, 35,897 mm³. Bearing at the low belt level (Z 29.45–39.45, belt A). |
| Front idler body + BFI housing, Right (Idler_Body_Right) | 1 | Same BFI housing rotated 180° about Y (bearing Z 39.5–49.5, belt B). One solid, 36,556 mm³. |
| BFI Carrier M5 symmetrical | 2 | Same print both sides; the right one is installed upside down. |
| BFI Front M5 symmetrical | 2 | Same print both sides. |

- **Right mount matched to the left:**
  - The mount-to-upright screw counterbore, the Ø5.3 hole and the belt-side pocket were raised 10.05 mm to line up with the flipped BFI side slot. The old low features were filled.
  - The M5x10 BHCS (idx 42) and M5 T-nut (43) are at Z 44.57. The head is reachable through the BFI side slot, like the left.
  - The upper locating tab in the 660FR slot is now Z 50–56 (lower tab Z 18–24 unchanged).
  - The top band (Z 50.25–56, Y < 9.5) was copied from the left's Z 40.2–46 band, mirrored, so the upper tab is attached. In v16/v17 the tab had been a floating 0.02 mm sliver.
- **Hidden (no longer used):** Idler_Bearing Insert L/R, Idler_Face L/R.
- **Component:** "BFI Front Idler carriers + fronts" holds the carriers and fronts.

## Hardware
- **Pins and stacks:** Ø5 × 18 pins, 2 × F695 + 2 shims per side (left centred Z 34.45, right Z 44.5).
- **Clamp screws:** 4 × M5x30 SHCS from the front face (Z ≈ 21 / 58). M5x40 hit the housing back wall.
  - The carrier nut/insert feature is not modeled; the designer's preference is heat-set inserts.
  - The old M5 inserts (idx 37/39/45/47) were removed.

## Checks (v18)
- **Both merged parts:** each is one lump. Belt and carrier/front overlap is 0. Pin/stack/clamp screw/mount screw/T-nut overlap is ≤ 0.01 mm³.
- **Frame contact:** mount vs 660FR is 3.0 mm³ and vs 495RTM is 63 mm³; both are unchanged (the slot keys).

## Open
- **Clamp screws:** model the BFI carrier's nut feature as an M5 heat-set insert pocket.
- **STL re-export:** both merged front idler bodies, plus 2 BFI carriers and 2 BFI fronts.
