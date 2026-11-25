# TV06+ fixed — XY joint, A/B mount and idler hardware (2026-10-22)

Saved as a new version of "TV06+ fixed". Follows [2026-10-21-bom](../build/2026-10-21-bom.md).

## Alignment fix
Both lower XY joints were offset from their uppers by the same amount at every hole: left +0.15 X / +0.51 Y, right +0.03 X / +0.29 Y. The uppers sit correctly on the X-beam slot centre (Y 451.0), so the lowers were moved back to match.
- The LM10LUU pockets were re-centred on the rods again.
- The bearings were moved −0.5 / −0.3 Y to stay flush with the back of the pocket. They now span Y 405.5–460.5.
- The M4 set screws moved with the joints.

## Hardware per XY joint (×2 joints)
| Location | Hardware | Status |
|---|---|---|
| Upper into X-beam top slot (2) | M5x12 BHCS + M5 T-nut | Was M5x16 (10 mm deep, past the 6.3 mm slot floor) with T-nuts modeled in the beam core. Fixed. |
| Upper-to-lower clamp bolts (2) | M5x40 SHCS + M5 heat-set insert | Was M5x45 + nyloc. The inserts go in the existing Ø6.5 × 6.4 pockets; ~6.2 mm of thread. |
| Idler pins (2) | **Ø5 × 45 dowel pin** (designer: these holes are dowel-pin seats, not bolts) | Through upper + idler gap + lower. Plain Ø5.2 holes; press-fit or glue. The insert pockets cut there by mistake were filled back in. |
| Lower into X-beam bottom slot (1) | M5x20 SHCS + M5 T-nut | Was missing. The head sits flush in the Ø9 counterbore. |
| Bearing retention (1) | M4x8 set screw (tap Ø3.3 M4) | — |

## A/B motor mounts (one idler axle per side)
- **Axle hole:** a Ø9 counterbore on one half, a Ø5.4 clearance hole, a 10 mm idler gap, then a tapered Ø5.1→4.2 thread-forming hole in the other half.
  - Right: head underneath, high belt level (Z 39.5–49.5).
  - Left (mirror): head on top, low belt level (Z 29.5–39.5).
- **Axle screw:** M5x25 SHCS, head flush, ~5 mm of thread, tip flush with the far face.
  - The right one was modeled as M5x30 into a frame T-nut (removed). The left one was missing.
- **Idler stack:** the pocket radius is 8.5 mm, too tight for a toothed idler's Ø18 flanges. It's shim + 2 × F695-2RS + shim (9.0 in a 10.0 gap; add a 1 mm washer if wanted).
- **Motor screws:** the M3x30 motor screws, with counterbores deepened 1.8 mm, were done earlier.

## Idlers (all modeled now)
| Where | Gap | Pocket | Stack (bottom → top) |
|---|---|---|---|
| XY joint "E" pin (left low belt Z≈34.6, right high Z≈44.75) | 10.2 | r ≥ 10 | shim 0.5 + GT2 20T toothed idler (Ø18 flanges, 8.5) + shim 0.5 |
| XY joint "F" pin (left high Z≈44.6, right low Z≈34.65) | 9.65–9.8 | r 8.5 | shim + 2 × F695-2RS back to back, flanges out + shim (9.0) |
| Front idlers (Idler_Bearing Insert L/R, Z≈34.4) | 9.95 | Ø16 in Idler_Face | shim + 2 × F695-2RS + shim on a Ø5 × 18 dowel (blind holes) |
| A/B motor mounts (left Z≈34.5, right Z≈44.5) | 10.0 | r 8.5 | shim + 2 × F695-2RS + shim on an M5x25 SHCS |

- **Totals:** 2 GT2 20T toothed idlers, 12 F695-2RS, 16 M5 shims 5×10×0.5, 4 dowels 5×45, 2 dowels 5×18. Add shims to take up the 0.5–1.2 mm of play.
- **Front idler clamp:** the model had each M5 head buried in the insert's Ø6.5 pocket and a nut on the front face. It's now M5x30 SHCS from the front face into an M5 heat-set insert at the back of the Idler_Bearing Insert, 4 in total.
- **Belt-height check (open):** both front idlers sit at the low belt level (Z≈34.4). The XY joints and A/B mounts each carry one low (≈34.5) and one high (≈44.6) idler. The motor pulleys are at different heights (left Z 29.9–45.9, right 32.7–48.7). Verify the belt path once the belts are modeled.
- **Clash check:** clean (≤0.5 mm³ at hole chamfers; the screw-thread overlaps in the thread-forming holes are expected).
- **Totals now:** 319 screws, 135 T-nuts, 8 M5 heat-set inserts (4 XY clamp + 4 front idler), 0 nylocs, 0 M5 hex nuts.
- **STL re-export:** both lower XY joints.
- **BOM:** the A/B motor line is now the designer's STEPPERONLINE 17HS15-1504S-X1 (45 Ncm, 1.5 A, 39 mm). The CAD still shows a 17HS19-2004S.
