# Key Matrix Wiring Guide

### Matrix Configuration

This project uses a **COL2ROW** key matrix configuration for the 10 Cherry MX key switches. 

In this arrangement:
- Columns connect directly to one side of each keyswitch
- The opposite switch pin connects to the anode of the diode
- The cathode of the diode connects to the row wire
  > Note: You can determine the cathode side of a 1N4148 by the end with the black stripe

You will repeat this process for each key to form the columns and rows. 

This table shows the connections for a single key: 
| Connection | Connects To |
|---|---|
| Column Wire | Switch Pin 1 |
| Switch Pin 2 | Diode Anode |
| Diode Cathode (black stripe) | Row Wire |

### Matrix current path:

```text
Column → Switch → Diode → Row
```

### Diode Orientation

| Diode Side | Connection |
|---|---|
| Anode | Switch Pin 2 |
| Cathode | Row Wire |

> [!WARNING]
> All matrix diodes **have** to face the exact same direction
>
> Reversed diode orientation may prevent proper matrix scanning or cause ghosting issues.

---

### Matrix GPIO Pinout

With the rows and columns formed, you can directly connect them (from anywhere on the wires) to the below GPIO pins: 

| Matrix Reference | GPIO Pin |
|---|---|
| COL1 | GPIO `8` |
| COL2 | GPIO `9` |
| COL3 | GPIO `10` |
| COL4 | GPIO `11` |
| COL5 | GPIO `12` |
| ROW1 | GPIO `7` |
| ROW2 | GPIO `6` |

---

> [!NOTE]
> Cherry MX switches are not polarized, therefore you can orient the switch any way you want as long as one pin follows the columns and the other follows the rows.
