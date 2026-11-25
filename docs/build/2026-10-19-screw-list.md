# Apexion-X — screw list from hole geometry (2026-10-19)

> **Historical note (2026-10-19).** This records the screw list at that date. For current figures see the [D3 BOM workbook](../../bom/D3_Apexion-X_BOM.xlsx) and the [Rev 06A hardware notes](../../bom/README.md).

Apexion-X was formerly named "TV06+ fixed" (renamed 2026-10-29). It is derived from the Terminal Velocity TV06+.

The full list was produced as a spreadsheet; its schedule now lives in the Fasteners tab of the [D3 BOM workbook](../../bom/D3_Apexion-X_BOM.xlsx). Every printed part's holes were measured (diameter, counterbore, countersink, blind/through) and ray-traced to what the screw lands in (2020 T-slot, M3 heat insert, stepper thread, nut). Related: [2026-10-21-bom](2026-10-21-bom.md).

**Totals:** about 267 screws. About 178 are high confidence; 89 are flagged "check". (The later BOM supersedes these counts: 316 screws, 78 M3 T-nuts.)
- 66 M3 T-nuts, 18 M4 T-nuts, 38 M5 T-nuts
- 64 M3 heat-set inserts confirmed, plus 22 more blind Ø4.0–4.7 holes with no screw found (86 in total)
- 12 M3 nuts, 4 M5 nuts, 4 M5 nylocs

**Calibration:** the method reproduces the screws already modeled. The 4 mm midspan clips come out at M3x8 and the 6 mm clips at M3x12, as in the CAD.

## Design issues found
- **Z motor screws (12):** seat-to-motor is 38.6 mm through the 30 mm Spacer_x6, and the motor thread is 5.35 mm deep, so the screw needs to be 41–43.6 mm.
  - M3x40 gets only 1.4 mm of thread. M3x45 bottoms out.
  - Fix: use M3x45 with about 2 mm of washers, or shorten Spacer_x6 by 2 mm and use M3x40.
- **A/B motor screws:** the through-hole needs about 31 mm. M3x30 gets 1.8 mm of thread; M3x35 bottoms out.
  - Two more M3 holes per side land on the NEMA face where the model has no threaded hole.
- **XY joint M5s into the X extrusion, hinge/latch M3s into the door frame:** these holes are not centred on a T-slot in the model.
- **Holes with no mating hole modeled:**
  - Skirt_CenterCap has 4 Ø3.6 blind holes, probably meant to be Ø4.0 inserts.
  - The OpenGrid tiles have no matching holes in the electronics panel.
  - The bed carriage screws go into the bed plate, which has no threaded holes modeled.
- **Dragon Burner internals:** the hole mates are incomplete. Use the Dragon Burner BOM.
- **Not in the list:** frame corner joints, MGN rails/blocks, pulleys and the electronics have no printed-part holes in this file.
