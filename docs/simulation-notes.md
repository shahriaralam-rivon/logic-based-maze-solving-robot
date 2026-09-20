# Simulation notes and dependency checkpoint

**Status:** File integrity and embedded schematic structure checked; **Proteus run, waveform checks, and output screenshots not performed**.

1. Use Proteus 8.13 or an installed compatible version; open the `.pdsprj` directly. Each archived project contains an embedded `ROOT.DSN` and `PROJECT.XML`.
2. Verify that installed models for logic ICs and `TB6612FNG` are present, and confirm each sensor's expected active level.
3. Open the `logic-only` variant first; check motor driver `STBY`, `PWMA`, `PWMB` and power rails. Test the eight possible front/left/right input combinations against `docs/navigation-logic.md`.
4. The `ultrasonic-experiment` variant references **`UltraSonicSensor.HEX`**, which was **not supplied** directly in the source archive. The archive does include `UltraSonicTEP.HEX`, but its ownership/license and runtime need remain unverified. Do not distribute either as a claim of complete standalone simulation.
5. Record any missing model errors and results, export an authentic circuit screenshot, and update README results only after confirming real behavior.

No hardware photo, measured current, timing trace, or reliable head-to-head performance number was supplied for this audit. Do not fabricate these artifacts.
