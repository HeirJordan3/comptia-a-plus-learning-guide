# The BIOS

CompTIA A+ Core 1 — 220-1201  
Objective 3.5 — Motherboards, CPUs, and Add-on Cards

## What You Need to Know

By the end of this lesson, you should understand:

- What the BIOS is and what it does at startup
- What POST is and when it runs
- What a bootloader does after POST
- Where BIOS software is stored on modern motherboards
- The difference between legacy BIOS and UEFI BIOS
- Why UEFI is used on modern systems
- Why BIOS changes should be documented and backed up

## What Is It?

The **BIOS** is the **Basic Input/Output System** — firmware that starts the computer before the operating system loads.

You may also hear:

- **Firmware**
- **System BIOS**
- **ROM BIOS** (older wording)

On modern systems, BIOS software is usually stored in **flash memory** on the motherboard — not old-style read-only chips you cannot update.

When you press the power button, what you see first is often the BIOS process — not Windows, macOS, or Linux yet.

## Why Does It Matter?

Help desk and field techs need BIOS concepts when:

- A PC fails to start or stops before the OS loads
- POST reports missing CPU, memory, keyboard, or other core hardware
- An older PC cannot support newer hardware because of a **legacy BIOS**
- A modern system needs UEFI features (graphics UI, virtualization options, security, boot settings)
- Someone plans a BIOS/UEFI change and must not lock the system into a bad configuration

Exam questions often ask what runs first at power-on, what POST checks, or legacy BIOS vs UEFI.

## Real-World Analogy

Think of the BIOS as the **building’s startup checklist** before the store opens:

1. Power comes on
2. Staff check that key systems work (lights, doors, registers)
3. If something critical fails, you get an alert
4. If checks pass, the store “opens” — the operating system loads

POST is the checklist. The bootloader is the handoff to the day’s work (the OS).

## How It Works

### Startup Order (Simple View)

1. You press the power button
2. BIOS/UEFI firmware starts from flash memory on the motherboard
3. **POST** (Power-On Self-Test) checks core hardware
4. If POST succeeds, the **bootloader** may appear (or boot may start automatically)
5. The operating system loads

If POST finds a serious problem with core systems, you may see an error on screen before the OS ever starts.

### POST — Power-On Self-Test

**POST** is the short diagnostic that runs at power-on.

It typically checks for things like:

- CPU present and usable
- Memory installed
- Keyboard / mouse connected (and other core input)

POST usually takes only a few seconds. When it finishes successfully, the system is ready to start loading an operating system.

### Bootloader

After POST, you may:

- Go straight into the OS, or
- See a prompt asking which OS to load

That prompt is the **bootloader**. It means POST is done and the system is ready to hand control to an operating system.

### Where the BIOS Lives

On modern motherboards, BIOS software is stored in **flash memory**.

Some boards even mark the chips. A board may have:

- A **main** BIOS chip
- A **backup** BIOS chip

That backup can help if an upgrade fails — another copy may still be available.

### Legacy BIOS

A **legacy BIOS** (sometimes called a traditional BIOS) has been around for decades.

Key ideas:

- Common on older PCs and older operating systems
- Built for older hardware
- Often a **text-based** setup screen
- Navigate with keyboard keys (arrows, Enter, Space, function keys)
- Options often listed at the bottom of the screen

Limitation: newer hardware may not work well (or at all) with an older legacy BIOS.

### UEFI BIOS

**UEFI** means **Unified Extensible Firmware Interface**.

Key ideas:

- Used on modern computers
- Created as a standard (associated with Intel’s work / modern firmware standards)
- Because it is standardized, features feel similar across manufacturers
- Modern UI: graphics and **mouse** support are common
- Includes the settings needed to get a system ready to boot (CPU overview, devices, storage, audio, network, advanced options, power, security, startup, and more)

Advanced areas may include CPU features such as **virtualization** settings.

Important: some UEFI settings are critical for reliability. Do not change them unless you understand the result.

### Changing BIOS Settings Safely

Before updating or changing BIOS/UEFI configuration:

- Make **backups** when possible
- Keep **documentation** of what you changed
- Know how to return to the previous setup if something goes wrong

(Detailed individual settings are covered in the next lesson: [BIOS Settings](bios-settings.md).)

## Side-by-Side Comparison

| Topic | Legacy BIOS | UEFI BIOS |
| --- | --- | --- |
| Age / use | Older systems | Modern systems |
| Interface | Mostly text / keyboard | Often graphical / mouse |
| Hardware support | Older hardware focus | Designed for modern hardware |
| Across brands | Varies more by era/vendor | More consistent standard features |
| Exam idea | “Old / traditional / text BIOS” | “Modern firmware / UEFI” |

## Key Terms

| Term | Meaning |
| --- | --- |
| BIOS | Basic Input/Output System; firmware that starts the PC |
| Firmware | Software stored on hardware (here, on the motherboard) |
| Flash memory | Rewritable storage on the board that holds modern BIOS/UEFI |
| POST | Power-On Self-Test; startup hardware checks |
| Bootloader | Program that starts after POST and loads the OS |
| Legacy BIOS | Older traditional BIOS (often text-based) |
| UEFI | Unified Extensible Firmware Interface; modern BIOS standard |
| ROM BIOS | Older name referring to BIOS stored in read-only memory |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| First screens after power-on, before the OS | BIOS / UEFI firmware |
| Checks CPU, memory, keyboard at startup | POST |
| Prompt to choose an OS after startup checks | Bootloader |
| BIOS stored on motherboard today | Flash memory |
| Main + backup BIOS chips | Upgrade safety / recovery |
| Text menu, keyboard-only setup on old PC | Legacy BIOS |
| Graphical BIOS with mouse on modern PC | UEFI |
| Same kinds of options across modern brands | UEFI as a standard |
| Do not change critical settings casually | Backup + document first |

## Common Mix-Ups

### BIOS vs operating system

The BIOS/UEFI starts the machine. The OS (Windows, etc.) loads **after** POST (and the bootloader).

### ROM BIOS vs modern storage

People still say “ROM BIOS,” but modern systems usually store firmware in **flash memory** so it can be updated.

### Legacy BIOS vs UEFI

Similar job (start the system), different generation and interface. UEFI is the modern standard.

### POST failure vs OS problem

If the PC never gets past early startup checks, think hardware/POST/BIOS path — not necessarily a Windows user profile issue.

## Quick Review

| Topic | Remember |
| --- | --- |
| BIOS | Firmware that starts the PC before the OS |
| POST | Power-on checks for core hardware |
| Bootloader | Hands off to the operating system |
| Storage | Modern BIOS lives in flash on the motherboard |
| Legacy BIOS | Older, often text-based, limited for new hardware |
| UEFI | Modern standard BIOS with richer UI/features |
| Safety | Backup and document before changing critical settings |

---

## Continue Learning

- Previous Topic: [Motherboard Compatibility](motherboard-compatibility.md)
- Next Topic: [BIOS Settings](bios-settings.md)
- Related: [Motherboard Connections](motherboard-connections.md)
- Back to [Domain 3 — Hardware](README.md)
