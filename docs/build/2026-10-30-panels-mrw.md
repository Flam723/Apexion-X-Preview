# Apexion-X — enclosure panel DXFs for Mandala Rose Works (2026-10-30)

> **Historical note (2026-10-30, v21).** This records the first panel package at that date. For current figures see the [Rev 06A panel DXFs and cutting notes](../../dxf/panels-mrw/README.md).

Fusion "Apexion-X" saved as **v21**. The panel package (material folders, `_xN` names, README, overview PNG) was built to MRW's custom-panel rules (mandalaroseworks.com/pages/custom-projects): DXF only, zip with one folder per material, quantity in file name, send via Discord @MandalaRose or sales@mandalaroseworks.com. The current Rev 06A DXFs are in [`dxf/panels-mrw/`](../../dxf/panels-mrw/).

## Panels
| File | Size (mm) | Model thk | Default material folder |
|---|---|---|---|
| side_panel_x2 | 514 × 624 | 3 | SmokedPolycarbonate_3mm |
| rear_panel_x1 | 439 × 624 | 3 | SmokedPolycarbonate_3mm |
| top_panel_x1 | 439 × 514 | 3 | SmokedPolycarbonate_3mm |
| door_panel_x1 | 436 × 616.2 | **4** | SmokedPolycarbonate_3mm |
| chamber_floor_panel_x1 | 425 × 500, 8 × Ø6 | 3 | BlackACM_3mm |
| electronics_bottom_panel_x1 | 447 × 517.63, 12 × Ø3.4 csk (bottom face, Ø6.4 90°) + 12 × Ø3.2 | **4** | Aluminum6061_3.175mm |

DXFs were written from the model's face geometry (true lines/arcs/circles, no duplicate lines); each profile's area matches the Fusion face to 0.1 mm². Where top and bottom faces differ, the min-material profile was used (the cut never leaves material where the model has none).

## Model changes made before export (v21)
- Door (Clacky) panel: left, right and top slot edges trimmed 0.5 mm (was 0.06 mm interference at the slot bottoms) → 436 × 616.2.
- TV06+Motor_Mount_Left/Right (front Z) and A/B_Motor_Mount_Lower_Left: outer face cut flush with the frame (they were 0.06–0.07 mm proud under the side panels). **Re-export these 3 STLs.**
- Stray hidden M3x8 SHCS + T-nut of the root-level rear-top midspan clip moved onto the clip (they sat inside the rear panel).
- Re-sweep: no panel overlaps anything by more than 0.005 mm (face contact only).

## Open decisions
- Door and electronics panel are modeled 4 mm; MRW stocks acrylic/PC in 3/6 mm and 3.175 mm 6061.
- Chamber-floor Ø6 holes are 1 mm blind pockets in the model; the DXF cuts them through.
