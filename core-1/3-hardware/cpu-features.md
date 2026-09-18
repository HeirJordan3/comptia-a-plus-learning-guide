# CPU Features

CompTIA A+ Core 1 — 220-1201  
Objective 3.5 — Motherboards, CPUs, and Add-on Cards

## What You Need to Know

By the end of this lesson, you should understand:

- What 32-bit vs 64-bit means for CPUs and operating systems
- Rough memory addressing limits (4 GB for 32-bit)
- x86 vs x64 naming
- How 32-bit and 64-bit apps and drivers relate
- Where Windows stores 32-bit vs 64-bit programs
- What ARM processors are and why they matter
- What CPU cores are and why more cores can help

## What Is It?

Modern CPUs include features that affect how much memory they can address, what software they can run, how efficient they are, and how much work they can do at once.

This lesson focuses on:

- **32-bit vs 64-bit** processors and OSes
- **ARM** architecture
- **CPU cores**

You may see these details in System Information (for example: “64-bit operating system” and “ARM-based processor”).

## Why Does It Matter?

Help desk and build techs need these ideas when:

- Choosing the right OS install (32-bit vs 64-bit)
- Installing drivers that match the OS bitness
- Explaining why a 64-bit app will not run on a 32-bit OS
- Finding 32-bit apps under `Program Files (x86)`
- Comparing Intel/AMD PCs with ARM phones, tablets, and some laptops
- Reading “8-core” or “16-core” on a CPU spec sheet

Exam questions often compare bitness, app compatibility, ARM efficiency, or cores.

## Real-World Analogy

- **32-bit vs 64-bit** = how wide the desk is for working papers. A 64-bit desk can hold far more address space at once.
- **ARM** = an engine designed to do a lot of work on less fuel and less heat — ideal for phones and efficient laptops.
- **Cores** = multiple workers in one office building. More cores can handle more tasks at the same time.

## How It Works

### 32-Bit vs 64-Bit

**32-bit** and **64-bit** describe CPU (and OS) capability:

- How much information the CPU can process in related operations
- How much **address space** a CPU can reference

| Type | Address idea | Practical memory scale |
| --- | --- | --- |
| 32-bit | About 2³² addressable units | Roughly **4 GB** of memory addressing |
| 64-bit | About 2⁶⁴ addressable units | Extremely large theoretical space (far beyond a typical PC’s installed RAM) |

A 64-bit OS on a 64-bit CPU can scale to much larger amounts of RAM than a classic 32-bit design. Real systems still have motherboard/OS limits — they will not magically use “17 billion GB” of RAM — but 64-bit is what makes large memory support practical.

### Drivers Must Match

| OS type | Drivers needed |
| --- | --- |
| 64-bit OS | 64-bit drivers |
| 32-bit OS | 32-bit drivers |

### Intel Naming: x86 and x64

In the Intel/PC world:

| Name | Meaning |
| --- | --- |
| **x86** | Common label for 32-bit PC processors (roots in the older 8086 family) |
| **x64** | Common label for 64-bit PC processors |

### Applications and Compatibility

| Situation | Result |
| --- | --- |
| 32-bit OS running a 64-bit app | **No** — will not run |
| 64-bit OS running a 32-bit app | **Usually yes** |

### Windows Program Folders

On a 64-bit Windows system:

| Folder | Typical contents |
| --- | --- |
| `Program Files` | 64-bit applications |
| `Program Files (x86)` | 32-bit applications |

### ARM Processors

**ARM** = **Advanced RISC Machine** (architecture from Arm Limited).

Key ideas:

- Arm creates the architecture specification and **licenses** it to chip makers
- ARM designs are known for **efficiency**: less power, less heat, strong performance for the energy used
- About **99%** of modern mobile phones use ARM processors
- ARM is increasingly used in some laptops and desktops as well

You may see System Information report an **ARM-based processor** alongside a 64-bit OS.

### CPU Cores

A single CPU package often contains multiple **cores**.

Each core typically includes:

- Its own processing unit
- Cache memory associated with that core

| Idea | Meaning |
| --- | --- |
| 8-core / 16-core | Number of cores inside the CPU package |
| Why it helps | Multiple cores can work on multiple instructions / tasks at the same time |

More cores can improve overall efficiency for multitasking and parallel workloads. Exact gains depend on the software and workload — not every program uses every core equally.

## Side-by-Side Comparison

| Topic | 32-bit (x86) | 64-bit (x64) |
| --- | --- | --- |
| Memory addressing | About 4 GB class limit | Much larger scale |
| Drivers | 32-bit drivers | 64-bit drivers |
| Runs 64-bit apps | No | Yes |
| Runs 32-bit apps | Yes | Usually yes |
| Windows folders | Typically `Program Files` | 64-bit in `Program Files`; 32-bit in `Program Files (x86)` |

| Topic | Intel/AMD PC CPUs | ARM |
| --- | --- | --- |
| Common devices | Many desktops/laptops | Phones, many tablets, growing PC use |
| Strength | Broad PC software history | Power efficiency / low heat |
| Business model | Companies design/sell chips | Architecture licensed to makers |

## Key Terms

| Term | Meaning |
| --- | --- |
| 32-bit / 64-bit | CPU/OS addressing and processing width |
| Address space | How much memory a CPU can reference |
| x86 | Common name for 32-bit PC CPU architecture |
| x64 | Common name for 64-bit PC CPU architecture |
| ARM | Advanced RISC Machine architecture (efficient, widely used in mobile) |
| Core | Individual processing unit inside a CPU package |
| Cache | Fast memory near the core |
| Driver | Software that lets the OS talk to hardware (must match bitness) |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| About 4 GB memory limit | 32-bit |
| Need lots of RAM / modern OS default | 64-bit |
| x86 | 32-bit PC architecture |
| x64 | 64-bit PC architecture |
| 64-bit app on 32-bit OS | Will not run |
| 32-bit app on 64-bit Windows | Usually runs; often in Program Files (x86) |
| Phone CPU / low power / cool running | ARM |
| 8-core / 16-core | Multiple cores in one CPU package |
| Drivers fail after OS bitness mismatch | Wrong 32/64-bit drivers |

## Common Mix-Ups

### CPU bitness vs OS bitness

You need a matching pair for full capability. A 64-bit OS requires a 64-bit-capable CPU.

### “64-bit means unlimited RAM on my PC”

64-bit removes the classic 4 GB class ceiling, but the motherboard, OS edition, and installed modules still set real limits.

### x86 means “old and unused”

x86 is the common label for 32-bit PC software/architecture naming. 64-bit is x64.

### ARM vs “not a real CPU”

ARM is a full CPU architecture. Phones and many modern devices are ARM-based.

### More cores always means faster for every task

More cores help when software can use them. A single-threaded task may not speed up much.

## Quick Review

| Topic | Remember |
| --- | --- |
| 32-bit | ~4 GB addressing; x86 |
| 64-bit | Large addressing; x64; modern default |
| Apps | 32-bit OS cannot run 64-bit apps; 64-bit OS usually runs 32-bit apps |
| Windows | `Program Files` = 64-bit; `Program Files (x86)` = 32-bit |
| ARM | Efficient architecture; dominant in phones; licensed design |
| Cores | Multiple CPUs + cache in one package; parallel work |

---

## Continue Learning

- Previous Topic: [HSM and TPM](hsm-and-tpm.md)
- Next Topic: [Expansion Cards](expansion-cards.md)
- Related: [Motherboard Compatibility](motherboard-compatibility.md)
- Back to [Domain 3 — Hardware](README.md)
