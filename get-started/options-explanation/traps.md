# Traps

## **Under `Ruins.Traps.Fire.<Trap ID>`:**

| Parameters | Explanation                                           | Examples                                                                                                                                                                      |
| ---------- | ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Count      | Duration of spawning particles and the interval of it | `10 10 20 10 40 10`, means `10 ticks particle -> wait 10 ticks -> 20 ticks particle -> wait 10 ticks -> 40 ticks particle -> wait 10 ticks -> ...`                            |
| Particles  | Options of the particle                               | `FLAME 0 0 0 0` means `Flame particle` with `0 x offset`, `0 y offset`, `0 z offset`, some particles have extra data to be configured, it is controlled by the last parameter |
