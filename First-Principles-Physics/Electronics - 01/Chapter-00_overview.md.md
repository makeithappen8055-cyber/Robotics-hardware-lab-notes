##**All electrical phenomena emerge from a single property of subatomic particles: **Electric Charge ($Q$ or $q$)**, measured in **Coulombs ($C$)**.

--When we say **"all electrical phenomena,"** we mean **every single event or behavior in the universe that happens because of electric charge ($q$)**—from a bolt of lightning to an LED lighting up, to a microcontroller executing code, down to why your hands don't pass through a solid table.

In classical physics, nature only has four fundamental forces: 
**Gravity**, Strong Nuclear, Weak Nuclear, and **Electromagnetism**.

### 1. The Core Trio: Subatomic Particles

Everything in circuits begins inside the atom. An atom consists of a dense central nucleus surrounded by a cloud of orbiting particles.

```
         Electron Cloud (Orbiting)
               [ - e ]
                 │
           ┌─────┴─────┐
           │  Nucleus  │
           │  [ +e ]   │  <-- Proton
           │  [  0 ]   │  <-- Neutron
           └───────────┘
```

#### A. The Proton ($p^+$)

- **Location:** Locked inside the nucleus.
    
- **Mass:** $1.673 \times 10^{-27}\text{ kg}$ (about $1836\times$ heavier than an electron).
    
- **Intrinsic Charge:** $+1e = +1.602 \times 10^{-19}\text{ C}$.
    
- **Hardware Insight:** Protons do not move through copper wires. They stay fixed in place within the metal crystal lattice. The positive terminal of a battery does not push protons; it attracts electrons.
    

#### B. The Neutron ($n^0$)

- **Location:** Inside the nucleus alongside protons.
    
- **Mass:** $1.675 \times 10^{-27}\text{ kg}$ (nearly identical to a proton).
    
- **Intrinsic Charge:** $0\text{ C}$ (electrically neutral).
    
- **Hardware Insight:** Neutrons provide strong nuclear binding force to keep the positively charged protons from repelling each other violently. In electrical circuits, neutrons are entirely inert.
    

#### C. The Electron ($e^-$)

- **Location:** Orbiting the nucleus in quantum energy shells.
    
- **Mass:** $9.109 \times 10^{-31}\text{ kg}$ (extremely light).
    
- **Intrinsic Charge:** $-1e = -1.602 \times 10^{-19}\text{ C}$.
    
- **Hardware Insight:** Because electrons are extremely light and exist on the outer shell (the **valence shell**), they can be pulled away with very little energy. **All electronics, microcontrollers, and circuit boards operate by manipulating electron motion.**

### 2. Electric Charge ($Q$ or $q$) — _The Source Property_

Charge is not a physical object; it is an **intrinsic property of matter**, just like mass. While mass determines how an object reacts to gravity, charge determines how an object reacts to the electromagnetic force.

- **Unit:** Coulomb ($\text{C}$).
    
- **Quantization:** Charge cannot exist in continuous fractions; it only occurs in integer packets of the elementary charge $e$:
    
    $$Q = n \cdot e \quad (n \in \mathbb{Z})$$
    
- **The Scale:**
    
    $$1\text{ Coulomb} \approx 6.242 \times 10^{18}\text{ electrons}$$
    
