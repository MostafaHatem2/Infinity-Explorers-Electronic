# Three-Stage Common-Emitter Amplifier

**Team Infinity Explorers 2**  
_Supervised by Dr. Mostafa Wageh and Eng. Mohamed Tawhid_

---

## 📝 Description

A three-stage BJT common-emitter amplifier using **2N2222 NPN transistors**, designed to amplify weak AC signals (e.g., audio). The circuit achieves high voltage and current gain through cascaded stages, direct coupling, and bypass capacitors. Applications include audio amplification and communication systems.

---

## 🛠️ Circuit Components

### **Core Components**

- **Transistors**: Q1, Q2, Q3 (2N2222 NPN) in common-emitter configuration.
- **Resistors**:
  - Stage 1: R1 (47 kΩ), R2 (4.7 kΩ), R3 (4.7 kΩ), R4 (820 Ω).
  - Stages 2 & 3: Similar resistor configurations (R6–R12).
- **Capacitors**:
  - Coupling: C1 (100 µF), C2 (100 µF), C3 (50 µF), C4 (22 µF).
  - Bypass: C5–C7 (4.7 µF) across emitter resistors.
- **Output Load**: 8Ω speaker.

### **Key Features**

- Direct coupling between stages for signal continuity.
- Bypass capacitors to enhance AC gain.
- Biasing resistors to stabilize DC operating points.

---

## 🔧 Circuit Design and Operation

### **Design Principles**

1. **Biasing**: Resistors set DC operating points (e.g., VB ≈ 1.09V for Q1).
2. **Coupling**: Capacitors transfer AC signals while blocking DC offsets.
3. **Bypassing**: Emitter capacitors (C5–C7) reduce AC feedback, boosting gain.

### **Operation Flow**

1. **Input Signal**: AC signal (e.g., 1 mV) coupled via C1 to Q1.
2. **Stage 1**: Amplifies signal (gain ≈ -85).
3. **Stage 2 & 3**: Further amplify the signal (total gain ≈ -632,954).
4. **Output**: Drives an 8Ω speaker via C4.

---

## 🚧 Challenges Faced

1. **No Amplification**: Caused by a damaged transistor. **Fix**: Replaced faulty component.
2. **Weak/Unclear Output**: Signal loss due to emitter resistors. **Fix**: Added bypass capacitors (C5–C7).
3. **Transistor Suitability**: 2N3904 transistors failed under continuous operation. **Fix**: Upgraded to 2N2222.

---

## 📊 DC and AC Analysis

### **DC Analysis (Q1 Example)**

- **Base Voltage (VB)**: \( 12V \times \frac{4.7kΩ}{47kΩ + 4.7kΩ} ≈ 1.09V \)
- **Emitter Current (IE)**: \( \frac{0.39V}{820Ω} ≈ 0.475 \, \text{mA} \)
- **Collector Voltage (VC)**: \( 12V - (0.475 \, \text{mA} \times 4.7kΩ) ≈ 9.77V \)

### **AC Analysis**

- **Transconductance (gm)**: \( \frac{0.475 \, \text{mA}}{26 \, \text{mV}} ≈ 18.27 \, \text{mS} \)
- **Voltage Gain per Stage**: \( -g_m \times R_C ≈ -85.86 \)
- **Total Gain**: \( (-85.86)^3 ≈ -632,954 \)

---

## 🎯 Conclusion

The amplifier successfully demonstrates multi-stage signal amplification with stable DC biasing and high AC gain. Applications include audio systems and communication circuits.

---

## 🔮 Future Improvements

1. **Frequency Response**: Use smaller capacitors (e.g., 1 µF) for high-frequency signals.
2. **Distortion Reduction**: Implement negative feedback networks.
3. **Impedance Matching**: Optimize resistor values for the 8Ω speaker.

---

## 📚 References

1. Sedra & Smith, _Microelectronic Circuits_ (7th ed.).
2. Floyd, _Electronic Devices_ (9th ed.).
3. Beni-Suef University Lecture Notes.
