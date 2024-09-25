# Frequently Asked Questions for Matter over Thread

## Demo

  - When using an alternative crystal value (i.e.: different than 39.0 MHz), updating the clock speed for both the HFXO and DPLL values is needed and both must match, where the DPLL is set to 2x the HFXO value. These values are used by the RAIL library to determine the radio frequency and the proper timings for the BLE packets.
  - If the DPLL value is left unchanged with a modified HFXO, the radio will be on the right frequency but the BLE packet timings will not be correct, which will cause issues within a few packets due to BLE's strict timing requirements.
