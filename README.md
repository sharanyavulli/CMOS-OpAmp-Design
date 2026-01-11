# Telescopic Operational Amplifier Design

A two-stage telescopic operational amplifier designed in SCL 180nm CMOS technology, optimized for low-power and moderate-voltage analog applications.

## Authors

- Krishna Gorai (T25111)
- Vani (B23505)
- Sharanya (B23506)

**Institution:** School of Computing and Electrical Engineering, IIT Mandi

---

## Overview

This project presents a comprehensive design and simulation of a telescopic operational amplifier that achieves high intrinsic gain and wide bandwidth while maintaining low power dissipation. The amplifier employs a telescopic cascode architecture with Miller compensation to ensure closed-loop stability.

### Key Features

- **High Differential Gain:** 102 dB
- **Excellent CMRR:** 106 dB
- **Low Power Consumption:** 58.482 µW
- **Stable Operation:** 58° phase margin
- **Unity-Gain Bandwidth:** 610.2 kHz

---

## Design Specifications

### Operating Conditions

| Parameter | Value |
|-----------|-------|
| Supply Voltage (VDD) | 1.8 V |
| Load Capacitance (CL) | 1 pF |
| Input Common-Mode Voltage | 500 mV |
| Technology | SCL 180nm CMOS |

### Transistor Dimensions

| Transistor(s) | W/L (µm) | Purpose |
|---------------|----------|---------|
| M1, M2 | 0.42/4 | Input differential pair |
| M3, M4 | 0.42/2 | Cascode transistors |
| M5–M8 | 0.42/1 | Load and bias branches |
| M9 | 0.42/0.2 | High current density support |
| M10, M11 | 5/2 | Bias voltage generation |
| M12–M15 | 0.42/0.54 | Current mirroring |

---

## Performance Summary

| Parameter | Value |
|-----------|-------|
| Differential Gain | 102 dB |
| Common-Mode Gain | −4 dB |
| CMRR | 106 dB |
| Unity-Gain Bandwidth (UGBW) | 610.2 kHz |
| Phase Margin | 58° |
| PSRR | 71 dB |
| Slew Rate | 0.44 V/µs |
| ICMR (min–max) | 0.499–0.810 V |
| OCMR (min–max) | 0.553–0.873 V |
| Power Dissipation | 58.482 µW |

---

## Architecture

### Amplifier Topology

The design utilizes a **two-stage telescopic cascode** architecture that provides:

- High output resistance through cascoded transistors
- Enhanced intrinsic gain in a single signal path
- Relatively simple structure with low power consumption

### Compensation Technique

**Miller compensation** is implemented using a 1 pF capacitor between the first and second stages to:

- Introduce a dominant pole at low frequency
- Achieve adequate phase margin for stable closed-loop operation
- Ensure system stability across operating conditions

### Biasing Circuit

A dedicated biasing network generates stable bias voltages (vbias1, nbias) to ensure reliable operation across process and voltage variations.

---

## Simulation Results

### AC Analysis

- **Differential Gain:** 102 dB at low frequency with 0 dB crossover at 610.2 kHz
- **Common-Mode Gain:** −4 dB, confirming effective suppression
- **CMRR:** 106 dB, indicating excellent differential-to-common-mode signal rejection
- **Phase Margin:** 58° at unity-gain frequency
- **PSRR:** 71 dB at low frequency

### Transient Analysis

- **Slew Rate:** 0.44 V/µs (measured from unity-gain feedback configuration)
- Stable square-wave response with minimal distortion

### DC Analysis

- **ICMR Range:** 0.499 V to 0.810 V
- **OCMR Range:** 0.553 V to 0.873 V
- All transistors maintained in saturation over the operating range

---

## Applications

This telescopic op-amp is well-suited for:

- Sensor interfaces
- Data converters (ADCs/DACs)
- Sample-and-hold circuits
- Precision analog front-end circuits
- Low-power analog integrated circuits

---

## Design Challenges & Tradeoffs

The telescopic topology inherently faces:

- **Limited voltage headroom** restricting ICMR and output swing
- **Supply voltage constraints** in low-voltage CMOS technologies
- **Tradeoffs** between gain, swing, stability, and power dissipation

These challenges were addressed through:

- Careful device sizing and aspect ratio selection
- Proper biasing network design
- Miller compensation for stability
- Optimization for 1.8V supply operation

---

## Conclusion

The proposed two-stage telescopic operational amplifier successfully demonstrates that careful design considerations enable the telescopic architecture to remain a viable and efficient solution for low-power and moderate-voltage analog applications. Despite inherent swing limitations, the design achieves excellent gain, stability, and power efficiency through optimized device sizing, biasing, and compensation techniques.

---

## References

1. Adel S. Sedra and Kenneth C. Smith, "Microelectronic Circuits," 7th Edition, Oxford University Press, 2015.
2. Behzad Razavi, "Design of Analog CMOS Integrated Circuits," McGraw Hill, 2001.
3. Jan M. Rabaey, "Digital Integrated Circuits: A Design Perspective," 2nd Edition, Prentice Hall, 2002.
