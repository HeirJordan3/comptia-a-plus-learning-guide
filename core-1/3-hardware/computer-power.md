# Computer Power

CompTIA A+ Core 1 — 220-1201  
Objective 3.6 — Power Supplies

## What You Need to Know

By the end of this lesson, you should understand:

- Critical electrical safety rules before opening a PC
- What a PSU does (AC in → DC out)
- Amps, volts, and watts in plain language
- US/Canada vs Europe AC input differences
- Manual voltage switches vs auto-switching PSUs
- Common DC output rails (+12 V, +5 V, +3.3 V, +5 VSB, −12 V, −5 V)
- 20-pin vs 24-pin motherboard power
- Redundant / hot-swappable power supplies
- Fixed vs modular cabling
- How to size wattage (with headroom)
- 80 PLUS efficiency ratings

## What Is It?

A **power supply unit (PSU)** converts wall **AC** power into the **DC** voltages a computer needs.

Motherboards and components need DC. Wall outlets provide AC. The PSU is the converter in between.

Typical DC outputs include **3.3 V**, **5 V**, and **12 V**.

## Why Does It Matter?

Everything in the PC depends on clean, correct power. Techs use this knowledge when:

- Replacing or upgrading a PSU
- A system will not power on
- Moving a PC between countries with different wall voltages
- Building a PC with a power-hungry GPU
- Working on servers with redundant PSUs
- Choosing an efficient (cooler / cheaper to run) supply

### Safety First (Non-Negotiable)

Before working inside a computer:

1. **Disconnect** from the wall / power source
2. Remember capacitors can store charge — know what you are touching
3. **Never** connect yourself to building electrical wiring (including ground)

Treat electricity with respect. Double-check that mains power is disconnected.

## Real-World Analogy

Think of electricity like water in a hose:

| Term | Hose idea | Meaning |
| --- | --- | --- |
| **Amps (A)** | How much water flows | Amount of electrical current |
| **Volts (V)** | Water pressure | Electrical “pressure” |
| **Watts (W)** | Real work done | Real power use |

**Watts = Volts × Amps**

Example: 120 V × 0.5 A = **60 W**

## How It Works

### AC vs DC

| Type | Idea | Where you see it |
| --- | --- | --- |
| **AC** (Alternating Current) | Direction keeps reversing (wave-like) | Wall outlet → PSU input |
| **DC** (Direct Current) | Flows one way at a steady voltage | PSU output → motherboard / drives / cards |

AC is often described with:

- Voltage (VAC)
- Frequency in **hertz (Hz)** — how many cycles per second

### Wall Power Around the World

| Region | Typical AC | Frequency |
| --- | --- | --- |
| United States / Canada | About **110–120 VAC** | **60 Hz** |
| Europe | About **220–240 VAC** (often ~230) | **50 Hz** |

Older PSUs may have a **manual switch** (120 V / 230 V) on the back.

Modern PSUs are often **auto-switching** — they detect input and adjust.

**Danger:** Setting a manual PSU to 120 V and plugging into 230 V can destroy the supply (spectacular failure). Always verify before connecting.

If unsure what an outlet provides, measure with a multimeter.

### DC Outputs From the PSU

Positive/negative labels describe potential relative to a reference (like floors above/below a front door).

| Rail | Common use |
| --- | --- |
| **+12 V** | PCIe adapters, many drives, higher-power devices |
| **+5 V** | Some motherboard components (less common as primary on newest boards) |
| **+3.3 V** | Motherboard parts — M.2, RAM, assorted onboard components |
| **+5 VSB** | Standby power while sleeping — wake-on-LAN / front power button signals |
| **−12 V** | Some integrated LAN / older PCI needs |
| **−5 V** | Legacy older cards; many modern PSUs omit it |

Amp capacity per rail is listed in the PSU manual or on the PSU label.

### Main Motherboard Power Connector

| Connector | Role |
| --- | --- |
| **24-pin** | Modern main motherboard power (3.3 V / 5 V / 12 V) |
| **20-pin** | Older main connector |

A 24-pin PSU cable can often mate with a 20-pin board by leaving the extra four pins unused.

The connector is **keyed** so it only fits one way.

### Redundant Power Supplies

Servers and infrastructure devices may have **two (or more) PSUs**:

- Each can often support **100%** of the system load alone
- Together they may share load (for example, ~50% / 50%)
- If one fails or loses power, the other takes the load
- Often **hot-swappable** — replace while the system stays up

Goal: uptime during PSU failure or replacement.

### Fixed vs Modular Cables

