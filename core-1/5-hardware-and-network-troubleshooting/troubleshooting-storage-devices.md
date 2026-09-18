# Troubleshooting Storage Devices

CompTIA A+ Core 1 — 220-1201  
Objective 5.2 — Given a scenario, troubleshoot storage issues

## What You Need to Know

By the end of this lesson, you should understand how to approach:

- Read/write failures and retry slowdowns
- Clicking / grinding hard drive noises (“click of death”)
- Drive not recognized / boot device not found
- Operating system not found
- Data loss and why backups matter
- RAID failure symptoms and RAID 0 / 1 / 5 / 6 / 10 recovery differences
- S.M.A.R.T. monitoring
- IOPS as a performance comparison metric
- Missing drives (BIOS, cables, mapped network drives)
- Drive controller / HBA errors

## What Is It?

**Storage troubleshooting** finds why a drive will not read, write, boot, stay healthy in a RAID array, or perform well — then fixes the cause or recovers data from backups.

Storage includes:

- HDDs (spinning platters)
- SSDs
- RAID arrays
- External drives
- Mapped network drives (appear as letters but live on a server)

## Why Does It Matter?

Drives hold long-term documents and OS files. Failures cause:

- Slow or failed reads/writes
- Boot failures
- Lost data
- Degraded RAID and downtime

Exam scenarios often pair a symptom (clicking, “drive not found,” RAID degraded, SMART warning) with the next best action.

## Real-World Analogy

Think of a library:

- **Retry errors** = the librarian keeps walking back to the same shelf that will not open
- **Click of death** = the shelves are grinding — stop and copy what you can
- **RAID** = multiple shelf rooms with spare copies or parity notes
- **SMART** = sensors warning before the shelves collapse
- **IOPS** = how many checkout transactions per second the library can handle

## How It Works

### Read / Write Failures and Retries

Messages like **“cannot read from the source disk”** mean the system cannot read stored data or write new data.

The drive may **retry** the same area again and again. Retries make the PC feel **very slow**.

The problem may be:

- One bad area of the drive
- Intermittent
- Spreading across the drive

On HDDs, failures can come with loud **clicking** (sometimes called the **click of death**). Once that starts, recovery is often difficult — prioritize backups immediately.

### Why HDDs Click or Grind

Hard drives are mechanical:

- Platters spin at high RPM (often 5,400+ RPM)
- Actuator arms and heads move across the platters
- Tight tolerances — one failure can cascade

Metal-on-metal sounds (clicking, grinding) are serious physical failure signs.

### First Response When a Drive Is Failing

1. **Stop heavy use** if you hear failure noises and lack a recent backup
2. **Back up what you still can** right away
3. Then troubleshoot:
   - Reseat / replace loose or damaged **data and power cables** (desktops)
   - Check **drive and case temperatures**
   - Audit **PSU capacity** if you recently added hardware
   - Run the manufacturer’s **overnight diagnostics** (read/write every sector) if the drive still responds

### Drive Not Recognized / No Boot Device

| Message / symptom | Meaning / next check |
| --- | --- |
| Drive not recognized / boot device not found | System may not see the drive at all |
| No activity lights | Drive may be unresponsive or unpowered |
| Beeps + on-screen POST detail | Use firmware messages with docs |
| **Operating system not found** | Drive is seen, but no bootable OS on it |

Basic fixes:

- Reseat SATA/power (or equivalent) connectors
- Confirm BIOS **boot order** (USB flash ahead of SSD is a common trap)
- For a brand-new drive: cables, power, BIOS detection
- Swap in known-good cables
- Test the drive in another PC to separate drive vs motherboard/SATA port issues

### Data Loss Reality

- HDDs: failure is a matter of **when**, not if
- Professional recovery is expensive and slow
- Failed SSDs may still allow **reads** even when writes fail — still not a substitute for backups

**Backup is the real recovery plan.**

### RAID Troubleshooting Basics

**RAID** = Redundant Array of Inexpensive (or Independent) Disks.

When an array has problems, check:

- Controller messages / emails / audible alarms
- Which **physical** drive failed (do not pull the wrong identical-looking drive)
- RAID type (recovery path depends on it)

| RAID | Min drives | Failure tolerance (basic idea) | If a drive fails |
| --- | --- | --- | --- |
| **RAID 0** (stripe) | 2 | **None** | Array broken; restore from backup after replacing drive |
| **RAID 1** (mirror) | 2 | 1 drive | Array stays up; replace and rebuild |
| **RAID 5** (stripe + 1 parity) | 3 | 1 drive | Array stays up; replace and resync |
| **RAID 6** (stripe + 2 parity) | 4 | 2 drives | Array stays up; replace and resync |
| **RAID 10** (1+0 stripe of mirrors) | 4 | Can survive loss within mirrors (not all drives) | Replace failed member(s) and rebuild |

Always identify the **failed** drive before hot-swapping identical bays.

