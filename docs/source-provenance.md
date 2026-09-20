# Source provenance and publication checks

The two design archives in this package were copied byte-for-byte from `document.zip` supplied by the owner. No other items from that archive are needed to understand the basic navigation policy. The source ZIP and the owner’s original files have **not** been edited or deleted.

| Published candidate | ZIP member | SHA-256 |
| --- | --- | --- |
| `proteus/logic-only/Maze solving robot.pdsprj` | `document/Maze solving robot.pdsprj` | `b9e43e869a7057787e6bd65143a9d9b0e9f45d65adbcd55995271146588970ca` |
| `proteus/ultrasonic-experiment/Last edition of maze solving Project.pdsprj` | `document/Last edition of maze solving Project.pdsprj` | `8074ccea0d48ff4d4e5ac7c0567766368944990a89c633bbf4afdff281d2c13a` |

## Before public publication

- Author supplied both versions as their work, but individual third-party simulation models, HEX programs or group-owned files are **not** automatically covered by that permission.
- Confirm how ultrasonic simulation was used and resolve `UltraSonicSensor.HEX` if running the second variant. Neither the missing model nor `UltraSonicTEP.HEX` is bundled here.
- Check whether physical AND IC was `74LS08` or `74HC08` (schematic mentions HC08); reflect the real build accurately.
- Add measured comparison or screenshots only after running Proteus or testing the robot.
- Prefer a separate GitHub commit for each meaningful documentation/simulation update, and credit contributors where applicable.
