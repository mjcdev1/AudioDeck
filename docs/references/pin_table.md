# Pinout Table

> [!IMPORTANT]
> Cherry MX keyswitch pinouts are not included in this document, as they require a row/column matrix setup. Please refer to the [Key Matrix Wiring Guide](guides/key_matrix_wiring_guide.md).

> [!NOTE]
> - Unused pins from the schematic are not included in this table.
> - Unless otherwise specified, all GPIO references refer to RP2040 GPIO pins.
> - This document only covers connections from external components.
> - The RP2040 only needs to provide the shared 3V3 and GND rails used throughout the project.
> - Subscript text in the “Pin From” column shows more common pin names, while the main label matches the naming used in the project schematic.

> [!CAUTION]
> - Components purchased from different vendors than recommended in our component purchase guide may have different pin layouts or orientations. As a result, some pinouts in this document may not exactly match your components.
> - For the best results and to help keep this document accurate, please use the components listed in the [Project Component Purchase Guide](guides/key_matrix_wiring_guide.md).

### EC11 1/2
| Pin From | Pin To |
| --- | --- |
| **S** <sub>Switch</sub> |  GPIO `1` |
| **A** <sub>Out A</sub> | GPIO `2` |
| **B** <sub>Out B</sub> | GPIO `0` |
| **G** <sub>Ground</sub> | GND Rail |

### EC11 2/2
| Pin From | Pin To |
| --- | --- |
| **S** <sub>Switch</sub> | GPIO `4` |
| **A** <sub>Out A</sub> | GPIO `5` |
| **B** <sub>Out B</sub> | GPIO `3` |
| **G** <sub>Ground</sub> | GND Rail |

### Slider Pot 10ko
| Pin From | Pin To |
| --- | --- |
| **OTA** | GPIO `26` |
| **VCC** | 3.3V Rail |
| **GND** | GND Rail |

### Piezo Buzzer
> The longer leg of piezo buzzer is the positive and the shorter leg the nagtive

| Pin From | Pin To |
| --- | --- |
| **Positive** | GPIO `23` |
| **Negative** | GND Rail |

### LED 
> The shorter leg of a through-hole LED is called the cathode (negative), the longer leg the anode (positive) 

| Pin From | Going Through | Pin To  | 
| --- | --- |--- |
| **Cathode**|  | GND Rail |
| **Anode**| 470ohm resistor | GPIO `16` |

### ILI9341 2.4" display 
| Pin From | Pin To |
| --- | --- |
| **LED** | 3.3V Rail |
| **SCK** | GPIO `22` |
| **SDI<MOSI>** | GPIO `21` |
| **DC** | GPIO `20` |
| **RESET** | GPIO `19` |
| **CS** | GPIO `18` |
| **GND** | GND Rail |
| **VCC** | 3.3V Rail |



