# Troubleshooting Hardware

CompTIA A+ Core 1 — 220-1201  
Objective 5.1 — Given a scenario, troubleshoot common hardware issues

## What You Need to Know

By the end of this lesson, you should understand how to approach:

- POST failures, beep codes, and boot-order problems
- Incorrect BIOS date/time (motherboard battery)
- Windows stop errors / BSoD
- Proprietary application crash messages
- Blank or black screens
- No power / partial power symptoms
- Sluggish performance
- Overheating and random shutdowns
- Application crashes and Reliability Monitor
- Unusual noises and capacitor failure
- Motherboard battery vs BIOS reset on modern boards

## What Is It?

**Hardware troubleshooting** is the process of finding why a computer, laptop, or related device will not start, display, run stably, or perform correctly — then fixing the cause.

This lesson focuses on common Core 1 scenarios:

- Startup / POST problems
- Crash screens
- Display and power issues
- Performance, heat, noise, and failing components

## Why Does It Matter?

Help desk and field techs see these problems constantly:

- PC beeps and will not boot
- Blue screen after a driver or hardware change
- Monitor is black
- Fans spin but nothing else happens
- Laptop is slow on battery
- System shuts off with no warning
- Grinding, clicking, or smoke from the case

Exam questions often give a symptom and ask what to check next.

## Real-World Analogy

Think of the PC as a car that will not start or run right:

- **POST** = dashboard lights and startup self-check
- **Beep codes / BSoD** = warning lights with codes you look up
- **Blank screen** = headlights/wiring before you blame the engine
- **No power** = battery, cable, or alternator path
- **Overheating shutdown** = engine temperature protection
- **Odd noises** = something loose, scraping, or failing mechanically

## How It Works

### POST — Power-On Self-Test

At power-on, **POST** checks core hardware:

- CPU present and talking to firmware
- Video subsystem
- Memory installed

If something fails, you may get:

- An on-screen error (if video works)
- **Beep codes** from the motherboard

**Important:** Beep codes differ by manufacturer. Do **not** memorize one vendor’s codes for the exam or the job — use the motherboard documentation.

When you hear beeps:

1. Note long/short pattern and any on-screen codes
2. Look them up in the manufacturer docs
3. That points to which subsystem failed

### Beeps but Black Screen

If you hear beeps but see nothing:

Likely suspects:

- Bad / misconfigured video
- Bad memory
- Bad CPU

Also check BIOS video settings if you can enter setup on another known-good display path.

### Incorrect BIOS Date and Time

Prompt for date/time every boot often means the **motherboard battery** failed.

That battery keeps the clock when the PC is unplugged. Replace the battery, set date/time once, and the prompt should stop.

### Unexpected Boot Device (USB First)

If the PC boots from a USB drive instead of the internal SSD:

- Check **BIOS boot order**
- Put the internal drive higher than USB when you want normal boots
- Ensure a valid OS exists on the chosen device
- Some firmware skips empty USB ports and moves to the next boot device

### Windows Stop Error / BSoD

A **Windows stop error** (often called the **Blue Screen of Death / BSoD**) means Windows hit a problem it could not recover from.

Common causes:

- Bad hardware
- Bad drivers
- Bad application / software conflict

What to capture from the blue screen:

- Driver name (if shown)
- **Stop code** (use with Microsoft’s stop-code resources)

Recovery ideas after a recent change:

- Last Known Good (where available)
- System Restore
- Roll back the newest driver
- Safe Mode if the crash happens at startup

Hardware checks:

- Reseat adapter cards and memory
- Run motherboard / vendor **hardware diagnostics** (quick or overnight tests)

### Proprietary Crash Screens

Apps can show their own crash dialogs. Messages may be clear — or useless (“Error 47829…”, “Unknown error”).

Technician habits:

- Document the exact text
- Screenshot or photograph the error
- Check Event Viewer / app logs
- Send details to the application vendor

On a help desk, ask users to attach a screenshot when they open a ticket.

### Blank / Black Screen

Work the basics first:

1. Is the video cable seated on PC **and** monitor?
2. Is the **power** cable connected to the monitor?
3. Is the monitor input set to the correct port (HDMI vs DP vs VGA vs USB-C)?
4. Check brightness/contrast in the monitor OSD
5. Try a **known-good monitor**

If you see BIOS/POST video but a black screen after Windows starts:

- Suspect Windows video configuration / drivers
- Try starting with a generic video mode (historically **VGA mode** via advanced boot options — process can vary by Windows version)

### No Power / Partial Power

Ask where power is missing:

| Check | Tool / idea |
| --- | --- |
| Wall outlet | Multimeter — AC present? |
| Power cord | Damaged / loose? |
| PSU DC outputs | Multimeter — rails present? |

Symptom pattern:

- **Fans spin, no video / no other lights** → often POST / motherboard / video path, or weak PSU rails (fans need little power; motherboard needs more)
- Trace what *is* powered (PSU direct vs motherboard headers)

### Sluggish Performance

Start with **Task Manager**:

- Processes: CPU, memory, disk, network hogs
- Performance tab: trends over the last minute

Then widen the search:

| Check | Why |
| --- | --- |
| Windows Update | Missing patches/drivers |
| Disk free space | OS needs working space |
| Defrag (HDD only) | Fragmentation can hurt spinning disks |
| Laptop power mode | CPU may throttle on battery |
| Antivirus / antimalware scan | Malware can burn resources |

### Overheating

Heat sources: CPU, GPU, memory, and more.

Cooling depends on:

- Clean fans and clear airflow
- Proper heat sinks and thermal paste
- Intake/exhaust not blocked (dust under desks is common)

