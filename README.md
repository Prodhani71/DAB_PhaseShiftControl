# Isolated Dual Active Bridge (DAB) DC-DC Converter

An open-loop simulation model of an isolated, bidirectional Dual Active Bridge (DAB) DC-DC converter developed in MATLAB/Simulink.

The model demonstrates high-frequency power transfer between two active full bridges linked via an isolation transformer and explicit series leakage inductance, using Single Phase Shift (SPS) modulation.

---

## Operating Principle

* **Primary Bridge:** Converts the 400 V DC input into a high-frequency AC square wave.
* **Leakage Inductance & Transformer:** Acts as the main instantaneous energy transfer element while providing galvanic isolation.
* **Secondary Bridge:** Rectifies the high-frequency AC back into DC.
* **Phase Shift Modulation:** Power flow magnitude and direction are controlled by adjusting the phase delay angle between the primary and secondary square waves.

---

## Governing Equation

Power transferred across the leakage inductance under single phase shift operation is defined by:

$$P = \frac{n \cdot V_1 \cdot V_2}{2\pi f_s L_k} \cdot \phi \left(1 - \frac{|\phi|}{\pi}\right)$$

Where:
* $V_1$: Primary DC input voltage (400 V)
* $V_2$: Secondary DC output voltage (360.3 V)
* $n$: Transformer turns ratio
* $f_s$: Switching frequency (20 kHz, period $T_s = 50\ \mu\text{s}$)
* $L_k$: Series leakage inductance
* $\phi$: Phase shift angle (radians)

---

## Simulation Parameters & Results

| Parameter | Value |
| :--- | :--- |
| DC Input Voltage ($V_{in}$) | 400 V |
| Switching Frequency ($f_s$) | 20 kHz |
| Phase Shift Delay | 1.39 us (~10 deg) |
| Output DC Voltage ($V_o$) | 360.3 V |
| Output DC Current ($I_o$) | 3.604 A |
| Delivered Output Power ($P_o$) | 1299 W (~1.3 kW) |

---

