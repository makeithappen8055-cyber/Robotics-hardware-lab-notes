
---

**Source** : "https://craftingtable.com/courses/30-days-lost-in-space/lessons/2" 
**Curriculum** : "**CraftingTable** — 30 Days Lost in Space (Day 1: Incoming Broadcast)"

---

# 💻 Arduino C++: Core Structure, Functions & Pin Control

> Quick-reference guide covering sketch structure, pin configuration, and digital signal control.

---

## 1. Core Structure & Keywords

* **`void`**
  * **What it means:** A keyword indicating that a function returns no value to the caller—it executes its block and exits
  * **Under the hood:** In standard C++, functions return types like `int` or `float`; `void` explicitly tells the compiler that no data is passed back

* **`setup()`**
  * **What it does:** The initialization function that executes **exactly once** when the board is powered on or reset[
  * **Usage:** Used to configure hardware states (e.g., `pinMode()`), set serial communication baud rates (`Serial.begin()`) or initialize sensor libraries.

* **`loop()`**
  * **What it does:** The main execution block that begins immediately after `setup()` completes
  * **Usage:** Runs continuously in an infinite cycle (`for (;;) { loop(); }` in the hidden C++ `main()` loop) until power is disconnected or a reset triggers
---

## 2. Functions & Pin Configuration

* **`pinMode(pin, mode)`**
  * **What it does:** Sets the electrical role of a digital GPIO pin
  * **Parameters:**
    * `pin`: The physical pin number (`0` to `13` or `A0` to `A5`)[
    * `mode`: `INPUT` (high impedance to measure voltage), `OUTPUT` (low impedance to supply or sink current), or `INPUT_PULLUP` (enables the internal pull-up resistor)
  * **Syntax Example:**
    ```cpp
    pinMode(LED_BUILTIN, OUTPUT); // Sets pin 13 to drive voltage
    ```

* **`digitalWrite(pin, value)`**
  * **What it does:** Sets the voltage state of a pin configured as an `OUTPUT`
  * **Parameters:**
    * `pin`: The pin being driven
    * `value`: `HIGH` (~5V) or `LOW` (0V)
    ```cpp
    digitalWrite(LED_BUILTIN, HIGH); // Powers on the onboard LED
    ```

---

## 3. Parameters, Constants & Timing

* **`HIGH`**
  * **What it means:** Represents digital Logic `1` (supply rail voltage, typically $+5.0\text{V}$ on an Uno)
  * **Circuit effect:** Turns on the internal P-MOSFET to supply current through the pin to a component (like an LED)

* **`LOW`**
  * **What it means:** Represents digital Logic `0` (system ground potential, $0.0\text{V}$)
  * **Circuit effect:** Turns on the internal N-MOSFET to drain current straight to `GND`

* **`delay(ms)`**
  * **What it does:** Halts program execution for a specified duration in milliseconds ($1000\text{ ms} = 1\text{ second}$)
  * **Syntax Example:**
    ```cpp
    delay(1000); // Pauses the CPU for 1000 milliseconds
    ```

---

## 4. Complete Skeleton Sketch

```cpp
// 1. Setup: Runs once at power-on
void setup() {
  pinMode(13, OUTPUT); // Configure Pin 13 as a voltage driver
}

// 2. Loop: Runs over and over indefinitely
void loop() {
  digitalWrite(13, HIGH); // Send +5V (LED ON)
  delay(1000);            // Wait 1 second
  digitalWrite(13, LOW);  // Send 0V (LED OFF)
  delay(1000);            // Wait 1 second
}