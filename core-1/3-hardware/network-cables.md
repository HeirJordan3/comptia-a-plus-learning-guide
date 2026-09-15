# Network Cables

CompTIA A+ Core 1 — 220-1201  
Objective 3.2 — Cables and Connectors

## What You Need to Know

By the end of this lesson, you should understand:

- Why twisted pair cable is used for Ethernet
- How cable categories relate to Ethernet standards
- The difference between UTP and STP
- How to read shielding abbreviations such as S/FTP and F/UTP
- What direct burial STP cable is for
- What plenum-rated cable is and when to use it
- Where coaxial cable still shows up in networking

## What Is It?

Network cables are the foundation of wired connectivity. Even wireless networks usually depend on cable behind the access point.

This lesson focuses on copper network cabling:

- Twisted pair Ethernet cable
- Cable categories (Cat5 / Cat5e / Cat6 / Cat6A)
- Unshielded vs shielded twisted pair
- Direct burial STP
- Plenum-rated cable
- Coaxial cable for cable modem / digital cable links

## Why Does It Matter?

Bad or wrong cabling causes real support problems:

- Gigabit or 10-gig links fail or are unstable
- Interference in noisy environments
- Outdoor runs between buildings get damaged by water
- Non-plenum cable installed above a drop ceiling creates fire/code risks

Help desk and field techs need to know what cable they are looking at and what it can safely support.

## Real-World Analogy

Think of twisted pair like two people walking while holding opposite ends of a rope during a windy parade.

Noise hits both sides in similar ways. At the end, the receiver compares the two signals and cancels out the interference.

Shielding is like adding a jacket around the rope so outside noise has a harder time getting in. Plenum cable is like using fire-safe materials in the building’s air return pathway.

## How It Works

### Twisted Pair Copper

Most wired Ethernet uses **twisted pair** copper cable.

Inside the cable are wire pairs twisted together, commonly:

- Blue pair
- Green pair
- Orange pair
- Brown pair

Each pair carries equal and opposite signals (for example Transmit+ and Transmit−).

Why twist?

- One wire in the pair is constantly moving relative to nearby interference
- The receiver compares both wires and can separate real signal from noise
- Each pair is twisted at a different rate, so interference patterns differ across pairs

### Cable Categories and Ethernet Speed

The cable itself does not “have a speed.” Copper is just copper. The **signal standard** has a speed, and IEEE documents the **minimum cable category** needed for that standard.

Look at the printing on the cable jacket for the category rating.

| Ethernet idea | Minimum category idea from the lesson | Distance notes |
| --- | --- | --- |
| 1000BASE-T (Gigabit) | Cat5 minimum; new installs usually Cat5e | Up to 100 meters |
| 10GBASE-T (10 Gigabit) | Cat6 minimum | UTP Cat6 up to 55 meters; shielded Cat6 up to 100 meters |
| 10GBASE-T | Cat6A (Augmented) | Up to 100 meters |

Extra notes:

- Cat5 is deprecated for new purchases; **Cat5e** (Enhanced) added extra qualification tests
- Older Cat5 installs can still run 1000BASE-T to 100 meters
- Always check the IEEE standard for the Ethernet type you plan to run

### Coaxial Cable

**Coaxial** (“co-ax”) means conductors sharing a common axis:

- Inner conductor carries the signal
- Outer shield helps protect that signal

In networking, coax is commonly used with:

- Cable modems
- Digital cable / cable internet infrastructure

### UTP vs STP

| Type | Meaning |
| --- | --- |
| UTP | Unshielded Twisted Pair — no overall shield and no per-pair shield |
| STP | Shielded Twisted Pair — shield helps protect against interference |

Shielding may wrap:

- All four pairs together, and/or
- Each individual pair

#### Shielding Abbreviations on the Jacket

Cable print often uses letters for shielding:

| Letter | Meaning |
| --- | --- |
| U | Unshielded |
| S | Braided shielding |
| F | Foil shielding |

Format idea:

**overall shield / pair shield + TP**

Examples from the lesson:

| Label | Meaning |
| --- | --- |
| S/FTP | Braided shield around the whole cable; foil around each pair |
| F/UTP | Foil around the whole cable; unshielded individual pairs |

