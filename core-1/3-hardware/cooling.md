# Cooling

CompTIA A+ Core 1 — 220-1201  
Objective 3.5 — Motherboards, CPUs, and Add-on Cards

## What You Need to Know

By the end of this lesson, you should understand:

- Why computers need cooling
- How case airflow works (cool air in, hot air out)
- Case fan sizes and variable-speed fans
- Passive (fanless) cooling and when it is used
- What heat sinks do
- Thermal paste vs thermal pads
- A typical CPU cooling stack (paste/pad + heat sink + fan)
- What liquid cooling is and when it is used

## What Is It?

Computing creates **heat**. Cooling systems move that heat away from components so the PC stays stable and lasts longer.

Common cooling tools:

- **Fans** (case fans and fans on cards / CPU coolers)
- **Passive cooling** (no fan)
- **Heat sinks**
- **Thermal paste** or **thermal pads**
- **Liquid cooling**

## Why Does It Matter?

Poor cooling leads to:

- Thermal throttling (CPU/GPU slows down)
- Unexpected shutdowns
- Loud fans
- Shorter component life

Techs deal with cooling when:

- Building or upgrading a PC
- Replacing a CPU cooler (paste/pad work)
- A GPU has its own onboard fan
- A quiet HTPC needs passive cooling
- A gaming / overclocked system needs liquid cooling

## Real-World Analogy

Think of the case as a **house on a hot day**:

- Open a cool window on one side (**intake**)
- Hot air leaves another opening (**exhaust**)
- Heat sinks are like metal radiators that spread heat so air can carry it away
- Thermal paste is the thin contact layer so the radiator actually “touches” the hot part
- Liquid cooling is like a car radiator loop — coolant moves heat to a bigger cooling area

## How It Works

### Airflow Through the Case

Typical airflow idea:

1. Cool air is pulled into one side of the case
2. Air passes over warm components and heats up
3. Hot air is pushed out the other side

What helps airflow:

- Sensible layout of motherboard and cards
- Cables and clutter kept out of the air path
- Matching intake and exhaust paths for the case design

Cases and cooling setups vary, but the goal is the same: move heat out efficiently.

### Fans on Adapter Cards

Some expansion cards (especially high-end **graphics cards**) include their own fans.

- They pull cool case air onto a hot part of the card
- They need physical space — more common on larger cards

### Case Fan Sizes and Speed

Common case fan sizes:

- **80 mm**
- **120 mm**
- **200 mm**

Many fans are **variable speed**:

- Slower when the system is cool (quieter)
- Faster when the system heats up (more cooling, more noise)

Fan noise matters in quiet rooms. Different brands/models trade cooling vs sound.

### Passive Cooling (Fanless)

**Passive cooling** cools without a fan.

Often used when quiet operation matters:

- Set-top / media boxes near a TV
- Some video servers or appliances
- Purpose-built devices with manageable heat

Passive cooling is often paired with a **heat sink** to spread heat over a larger surface.

### Heat Sinks

A **heat sink** pulls heat from a hot component and spreads it across many fins.

Air passing through the fins carries heat away.

Safety tips:

- Heat sinks get **very hot** — do not touch after the system has been running
- The heat sink needs a good thermal connection to the component (paste or pad)

### Thermal Paste

Also called **thermal grease** or **conductive grease**.

Role:

- Fills tiny gaps between the hot component (often CPU) and the heat sink
- Creates a strong thermal connection

Install tip from the video:

- Usually only a **pea-sized** amount is needed
- It spreads thin when the heat sink is seated

Too much paste is messy and not helpful.

### Thermal Pads

A **thermal pad** is a solid pad placed between the hot part and the heat sink.

| | Thermal paste | Thermal pad |
| --- | --- | --- |
| Form | Grease / paste | Soft pad |
| Mess | Can be messy | Cleaner install |
| Leak concern | Can squeeze out | Preferred when leak risk matters |
| Effectiveness | Generally better contact | Good, usually slightly less effective |
| Reuse | Clean and reapply as needed | **Not reusable** — replace if removed |

