# Navigation logic and motor-control reference

This document records the **author-described navigation policy**, not an independently simulated truth-table extraction of the supplied binary Proteus schematic.

Define `F`, `L`, `R` as **1 when that direction is clear**, and `0 when blocked`. The IR sensors were described as active-low obstacle outputs; verify each actual module's polarity and inversion before wiring.

| F | L | R | Action |
| :-: | :-: | :-: | --- |
| 1 | X | X | Forward |
| 0 | 1 | X | Left |
| 0 | 0 | 1 | Right |
| 0 | 0 | 0 | Stop |

From that policy, ideal action-select expressions are:

```text
FORWARD = F
LEFT    = NOT(F) AND L
RIGHT   = NOT(F) AND NOT(L) AND R
STOP    = NOT(F) AND NOT(L) AND NOT(R)
```

The mapping documented for the two TB6612FNG motor channels is:

| Action | AIN1 | AIN2 | BIN1 | BIN2 |
| --- | :-: | :-: | :-: | :-: |
| Forward | H | L | H | L |
| Left | L | H | H | L |
| Right | H | L | L | H |
| Stop | L | L | L | L |

`STBY`, `PWMA` and `PWMB` must also be driven to appropriate enabled levels for motor movement. The direction table describes commanded channel polarities; reversing a motor's wiring changes its physical turning direction.

The Proteus schematic lists `74HC08`; the author previously listed `74LS08` for the real hardware. Treat the logic-family discrepancy as unverified until the build is checked. Do not substitute HC/LS parts without checking valid input/output levels and fanout in the actual circuit.