- **Core Law (Coulomb's Law):**
    
    Like charges repel; opposite charges attract with a force proportional to the product of charges and inversely proportional to the square of the distance:
    
    $$F = k_e \frac{\vert{}q_1 q_2\vert{}}{r^2}$$ 
### 3. Electric Field ($\vec{E}$) — _The Influence Zone_

- **What it is:** The property that a charge gives to the empty space around it.
    
- **Definition:** Electric force per unit charge:
    
    $$\vec{E} = \frac{\vec{F}}{q} \quad \left(\text{Units: }\frac{\text{Newtons}}{\text{Coulomb}}\text{ or }\frac{\text{Volts}}{\text{meter}}\right)$$
    
- **Nature:** It is a **vector**. It points away from positive charges and toward negative charges.
    
- **Key Reality:** The electric field exists even if no second charge is there to feel it. It represents the _potential to exert force_ on any charge that enters that region.
    




. A Core Trap to Write in Your Notes

- **Charge can exist without current:** A disconnected $9\text{V}$ battery or a charged capacitor holds separated electric charge, but the current is $0\text{A}$ because there is no closed loop for charges to move.
    
- **Current cannot exist without charge:** You cannot have current unless physical charges (electrons in metals, or ions in batteries) are actively moving through a conductor under the influence of an electric field.
- 
### 4. Electric Force ($\vec{F}$) — _The Interaction_

- **What it is:** The actual push or pull experienced between two physical charges.
    
- **Governing Rule (Coulomb's Law):**
    
    $$F = k_e \frac{\vert{}q_1 q_2\vert{}}{r^2}$$
    
- **Nature:** It is a **vector** (has magnitude and direction). Like charges repel; opposites attract.
    
- **Key Reality:** Electric force requires at least **two** charges to exist ($q_1$ and $q_2$). A single charge sitting alone exerts no force on itself.
    



### 5. Electric Potential / Voltage ($V$) — _The Energy Push_

A sea of electrons sitting in a wire does nothing on its own because they move randomly in all directions (thermal motion), yielding zero net flow. To make them move together, we must apply **work**.

- **Definition:** Voltage is the **potential energy difference per unit charge** between two points.
    
    $$V = \frac{\text{Work}}{Q} = \frac{\Delta U}{Q} \quad \left(1\text{ Volt} = 1\frac{\text{Joule}}{\text{Coulomb}}\right)$$
    
- **Deep Insight:** A battery or a $5\text{V}$ Arduino pin is not a "bucket of electrons." It is an **energy pump**.
    
    - A $5\text{V}$ rail means that every Coulomb of charge sitting at that pin has $5\text{ Joules}$ more potential energy than if it were sitting at **Ground ($0\text{V}$)**.
        
    - Ground is simply your arbitrary reference point ($0\text{V}$), like setting the floor as height $h=0$.

### 6. Electric Current ($I$) — _The Flow Rate_

- **Definition:** The rate at which electric charge passes through a cross-section of a conductor over time.
    
    $$I = \frac{dQ}{dt} \quad \left(1\text{ Ampere} = 1\frac{\text{Coulomb}}{\text{second}}\right)$$
    
- **What $1\text{A}$ actually means:**
    
    If your circuit draws $1\text{A}$, exactly $6.242 \times 10^{18}$ electrons cross through that wire every single second.


### Quick Conceptual Map for Your Repo

```
[Proton / Neutron / Electron]  (Subatomic Matter)
            │
            ▼
     [Electric Charge]         (The intrinsic property)
            │
            ▼
     [Electric Field]          (Influence radiating through space)
            │
            ▼
      [Electric Force]         (Push/pull felt when charges interact)
            │
            ▼
    [Electric Potential (V)]   (Energy per charge / Voltage push)
            │
            ▼
     [Electric Current (I)]    (Rate of charge flow through wires)
            │
            ▼
      [Electromagnetism]       (Moving charges generate magnetic fields -> Motors turn)
```

### Quick Reference Matrix

| **Physical Quantity**  | **Symbol** | **SI Unit**                                                              | **Type** | **Governing Equation**                    | **Primary Role in Robotics**                                                   |
| ---------------------- | ---------- | ------------------------------------------------------------------------ | -------- | ----------------------------------------- | ------------------------------------------------------------------------------ |
| **Electric Charge**    | $q, Q$     | Coulomb ($\text{C}$)                                                     | Scalar   | $Q = n \cdot e$                           | The source material property; causes ESD hazards                               |
| **Electric Field**     | $\vec{E}$  | $\text{V/m}$ (in term of potential) or $\text{N/C}$ ( in term of force ) | Vector   | $\vec{E} = -\nabla V = \frac{\vec{F}}{q}$ | Gate control in MOSFETs; capacitive proximity sensing                          |
| **Electric Force**     | $\vec{F}$  | Newton ($\text{N}$)                                                      | Vector   | $\vec{F} = q\vec{E}$                      | Deflects proof masses in MEMS accelerometers/IMUs                              |
| **Electric Potential** | $V$        | Volt ($\text{V}$)                                                        | Scalar   | $V = \frac{W}{Q}$                         | Voltage rails ($3.3\text{V}, 5\text{V}, 12\text{V}$) providing the energy push |
| **Electric Current**   | $I$        | Ampere ($\text{A}$)                                                      | Scalar   | $I = \frac{dQ}{dt} = n e A v_d$           | Flow rate supplying power to actuators and logic                               |
