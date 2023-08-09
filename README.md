# Voron2.4
Backup and config repo for my 2.4



To do:
- Z-joints swap to PETG modified parts --> Print ABS and swap
  - 4x corners
- New PETG x-carrige (single MGN9) CW1 --> Print ABS and swap
- New PETG extruder front (galileo 1) --> Print ABS and swap

- Measure Z-belts and synchronise.
- Mount last corner spacer on bed
- Swap bed tape with alu tape


- Filament calibration (Esun)
  - ABS+ (Black, white) []
  - ABS (green, purple) []
  - PLA []
  - PETG []
  - PETG refillament []  


Use the following to checkout pullrequests 
```Bash
git fetch upstream pull/ID/head && git checkout FETCH_HEAD
```
To revert back to main branch
```Bash
git switch -
```

Note for the pid_v implementation that might be in klipper. Using something like velocity [pid](https://taketake2.com/N23_en.html) seems to make it less good at disturbences but more stable overall. Could be interesting to see an implementation of other PID algos as well.
- I-PD
- PI-D
- 2-pid [Omron](https://assets.omron.eu/downloads/publication/en/v2/2-pid_white_paper_en.pdf) Weightet error/measurement probably
- RRF feedforward with fan speed. [RRF discusion](https://forum.duet3d.com/topic/19761/new-heater-tuning-algorithm/51)

Different autotuning alogs would also be cool, not only the Sigler nichols quarter wave but others as well
