# Upgrading Windows

CompTIA A+ Core 2 — 220-1202  
Objective 1.2 — Installing Operating Systems

## What You Need to Know

By the end of this lesson, you should understand:

- The difference between upgrade and clean install
- When an in-place upgrade is the better choice
- What to check before upgrading (hardware, apps, drivers, licenses)
- Windows 11 requirements such as TPM 2.0, UEFI, and Secure Boot
- Basic Windows lifecycle / update ideas

## What Is It?

When moving to a newer Windows version, you usually choose:

- **Upgrade** — keep apps, files, accounts, and settings; update the OS around them
- **Install (clean install)** — start fresh; wipe existing OS, apps, and user data on that drive

Neither is always “better.” Use the right method for the situation.

## Why Does It Matter?

Help desk techs get upgrade tickets constantly:

- “Can this PC run Windows 11?”
- “I don’t want to lose my apps and files.”
- “Secure Boot / TPM failed the health check.”

Knowing upgrade vs clean install — and the Windows 11 hardware gates — prevents failed upgrades and lost data.

## Real-World Analogy

Think of upgrading Windows like remodeling a house while people still live there:

- **In-place upgrade** = renovate rooms without throwing out furniture
- **Clean install** = empty the house, rebuild, then move belongings back from storage (backup)

Always pack a backup before a gut renovation.

## How It Works

### Upgrade vs Clean Install

| Method | What stays | How it usually starts | Best when |
| --- | --- | --- | --- |
| In-place upgrade | Apps, documents, settings, local user accounts | Launch setup from inside the current OS | You need to keep configs and user data |
| Clean install | Nothing from the old system | Boot from install media | You want a fresh system or the old OS is too broken |

Upgrade advantages from the lesson:

- Saves time — no full reinstall of apps
- Keeps user data without restore-from-backup as the main path
- Keeps user settings and specialized configurations
- Keeps multiple local user accounts in place

Clean install notes:

- Back up first — even if the user “thinks” nothing matters
- Check for existing data and unexpected partitions before wiping
- Partition/format tools are usually built into setup
- After wipe, recovery is hard or impossible without a backup
- Optionally save user preferences to copy back later

### Before You Upgrade: Checklist

Check OS documentation for recommended requirements:

- Enough RAM
- Enough free disk space
- Feature support for the new OS

Also prepare answers for setup questions:

- Which drive to install to
- Partition layout
- License / product keys

Compatibility checks:

- Application vendors — will apps run on the new OS?
- Device drivers — storage, network, and other hardware support

Microsoft provides a hardware compatibility check. For Windows 11, this is the **PC Health Check** app.

### PC Health Check Example (Windows 11)

PC Health Check reports whether the PC meets Windows 11 requirements and lists what passed or failed.

Example failures from the lesson:

- Secure Boot not supported / not enabled
- TPM 2.0 not supported / not enabled

Example passes from the lesson:

- Supported processor
- Enough memory

### Windows Lifecycle Basics

Vendors publish a support lifecycle calendar showing when an OS is supported and when support ends.

Common update ideas from the lesson:

| Update type | Idea |
| --- | --- |
| Quality updates | Monthly security updates and bug fixes |
| Feature updates | New capabilities; often every 6–12 months |

Many Windows versions are supported for roughly **18 to 36 months**, depending on edition/version. Microsoft documents this under the **Modern Lifecycle Policy**.

### Windows 11 Hardware Gates

Windows 11 adds stricter requirements than a typical Windows 10 upgrade path.

| Requirement | Why it matters | How to check (from lesson) |
| --- | --- | --- |
| TPM 2.0 (or later) | Cryptographic hardware used by BitLocker, Windows Hello, and other features | `tpm.msc` MMC snap-in |
| UEFI BIOS | Modern firmware required for Secure Boot | System firmware / system docs |
| Secure Boot enabled | Required for Windows 11 | System Information → System Summary → **Secure Boot State** should be On |

If a PC is too old and has no UEFI BIOS, replacement may be required to support Windows 11.

## Key Terms

| Term | Meaning |
| --- | --- |
| In-place upgrade | Upgrade OS while keeping apps, files, and settings |
| Clean install | Wipe and install Windows as new |
| PC Health Check | Microsoft tool to validate Windows 11 readiness |
| TPM | Trusted Platform Module; Windows 11 needs 2.0+ |
| UEFI | Modern BIOS/firmware style |
| Secure Boot | UEFI security feature required by Windows 11 |
| Quality updates | Monthly security/bug-fix updates |
| Feature updates | Larger updates that add capabilities |
| Modern Lifecycle Policy | Microsoft’s product support lifecycle documentation |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Keep apps and files; update Windows | In-place upgrade |
| Wipe drive and start fresh | Clean install |
| Always do this before a clean install | Backup |
| Tool that checks Windows 11 readiness | PC Health Check |
| Windows 11 crypto hardware requirement | TPM 2.0 |
| Windows 11 firmware/boot requirement | UEFI + Secure Boot |
| Check Secure Boot status in Windows | System Information |
| Check TPM details | tpm.msc |

## Common Mix-Ups

### Upgrade vs install

Upgrade keeps the house furnished. Clean install empties it first.

### “Health Check failed” vs “CPU too weak”

Failures are often Secure Boot / TPM, not always processor or RAM.

### TPM present vs TPM enabled

Hardware may exist but still be disabled in firmware — both support and enablement matter.

### Backups “only if needed”

Users often remember one important file after the wipe. Back up anyway.

## Quick Review

| Topic | Remember |
| --- | --- |
| In-place upgrade | Keep apps/data/settings |
| Clean install | Wipe and start over; back up first |
| Pre-check | RAM, disk, apps, drivers, license keys |
| Win 11 gates | TPM 2.0, UEFI, Secure Boot |
| Tools | PC Health Check, tpm.msc, System Information |

---

## Continue Learning

- Previous Topic: [Installing Operating Systems](installing-operating-systems.md)
- Next Topic: [An Overview of Windows](an-overview-of-windows.md)
- Related: [The BIOS](../../core-1/3-hardware/the-bios.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Back to [Core 2](../README.md)
