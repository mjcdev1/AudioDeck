<!--
COLLAPSIBLE CHANGELOG ENTRY TEMPLATE

<details>
<summary><strong>Prototype X.X — YYYY/MM/DD</strong></summary>

- Main change
  - Sub change
  - Sub change

- Another main change
  - Sub change

</details>

-->

# Changelog!

## 🔌 HARDWARE — Prototype 0.3

### ENCLOSURE

<details>
<summary><strong>Prototype 0.3</strong></summary>

#### 2026/05/19
- Added four additional LED slots
- Added slot for a second ON-OFF-ON SPDT toggle

</details>

<details>
<summary><strong>Prototype 0.2</strong></summary>

#### 2026/05/12
- Added three additional LED slots
- Added slot for an ON-OFF-ON SPDT toggle switch
- Tested fitment of all component cutouts using 3D printed test pieces
  - Adjusted EC11 cutouts for improved fitment

</details>

<details>
<summary><strong>Prototype 0.1</strong></summary>

#### 2026/05/10
- Designed initial prototyping plate with mounts and cutouts for all planned components
  - Created individual fit-test cutouts before printing the full plate

</details>

### ELECTRONICS

<details>
<summary><strong>Prototype 0.5 </strong></summary>

#### 2026/05/19

- Added three more WS2812B ARGB LEDs
  - Intended to indicate the current macro layer
- Added another 3-pin ON-OFF-ON toggle switch (Referred to as Toggle Switch B)
  - Will allow the user to switch between three macro layers
- Rearranged some pin placements, specifically affecting the key matrix, EC11-A and Toggle Switch A.
- Updated pinout reference to reflect changes

</details>

<details>
<summary><strong>Prototype 0.4 </strong></summary>

#### 2026/05/18

- Added 5V rail net from VOUT on RP2040
- Created and added a custom schematic symbol for WS2812B ARGB LEDs (through-hole, individual)
- Replaced all common cathode 4-pin RGB LEDs with WS2812B ARGB LEDs
- Added support circuitry for addressable LED communication
- Added double-transistor level shifter for 3.3V to 5V data conversion
- Added additional (5th) ARGB LED

</details>

<details>
<summary><strong>Prototype 0.3 </strong></summary>

#### 2026/05/13
- Completely rewired the 10-key matrix
- Converted matrix wiring to a COL2ROW configuration
- Corrected previous matrix routing issues to ensure proper electrical functionality

</details>

<details>
<summary><strong>Prototype 0.2</strong></summary>

#### 2026/05/12

- Changed MIC MUTE LED to a 4-pin common cathode RGB LED
- Added three additional RGB LEDs
  - Intended to indicate active macro layers or custom audio profiles
- Created and added a custom schematic symbol for a 3-pin ON-OFF-ON SPDT toggle switch
  - Intended for macro layer and audio profile selection
- Rearranged several GPIO assignments
  - Primarily affecting EC11 (B) and the piezo buzzer
- Redesigned the piezo buzzer circuit
  - Added transistor driver and flyback diode protection
- Added additional decoupling capacitors throughout the circuit

</details>

<details>
<summary><strong>Prototype 0.1</strong></summary>

#### 2026/05/10

- Designed the initial wiring schematic
- Created custom symbols for unsupported components
  - RP2040
  - ILI9341
- Added shared VCC and GND nets
- Connected all primary external components to the RP2040

</details>

## 💻 SOFTWARE — v0.0.0

### FIRMWARE — v0.0.0

No changes yet.

### PC APP — v0.0.0

No changes yet.
