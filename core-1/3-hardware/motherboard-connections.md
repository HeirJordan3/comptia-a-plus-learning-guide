# Motherboard Connections

CompTIA A+ Core 1 — 220-1201  
Objective 3.5 — Motherboards, CPUs, and Add-on Cards

## What You Need to Know

By the end of this lesson, you should understand:

- The main motherboard power connector (20-pin vs 24-pin)
- Extra PCIe power connectors for cards that need more power
- SATA and eSATA data interfaces on a motherboard
- What pin headers are used for
- How M.2 storage connects to the board

## What Is It?

A motherboard has many connectors beyond the CPU and memory slots.

This lesson covers common motherboard connections:

- Main power (20-pin / 24-pin)
- PCIe supplemental power (6-pin / 8-pin)
- SATA / eSATA storage interfaces
- Pin headers (front panel, USB, and more)
- M.2 storage slots

## Why Does It Matter?

Help desk and build/repair work often fails because of simple connection mistakes:

- Main power not fully seated or unlocked incorrectly
- Graphics card installed without its extra power plugs
- Front-panel power/reset wires on the wrong header pins
- M.2 drive not fastened into the board slot

## Real-World Analogy

Think of the motherboard like a building’s utility panel:

- **24-pin power** = main electrical feed to the building
- **PCIe 6/8-pin** = extra high-power circuit for a big appliance (often the GPU)
- **SATA / M.2** = data lines to storage rooms
- **Pin headers** = small labeled terminals for doorbells, lights, and switches on the front of the building (case buttons/LEDs)

## How It Works

### Main Motherboard Power

The large motherboard power connector supplies **3.3 V, 5 V, and 12 V DC** to the board and connected components.

| Connector | Notes |
| --- | --- |
| 20-pin | Common on older motherboards |
| 24-pin | Common on newer motherboards |

Compatibility idea from the lesson:

- A 24-pin PSU cable can often work on a 20-pin board (four pins unused)
- Some modular PSU cables let you remove four pins and use 20

The connector is **keyed** so it only fits one way. Line up the keys and push it fully in. A latch/lip locks it so it will not pull out until unlocked.

### Extra PCIe Power for Adapter Cards

Some adapter cards — especially graphics cards — need more power than the motherboard slot provides.

Common supplemental connectors:

| Connector | Power idea from the lesson |
| --- | --- |
| PCIe 6-pin | About 75 watts of 12 V DC |
| PCIe 8-pin | About 150 watts of 12 V DC |

Notes:

- Used for video cards and other power-hungry adapters
- Some 8-pin cables can split/remove two pins to act as a 6-pin
- Look for extra power ports on the card itself and plug them in during install

### SATA and eSATA Interfaces

**SATA** motherboard connectors provide **data** connectivity to SATA drives.

- Distinctive **L-shaped** keying
- Data only on these motherboard ports (power comes separately from the PSU)

**eSATA** is external SATA. It may be:

- Built into the motherboard, or
- Provided by an expansion card with rear-panel eSATA ports

### Pin Headers

**Headers** (pin headers) are rows of pins sticking up from the motherboard.

They are simple electrical interfaces for case and board features, such as:

- Speakers
- Power / reset buttons
- Case LEDs / hard drive activity light
- USB ports from the case
- TPM (Trusted Platform Module) headers on some boards

Front-panel connectors are often single pairs of wires for reset, power, and lights. Motherboard silkscreen labels show where each wire goes.

Always match the case wires to the labeled header pins.

### M.2 Connections

**M.2** slots are small board connectors for compact storage devices (often SSDs).

Install idea:

1. Find the M.2 slot on the motherboard
2. Slide/push the module into the slot
3. Fasten it down to complete the install

No separate SATA data cable is needed for a board-mounted M.2 drive.

## Key Terms

| Term | Meaning |
| --- | --- |
| 24-pin / 20-pin | Main ATX-style motherboard power connector sizes |
| Keying | Shape that forces correct connector orientation |
| PCIe 6-pin / 8-pin | Extra power connectors for high-power cards |
| SATA interface | Motherboard data ports for SATA drives |
| eSATA | External SATA connection |
| Pin header | Pin row on the board for case/front-panel/USB/TPM links |
| Front panel | Case power/reset/LED wiring to motherboard headers |
| M.2 | Compact direct-board storage interface |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Main board power, 3.3/5/12 V | 20-pin or 24-pin connector |
| Newer boards’ main power | 24-pin |
| GPU needs more power than the slot gives | PCIe 6-pin / 8-pin |
| ~75 W extra / ~150 W extra | 6-pin / 8-pin |
| L-shaped drive data port | SATA |
| External SATA on the case rear | eSATA |
| Tiny pins for power button / LEDs | Pin headers / front panel |
| Small board slot for SSD module | M.2 |

## Common Mix-Ups

### Main Power vs PCIe Power

Main 24-pin powers the board. PCIe 6/8-pin is extra power for a hungry card.

### SATA Data vs SATA Power

Motherboard SATA ports are data. Drive power still comes from the PSU.

### Headers vs Expansion Slots

Headers are pin rows for wires/ports. Expansion slots are for full adapter cards.

### M.2 vs SATA cable installs

M.2 mounts on the board directly. SATA drives usually need a data cable plus power.

## Quick Review

| Connection | Remember |
| --- | --- |
| 20/24-pin | Main motherboard power |
| PCIe 6/8-pin | Extra card power |
| SATA | L-shaped data ports |
| eSATA | External SATA |
| Headers | Case buttons, LEDs, USB, TPM |
| M.2 | Small direct storage slot |

---

## Continue Learning

- Previous Topic: [Motherboard Expansion Slots](motherboard-expansion-slots.md)
- Next Topic: [Motherboard Compatibility](motherboard-compatibility.md)
- Related: [Storage Cables](storage-cables.md)
- Back to [Domain 3 — Hardware](README.md)
