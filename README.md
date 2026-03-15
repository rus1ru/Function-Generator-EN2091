# Function Generator – EN2091

**3rd Semester Analog Electronics Project**
Department of Electronic and Telecommunication Engineering

---

## Overview

This repository contains all design files, simulation results, schematics, and documentation for the **EN2091 Function Generator** project. The function generator is capable of producing **sine**, **square**, and **triangular** waveforms across a selectable range of frequencies and amplitudes.

---

## Features

- Output waveforms: **Sine**, **Square**, **Triangle**
- Frequency range: ~**10 Hz – 100 kHz** (tunable)
- Amplitude control via potentiometer
- DC offset adjustment
- Duty-cycle control for square wave output
- Built around the **ICL8038** / **XR2206** waveform generator IC (or op-amp based design)

---

## Repository Structure

```
Function-Generator-EN2091/
├── schematics/          # Circuit schematics (KiCad / Eagle / PDF)
├── simulation/          # SPICE / LTspice simulation files
├── docs/                # Design notes, calculations, and theory
├── datasheets/          # IC and component datasheets
├── reports/             # Lab reports and project report
├── images/              # Photos, screenshots, waveform captures
└── README.md
```

---

## Getting Started

### Prerequisites

To open and edit the design files you may need:

| Tool | Purpose |
|------|---------|
| [KiCad](https://www.kicad.org/) | Schematic & PCB layout |
| [LTspice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) | Circuit simulation |
| Any PDF viewer | Viewing schematics / datasheets |

### Cloning the Repository

```bash
git clone https://github.com/rus1ru/Function-Generator-EN2091.git
cd Function-Generator-EN2091
```

---

## Circuit Description

The function generator is designed using the following building blocks:

1. **Waveform Generation Core** – generates the primary triangle/sine wave using a waveform generator IC or a relaxation oscillator built with op-amps.
2. **Square Wave Output** – derived from the Schmitt trigger / comparator stage.
3. **Sine Wave Shaping** – triangle-to-sine conversion using a differential amplifier or diode shaping network.
4. **Frequency Control** – RC network with a variable resistor (potentiometer) to sweep frequency.
5. **Amplitude & Offset Control** – output stage with gain adjustment and DC offset capability.

---

## Block Diagram

```
 ┌──────────────────────────────────────────────────────┐
 │                   Function Generator                  │
 │                                                       │
 │  ┌───────────┐    ┌──────────────┐   ┌────────────┐  │
 │  │ Frequency │───▶│  Waveform    │──▶│  Triangle  │  │
 │  │  Control  │    │  Generator   │   │   Output   │  │
 │  └───────────┘    │    Core      │   └────────────┘  │
 │                   │              │──▶┌────────────┐  │
 │  ┌───────────┐    │              │   │   Square   │  │
 │  │ Amplitude │───▶│              │   │   Output   │  │
 │  │  Control  │    └──────┬───────┘   └────────────┘  │
 │  └───────────┘           │                            │
 │                          ▼                            │
 │                   ┌──────────────┐   ┌────────────┐  │
 │                   │  Sine-Shape  │──▶│    Sine    │  │
 │                   │   Network    │   │   Output   │  │
 │                   └──────────────┘   └────────────┘  │
 └──────────────────────────────────────────────────────┘
```

---

## Team Members

| Name | Index Number |
|------|-------------|
| _(Add team member names here)_ | |

**Module:** EN2091 – Analog Electronics Laboratory  
**Semester:** 3rd Semester  
**Academic Year:** _(Add year)_

---

## Progress

- [ ] Literature review and component selection
- [ ] Circuit design and calculations
- [ ] Schematic capture
- [ ] Simulation and verification
- [ ] PCB layout (if applicable)
- [ ] Hardware construction and testing
- [ ] Final report

---

## References

- Horowitz, P. & Hill, W. – *The Art of Electronics*, 3rd Edition
- ICL8038 / XR2206 Datasheet
- EN2091 Lab Manual

---

## License

This project is for academic purposes as part of the EN2091 module.
