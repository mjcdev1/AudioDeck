<!--
COLLAPSIBLE CHANGELOG ENTRY TEMPLATE

<details>
<summary><strong>Rev A# (TYPE) — YYYY/MM/DD</strong></summary>

- Main change
  - Sub change
  - Sub change

- Another main change
  - Sub change

</details>

-->
# Changelog!

### PROJECT — Prototype 1.0 (In Progress)

--- 

### 🔌 HARDWARE — Rev 1.1

#### ENCLOSURE — Prototype 1.1
<details>
<summary><strong>Additions and Changes for Prototype 1.1 — 2026/05/12</strong></summary>

- Added three additional LED slots
- Added SPDT Toggle ON-OFF-ON slot
- Tested fitment of all slots with 3D printed cutouts
  - Adjusted EC11 slots for better fitment

</details>

#### ENCLOSURE — Prototype 1.0
<details>
<summary><strong>Initial Prototype 1.0 Designs — 2026/05/10</strong></summary>

- Designed prototyping plate with cutouts and mounts for all parts
  - Sliced and included individual fit test slots to print and confirm fit before printing the full plate

</details>

#### ELECTRONICS — Prototype 1.1

<details>
<summary><strong>Additions and Changes for Prototype 1.1 — 2026/05/12</strong></summary>

- Changed MIC MUTE LED to use a 4-pin common cathode full-color LED
- Added three more full-color LEDs. Each one will indicate the on status one of three macro layers or one of three custom audio profiles
- Created custom symbol for a 3 pin, ON-OFF-ON SPDT Toggle Switch, and added it to the schematic. This will act as the macro layer/ audio profile selector
- Rearranged pinouts, specifically of EC11 (B), and the Piezo Buzzer
- Redid the piezo buzzer, as it is an active buzzer and requires a transistor and flyback diode for safety
- Added various decoupling capacitors throughout the circuit 

</details>
   
#### ELECTRONICS — Prototype 1.0 

<details>
<summary><strong>Initial Electronic Architecture Design — 2026/05/10</strong></summary>

- Designed initial wiring schematic
  - Created custom symbols of core components where suitable presets could not be found (RP2040, ILI9341)
  - Made VCC and GND NETs
  - Created a realistic wiring scheme between all components and the RP2040 processor

</details>

--- 

### 💻 SOFTWARE — v0.0.0
#### FIRMWARE — v0.0.0
No changes yet.

#### PC APP — v0.0.0
No changes yet.