### S.M.A.R.T.

**SMART** = Self-Monitoring, Analysis, and Reporting Technology.

Drives track health metrics such as:

- Power-on hours
- Power cycle count
- Temperature
- Other manufacturer attributes

Use:

- Raw SMART viewers, or
- Tools that analyze trends over time

Degrading SMART stats can warn you to back up and replace a drive **before** total failure. RAID controllers and third-party tools may email/text alerts.

### IOPS — Performance Comparison

**IOPS** = Input/Output Operations Per Second — a broad performance metric.

Rough comparison from the video:

| Drive type | Approx. IOPS scale |
| --- | --- |
| HDD | About **200** |
| SSD | About **1,000,000** |

That gap is why replacing an HDD with an SSD often feels like a major PC upgrade.

Many layers add delay: memory, bus, mechanical seek (HDD), large vs small transfers. Any weak step can slow the system.

### Missing Drives After Boot

| Cause | Check |
| --- | --- |
| Disabled / BIOS issue | BIOS config and logs |
| Loose internal cable | Reseat data/power |
| External drive | Data cable + power brick |
| Mapped network drive | Login script / Map Network Drive / “Reconnect at sign-in” |

A missing “drive” is not always local hardware — it may be a **network share** that failed to map.

### Drive Controller / HBA Problems

External or server **RAID controllers / HBAs** can fail or report array problems even when some disks are fine.

Boot messages may show controller model and status (for example, RAID exception, volume inactive). Use the controller utility to investigate further.

## Side-by-Side Comparison

| Symptom | First useful direction |
| --- | --- |
| Slow retries / cannot read disk | Failing media; back up; diagnostics |
| Clicking / grinding HDD | Physical failure; backup now |
| Drive not found | Cables, power, BIOS detection, other PC test |
| OS not found | Drive seen but not bootable |
| RAID degraded | Identify bad drive; know RAID type |
| RAID 0 single failure | Data loss without backup |
| SMART warnings | Proactive replace + backup |
| Slow storage feel | HDD vs SSD IOPS; health/cables |
| Letter missing but share exists | Remap network drive |
| Controller exception at boot | RAID/HBA utility |

## Key Terms

| Term | Meaning |
| --- | --- |
| Click of death | Severe HDD clicking that often signals failure |
| Retry | Drive repeatedly attempts a failed read/write |
| SMART | Drive self-monitoring health statistics |
| IOPS | Input/output operations per second |
| RAID | Multiple disks combined for speed and/or redundancy |
| Parity | Extra data used to rebuild after a disk failure (RAID 5/6) |
| Rebuild / resync | Array restores redundancy after a replacement |
| HBA / RAID controller | Hardware that manages drives/arrays |
| Mapped drive | Network share assigned a drive letter |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Clicking HDD | Failing drive; back up immediately |
| Cannot read from source disk | Media/retry failure |
| Drive not recognized | Cable, power, BIOS, port |
| OS not found | Drive present; boot files/OS missing |
| USB boots instead of SSD | Boot order |
| RAID 0 failed | No redundancy — restore backup |
| RAID 1 / 5 / 6 still online after failure | Replace failed disk and rebuild |
| SMART alerts over weeks | Replace before total failure |
| Huge speed jump after upgrade | HDD → SSD (IOPS) |
| Missing G: after login | Mapped network drive |
| PERC / RAID exception at POST | Controller/array troubleshooting |

## Common Mix-Ups

### “OS not found” vs “drive not found”

- **Drive not found** → hardware path may be dead
- **OS not found** → drive is visible but not bootable

### Pulling a random RAID disk

Identical drives are easy to mix up. Confirm the failed bay/serial first.

### RAID replaces backups

RAID protects against some disk failures. It does **not** replace backups (corruption, deletion, site loss, RAID 0).

### SMART raw numbers without context

Use trends/analysis tools — raw attributes need interpretation.

### Missing drive = always dead HDD

Could be cable, BIOS, external power, or a failed network map.

## Quick Review

| Topic | Remember |
| --- | --- |
| Retries | Slow performance; possible media failure |
| HDD noises | Click/grind = urgent backup |
| Not recognized | Reseat cables; BIOS; known-good cable; other PC |
| OS not found | Drive OK path; no bootable OS |
| Backup | Best recovery for any storage failure |
| RAID | Type decides if array survives a disk loss |
| SMART | Early warning system |
| IOPS | SSD vastly outperforms HDD |
| Missing letter | Local vs mapped network drive |
| Controller | Check HBA/RAID messages and utility |

---

## Continue Learning

- Previous Topic: [Troubleshooting Hardware](troubleshooting-hardware.md)
- Next Topic: [Troubleshooting Display Issues](troubleshooting-display-issues.md)
- Related: [RAID](../3-hardware/raid.md)
- Back to [Domain 5 — Hardware and Network Troubleshooting](README.md)
