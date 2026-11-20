# Apexion-X

Apexion-X is an enclosed CoreXY 3D printer with three independently driven Z axes.

![Apexion-X front render](docs/images/apexion-x-render-front.png)

## Rev 06A mechanical preview

Rev 06A is the baseline for a first mechanical fit-up. It uses three WobbleX WS8 stacks in the existing dowel seats and unbraced Ø10 × 468 mm Y rods. The build manual is provisional. Before ordering a heater, get supplier approval for the cutout pattern. Verify installed hardware, sweep the loaded bed through Z and tilt, and review the wiring, protections and Klipper configuration before power-on.

- [Editable Fusion source](cad/Apexion-X-Rev-06A.f3d). Open or upload the .f3d archive in Autodesk Fusion.
- [Rev 06A mechanical fit check](docs/design-reviews/2026-11-19-rev06a-mechanical-fit-check.md). The nine fit-up checks and the native CAD inspection views.
- [Build Manual, Rev B.2](docs/Apexion-X%20Build%20Manual.pdf). The steps include Rev 06A changes and Voron electrical references. The illustrations show the earlier v5 model.
- [Printer specification](docs/Apexion-X%20Printer%20Specification.pdf). Travel and performance figures are design targets pending prototype measurements.

Production STLs, BOM spreadsheets, panel DXFs and machine-specific firmware are pending. Use the fit check and actual measurements when choosing and fitting hardware.

Fusion file SHA-256  
`d5ef0b1e3e074932542bbbcaf8950234348e8cf20a4cbbd005f501e615de129b`

## Credits & license
Copyright © 2026 Flam723 for the Apexion-X contributions. The project's contributions are licensed under the [GNU General Public License, version 3](LICENSE) (GPL-3.0-only). The GPL permits commercial and noncommercial redistribution under its terms.

> Apexion-X by Flam723 · [project](./) · [GNU GPLv3](LICENSE) · Changes: [describe any changes].

Please credit Apexion-X by Flam723 and link to the project when posting a build.

Apexion-X preserves the copyright and license notices of the upstream projects below.

**TV06+ skirt design credit.** The Apexion-X skirts and front diffusers are a remix of [TV06+](https://github.com/Terminal-Velocity-Collective/TV06_Plus), designed by [VectorForce3D](https://github.com/VectorForce3D) and published by Terminal Velocity Collective. Apexion-X removes the original TV badge from the front diffusers and uses a separate left diffuser. [VectorForce3D approved GPLv3 redistribution of the adapted skirt geometry](https://github.com/Terminal-Velocity-Collective/TV06_Plus/issues/1#issuecomment-7044320758), including its use in the full Apexion-X printer assembly.

| Part of Apexion-X | Derived from | Author | Upstream license |
|---|---|---|---|
| Printer kinematics | [RIFF220](https://github.com/itesdahl/RIFF220) — itself a remix of the [Voron Trident](https://github.com/VoronDesign/Voron-Trident), BFI and Dragon Burner | V4projects ([itesdahl](https://github.com/itesdahl)) | GPL-3.0 ([LICENSE](https://github.com/itesdahl/RIFF220/blob/main/LICENSE)) |
| Skirts and front diffusers | [TV06+](https://github.com/Terminal-Velocity-Collective/TV06_Plus) | [VectorForce3D](https://github.com/VectorForce3D), published by Terminal Velocity Collective | [GPLv3 permission for the Apexion-X remix](https://github.com/Terminal-Velocity-Collective/TV06_Plus/issues/1#issuecomment-7044320758) |
| Electronics and wiring reference | [Voron Electrical Wiring](https://docs.vorondesign.com/build/electrical/index.html) and [Voron Trident](https://github.com/VoronDesign/Voron-Trident) | Voron Design and documentation contributors | [Trident GPL-3.0](https://github.com/VoronDesign/Voron-Trident/blob/main/LICENSE). The wiring guide is linked as a reference. |
| Door | [Clicky-Clack Fridge Door](https://github.com/tanaes/whopping_Voron_mods/tree/main/clickyclacky_door) | Jon Sanders ([tanaes](https://github.com/tanaes)) | GPL-3.0 ([LICENSE](https://github.com/tanaes/whopping_Voron_mods/blob/main/LICENSE)) |
| Toolhead | [Dragon Burner](https://github.com/chirpy2605/voron/tree/main/V0/Dragon_Burner) | chirpy ([chirpy2605](https://github.com/chirpy2605)) | GPL-3.0 ([LICENSE](https://github.com/chirpy2605/voron/blob/main/LICENSE)) |
| Front idlers | [Beefy Front Idlers for Trident](https://github.com/clee/VoronBFI) | clee | GPL-3.0 |
| WobbleX WS8 interfaces | [Interfaces for WobbleX integration](https://github.com/MirageC79/Interfaces-for-WobbleX-integration) | MirageC | GPL-3.0 |

Licensing notes (not legal advice):
- **RIFF220:** the kinematics were first noted as derived from "RIFF200"; the upstream design is the RIFF220 by V4projects.
- **GPLv3 contributions:** preserve upstream copyright and license notices, identify modifications, and make the corresponding editable CAD available when distributing covered exports or derived files.
