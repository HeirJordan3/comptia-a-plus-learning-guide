# BIOS Settings

CompTIA A+ Core 1 — 220-1201  
Objective 3.5 — Motherboards, CPUs, and Add-on Cards

## What You Need to Know

By the end of this lesson, you should understand:

- How to enter BIOS/UEFI setup
- Why Windows Fast Startup can block BIOS access
- Why you must document and back up BIOS changes
- Boot order / boot sequence
- Disabling hardware in BIOS (especially USB)
- Fan and temperature controls
- Secure Boot (UEFI)
- Boot / user password vs supervisor / BIOS password
- CMOS vs modern flash storage of settings
- How to reset BIOS when a password is lost
- Enabling CPU virtualization (Intel VT / AMD-V)

## What Is It?

**BIOS settings** are the configuration options inside BIOS/UEFI setup that control how the system starts and which hardware features are available.

These settings run **before** the operating system. If you disable something in BIOS, the OS often cannot see that hardware at all.

Common categories:

- Boot sequence
- USB / device enable-disable
- Cooling and temperature monitoring
- Secure Boot
- BIOS passwords
- Virtualization features

## Why Does It Matter?

Technicians use BIOS settings when:

- Installing an OS from USB and need the USB drive first in boot order
- Hardening a PC by disabling USB storage
- An older OS will not boot because Secure Boot is on
- Someone forgot a BIOS password and the board must be reset
- A hypervisor needs Intel VT or AMD-V enabled
- Fans are too loud or the system is overheating

Exam scenarios often describe boot order, Secure Boot, passwords, USB disable, or virtualization toggles.

## Real-World Analogy

BIOS settings are like the **building’s master control panel** before the store opens:

- Which door opens first (boot order)
- Whether the side entrance is locked (USB enable/disable)
- Whether security checks IDs at the door (Secure Boot)
- Who can change the panel itself (supervisor password)

If a switch is off at the panel, the staff inside (the OS) may never know that door existed.

## How It Works

### Entering BIOS Setup

At power-on, press the vendor’s setup key. Common examples:

- **Delete**
- **F1**
- **F2**
- Combinations such as **Ctrl+S** or **Ctrl+Alt+S**

Check the splash screen or motherboard manual for the exact key.

Other practice options:

- Some hypervisors (Hyper-V, VMware Workstation / Fusion) can open a VM’s firmware setup
- Online **UEFI BIOS simulators** for practice without hardware
- VirtualBox generally does **not** provide the same virtual BIOS setup experience

### Windows Fast Startup Problem

Windows 10 / 11 often uses **Fast Startup**. The PC may not fully power off, so you never get a chance to press the BIOS key.

Ways to get a full restart into firmware setup:

- Hold **Shift** while clicking **Restart**
- **Settings → Update & Security → Recovery → Advanced startup → Restart now**
- Temporary changes in **msconfig** (System Configuration)
- Interrupt the boot process **three times in a row** so the next boot starts from the beginning

### Safety Before Changing Anything

BIOS mistakes can cause no-boot or unstable systems.

Before changing settings:

1. **Document** the current values (write them down or photograph the screen)
2. Understand what you are changing — do not randomly toggle memory/CPU options
3. Keep a **backup** / known-good configuration when possible

### Hardware Enable / Disable

BIOS can enable or disable hardware at the firmware level.

If USB (or another device) is disabled in BIOS:

- The operating system may not see it at all
- That is useful for security policies
- It is also a common help-desk “device missing” root cause

### Boot Order (Boot Sequence)

**Boot order** tells the PC which device to try first, second, third, and so on.

Possible boot devices include:

- SATA drives
- M.2 drives
- USB drives
- Network boot

Examples:

- To install from a USB installer → move **USB** to the top
- After installing to a new M.2 SSD → move that drive higher so it boots first

If the first device has no OS, the BIOS tries the next device in the list.

### USB Permissions

Organizations may disable USB storage in BIOS to reduce malware risk from flash drives.

Convenience vs security:

- USB is useful for file transfer and OS installs
- USB can also introduce malware

Historical example from the video: a DoD USB flash-drive ban after a worm infection — admins disabled USB in BIOS as part of the response.

In setup, USB options are often under a **Devices / USB Setup** menu (enable/disable ports or USB features).

### Fan Controls and Cooling

Motherboards include temperature sensors and fan headers (for example, **CPU_FAN**).

BIOS fan modes may include options such as:

- Best performance (stronger cooling)
- Best experience (quieter)
- Full speed (always max)

Use quieter modes in quiet offices; louder/full-speed modes may make more sense in hot or always-on environments.

### Secure Boot (UEFI Only)

**Secure Boot** is a UEFI feature (not found on legacy BIOS).

What it protects:

- The OS image / boot path with known digital signatures
- Unauthorized BIOS updates (signature must match manufacturer trust)
- The bootloader before the OS starts

If malware changes signed boot software, Secure Boot can **stop the boot**.

Trade-off:

- Older OS installers without a trusted signature may fail
- You may need to **disable Secure Boot** temporarily for that software
- Re-enable Secure Boot afterward for modern OS security

Manage Secure Boot under **Security** settings (enable/disable and key management).

### BIOS Passwords