| Style | Idea |
| --- | --- |
| **Fixed** | Cables permanently attached — unused cables stay in the case |
| **Modular** | Plug in only the cables you need |
| **Hybrid** | Some fixed + some modular |

Modular designs improve cable management and airflow.

### Choosing Wattage

Higher-wattage PSUs cost more but do **not** make the PC faster by themselves. They provide capacity.

To size a PSU:

1. Add up power needs (CPU, storage, GPU, other parts) from documentation
2. Pay special attention to discrete **video cards** — they often need a lot of power
3. Leave headroom — a common rule of thumb from the video: size for about **50% more** than today’s total load so the PSU is not maxed out and you can grow later

Physical PSU size for a given case form factor usually stays the same when you upgrade wattage.

### Efficiency and 80 PLUS

Converting AC to DC wastes some energy as **heat**. More efficient PSUs:

- Waste less power
- Run cooler
- Cost less to operate

Typical efficiency range discussed: about **80%–96%**, depending on quality/load.

**80 PLUS** certification tiers (least → most efficient in the video’s framing):

1. 80 PLUS (no metal tier)
2. Bronze
3. Silver
4. Gold
5. Platinum
6. Titanium

## Side-by-Side Comparison

| Topic | Remember |
| --- | --- |
| Input | AC from the wall |
| Output | DC to components |
| US/Canada | ~120 VAC @ 60 Hz |
| Europe | ~230 VAC @ 50 Hz |
| Manual switch | Must match outlet or risk failure |
| Auto-switch | Detects and adapts |
| Redundant PSU | Failover + often hot-swap |
| Modular | Cleaner cabling |
| Higher watts | More capacity, not more speed |
| 80 PLUS Titanium | Highest efficiency tier listed |

## Key Terms

| Term | Meaning |
| --- | --- |
| PSU | Power supply unit |
| AC / DC | Alternating current / direct current |
| Amp (A) | Current — electrons past a point per second |
| Volt (V) | Electrical pressure |
| Watt (W) | Real power (V × A) |
| Hertz (Hz) | AC cycles per second |
| VAC | Volts of alternating current |
| +5 VSB | Standby 5 V rail |
| 24-pin | Main modern motherboard power connector |
| Redundant PSU | Multiple supplies for failover |
| Hot-swappable | Replace while system stays powered |
| Modular PSU | Detachable cables as needed |
| 80 PLUS | Efficiency certification program |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Wall power vs motherboard power | AC in → DC out via PSU |
| 120 vs 230 / manual switch | Match voltage or destroy PSU |
| No switch on modern PSU | Often auto-sensing |
| Main board power | 24-pin (older 20-pin) |
| Server stays up if one PSU dies | Redundant power supplies |
| Replace PSU without shutting down | Hot-swappable |
| Extra cables cluttering case | Fixed vs modular |
| GPU upgrade / random shutdowns under load | PSU wattage too low |
| Cooler / greener PSU | Higher 80 PLUS tier |
| Safety before internal work | Unplug from mains |

## Common Mix-Ups

### Higher wattage = faster PC

No. Wattage is capacity, not CPU/GPU speed.

### Pulling the battery clears PSU settings

Unrelated. PSU safety is about disconnecting AC and respecting stored charge.

### 20-pin vs 24-pin

24-pin is modern. A 24-pin cable can often work on 20-pin boards by not using the extra pins.

### −5 V on every modern PSU

Legacy. Many new supplies do not provide −5 V.

### Connecting an ESD strap to building ground wiring incorrectly

Never attach yourself to building electrical conductors. Follow proper ESD grounding practices taught for tech work — do not improvise on building wiring.

## Quick Review

| Topic | Remember |
| --- | --- |
| Safety | Disconnect mains; respect capacitors; never tie yourself to building wiring |
| Job of PSU | AC → DC (3.3 / 5 / 12 V and related rails) |
| Formula | Watts = Volts × Amps |
| Regions | US ~120/60 Hz; Europe ~230/50 Hz |
| Main connector | 24-pin keyed |
| Servers | Redundant, often hot-swap |
| Cabling | Modular = only what you need |
| Sizing | Calculate load + headroom (~50% extra rule of thumb) |
| Efficiency | 80 PLUS Bronze → Titanium |

---

## Continue Learning

- Previous Topic: [Cooling](cooling.md)
- Next Topic: [Multifunction Devices](multifunction-devices.md)
- Related: [Motherboard Connections](motherboard-connections.md)
- Back to [Domain 3 — Hardware](README.md)