Example: a Cat7 cable marked **S/FTP** has an outer shield plus foil on each pair.

### Direct Burial STP

For campus or multi-building runs, cable may go underground.

**Direct burial STP** Ethernet cable is made for installation in the ground:

- Usually waterproofed
- Often filled with gel to repel water
- May not need conduit
- Usually shielded for interference protection and grounding
- Adds mechanical strength for burial

Inside, it still looks like shielded Ethernet: four pairs, often an overall shield, waterproof gel, and a continuous **drain wire** used as an electrical ground.

### Plenum-Rated Cable

Above a commercial drop ceiling you may find:

- Supply air ducts
- Return-air pathways

If return air uses the open space above the drop ceiling, that space is **plenum** space.

Fire, smoke, and toxic fumes can move easily through plenum areas. Network cable installed there must be **plenum-rated**.

| Jacket type | Use |
| --- | --- |
| PVC (PolyVinyl Chloride) | Common non-plenum Ethernet jacket |
| Plenum-rated | FEP (Fluorinated Ethylene Polymer) or low-smoke PVC |

Plenum cable works like normal Ethernet electrically, but the jacket can be less flexible and harder to work with. Use it when cable runs through plenum space above a drop ceiling.

## Key Terms

| Term | Meaning |
| --- | --- |
| Twisted pair | Copper pairs twisted to reduce interference |
| Category (Cat5e / Cat6 / Cat6A) | Cable performance rating |
| 1000BASE-T | Gigabit Ethernet over twisted pair |
| 10GBASE-T | 10-Gigabit Ethernet over twisted pair |
| UTP | Unshielded Twisted Pair |
| STP | Shielded Twisted Pair |
| S/FTP, F/UTP | Shielding abbreviations on cable jackets |
| Coaxial / coax | Center conductor plus outer shield |
| Direct burial | Outdoor cable designed for underground install |
| Drain wire | Grounding wire in shielded / burial cable |
| Plenum | Air-return space, often above a drop ceiling |
| Plenum-rated | Fire/low-smoke jacket for plenum installs |
| PVC / FEP | Common non-plenum / plenum jacket materials |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Pairs twisted to fight interference | Twisted pair |
| Gigabit Ethernet minimum cable | Cat5 / usually Cat5e for new installs |
| 10G over UTP Cat6 short run | About 55 meters |
| 10G to 100 meters | Shielded Cat6 or Cat6A |
| No shielding on pairs or cable | UTP |
| Foil/braid protection against EMI | STP |
| S/FTP printed on jacket | Overall braid + foil per pair |
| Cable buried between buildings | Direct burial STP |
| Cable above drop ceiling in air return | Plenum-rated |
| Cable modem / digital cable plant | Coax |

## Common Mix-Ups

### Cable “Speed” vs Signal Standard

The cable category supports a signaling standard. The copper itself is not “a gigabit cable” by magic — the Ethernet standard and category rating matter together.

### UTP vs STP

- UTP = no shield
- STP = shield present (overall and/or per pair)

### Cat6 vs Cat6A for 10G

- Cat6 UTP: shorter 10G distance (about 55 m)
- Cat6A: 10G to 100 m

### Plenum vs Non-Plenum

- Same networking function
- Different jacket for fire/smoke safety in plenum spaces

### Coax vs Twisted Pair

- Twisted pair = typical office Ethernet drops
- Coax = common for cable internet / cable modem paths

## Quick Review

| Topic | Remember |
| --- | --- |
| Twisted pair | Twists cancel interference |
| Category | Match IEEE Ethernet minimums |
| Gigabit | Cat5/Cat5e, 100 m |
| 10G | Cat6/Cat6A distance rules |
| UTP / STP | Unshielded vs shielded |
| Burial cable | Waterproof gel + often drain wire |
| Plenum | FEP or low-smoke PVC above drop ceiling |

---

## Continue Learning

- Previous Topic: [Display Attributes](display-attributes.md)
- Next Topic: [568A and 568B Colors](568a-and-568b-colors.md)
- Related: [Optical Fiber](optical-fiber.md)
- Back to [Domain 3 — Hardware](README.md)