| Password type | Also called | What it does |
| --- | --- | --- |
| Boot password | User / power-on password | Must enter password before the OS can boot |
| Supervisor password | BIOS password | Must enter password before changing BIOS settings |

Example: disable USB for security, then set a **supervisor password** so users cannot re-enable USB in setup.

If either password is forgotten:

- You typically must **reset BIOS** using the motherboard manufacturer’s procedure
- Remember both passwords — lost boot password = no boot; lost supervisor password = no setup access

### Where Settings Are Stored (CMOS vs Flash)

| Item | Where it lives |
| --- | --- |
| BIOS/UEFI **firmware** (the program) | Flash memory on the motherboard |
| BIOS **configuration settings** | Usually separate flash on modern boards |

**CMOS** (Complementary Metal-Oxide Semiconductor) is older terminology for the memory that held settings.

Older systems:

- Settings in volatile memory
- Kept alive by a motherboard battery

Modern systems:

- Settings in **non-volatile flash**
- Removing the battery often **will not** clear settings

### Resetting BIOS

Modern reset usually needs **physical access** to the board:

1. Power down and open the case
2. Find the clear/reset jumper (example label: **CLRTC** — Clear Real-Time Clock RAM)
3. Place a **jumper** across the pins (shorts the two pins)
4. Power on per manufacturer instructions to clear settings

Always follow the specific motherboard manual.

### Temperature Monitoring

BIOS can show CPU and other component temperatures without loading an OS.

Useful after installing new hardware to confirm cooling before relying on Windows tools.

### Virtualization Settings

CPU virtualization features make hypervisors faster and more stable. Enable them in BIOS:

| CPU brand | Feature name |
| --- | --- |
| Intel | Intel VT / Virtualization Technology |
| AMD | AMD-V / AMD Virtualization (may appear as SVM / Secure Virtual Machine) |

Often found under **Advanced → CPU Setup** (names vary by vendor).

## Side-by-Side Comparison

| Goal | Setting area |
| --- | --- |
| Boot from USB installer | Boot order — USB first |
| Hide USB from the OS | Disable USB in Devices |
| Stop pre-OS malware / unsigned boot | Secure Boot (UEFI) |
| Stop casual BIOS changes | Supervisor / BIOS password |
| Require password to start PC | Boot / user / power-on password |
| Quiet vs max cooling | Fan / Intelligent Cooling |
| Run Hyper-V / VMs well | Intel VT or AMD-V |
| Forgotten BIOS password | Motherboard jumper / CLRTC reset |

## Key Terms

| Term | Meaning |
| --- | --- |
| BIOS setup | Firmware configuration utility entered at startup |
| Fast Startup | Windows partial shutdown that can skip full BIOS entry |
| Boot order | Priority list of devices tried at startup |
| Secure Boot | UEFI feature that verifies signed boot components |
| Boot / user password | Password required to boot the OS |
| Supervisor / BIOS password | Password required to enter/change setup |
| CMOS | Older name for settings memory; often flash today |
| CLRTC / clear jumper | Motherboard pins used to reset BIOS settings |
| Intel VT / AMD-V | CPU virtualization features enabled in BIOS |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Need to boot from USB install media | Change boot order |
| USB device missing in OS after policy change | USB disabled in BIOS |
| Old OS will not boot on UEFI system | Secure Boot may be blocking |
| Users re-enable USB after tech disables it | Set supervisor password |
| Password prompt before any OS | Boot / user password |
| Forgot BIOS password | Reset via jumper / manufacturer process |
| Pulling battery does nothing on modern board | Settings in non-volatile flash |
| VMs slow / virtualization unavailable | Enable Intel VT or AMD-V |
| Cannot enter BIOS on Windows 10/11 | Fast Startup — use Shift+Restart / Advanced Startup |

## Common Mix-Ups

### Fast Startup vs “BIOS is broken”

Often the key never appears because Windows did not fully shut down.

### Boot password vs supervisor password

- Boot password → can the PC start?
- Supervisor password → can someone change setup?

### Secure Boot vs antivirus

Antivirus runs in the OS. Secure Boot protects the path **before** the OS loads.

### CMOS battery clear on modern boards

Old trick of removing the battery may not reset flash-stored settings. Use the clear jumper / official method.

### Disabling hardware in BIOS vs Device Manager

BIOS disable hides hardware from the OS. Device Manager disable is an OS-level action after boot.

## Quick Review

| Topic | Remember |
| --- | --- |
| Enter setup | Del / F1 / F2 (vendor-specific) |
| Windows tip | Shift+Restart or Advanced Startup for full firmware entry |
| Safety | Document, understand, back up |
| Boot order | First working OS device wins |
| USB disable | Security control; OS may not see ports |
| Secure Boot | UEFI signatures for OS, bootloader, BIOS updates |
| Passwords | Boot = start PC; Supervisor = change setup |
| Reset | Jumper / CLRTC — follow the board manual |
| Virtualization | Intel VT or AMD-V in CPU setup |

---

## Continue Learning

- Previous Topic: [The BIOS](the-bios.md)
- Next Topic: [HSM and TPM](hsm-and-tpm.md)
- Related: [Motherboard Compatibility](motherboard-compatibility.md)
- Back to [Domain 3 — Hardware](README.md)
