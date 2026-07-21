# Servo Motor Tester

A simple 555-timer-based servo tester designed in KiCad — generates a variable-width pulse signal to manually test and center RC servo motors without needing a microcontroller or transmitter.

## Circuit Overview

- **Pulse generator**: NE555P timer IC (U1) configured to output a PWM-style signal on the SIGNAL pin
- **Pulse width adjustment**: Potentiometer (RV1) lets you sweep the servo across its range by hand
- **Timing components**: Resistors (R2, R3) and capacitor (C1, 22nF) set the timer's frequency and pulse characteristics
- **Reverse polarity protection**: Diode (D1, 1N4148) on the power input
- **Power indicator**: LED (D2) with current-limiting resistor (R1), lit whenever the board is powered
- **Output connector**: 3-pin header (J1) for Signal / Vcc / GND, matching standard servo connector pinout
- **Input connector**: 2-pin header (J2) for DC power input

## Schematic

![Schematic](https://github.com/Noraiz963/Servo-tester/blob/30aeaa3eda645aa48485cb839a36afd55ef2ab6f/Screenshot%202026-07-21%20121913.png)

## PCB Layout

![PCB Layout](https://github.com/Noraiz963/Servo-tester/blob/30aeaa3eda645aa48485cb839a36afd55ef2ab6f/Screenshot%202026-07-21%20121841.png)

## 3D Render

![3D Render](https://github.com/Noraiz963/Servo-tester/blob/30aeaa3eda645aa48485cb839a36afd55ef2ab6f/Screenshot%202026-07-21%20121826.png)

## Bill of Materials

| Ref | Component | Value |
|-----|-----------|-------|
| U1 | Timer IC | NE555P |
| RV1 | Potentiometer | — |
| R1 | Resistor | 1kΩ |
| R2 | Resistor | — |
| R3 | Resistor | 56kΩ |
| C1 | Capacitor | 22nF |
| D1 | Diode | 1N4148 |
| D2 | LED | Power indicator |
| J1 | Header (3-pin) | Signal / Vcc / GND (servo output) |
| J2 | Header (2-pin) | DC input |

## Tools Used

- KiCad 10.0 (schematic capture, PCB layout, 3D visualization)

## Status

Completed — third PCB design project, first design built around an active timing IC (NE555) rather than passive rectification/regulation only.

## Notes

Built as a learning project to practice designing around a general-purpose timer IC and generating a controllable output signal, following on from the two power-supply-focused boards in this series.
