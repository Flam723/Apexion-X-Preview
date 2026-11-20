# Apexion-X Rev 06A mechanical fit check

November 19, 2026 · Rev 06A incorporates the correction to use the existing WobbleX dowel seats in P17–P19. It supersedes the separate upper-receiver arrangement in Rev 06.

Rev 06A is approved for the first mechanical build and fit-up. Supplier dimensions, installed hardware and commissioning measurements govern final travel limits and operating settings.

[Native Fusion archive](../../cad/Apexion-X-Rev-06A.f3d) · SHA-256 `d5ef0b1e3e074932542bbbcaf8950234348e8cf20a4cbbd005f501e615de129b`

In Fusion, expand **REV06 - fit-check parts and hardware**. The revised heater, front idler carriers and bed mount bodies are inside their original subassemblies.

| Item | Changes in Rev 06A | Check before ordering or running |
| --- | --- | --- |
| **01 Bed and Z stack** | Three M4-threaded steel balls, three Ø12 × 3 mm countersunk disc magnets and three WobbleX WS8 stacks are placed on the existing Z axes. The upper WS8 balls ride on Ø3 mm dowels modeled in the four existing Ø3.1 mm cutouts per Z travel mount. No separate upper adapter is used. The native bed mounts now have Ø12.24 mm nominal magnet pockets and the mating guide braces have relief for the balls and metal seats. The hard contacts are arranged as a left datum, right vee and rear flat. | The M4-threaded steel balls have a **confirmed Ø10 mm nominal OD**. Verify the ball's thread depth, the magnet's countersink and rated hot holding force, the hardened seat details and printed brace strength. Confirm the Tr8 nut flange and screw lead, actual WS8 pin fit and retention in the existing seats, stack preload at all three stations, hot cycling and the power-off state. |
| **02 Heater** | Native heater body checked at all 18 screw locations. The four outer and four inner Ø15 mm holes are retained. The ten missing inner openings are Ø8.5 mm trial keep-outs. | Have the heater supplier approve the whole pattern, resistance element routing and spacer clearances in the final plate/carriage stack. |
| **03 Brace screws** | Two right P16 M5×14 screws replaced by M5×16. Two P15 M5×16 and two P14 M5×10 with T-nut references added. | Verify installed T-nut depth and clamp at all three braces. H22 bed-tee, H27 rear motor mount and H31 A/B T-slot screw lengths depend on the actual stacks. |
| **04 Motor screws** | Twelve Z screws use an M3×45 and 4 mm trial spacer stack. Six A/B screws use M3×30 and 1.5 mm trial spacers. Nominal entry is 4.4 mm at Z and 3.5 mm at A/B. | Measure full thread depth, seat diameter, tip clearance and pulley location on the actual motors. The legacy motor models remain the body references. |
| **05 Front idlers** | Four Ø6.1 mm × 6.4 mm rear-entry insert seats with lead-ins cut into the original P11 carriers. The nominal belt-center planes are preserved. | Match pocket geometry to the selected H40 insert. Check the residual wall, screw reach, belt tracking and hot retention. |
| **06 C-clips** | Hidden Z-shell C-clip fit examples. Samick lists Ø18 × 1.3 mm grooves on both Ø19 mm shell sizes, with 22 mm spacing on LM10UU and 44 mm on LM10LUU. THK lists a size 19 C-shape option. | Check the actual bearing grooves, access and housing shoulders. Confirm Y end clearance on the long bushings before changing retention. Use positive end capture suited to the housing if the installed shells lack usable grooves. |
| **07 Drag chain** | Six M3×8 countersunk trial fasteners with insert references at P19 and P28. | Check both seat stacks, flush heads and tip clearance with the real chain. Sweep Z and tilt with the loaded cable bundle. |
| **08 X travel** | The original upper joints are used. The hidden X-travel datums show the 261.7 mm nominal soft span derived from the previous CAD estimate. | Establish the actual nozzle and probe reach with the final toolhead across Y. |
| **09 Y travel** | Existing Ø10 × 468 mm Y rods. The model contains no additional Y brace or intermediate support. | Use the production Y hardware to measure stiffness and travel. |

## WobbleX Z travel

The existing P17–P19 upper pin channels are 5.0 mm apart on center. The nominal Ø3 × 8 mm pins fit within their original cutouts in the CAD. The WS8 upper ball paths were aligned to those pins, and the lower adapter was aligned to the perpendicular lower ball paths. The modeled stack now reaches about **19.5 mm** below the guide brace, compared with about 27 mm in Rev 06. At the reference pose, the check found no solid overlap of the WS8 mockup with any of the three moving Z mounts or lead screws.

The Fusion BRep sweep bracketed first contact between the rear lower Tr8 adapter and the rear motor mount between **230.895 and 230.925 mm down from the v5 CAD pose**, with a 0.03 mm³ overlap threshold. This recovers about **7.4 mm** of down travel relative to Rev 06. The local trial stop in the file is **228.8 mm down from the CAD pose**. Use the complete loaded and tilted sweep from actual homing to establish the firmware travel limits.

Expand **REV06 - fit-check parts and hardware** and inspect **01b WS8 - native upper pin seats and lower Tr8 adapters**. Apply **Rev 06A WS8 existing upper pin seats** for the assembled close-up. To inspect travel, enable **01c WS8 revised travel** and apply **Rev 06A WS8 lower travel check**. Blue reference geometry shows the local trial stop. Orange solids show overlap at the old 246 mm down position.

## References

- [MirageC WobbleX integration and source CAD, GPL-3.0](https://github.com/MirageC79/Interfaces-for-WobbleX-integration)
- [MirageC Trident WS8 stack and adapters](https://github.com/MirageC79/Interfaces-for-WobbleX-integration/tree/main/Voron/Trident)
- [Samick LM10UU short bushing dimensions](https://www.mysamick.com/English/product/goods_list.asp?lcode=B1&sg=2) and [LM10LUU long bushing dimensions](https://mysamick.com/English/product/goods_list.asp?lcode=B1&mcode=01&scode=02)
- [THK bushing retention and snap-ring selection](https://www.thk.com/jp/en/products/other_linear_motion_guides/linear_bushing/design/0001/)
- [A/B motor drawing](https://omc-stepperonline.com/download/17HS15-1504S-X1.pdf) and [heater cutout guidance](https://www.watlow.com/-/media/documents/specification-sheets/colsrh0618.ashx)