Dust-clogged cooling → thermal throttling → sluggish performance.

Use vendor or third-party sensor tools (example from the video: HWMonitor) to read temperatures.

### Smoke or Burning Smell

1. **Remove power immediately**
2. After it is safe, open the case
3. Look (and carefully smell) for the damaged area
4. Replace the failed component or motherboard as needed

### Random Power-Off (No Message)

Often **thermal protection** — sensors shut the system down to prevent damage.

Also check:

- Fans, airflow, heat sinks, thermal paste
- Temperature monitoring software
- Newly added hardware / Device Manager disables
- Hardware diagnostics

Check **Event Viewer** after reboot for any last messages before the shutdown.

### Application Errors and Crashes

Symptoms:

- “X has stopped working”
- App vanishes with no message

Tools:

- **Event Viewer**
- Application-specific logs
- **Reliability Monitor** — timeline of app/Windows failures, warnings, info; links into Event Viewer details
- Uninstall/reinstall if install corruption is suspected

### Unusual Noises

| Sound | Likely direction |
| --- | --- |
| Rattle when moving case | Loose part (often heat sink) |
| Scraping | Hard drive mechanical issue |
| Methodical clicking | Fan obstruction / dirty fan |
| Pop + smoke | Capacitor failure |

### Capacitors

Look for:

- Flat tops (healthy)
- Bulging tops (failing)
- Blown debris (catastrophic)

Blown capacitors usually mean hardware replacement (often the board).

### Motherboard Battery Notes

| Situation | Action |
| --- | --- |
| Date/time lost every boot | Replace CMOS/motherboard battery |
| Need full BIOS reset on modern board | Usually **jumper / CLRTC** — removing battery alone may not clear settings or passwords |

## Side-by-Side Comparison

| Symptom | First useful checks |
| --- | --- |
| Beeps + codes | Manufacturer POST docs |
| Beeps + black screen | Video / RAM / CPU |
| Date/time prompt | Motherboard battery |
| Boots USB instead of SSD | Boot order |
| BSoD | Stop code, recent drivers/hardware, Safe Mode |
| App crash dialog | Screenshot + logs + vendor |
| Black monitor | Cables, power, input select, known-good display |
| Fans only | PSU rails, POST path |
| Slow PC | Task Manager, updates, disk space, power plan, malware |
| Random off | Heat, fans, Event Viewer, diagnostics |
| Smoke | Kill power, inspect, replace parts |
| Odd noise | Loose sink / HDD / fan / capacitor |

## Key Terms

| Term | Meaning |
| --- | --- |
| POST | Power-On Self-Test at startup |
| Beep code | Audible POST failure pattern (vendor-specific) |
| BSoD / stop error | Windows fatal system crash screen |
| Stop code | Code used to research a BSoD |
| Safe Mode | Minimal Windows start for troubleshooting |
| VGA mode | Generic video boot option for display issues |
| Reliability Monitor | Windows history of failures and warnings |
| Thermal throttling | CPU slows when too hot |
| Capacitor | Board component that can bulge/blow |
| CMOS / motherboard battery | Keeps clock (and historically some settings) |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Beeps differ by board | Check manufacturer documentation |
| Beeps, blank display | Video, RAM, or CPU |
| Asks for time every boot | Replace motherboard battery |
| Boots flash drive unexpectedly | Boot order |
| Blue screen after new driver | Roll back driver / Safe Mode / restore |
| Capture stop code | Use for Microsoft troubleshooting path |
| Monitor power/cable/input | Blank screen basics |
| Fans spin, no POST video | Motherboard/video/PSU voltage |
| Slow laptop unplugged | Power-saving CPU throttle |
| Dusty case, slow PC | Overheating / throttling |
| Sudden black shutdown | Often overheating protection |
| Clicking fan / scraping drive | Mechanical noise diagnosis |
| Bulging capacitor | Hardware failure — replace board/part |

## Common Mix-Ups

### Memorizing beep codes

Codes are vendor-specific. Look them up.

### BSoD is “just Windows being Windows”

Treat it as a serious stop — gather the code and recent changes.

### Black screen = dead PC

Often cable, power, or input select on the monitor.

### Fans spinning means PSU is fine

Fans can run on limited power while motherboard rails are bad.

### Removing the battery always clears BIOS passwords

On many modern boards, settings live in flash — use the clear jumper process.

### Defrag on SSD for sluggishness

Defrag is for HDDs; SSDs are handled differently — focus on free space and health tools.

## Quick Review

| Topic | Remember |
| --- | --- |
| POST | Core hardware check; use vendor beep docs |
| Battery | Fixes repeating date/time prompts |
| Boot order | Controls USB vs internal drive priority |
| BSoD | Stop code + recent change + Safe Mode / rollback |
| Crashes | Document/screenshot; Event Viewer; Reliability Monitor |
| Blank screen | Cable, power, input, known-good monitor |
| No power | Outlet → cord → PSU (multimeter) |
| Slow | Task Manager → updates → disk → power → malware |
| Heat | Clean airflow; sensors; thermal paste/sinks |
| Smoke / random off | Cut power; heat or failing hardware |
| Noise | Loose / HDD scrape / fan click / capacitor pop |

---

## Continue Learning

- Previous Topic: [Cloud Characteristics](../4-virtualization-and-cloud/cloud-characteristics.md)
- Next Topic: [Troubleshooting Storage Devices](troubleshooting-storage-devices.md)
- Related: [The BIOS](../3-hardware/the-bios.md)
- Related: [Cooling](../3-hardware/cooling.md)
- Back to [Domain 5 — Hardware and Network Troubleshooting](README.md)
