### 📖 Introduction

**Electrostatics** is the branch of physics that deals with the study of static (stationary) electric charges. This chapter lays the foundation by exploring the nature of **electric charge**, the behavior of **charged bodies**, and the **fundamental electric forces** acting between them.

### 🔋 What is Electric Charge?

**Electric Charge** is an intrinsic, fundamental property of matter responsible for generating electric forces between objects.

- **Example:** When two electrons are placed at a small separation, they exert a repulsive electric force on one another solely due to the electric charge they carry.

### ⚛️ Fundamental Properties of Electric Charge

#### 1. Dual Nature (Polarity)

There are two distinct types of electric charges in nature. By convention:
- **Proton ($p^+$):** Assigned a **positive ($+$)** charge.
- **Electron ($e^-$):** Assigned a **negative ($-$)** charge.

#### 2. Fundamental Law of Interaction

- **Like charges repel** each other ($+ \leftrightarrow +$ or $- \leftrightarrow -$).
- **Unlike charges attract** each other ($+ \rightarrow \leftarrow -$).

#### 3. Quantization of Charge

An electrically charged object always possesses an excess or deficiency of a **whole number** of electrons. Because an electron cannot be divided into fractions, the total charge on any body is always an integral multiple of the elementary charge of a single electron.

- _Invalid charges:_ You can never observe a charge equivalent to $0.5$ or $1000.5$ electrons.
- **Mathematical Formulation:**$$q = \pm ne$$
    - $q$ = Total charge on the body
    - $n = 1, 2, 3, \dots$ (number of electrons transferred)
    - $e = 1.6 \times 10^{-19}\text{ C}$ (elementary charge in Coulombs)

#### 4. Conservation of Electric Charge

When an object becomes charged, **no electrons are ever created or destroyed**—they are merely transferred from one material to another. Whether at a macroscopic circuit level or a subatomic nuclear level, the total electric charge of an isolated system remains strictly constant.

#### 5. Relativistic Invariance (Non-Relativistic Nature)

Unlike mass, **electric charge is independent of the velocity of the object**. According to Einstein's Theory of Special Relativity, the mass ($m$) of a moving body varies with its speed ($v$) relative to the speed of light ($c$):
$$m = \frac{m_0}{\sqrt{1 - \frac{v^2}{c^2}}}$$
While mass increases at high velocities, **electric charge remains completely invariant** ($q_{\text{moving}} = q_{\text{rest}}$).


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

> [!info] Electronics = Studying the Electron
> * **Never mess with the nucleus:** Splitting the nucleus is nuclear physics.
> * **Electronics** is strictly the study and management of **electron behavior**—specifically the electrons in the outermost orbital shell.
> * **Neutral Natural State:** In nature, all matter normally has an **equal number of protons and electrons**. Because $+ = -$, they cancel each other out, leaving the atom electrically neutral (balanced).

### 🔢 Atomic Numbers & Weights
* **Atomic Number:** The exact number of **protons** in the nucleus of the atom. Every element has a unique atomic number, which determines its position on the Periodic Table (and equals the number of electrons in a neutral atom).
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
* **Unit of Measure:** **Ampere (Amp)**, represented by the capital letter **$A$**.

### B. The Coulomb ($C$)
Because a single electron is unimaginably tiny, we measure electric charge in bulk "buckets" of electrons called **Coulombs** (named after Charles-Augustin de Coulomb):
* **Symbol:** Capital letter **$C$**.
* **Value of 1 Coulomb:**
  $$1\text{ Coulomb (C)} = 6.24 \times 10^{18}\text{ electrons}$$
  *(Written out: $6,240,000,000,000,000,000$ electrons—like saying "a dozen eggs" or "a gallon of gas," a Coulomb is simply a specific count of electrons).*

### C. The Ampere ($A$)
Named after French physicist André-Marie Ampère, the **Ampere** links charge ($Q$) and time ($t$):
* **Definition:** **1 Ampere** is defined as **1 Coulomb of electrons ($6.24 \times 10^{18}$ electrons) moving past a single point in 1 second**.
* **Mathematical Formula:**
  $$I = \frac{Q}{t}$$
  * $I$ = Current in **Amperes ($\text{A}$)**
  * $Q$ = Electric Charge in **Coulombs ($\text{C}$)**
  * $t$ = Time in **Seconds ($\text{s}$)**
* **Examples & Hardware Meaning:**
  * $1\text{ C/s} = 1\text{ Amp}$
  * $15\text{ C/s} = 15\text{ Amps}$
  * When you pull a **$15\text{A}$ fuse** from a car fuse box or trip a **$15\text{A}$ circuit breaker**, that rating means the wire/fuse is physically designed to handle a maximum of $15 \times (6.24 \times 10^{18})\text{ electrons}$ forced through it every single second before overheating and melting!


