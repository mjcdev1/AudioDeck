# Pinout Table

> [!NOTE]
> This document provides the pinouts for the latest stable Electronics release version.
>
> Currently, it reflects the pinouts for [Electronics Prototype 0.5](/hardware/Electronics/Prototype%201.1).

> [!IMPORTANT]
> Cherry MX keyswitch pinouts are not included in this document, as they require a row/column matrix setup.
>
> Please refer to the [Key Matrix Wiring Guide](/docs/guides/key_matrix_wiring_guide.md)

> [!NOTE]
> - Unused pins from the schematic are not included in this table.
> - Unless otherwise specified, all GPIO references refer to RP2040 GPIO pins.
> - This document only covers connections from external components.
> - The RP2040 only needs to provide the shared 3V3 and GND rails used throughout the project.
> - Subscript text in the “Pin From” column shows more common pin names, while the main label matches the naming used in the project schematic.

> [!CAUTION]
> - Components purchased from vendors other than those listed in the recommended component purchase guide may have different pin layouts or orientations. As a result, some pinouts in this document may not exactly match your components.
> - For the best results and to help keep this document accurate, please use the components listed in the [Project Component Purchase Guide](/docs/guides/component_purchase_guide.md).

### EC11 Encoder A

| Pin From | Pin To |
| --- | --- |
| **S** <sub>Switch</sub> | GPIO `2` |
| **A** <sub>Out A</sub> | GPIO `3` |
| **B** <sub>Out B</sub> | GPIO `1` |
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

### ON-OFF-ON SPDT Toggle Switch A

| Pin From | Pin To |
| --- | --- |
| **ON_A** | GPIO `5` |
| **ON_B** | GPIO `4` |
| **GND** | GND Rail |

### ON-OFF-ON SPDT Toggle Switch B

| Pin From | Pin To |
| --- | --- |
| **ON_A** | GPIO `7` |
| **ON_B** | GPIO `6` |
| **GND** | GND Rail |

### Piezo Active Buzzer Circuit

> The longer leg of the piezo buzzer is positive, and the shorter leg is negative.

| Pin From | Through | Pin To |
| --- | --- | --- |
| 2N4401 **Base** | 1kΩ resistor | GPIO `2` |
| 2N4401 **Emitter** |  | GND Rail |
| Piezo **Negative** |  | 2N4401 **Collector** |
| Piezo **Positive** |  | 3V3 Rail |
| 1N4007 **Anode** |  | Piezo **Negative** / 2N4401 **Collector** |
| 1N4007 **Cathode** |  | 3V3 Rail |

### WS2812B ARGB LED Chain (8)

| Pin From | Through | Pin To |
| --- | --- | --- |
| LSQ1 **Base** | 1kΩ resistor | GPIO `16` |
| LSQ1 **Emitter** |  | GND Rail |
| LSQ1 **Collector** | 2.2kΩ resistor | 5V Rail |
| LSQ1 **Collector** / 2.2kΩ node | 1kΩ resistor | LSQ2 **Base** |
| LSQ2 **Emitter** |  | GND Rail |
| LSQ2 **Collector** | 2.2kΩ resistor | 5V Rail |
| LSQ2 **Collector** / 2.2kΩ node | 470Ω resistor | LED 1 **DIN** |
| LED 1 **DOUT** |  | LED 2 **DIN** |
| LED 2 **DOUT** |  | LED 3 **DIN** |
| LED 3 **DOUT** |  | LED 4 **DIN** |
| LED 4 **DOUT** |  | LED 5 **DIN** |
| LED 5 **DOUT** |  | LED 6 **DIN** |
| LED 6 **DOUT** |  | LED 7 **DIN** |
| LED 7 **DOUT** |  | LED 8 **DIN** |
| All LED **VDD** pins |  | 5V Rail |
| All LED **GND** pins |  | GND Rail |


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
| R3 / 5V rail node | 0.1 µF ceramic capacitor | GND |
| R5 / 5V rail node | 0.1 µF ceramic capacitor | GND |
| LED1 VDD / 5V rail node | 0.1 µF ceramic capacitor | GND |
