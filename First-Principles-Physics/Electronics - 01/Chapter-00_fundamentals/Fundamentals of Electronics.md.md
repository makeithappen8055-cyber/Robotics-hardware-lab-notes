
# ⚡ Chapter 1: Fundamentals of Electricity (Part 1)

> [!quote] Engineering Philosophy
> *"To truly invent new hardware, one must not merely connect components—one must understand the physical laws governing them down to the electron level."*[cite: 2]
> 
> **Source Lecture:** [Basic Electronics Part 1 (ELC 110 - Joe Gryniuk)](https://www.youtube.com/watch?v=nb4ovfwqup8)

---

## 🎯 The "Big Four" of Electronics
Every electrical or electronic system—from a smartphone and automotive ECU to a satellite or robot—operates because of **four fundamental properties**:
1. **Voltage ($V$ or $E$)** – Electrical pressure / Electromotive Force.
2. **Current ($I$)** – The directed flow of electrons.
3. **Resistance ($R$)** – The opposition to current flow.
4. **Power ($P$)** – The rate at which electrical work is performed.

> [!tip] Diagnostic Rule
> If a circuit fails to operate on the bench, it is **always** because Voltage, Current, Resistance, or Power is not doing what it is supposed to be doing.

---

## 🌌 1. Matter, Elements & Atomic Structure

Everything in electricity and electronics is traceable back to **matter**. To extract electricity from matter, we first have to understand how matter is built:

* **Matter:** Anything that occupies space and has weight (mass).
* **Vacuum (Absence of Matter):** Empty space where all matter/gases have been pumped out of a vessel (industrial vacuum) or outer space. Used heavily in semiconductor and high-tech manufacturing so only desired materials enter the chamber.
* **Element:** The basic building block of nature that cannot be reduced to a simpler substance by chemical means. Found on the **Periodic Table** (~100+ known elements make up everything in the universe).
* **Atom:** The smallest particle an element can be broken down into while still retaining its chemical identity.

### ⚛️ Anatomy of an Atom
An atom consists of a central region and three fundamental subatomic particles:

| Component | Type | Charge | Location & Physical Scale |
| :--- | :--- | :--- | :--- |
| **Nucleus** | *Place* (Not a particle) | Net Positive | The dead center of the atom where protons and neutrons live. |
| **Proton ($p^+$)** | Subatomic Particle | **Positive ($+$)** | Located inside the nucleus. Very large and heavy. |
| **Neutron ($n^0$)** | Subatomic Particle | **Neutral ($0$)** *(Uncharged)* | Located inside the nucleus. Very large and heavy. |
| **Electron ($e^-$)** | Subatomic Particle | **Negative ($-$)** | Orbits far outside the nucleus at high speed. Extremely tiny (almost zero mass compared to protons). |
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

> [!info] Electronics = Studying the Electron
> * **Never mess with the nucleus:** Splitting the nucleus is nuclear physics.
> * **Electronics** is strictly the study and management of **electron behavior**—specifically the electrons in the outermost orbital shell.
> * **Neutral Natural State:** In nature, all matter normally has an **equal number of protons and electrons**. Because $+ = -$, they cancel each other out, leaving the atom electrically neutral (balanced).

### 🔢 Atomic Numbers & Weights
* **Atomic Number:** The exact number of **protons** in the nucleus of the atom. Every element has a unique atomic number, which determines its position on the Periodic Table (and equals the number of electrons in a neutral atom)

* **Atomic Weight:** The physical mass of the atom, determined by counting the **total number of protons + neutrons** in the nucleus (the mass of the electrons is so tiny it is ignored).

---

## 🪐 2. Electron Shells & The Valence Shell

* **Shells:** Concentric circular orbital paths around the nucleus where electrons reside.
* **The Parking Garage Analogy:** Electrons fill shells in sequence from the inside out—just like cars parking on the first floor of a garage until it is full, then moving up to the second floor, and so on.
* **Shell Naming Convention:** Shells are labeled alphabetically starting with the letter **$K$** (innermost shell closest to the nucleus) outward to **$Q$** (outermost shell of the most complex known elements):
  $$\text{Nucleus} \rightarrow \mathbf{K} \rightarrow \mathbf{L} \rightarrow \mathbf{M} \rightarrow \mathbf{N} \rightarrow \mathbf{O} \rightarrow \mathbf{P} \rightarrow \mathbf{Q}$$

### 🔥 The Valence Shell (Where the Action Happens)
* **Valence Shell:** The **outermost shell** of an atom containing electrons.
* **Valence:** The **number of electrons** contained inside that outermost valence shell.
* **Why Subatomic Structure Matters in Hardware:**
  1. It defines the **electrical properties of materials** (Conductors vs. Insulators vs. Semiconductors).
  2. It explains **where Voltage comes from**.

---

## 🔌 3. Conductors, Insulators, Semiconductors & Superconductors

In electronics, we classify every material by **how many electrons sit in its Valence Shell**:

| Material Class | Valence Electrons | How It Behaves Electrically | Common Materials (In Order of Precedence / Quality) |
| :--- | :---: | :--- | :--- |
| **Conductors** | **$\le 3$** *(3 or fewer)* | Readily accepts the flow of electrons; contains a large number of free electrons ("open parking spaces"). | 1. **Silver** *(Best in nature)*<br>2. **Copper**<br>3. **Gold**<br>4. **Aluminum**<br>5. **Tungsten**<br>6. **Iron**<br>7. **Nichrome** |
| **Semiconductors** | **$= 4$** *(Exactly 4)* | Can be altered to function as **either** a conductor or an insulator. The fundamental building block of **diodes, transistors, and microprocessors**. | 1. **Silicon** *(Most prevalent)*<br>2. **Germanium**<br>3. **Carbon** |
| **Insulators** | **$\ge 5$** *(5 or more)* | Prevents the flow of electricity; stabilized by absorbing valence electrons ("parking lot is full"). | 1. **Mica** *(Best in nature)*<br>2. **Glass**<br>3. **Teflon**<br>4. **Paper / Wax Paper**<br>5. **Rubber**<br>6. **Bakelite**<br>7. **Oils**<br>8. **Porcelain**<br>9. **Air** |
| **Superconductors** | *Cryogenic State* | Materials that exhibit **zero electrical resistance ($0\ \Omega$)** when cooled to extreme cryogenic temperatures. | **Ceramics** *(Best results in labs at cryogenic temperatures)* |

> [!bug] Hardware Bench Insights: Materials in the Real World
> * **Why Gold-Plated Connectors?** Silver is the best conductor in nature, and Copper is #2, but both **oxidize (corrode)** when exposed to oxygen in the air. **Gold (#3) does not oxidize or corrode**. Plating copper pins/pads with gold gives you copper's conductivity with a corrosion-free, highly reliable contact surface (pioneered by NASA for spacecraft interconnects).
> * **Why Oil & Mica in Electronics?**
>   * **Mica:** A flaky, rock-formed mineral that is both the best natural electrical insulator and a great thermal conductor (used as insulating washers behind hot power transistors).
>   * **Oil:** Acts as an electrical insulator while drawing heat away from submerged high-power transformers or overclocked processors.
> * **Humid Air Breakdown:** Air is normally an insulator between overhead high-voltage power lines, but on damp/humid days you can hear it crackling (corona discharge) as its insulating quality drops.

---

## ⚡ 4. Ionization: How Electricity & Voltage Are Created

How do we turn neutral matter into usable electricity? **By knocking valence electrons loose!**

1. **Neutral State:** A plastic calculator sitting on a desk has an equal number of protons ($+$) and electrons ($-$). Net charge = $0$.
2. **Applying Energy:** When we rub the calculator with a cloth, we apply **mechanical friction (energy)** to the matter, knocking electrons off the **valence shell** of the calculator and transferring them onto the cloth.
3. **Ionization (The Process of Gaining or Losing Electrons):**
   * **Positive Ion ($+$):** The atom/object that **lost electrons**. It now has more protons than electrons, giving it a net **positive charge**.
   * **Negative Ion ($-$):** The atom/object that **gained extra electrons**. It now has more electrons than protons, giving it a net **negative charge**.
4. **Creating Voltage & Current:**
   * Once separated, the excess electrons on the negative side desperately want to jump back to the positive ions to return to their **neutral natural state**.
   * Instead of letting them jump directly back (which is a **Short Circuit**), we place a **circuit and a load** (like a light bulb or motor) in between. We force the electrons to travel through our circuit and do useful work for us on their way back to neutrality!

> [!important] Core Principle of Electricity Generation
>$$\text{Apply Energy to Matter} \longrightarrow \text{Ionization (Separate Valence } e^-\text{)} \longrightarrow \text{Creates Voltage (Potential)} \longrightarrow \text{Drives Current Flow}$$

---

## 🌊 5. Current, The Coulomb & The Ampere

### A. Electric Current ($I$)
* **Definition:** The movement/flow of electrons from **negatively charged atoms to positively charged atoms** ($\text{Negative} \longrightarrow \text{Positive}$) as they seek to return to a neutral natural state.
* **Symbol / Abbreviation:** Capital letter **$I$** (for Intensity).
* **Unit of Measure:** **Ampere (Amp)**, represented by the capital letter **$A$**

- **Definition:** The rate at which electric charge passes through a cross-section of a conductor over time.
    
    $$I = \frac{dQ}{dt} \quad \left(1\text{ Ampere} = 1\frac{\text{Coulomb}}{\text{second}}\right)$$
    
- **What $1\text{A}$ actually means:**
    
    If your circuit draws $1\text{A}$, exactly $6.242 \times 10^{18}$ electrons cross through that wire every single second.

### B. The Coulomb ($C$)
Because a single electron is unimaginably tiny, we measure electric charge in bulk "buckets" of electrons called **Coulombs** (named after Charles-Augustin de Coulomb):
* **Symbol:** Capital letter **$C$**.
* **Value of 1 Coulomb:**
  $$1\text{ Coulomb (C)} = 6.24 \times 10^{18}\text{ electrons}$$
  *(Written out: $6,240,000,000,000,000,000$ electrons—like saying "a dozen eggs" or "a gallon of gas," a Coulomb is simply a specific count of electrons).*

### C. The Ampere ($A$)
Named after French physicist André-Marie Ampère, the **Ampere** links charge ($Q$) and time ($t$):
* **Definition:** 
* 
*            **1 Ampere** is defined as **1 Coulomb of electrons ($6.24 \times 10^{18}$ electrons) moving past a single point in 1 second**.
* 
* **Mathematical Formula:**
  $$I = \frac{Q}{t}$$
  * $I$ = Current in **Amperes ($\text{A}$)**
  * $Q$ = Electric Charge in **Coulombs ($\text{C}$)**
  * $t$ = Time in **Seconds ($\text{s}$)**
* **Examples & Hardware Meaning:**
  * $1\text{ C/s} = 1\text{ Amp}$
  * $15\text{ C/s} = 15\text{ Amps}$
  * When you pull a **$15\text{A}$ fuse** from a car fuse box or trip a **$15\text{A}$ circuit breaker**, that rating means the wire/fuse is physically designed to handle a maximum of $15 \times (6.24 \times 10^{18})\text{ electrons}$ forced through it every single second before overheating and melting!



---

## 🔋 6. Potential, Electromotive Force (EMF) & Voltage

* **Electric Potential (Potential Difference):** The ability of a source to perform electrical work. It is the electrical pressure or "pump" that forces electrons to move or flow through a circuit.

* **Synonyms:** Electromotive Force (EMF), Difference of Potential, Voltage.

* **Symbols:** Capital letter **$E$** or **$V$**.
* **Unit of Measure:** **Volt ($\text{V}$)**, named after Alessandro Volta.

---

## 🧱 7. Resistance ($R$) & Ohm's Law

### A. Resistance
* **Definition:** The physical opposition to the flow of electrons through a material.

* **Symbol:** Capital letter **$R$**.

* **Unit of Measure:** **Ohm ($\Omega$)**, named after Georg Simon Ohm, represented by the Greek letter Omega ($\Omega$).

* **What Has Resistance?** **Everything.** Conductors have low resistance, insulators have massive resistance, and *everything* in between has resistance (except ideal superconductors existing only under low-temperature laboratory conditions).
* **Factors Affecting Resistance:** Size (length and cross-sectional area) and temperature.



---


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


### Quick Conceptual Map 

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
