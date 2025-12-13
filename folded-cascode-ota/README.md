# Folded-Cascode Fully Differential OTA

## 📌 Project Overview
This project presents the **design, implementation, and verification of a folded-cascode fully differential Operational Transconductance Amplifier (OTA)** with a **Class-AB output stage**.  
The design was carried out at the **transistor level** and verified using industry-standard analog simulation techniques.

The OTA is intended for **low-noise, high-gain, mixed-signal applications**, such as data converters and continuous-time filters.

---

## 🧠 Architecture Description
A folded-cascode topology is selected to achieve:
- High open-loop gain
- Wide input common-mode range
- Improved output swing
- Good noise and supply rejection

A Class-AB output stage is used to enhance **large-signal drive capability** and **slew rate** while maintaining low quiescent power.

![Folded Cascode OTA Schematic](figures/folded_cascode_schematic.png)

---

## ⚙️ Biasing Network
A dedicated biasing circuit generates the required bias voltages for:
- Input differential pair
- Cascode devices
- Output stage

The bias network ensures stable DC operating points across the amplifier.

![Biasing Circuit](figures/biasing_circuit.png)

---

## 🧪 Testbench Configuration
The OTA is verified using multiple testbenches including:
- AC small-signal analysis
- Transient large-signal analysis
- Unity-gain follower configuration
- Supply and common-mode perturbation setups

![OTA Testbench](figures/ota_testbench.png)

---

## 📈 AC Gain & Phase Response
The open-loop AC response confirms:
- High DC gain
- Stable frequency response
- Adequate phase margin for closed-loop operation

![AC Gain and Phase Response](results/ac_gain_phase_response.png)

---

## ⏱️ Transient Response
Transient simulations were performed with sinusoidal inputs to verify:
- Linear operation
- Symmetry of differential outputs
- Output swing limits

![Transient Response](results/transient_response.png)

---

### Common-Mode Sweep Verification
The amplifier was tested across different common-mode voltages to ensure robust operation.

![Transient Response at Vcm = 1V](results/transient_response_vcm_1v.jpg)

---

## ⚡ Slew Rate Measurement
The slew rate was measured by configuring the OTA as a **unity-gain follower** and applying a step input using a PWL source.

- Load capacitance: 1 pF
- Large-signal linear ramp observed at the output

![Slew Rate Response](results/slew_rate_response.png)

---

## 🔁 Common-Mode Rejection Ratio (CMRR)
CMRR was evaluated by applying a common-mode AC input while monitoring the differential output response.

Key observation:
- High low-frequency CMRR indicating strong common-mode suppression

![CMRR Response](results/cmrr_response.jpg)

---

## 🔌 Power Supply Rejection Ratio (PSRR)
PSRR was measured by injecting an AC ripple on the supply rail while grounding the signal input.

Key observations:
- High PSRR at low frequencies
- Degradation at higher frequencies due to reduced loop gain

![PSRR Response](results/psrr_response.jpg)

---

## 📊 Key Performance Summary

| Parameter | Value |
|--------|------|
| Architecture | Folded-cascode fully differential OTA |
| Output stage | Class-AB |
| Supply voltage | 3 V |
| DC gain | > 100 dB |
| Slew rate | ~10 V/µs (1 pF load) |
| Stability | Stable with capacitive load |
| CMRR | High (low-frequency) |
| PSRR | High (low-frequency) |

---

## 🛠 Tools Used
- Cadence Virtuoso
- Spectre Simulator
- Analog Design Environment (ADE)

---

## 👤 Author
**Pankaj Wavre**  
Analog IC Design • CMOS Circuit Design • Mixed-Signal Systems  
🔗 [LinkedIn](https://www.linkedin.com/in/pankajwavre/)  
🔗 [GitHub](https://github.com/pankjawavre)
