# Build Manual Rev B (provisional)

**Rev B.2, 2026-11-19.** The [current manual](../Apexion-X%20Build%20Manual.pdf) incorporates [Rev 06A](../design-reviews/2026-11-19-rev06a-mechanical-fit-check.md) for mechanical fit-up. The v5 illustrations remain as orientation references. Updated steps cover the three-point bed and WobbleX stacks, heater clearance, fastener and bearing retention trials, the drag chain and measured travel. Phase J credits the [Voron Design wiring guide](https://docs.vorondesign.com/build/electrical/index.html) and the Voron Trident. Verify selected electronics, project wiring and protection, Klipper and loaded travel before commissioning.

## Rev B and B.1 history

**Rev B.1, same day:** the D5 rear-panel mark is dropped. The Apexion-X logo (inside the rear panel) and the AX badge (right front skirt) are official; each can be etched or a sticker. Steps I3 and K4, CR-24 and Appendix B were updated.

Rev B was 89 pages in US Letter landscape. It replaced the 33-page manual of 2026-10-31, which is in the Git history.

**Status: provisional, not build-ready.** The mechanics are documented. Electronics, wiring, firmware, torques and belt tension are not designed yet.

## Basis
- Machine version: Fusion "Apexion-X STYLING 2026-11-06" v5, exported to STEP (205 MB, not included here; the editable Rev 06A Fusion archive is in [`cad/`](../../cad/)).
- Sources: the D1–D5 build package (2026-11-07: specifications, illustrated step tables, D3 BOM, D4 CAD package, D5 rear-panel emblem) and the design reviews in `docs/design-reviews/` and `docs/build/`.
- The Voron Trident manual served only as a model for overall organisation. No text or artwork was copied.

## Contents
- Cover and document control, a source inventory and evidence statement, cross-source conflicts, and a review record.
- Overview, safety, tools, workspace, and a parts checklist from the D3 BOM.
- 52 steps in phases A–L, one page each:

  | Phase | Covers |
  |---|---|
  | A | Prep |
  | B | Frame and door frame |
  | C | Z drive |
  | D | Bed |
  | E | A/B drives |
  | F | Y rods and front idlers |
  | G | X beam and XY joints |
  | H | Toolhead and belts |
  | I | Feet, skirts and display |
  | J | Electronics bay |
  | K | Enclosure |
  | L | Inspection and commissioning |

  Each step has:
  - a true-shape render from the STEP with numbered callouts
  - parts and tools
  - an orientation cue
  - numbered actions
  - a fastener table with the CAD length status
  - a CHECK, plus NOTE / CAUTION / WARNING / CONFIRMATION REQUIRED callouts as needed
- Step support: 17 evidence-supported, 25 partly supported, 10 confirmation required.
- Appendices:
  - A: unresolved-items register (CR-01…CR-35)
  - B: source and verification map
  - C: fastener totals
  - D: visual index with art direction and illustration briefs
  - E: troubleshooting and maintenance

## Reviews
- **Gemini (Antigravity CLI, read-only): visual inspection of the earlier PDFs and images.** It found:
  - figures drawn in a different orientation from what their step text says
  - figures that show parts only as envelopes
  - labels cut off in the figures
  - that the D5 emblem is not the AX logo
- **ChatGPT (Codex CLI, read-only): editorial review of the draft.** All 8 findings were applied:
  - A/B mount assembly order flagged
  - door hardware details flagged
  - power-on gates applied to the D1 tests
  - N06 closed only after wiring
  - Tr8-nut hold point added before printing P17–P19
  - door installed before the rear panel
  - unsupported shop instructions removed
  - drag-chain end naming flagged
- Step fastener quantities match the D2/D4 totals for every screw callout, with one deliberate exception: H26 M5×14 is replaced by H28 M5×16 on the right upper Z brace.

## Conflicts logged in the manual
| Topic | Conflict |
|---|---|
| Ends to tap | 33 (D2) vs 28 (D3 tools tab). The manual uses 33. |
| M3 heat-set inserts | 79 vs 93 |
| A/B motor | 17HS19-2004S in CAD vs 17HS15-1504S-X1 in the BOM. Screw engagement was checked on the CAD motor only. |
| Rear-panel engraving | D5 ring-triangle-X mark vs the Apexion-X logo. **Resolved in B.1:** the official logo is used and D5 is dropped. |
| Door (N04) and electronics panel (N06) | 4 mm modelled vs vendor stock |
| M2 hex key | 1.3 vs 1.5 mm |

## Blocking items before a build
- **Electronics, wiring and firmware:** CR-01…CR-04, CR-32
- **Tr8 nut and its flange pattern:** CR-11
- **Rear bed joint:** CR-12
- **Heater pad cut-outs:** CR-13
- **Torques:** CR-05
- **Belt tension:** CR-06
- **Insert pockets missing in CAD:** CR-15
