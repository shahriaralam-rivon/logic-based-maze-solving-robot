# Logic-Based Maze-Solving Robot 🤖

A robot designed to navigate using three IR obstacle sensors, digital logic ICs, and a TB6612FNG motor driver **without a navigation microcontroller**.

> **Project status:** Physical robot and bench-level logic/motor tests reported by the author. The two supplied Proteus design variants are included in this repository under `proteus/`. They have been inspected structurally, **not** opened or run in Proteus during this portfolio preparation. They have been inspected structurally, **not** opened or run in Proteus during this portfolio preparation. Complete real-maze performance has not been independently documented here.

## Project overview

The navigation controller prioritizes: **forward → left → right → stop**. A front-clear reading selects forward even if a side route is also clear. Logic outputs command the two motor groups via the driver.

## Components

- Three IR obstacle sensors for front, left and right detection.
- 74HC14 inverter, 74HC11 three-input AND, and 74HC32 OR logic (design family observed in supplied schematics).
- AND gate: **74HC08 appears in the Proteus schematics**; the previously documented physical build lists **74LS08**. The physical IC marking needs confirmation before equating them.
- TB6612FNG dual motor driver; four DC gear motors.
- 18650 Li-ion cells and LM2596 buck converter for regulated 5 V logic supply (author's hardware description, not a file-based electrical measurement).

## Navigation and motor mapping

See [navigation logic](docs/navigation-logic.md) for the priority truth table, logic expressions, and driver inputs. PWM and STBY also need to be enabled for movement.

## Proteus designs

Two design variants were supplied because they represent development for better performance. **The file names do not prove which one produced better performance**.

| Variant | Original filename | Notes |
| --- | --- | --- |
| [Logic-only design](proteus/logic-only/Maze%20solving%20robot.pdsprj) | `Maze solving robot.pdsprj` | Contains 74HC08/11/14/32 and TB6612FNG references. No external HEX filename found by text inspection. |
| [Ultrasonic experiment](proteus/ultrasonic-experiment/Last%20edition%20of%20maze%20solving%20Project.pdsprj) | `Last edition of maze solving Project.pdsprj` | Contains ultrasonic simulation components and references to `UltraSonicSensor.HEX` / `UltraSonicTEP.HEX`; dependency and rights checks remain. Does **not** establish that the physical robot used ultrasonic navigation. |

**Source files available:** both original `.pdsprj` files are included under `proteus/`. See [simulation notes](docs/simulation-notes.md) before reproducing. Proprietary/missing third-party models and HEX files are not bundled here. Proprietary/missing third-party models and HEX files are not bundled here.

## Testing and evidence

The author reports successful bench testing of the logic and motor-control behavior. Neither supplied Proteus project has been rerun in this review; no quantitative navigation comparison or complete maze success metric is claimed. Add real schematic exports, hardware photographs, and recorded test conditions to `images/` when available.

## Author and links

**Md. Shahriar Alam Rivon** · Electrical & Electronic Engineering, East West University, Bangladesh  
[GitHub](https://github.com/shahriaralam-rivon) · [LinkedIn](https://www.linkedin.com/in/md-shahriar-alam-rivon-4449aa410/)
