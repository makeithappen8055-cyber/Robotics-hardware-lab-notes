# Day 2: LED Circuits and Basic Microcontroller Programming

## 1. Core Hardware Concepts

* **LED (Light Emitting Diode):** A highly efficient, durable semiconductor light source. They only require a small amount of electricity to operate and can last over 50,000 hours (compared to 1,000 hours for traditional incandescent bulbs).
* **Circuits:** A closed electrical loop. Electricity requires a complete, unbroken path to flow from the power source (microcontroller pin), through components, and back to the return source (Ground/GND). If the path is broken, current will not flow.
* **Resistors:** Components used to limit or slow down the flow of electrical current. LEDs are highly sensitive to current; too much power will burn them out, while too little prevents them from lighting up. A resistor acts as a physical throttle to ensure the exact, safe amount of current reaches the LED.
* **Microcontroller Control:** A microcontroller (like the HERO board) can toggle electrical flow on and off millions of times per second, enabling patterns, signals, and techniques like PWM (Pulse Width Modulation) for dimming.

## 2. The Solderless Breadboard
A prototyping tool used to build and test circuits without soldering.

* **Terminal Strips (Middle Section):** Used for placing components. Holes are connected internally in rows of five. Any component leads plugged into the same 5-hole row are electrically connected to each other.
* **Center Divider (Ravine):** Physically and electrically separates the left and right sides of the terminal strips, preventing accidental short circuits (especially useful for mounting IC chips).
* **Bus Strips (Power Rails):** Located along the long edges. These run the full length of the board to distribute power globally.
  * **Red Line (+):** Positive voltage (Power / 5V).
  * **Blue/Black Line (-):** Ground (Return path / 0V).
* **Orientation:** The board functions identically regardless of orientation. For following standard diagrams, rotate it so the number `1` is at the top.

## 3. Wiring Guidelines & Components

* **Jumper Wires:** Used to make connections. 
  * *Color Coding Convention:* Red for Power (5V), Black for Ground (GND), and other colors (Yellow, Green, etc.) for signal/data lines.
* **Resistor Values:** Standard kits include specific values (220Ω, 1KΩ, 10KΩ, 100KΩ). For standard 5V LED circuits, a **220-ohm** resistor is used.
* **LED Polarity (CRITICAL):** LEDs are polarized diodes, meaning they only allow current to flow in one direction.
  * **Anode (Long Leg):** Positive (+). Must connect toward the power source.
  * **Cathode (Short Leg):** Negative (-). Must connect toward Ground (GND).

### Standard LED Circuit Wiring Steps
1. **LED Anode (Long Leg)** $\rightarrow$ Connects to one end of the 220-ohm resistor.
2. **Resistor (Other End)** $\rightarrow$ Connects to Digital Pin 12 on the board (the switched power source).
3. **LED Cathode (Short Leg)** $\rightarrow$ Connects directly to the GND pin on the board.
*Flow: Pin 12 (5V) $\rightarrow$ Resistor $\rightarrow$ LED Anode $\rightarrow$ LED Cathode $\rightarrow$ GND.*

## 4. Programming Concepts (C++)

* **`#include "Arduino.h"`:** Loads the core libraries and fundamental toolkits required for the microcontroller to understand basic electrical commands.
* **`#define CONSTANT_NAME VALUE`:** Creates a macro/constant (e.g., `#define CABIN_LIGHTS_PIN 12`). It makes code readable and easy to update. Instead of hunting for every "12" in the code, you only change the pin assignment in one place.
* **`void setup() { ... }`:** The initialization block. Runs exactly **once** upon power-up or reset. `void` means it returns no value. Used to configure pin states and initialize systems.
* **`pinMode(pin, mode)`:** Configures a specific pin's electrical behavior. Takes two arguments: the pin number and the mode (e.g., `OUTPUT` to send voltage out).
* **`void loop() { ... }`:** The main program block. Runs continuously in an infinite cycle immediately after `setup()` finishes.
* **`digitalWrite(pin, state)`:** Sets the voltage of a digital pin. 
  * `HIGH`: Outputs approximately 5V (turns the circuit ON).
  * `LOW`: Outputs 0V (turns the circuit OFF).
* **`delay(milliseconds)`:** Pauses the microcontroller's execution for a precise time. `1000` = 1 second. Without delays, the LED would toggle on and off so fast (thousands of times per second) it would just appear dimly lit to the human eye.

## 5. Complete Code Example

```cpp
#include "Arduino.h"

#define CABIN_LIGHTS_PIN 12

void setup() {
  pinMode(CABIN_LIGHTS_PIN, OUTPUT);
}

void loop() {
  digitalWrite(CABIN_LIGHTS_PIN, HIGH); // Turn LED ON
  delay(1000);                          // Wait 1 second
  digitalWrite(CABIN_LIGHTS_PIN, LOW);  // Turn LED OFF
  delay(100);                           // Wait 0.1 seconds
}
```

## 6. Troubleshooting & Best Practices
* **LED remains dark:** 
  1. Check physical connections (ensure legs are in the correct 5-hole rows).
  2. Verify LED polarity (flip the LED around if plugged in backward).
  3. Ensure code uploaded successfully.
  4. Test with the built-in LED (Pin 13) to verify the code logic works independent of external wiring.

## 7. Real-World Applications & Bonus Facts
* **Timing & Patterns:** Modifying `delay()` values creates distinct signals (e.g., Morse code SOS, heartbeat indicators, status blinks).
* **Industry Uses:** Aircraft navigation lights (red/green positioning, white strobes), emergency vehicle flash patterns, and data center server status indicators all rely on these exact digital timing principles.
* **Efficiency:** The International Space Station utilizes over 8,000 LEDs for lighting, consuming 95% less power than traditional fluorescent tubes, freeing up energy for critical systems.