# Storage Devices

CompTIA A+ Core 1 — 220-1201  
Objective 3.4 — Storage Devices

## What You Need to Know

By the end of this lesson, you should understand:

- Why storage is needed when RAM is volatile
- How hard drives work and why RPM matters
- Why SSDs are faster than hard drives
- How PCIe, NVMe, and M.2 improve SSD performance
- What SAS is used for
- The difference between SATA, mSATA, and M.2
- Flash memory basics and optical drive uses

## What Is It?

Storage devices keep data available after power is removed.

RAM is volatile — it loses data when the computer shuts off. Long-term storage keeps that information for later.

This lesson covers:

- Hard drives (HDDs)
- Solid-state drives (SSDs)
- PCIe storage / NVMe
- SAS
- mSATA and M.2
- Flash memory
- Optical drives

## Why Does It Matter?

Help desk technicians deal with storage every day:

- Slow systems that still use spinning hard drives
- Upgrading to SSD / NVMe for big performance gains
- Choosing the right laptop drive size and interface
- Recovering data from flash drives or old optical media
- Server arrays using SAS for higher throughput

## Real-World Analogy

Think of storage options like different filing systems:

- **HDD** = a spinning record library with a mechanical arm finding tracks
- **SSD / flash** = an electronic filing cabinet with no moving drawers
- **NVMe / M.2** = that same electronic cabinet plugged into the building’s fastest hallway
- **Optical** = archived discs on a shelf — great for keeping old records, slower to retrieve

## How It Works

### Why Storage Exists

Memory is volatile. When power is off, RAM contents disappear.

Persistent storage options include hard drives, SSDs, flash drives, memory cards, optical drives, and more.

### Hard Drives (HDD)

A **hard drive** is magnetic storage with rapidly spinning **platters**.

It is random access: data can be stored anywhere and retrieved by address.

Inside (do not open — dust-free area):

| Part | Role |
| --- | --- |
| Platters | Where data is stored |
| Spindle | Spins the platters |
| Actuator / arm | Moves the read/write head |
| Read/write head | Reads and writes data on the platters |

Because HDDs are mechanical, any moving part can fail.

#### RPM and Latency

Common platter speeds:

| RPM | Idea |
| --- | --- |
| 5,400 | Slower / higher latency |
| 7,200 | Common desktop speed |
| 10,000 | Faster |
| 15,000 | Fastest of these; lower latency |

Faster spin means the needed data reaches the head sooner, so reads/writes feel faster.

Drives often have multiple platters, with heads on top and bottom surfaces.

#### Drive Sizes

| Form factor | Common use |
| --- | --- |
| 3.5-inch | Desktops |
| 2.5-inch | Laptops / mobile devices |
| ~22 mm wide | Modern SSD form factors (much smaller) |

### Solid-State Drives (SSD)

**SSDs** use non-volatile memory with **no moving parts**.

Benefits:

- Much faster reads/writes than HDDs
- Big overall system speed improvement just by replacing an HDD with an SSD

Inside an SSD you mostly see memory modules, not mechanical arms and platters.

### PCIe Storage and NVMe

SSDs quickly outgrew traditional **SATA** limits.

Connecting storage to the **PCI Express** bus gives much higher throughput than SATA.

Example ideas from the lesson:

| Path | Throughput idea |
| --- | --- |
| SATA | About 6 Gbps (SATA revision 3) |
| PCIe | About 64 Gbps per lane |

One common method is an adapter card that holds an SSD and plugs into a motherboard PCIe slot for power and speed.

#### AHCI vs NVMe

| Standard | Role |
| --- | --- |
| AHCI | Advanced Host Controller Interface; older SATA-oriented data movement method |
| NVMe | Non-Volatile Memory Express; low latency, higher throughput over PCIe |

NVMe can use PCIe even in laptops that cannot fit full adapter cards.

### M.2 Interface

**M.2** is a common compact interface for SSDs on desktops and laptops.

Benefits:

- No separate data/power cables
- Plugs directly into the board
- Can use PCIe speeds
- With NVMe on M.2, theoretical transfer around **20 Gbps** (much better than 6 Gbps SATA)

M.2 keys identify supported connectivity:

| Key | Idea |
| --- | --- |
| B key | One keying style / capability set |
| M key | Another keying style / capability set |
| B + M | Can fit interfaces that support either |

