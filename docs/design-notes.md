# Design Notes – EN2091 Function Generator

## 1. Objectives

- Design and implement a function generator capable of producing sine, square, and triangle waveforms.
- Achieve a frequency range of approximately 10 Hz to 100 kHz.
- Provide amplitude and DC offset control at the output.

---

## 2. Component Selection

### Core IC Options

| IC | Notes |
|----|-------|
| **XR2206** | Dedicated function generator IC; easy to use; supports AM/FM |
| **ICL8038** | Classic waveform generator; sine distortion ~1% |
| **Op-Amp based** | Uses integrators + comparators; fully discrete |

### Supporting Components (Typical Values)

| Component | Value / Part | Purpose |
|-----------|-------------|---------|
| R_timing  | 1 kΩ – 100 kΩ | Frequency setting |
| C_timing  | 1 nF – 100 nF | Frequency setting |
| VR1       | 100 kΩ potentiometer | Frequency sweep |
| VR2       | 10 kΩ potentiometer | Amplitude control |
| VR3       | 10 kΩ potentiometer | DC offset |
| Supply    | ±12 V or +5 V | Depending on IC |

---

## 3. Frequency Calculation

For a standard RC relaxation oscillator / timing network:

```
f = 1 / (2 × π × R × C)   [for sine/triangle core]

or

f = 1 / (R × C × k)        [IC-specific formula; see datasheet]
```

**Example** (XR2206):
```
f = 1 / (R_a × C)

With R_a = 10 kΩ, C = 10 nF:
f = 1 / (10×10³ × 10×10⁻⁹) = 10 kHz
```

---

## 4. Output Waveforms

| Output | Method |
|--------|--------|
| Triangle | Integrator of square wave |
| Square | Schmitt trigger / comparator |
| Sine | Diode shaping of triangle or internal IC sine output |

---

## 5. Design Calculations

_(Add your hand calculations, SPICE results, and measured values here.)_

---

## 6. References

- XR2206 / ICL8038 Application Notes
- EN2091 Lab Manual
- Sedra & Smith – *Microelectronic Circuits*
