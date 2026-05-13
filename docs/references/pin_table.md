# Pinout Table

> [!NOTE]
> This document provides the pinouts for the latest stable Electronics release version.
>
> Currently, it reflects the pinouts for [Electronics Prototype 1.1](hardware/electronics/Prototype 1.1).

> [!IMPORTANT]
> Cherry MX keyswitch pinouts are not included in this document, as they require a row/column matrix setup.
>
> Please refer to the [Key Matrix Wiring Guide](guides/key_matrix_wiring_guide.md).

> [!NOTE]
> - Unused pins from the schematic are not included in this table.
> - Unless otherwise specified, all GPIO references refer to RP2040 GPIO pins.
> - This document only covers connections from external components.
> - The RP2040 only needs to provide the shared 3V3 and GND rails used throughout the project.
> - Subscript text in the “Pin From” column shows more common pin names, while the main label matches the naming used in the project schematic.

> [!CAUTION]
> - Components purchased from vendors other than those listed in the recommended component purchase guide may have different pin layouts or orientations. As a result, some pinouts in this document may not exactly match your components.
> - For the best results and to help keep this document accurate, please use the components listed in the [Project Component Purchase Guide](guides/project_component_purchase_guide.md).

### EC11 Encoder A

| Pin From | Pin To |
| --- | --- |
| **S** <sub>Switch</sub> | GPIO `4` |
| **A** <sub>Out A</sub> | GPIO `5` |
| **B** <sub>Out B</sub> | GPIO `3` |
| **G** <sub>Ground</sub> | GND Rail |

### EC11 Encoder B

| Pin From | Pin To |
| --- | --- |
| **S** <sub>Switch</sub> | GPIO `27` |
| **A** <sub>Out A</sub> | GPIO `29` |
| **B** <sub>Out B</sub> | GPIO `23` |
| **G** <sub>Ground</sub> | GND Rail |

### Slider Potentiometer 10 kΩ

| Pin From | Pin To |
| --- | --- |
| **OTA** | GPIO `28` |
| **VCC** | 3V3 Rail |
| **GND** | GND Rail |

### ON-OFF-ON SPDT Toggle Switch

| Pin From | Pin To |
| --- | --- |
| **ON_A** | GPIO `1` |
| **ON_B** | GPIO `0` |
| **GND** | GND Rail |

### Piezo Active Buzzer Circuit

> The longer leg of the piezo buzzer is positive, and the shorter leg is negative.

| Pin From | Through | Pin To |
| --- | --- | --- |
| 2N4401 **Base** | 1 kΩ resistor | GPIO `2` |
| 2N4401 **Emitter** |  | GND Rail |
| Piezo **Negative** |  | 2N4401 **Collector** |
| Piezo **Positive** |  | 3V3 Rail |
| 1N4007 **Anode** |  | Piezo **Negative** / 2N4401 **Collector** |
| 1N4007 **Cathode** |  | 3V3 Rail |

### Mode LEDs (3)

> Pinout information for this specific 4-pin full-color LED is available [here](docs/references).

| LED | Pin From | Through | Pin To |
| --- | --- | --- | --- |
| LED_MODE_A | **B** <sub>Blue</sub> | 470 Ω resistor | GPIO `13` |
| LED_MODE_B | **G** <sub>Green</sub> | 470 Ω resistor | GPIO `14` |
| LED_MODE_C | **R** <sub>Red</sub> | 470 Ω resistor | GPIO `15` |
| ALL | **Common Cathode** |  | GND Rail |

### Status LEDs (1)

> Pinout information for this specific 4-pin full-color LED is available [here](docs/references).

| LED | Pin From | Through | Pin To |
| --- | --- | --- | --- |
| LED_MIC_MUTE | **B** <sub>Blue</sub> | 470 Ω resistor | GPIO `16` |
| LED_MIC_MUTE | **G** <sub>Green</sub> | 470 Ω resistor | GPIO `17` |
| LED_MIC_MUTE | **R** <sub>Red</sub> | 470 Ω resistor | GPIO `18` |
| ALL | **Common Cathode** |  | GND Rail |

### ILI9341 2.4" Display

| Pin From | Pin To |
| --- | --- |
| **LED** | 3V3 Rail |
| **SCK** | GPIO `26` |
| **SDI** <sub>MOSI</sub> | GPIO `22` |
| **DC** | GPIO `21` |
| **RESET** | GPIO `20` |
| **CS** | GPIO `19` |
| **GND** | GND Rail |
| **VCC** | 3V3 Rail |

### Power Filtering / Decoupling

| Pin From | Through | Pin To |
| --- | --- | --- |
| 3V3 Rail | 0.1 µF ceramic capacitor | GND Rail |
| 3V3 Rail | 4.7 µF ceramic capacitor | GND Rail |
| ILI9341 VCC | 0.1 µF ceramic capacitor | ILI9341 GND |