### Typical CPU Cooling Stack

Common order:

1. CPU
2. Thermal paste **or** thermal pad
3. Heat sink
4. Fan on top of (or blowing through) the heat sink

Larger coolers may place a bigger fan sideways so air is forced through the entire heat sink.

### Liquid Cooling

**Liquid cooling** moves heat with coolant instead of relying only on air at the CPU.

Typical loop idea:

1. Cold plate / heat-transfer unit on the CPU
2. Pipes carry warm coolant to a **radiator**
3. Fans blow through the radiator to cool the liquid
4. Coolant returns to the CPU

Where you see it:

- High-end / gaming PCs
- Overclocked systems that need stronger cooling
- Similar idea to car or mainframe liquid cooling concepts

Liquid cooling can reduce noise or improve cooling when air cooling is not enough — but it is more complex.

## Side-by-Side Comparison

| Method | Idea | Common use |
| --- | --- | --- |
| Case fans | Move air through the chassis | Most desktops |
| Card fans | Cool one hot adapter | High-end GPUs |
| Passive | No fan; heat sink / design | Quiet appliances, HTPC |
| Heat sink | Spread heat over fins | CPU, chipset, VRMs, more |
| Thermal paste | Best common thermal interface | CPU cooler installs |
| Thermal pad | Cleaner interface option | When paste mess/leak is a concern |
| Liquid cooling | Coolant + radiator loop | Gaming / high-end / overclocking |

## Key Terms

| Term | Meaning |
| --- | --- |
| Airflow | Path of cool air in and hot air out |
| Case fan | Fan mounted in/on the computer case |
| Passive cooling | Cooling without a fan |
| Heat sink | Metal finned part that spreads heat |
| Thermal paste / grease | Compound that improves heat transfer to the sink |
| Thermal pad | Pad that transfers heat; not reusable |
| Variable-speed fan | Speeds up as temperature rises |
| Liquid cooling | Coolant loop with radiator and fans |
| Overclocking | Running hardware faster than stock — often needs more cooling |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Cool air in / hot air out | Case airflow |
| 80 / 120 / 200 mm | Case fan sizes |
| Quiet media PC / set-top | Passive cooling |
| Fins on metal cooler | Heat sink |
| Pea-sized compound under CPU cooler | Thermal paste |
| Prefer no paste squeeze-out | Thermal pad |
| Pad removed during service | Replace pad — do not reuse |
| GPU with its own blower/fans | Onboard card cooling |
| Gaming / overclock / quieter high-end cooling | Liquid cooling |

## Common Mix-Ups

### More fans always = better

Fans help only if airflow is planned. Blocked cables or fighting intake/exhaust can hurt cooling.

### Thermal paste vs glue

Paste improves heat transfer. It is not structural adhesive for mounting — follow the cooler’s mounting hardware.

### Reusing thermal pads

Do not reuse a removed pad. Install a new one.

### Heat sink alone vs heat sink + fan

A heat sink spreads heat; a fan (or strong airflow) helps move that heat into the air. Passive systems rely on sink + ambient airflow only.

### Liquid cooling is only for servers

Home gaming and overclocked PCs commonly use liquid cooling too.

## Quick Review

| Topic | Remember |
| --- | --- |
| Goal | Move heat away from components |
| Airflow | Cool in → across parts → hot out |
| Fans | Case sizes 80/120/200 mm; often variable speed |
| Passive | Fanless; quiet devices; often with heat sinks |
| Heat sink | More surface area = better heat spread |
| Paste | Pea-sized; good thermal contact |
| Pad | Cleaner; not reusable; slightly less effective |
| Liquid | Coolant to radiator; high-end / gaming / overclock |

---

## Continue Learning

- Previous Topic: [Expansion Cards](expansion-cards.md)
- Next Topic: [Computer Power](computer-power.md)
- Related: [BIOS Settings](bios-settings.md)
- Back to [Domain 3 — Hardware](README.md)
