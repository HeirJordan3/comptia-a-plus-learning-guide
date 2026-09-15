# Motherboard Expansion Slots

CompTIA A+ Core 1 — 220-1201  
Objective 3.5 — Motherboards, CPUs, and Add-on Cards

## What You Need to Know

By the end of this lesson, you should understand:

- What a computer bus is
- What PCI is and how parallel 32-bit / 64-bit buses work
- What PCIe is and how serial lanes work
- How to read labels like PCIe x1, x4, and x16
- How PCI and PCIe slots differ visually
- Basic install and removal tips for expansion cards

## What Is It?

**Expansion slots** let you add features to a motherboard with adapter cards.

This lesson covers two bus technologies:

- **PCI** — Peripheral Component Interconnect
- **PCIe** — PCI Express

A **bus** is the pathway that connects motherboard components so they work as one system.

## Why Does It Matter?

Technicians add and replace cards for:

- Video / graphics
- Networking
- Storage controllers
- Other add-on features

Knowing PCI vs PCIe helps you pick the right card, slot, and removal method.

## Real-World Analogy

Think of a motherboard bus like city roads:

- **PCI** = a wide multi-lane boulevard where many cars leave at the same time (parallel)
- **PCIe** = modern one-way express lanes that send traffic bit by bit very quickly (serial lanes)
- **x1 / x4 / x16** = how many express lanes that ramp has

More lanes usually means more throughput.

## How It Works

### Computer Buses

Motherboards have pathways between parts, for example:

- Memory slots ↔ CPU
- Expansion slots ↔ the rest of the system

Those pathways are buses. Expansion buses let you increase functionality by adding cards.

### PCI — Peripheral Component Interconnect

**PCI** dates to about **1994**.

Key traits:

- Older expansion bus
- Parallel communication
- Two common widths: **32-bit** and **64-bit**
- Many newer boards no longer include PCI and use PCIe instead

#### Parallel Transfers

| Bus width | Idea |
| --- | --- |
| 32-bit PCI | 32 connections; send 32 bits at once across 32 lines |
| 64-bit PCI | 64 connections; send 64 bits at once across 64 lines |

Slots have keys/tabs that help match power and card type. A 64-bit card has extra connectors and a keyway that marks it as 64-bit.

#### Installing a PCI Card

1. Align the card keyways with the slot
2. Press carefully straight down — do not force or flex the board
3. Seat it so copper contacts are fully in the slot
4. Secure it to the case with a screw so it cannot pull out

### PCIe — PCI Express

**PCIe** is the common modern expansion bus.

Key traits:

- Serial communication
- Pathways are called **lanes**
- One bit at a time per direction on a lane path
- Much different from PCI’s wide parallel buses

#### Lane Notation

| Label | Pronounced | Meaning |
| --- | --- | --- |
| PCIe x1 | “by 1” | 1 lane |
| PCIe x2 | “by 2” | 2 lanes |
| PCIe x4 | “by 4” | 4 lanes |
| PCIe x8 | “by 8” | 8 lanes |
| PCIe x16 | “by 16” | 16 lanes |

A single lane has a path each direction. More lanes increase throughput — for example, x4 is roughly four times an x1 path set.

Because PCIe is serial, slots can be much shorter than old 32/64-bit PCI slots when only a few lanes are needed.

### PCI vs PCIe on the Same Board

Some motherboards have both.

Visual clues from the lesson:

| Clue | PCI | PCIe |
| --- | --- | --- |
| Keyway position | Farther from the motherboard edge | Closer to the motherboard edge |
| Shortest common slot | 32-bit PCI | PCIe x1 |
| Communication | Parallel | Serial lanes |

PCIe cards often also have a small hook/latch that locks into the motherboard. When removing a PCIe card:

1. Remove the case screw
2. Unlatch the motherboard connector/hook
3. Then lift the card out

## Key Terms

| Term | Meaning |
| --- | --- |
| Bus | Communication pathway between motherboard components |
| Expansion slot | Slot for add-on adapter cards |
| PCI | Older parallel Peripheral Component Interconnect bus |
| PCIe | Modern serial PCI Express bus |
| Lane | PCIe serial pathway |
| x1 / x4 / x16 | Number of PCIe lanes (“by 1”, “by 4”, etc.) |
| Keyway | Slot/card notch that helps alignment and type matching |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Older parallel expansion bus from the 1990s | PCI |
| 32-bit or 64-bit wide expansion slot | PCI |
| Modern serial expansion bus | PCIe |
| PCIe x16 | Sixteen lanes |
| Keyway closer to board edge | PCIe |
| Keyway farther from edge | PCI |
| Card locked with screw and motherboard latch | Often PCIe |

## Common Mix-Ups

### PCI vs PCIe

- PCI = older, parallel
- PCIe = newer, serial lanes

Similar names, different technologies.

### Slot Size vs Card Compatibility

A shorter slot is often fewer lanes (like x1), not “worse PCI.” Match the card to a compatible PCIe slot/lane setup.

### Removal

PCIe cards may need the motherboard latch released, not just the case screw.

## Quick Review

| Topic | Remember |
| --- | --- |
| Bus | Pathways connecting motherboard parts |
| PCI | Older parallel 32/64-bit slots |
| PCIe | Modern serial lanes |
| x1, x4, x16 | Lane counts (“by 1”, etc.) |
| Install | Align keys, press carefully, secure to case |
| Remove PCIe | Unscrew and unlatch |

---

## Continue Learning

- Previous Topic: [Motherboard Form Factors](motherboard-form-factors.md)
- Next Topic: [Motherboard Connections](motherboard-connections.md)
- Related: [Expansion Cards](expansion-cards.md)
- Back to [Domain 3 — Hardware](README.md)