Check motherboard docs for which keys and whether NVMe is supported. Install by sliding into the slot and fastening it down.

### SAS — Serial Attached SCSI

**SAS** (Serial Attached SCSI) is a serial version of older SCSI technology.

Use case: improve throughput for hard drive arrays and enterprise storage.

Speed idea from the lesson: about **22.5 Gbps**, faster than typical 6 Gbps SATA. Future SAS versions are expected to be faster.

SAS drives have separate data and power connectors and look similar to SATA, but connectors differ so you cannot accidentally mix SATA and SAS.

### mSATA vs M.2

As storage shrank and needed faster links, interfaces evolved:

| Interface | Idea |
| --- | --- |
| 2.5-inch SATA | Traditional drive style |
| mSATA (mini SATA) | Smaller SATA-based stopgap form factor |
| M.2 | Popular modern board-mounted interface, especially for SSDs |

mSATA helped with size and bus connectivity, but many manufacturers moved quickly to M.2.

### Flash Memory

Flash drives store data in a small removable form factor using **EEPROM** (Electrically Erasable Programmable Read-Only Memory).

Key points:

- Non-volatile — data remains without power
- Limited write cycles; eventually may become read-only
- Easy to lose; not ideal as the only archival/backup copy
- Always keep another backup elsewhere

Common flash formats:

| Format | Notes |
| --- | --- |
| USB flash drive | Very common everyday removable storage |
| CompactFlash (CF) | Older / larger flash card style |
| SD / miniSD / microSD | Common in mobile devices |
| xD-Picture Card | Older digital camera format |

### Optical Drives

Optical drives are less common in modern production systems, but lots of archives still use them.

How they work:

- Laser writes/reads microscopic bumps on the disc
- Relatively slow vs HDD/SSD
- Good archival capacity in a small physical disc

Common formats:

- CD-ROM
- DVD-ROM
- Blu-ray

If you need old archives, an external USB optical drive is often the practical answer.

## Key Terms

| Term | Meaning |
| --- | --- |
| Volatile | Loses data when power is removed (RAM) |
| HDD | Magnetic spinning hard disk drive |
| RPM | Revolutions per minute; platter spin speed |
| SSD | Solid-state drive; no moving parts |
| AHCI | Older SATA host controller interface |
| NVMe | High-speed PCIe storage interface |
| M.2 | Compact direct-board storage interface |
| SAS | Serial Attached SCSI; fast drive interface |
| mSATA | Mini SATA form factor |
| EEPROM | Non-volatile flash memory technology |
| Optical drive | Laser-based disc storage (CD/DVD/Blu-ray) |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Data survives power off | Storage / non-volatile |
| Spinning platters, actuator arm | HDD |
| Faster spin, lower latency | Higher RPM |
| No moving parts, much faster | SSD |
| SATA too slow for modern SSD | PCIe / NVMe |
| Laptop SSD slot, no cables | M.2 |
| Enterprise HDD array throughput | SAS |
| Stopgap mini SATA card | mSATA |
| Removable EEPROM stick | Flash drive |
| Laser disc archive | Optical (CD/DVD/Blu-ray) |

## Common Mix-Ups

### RAM vs Storage

RAM is temporary/volatile. Storage keeps data after shutdown.

### SSD vs NVMe

SSD is the drive type. NVMe is a fast communication method often used with SSDs over PCIe/M.2.

### SATA SSD vs NVMe M.2

Both can be solid-state. NVMe/M.2 is usually much faster than SATA-limited SSDs.

### mSATA vs M.2

mSATA was a smaller SATA-era step. M.2 is the common modern board interface.

### Flash as backup

Convenient, but write-limited and easy to lose — not your only archive.

## Quick Review

| Device / tech | Remember |
| --- | --- |
| HDD | Magnetic, mechanical, RPM matters |
| SSD | Fast, no moving parts |
| PCIe / NVMe | High-speed SSD path |
| M.2 | Direct board install; check B/M keys |
| SAS | Fast serial SCSI for drive arrays |
| mSATA | Mini SATA stopgap |
| Flash | Removable EEPROM; backup elsewhere |
| Optical | CD/DVD/Blu-ray archives |

---

## Continue Learning

- Previous Topic: [Memory Technologies](memory-technologies.md)
- Next Topic: [RAID](raid.md)
- Related: [Storage Cables](storage-cables.md)
- Back to [Domain 3 — Hardware](README.md)
