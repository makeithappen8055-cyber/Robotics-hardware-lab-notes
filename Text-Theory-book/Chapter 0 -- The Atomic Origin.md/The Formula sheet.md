### Quick Reference Matrix

| **Physical Quantity**  | **Symbol** | **SI Unit**                                                              | **Type** | **Governing Equation**                    | **Primary Role in Robotics**                                                   |
| ---------------------- | ---------- | ------------------------------------------------------------------------ | -------- | ----------------------------------------- | ------------------------------------------------------------------------------ |
| **Electric Charge**    | $q, Q$     | Coulomb ($\text{C}$)                                                     | Scalar   | $Q = n \cdot e$                           | The source material property; causes ESD hazards                               |
| **Electric Field**     | $\vec{E}$  | $\text{V/m}$ (in term of potential) or $\text{N/C}$ ( in term of force ) | Vector   | $\vec{E} = -\nabla V = \frac{\vec{F}}{q}$ | Gate control in MOSFETs; capacitive proximity sensing                          |
| **Electric Force**     | $\vec{F}$  | Newton ($\text{N}$)                                                      | Vector   | $\vec{F} = q\vec{E}$                      | Deflects proof masses in MEMS accelerometers/IMUs                              |
| **Electric Potential** | $V$        | Volt ($\text{V}$)                                                        | Scalar   | $V = \frac{W}{Q}$                         | Voltage rails ($3.3\text{V}, 5\text{V}, 12\text{V}$) providing the energy push |
| **Electric Current**   | $I$        | Ampere ($\text{A}$)                                                      | Scalar   | $I = \frac{dQ}{dt} = n e A v_d$           | Flow rate supplying power to actuators and logic                               |

### . Quick Summary Matrix for Instant Reference

| Quantity       | Symbol | Unit        | Physical Meaning                | Under-the-Hood Reality                                |
| -------------- | ------ | ----------- | ------------------------------- | ----------------------------------------------------- |
| **Charge**     | Q      | Coulomb (C) | Quantity of electrical property | Surplus or deficit of electrons (Q=n⋅e)               |
| **Voltage**    | V      | Volt (V)    | Potential difference            | Energy available per Coulomb of charge (J/C)          |
| **Current**    | I      | Ampere (A)  | Rate of flow                    | Number of Coulombs moving per second (C/s)            |
| **Resistance** | R      | Ohm (Ω)     | Opposition to flow              | Friction caused by collisions with the atomic lattice |
| **Power**      | P      | Watt (W)    | Rate of energy transformation   | Heat/light generated per second (P=V⋅I=I2R)           |
