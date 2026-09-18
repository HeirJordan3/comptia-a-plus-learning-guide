# Troubleshooting Mobile Devices

CompTIA A+ Core 1 — 220-1201  
Objective 5.4 — Given a scenario, troubleshoot common mobile device issues

## What You Need to Know

By the end of this lesson, you should understand how to approach:

- Battery drain, bad signal polling, and battery health settings
- Swollen batteries (safety first)
- Broken screens / glass
- Improper charging (port debris, cable, adapter, outlet)
- Weak Wi-Fi / cellular connectivity
- Liquid damage and LCI indicators
- Overheating and auto-shutdown
- Frozen/black touchscreen resets
- Damaged charge ports / board replacement
- Malware symptoms on mobile
- Cursor drift / digitizer problems
- Apps that will not install
- Stylus (battery, Bluetooth, tip damage)
- Slow / stuttering performance

## What Is It?

**Mobile troubleshooting** finds why phones, tablets, and similar devices will not charge, stay cool, connect, respond to touch, or run apps correctly — then fixes the cause safely.

This lesson focuses on laptops-as-mobile-power ideas only where battery drain patterns overlap; the core focus is phones and tablets.

## Why Does It Matter?

Users live on mobile devices. Common tickets:

- Battery dies in hours
- Will not charge
- Screen cracked
- Dropped in water
- Overheats in the sun
- Ghost touches / cursor drift
- App will not download
- Stylus dead

Exam questions often ask the **safest next step** (especially swollen batteries and liquid damage).

## Real-World Analogy

Think of a phone like a sealed mini-PC:

- Battery = fuel tank (can swell dangerously)
- Digitizer = touch layer on the glass
- Charge port = fuel door (debris blocks it)
- LCI = “wet paint” sticker that proves liquid got in
- Airplane mode = stop searching for a tower when the signal is hopeless

## How It Works

### Battery Drain and Health

Batteries wear out. Replace when they no longer hold a useful charge.

Rapid drain is not always an “old battery”:

| Cause | What to try |
| --- | --- |
| Bad cellular reception | Phone keeps searching for signal — try **Airplane Mode** in dead zones |
| Unused radios | Disable Wi-Fi, Bluetooth, GPS when not needed |
| Hungry apps | Check **Settings → Battery** (iOS / iPadOS / Android) for top consumers |

Battery screens often show:

- Last charge
- App usage
- Battery health / replace guidance

### Swollen Battery — Safety Critical

A failing lithium battery can **swell** with gas and push the case open.

| Do | Do not |
| --- | --- |
| Power off immediately | Pierce or open the cell |
| Stop using the device | Keep using “because it still works” |
| Replace the battery ASAP | Ignore swelling |

The pouch is designed to contain gas — better a damaged phone than a fire. Swelling can crack the device; replace the battery (and assess other damage).

### Broken Screens

Hardened glass can still break.

- Back up before screen service
- Glass is usually bonded to the display — replace the **display assembly**, not “just glass”
- Broken glass is sharp — avoid bare-finger use; temporary screen protector or tape can reduce cuts

### Will Not Charge

Check the whole path:

1. Charge **port** clear of debris
2. Try a **known-good cable**
3. Try another **wall adapter**
4. Confirm the **outlet** has power (multimeter if needed)

Worn cables from daily bending often fail intermittently.

### Connectivity Problems

| Network | Checks |
| --- | --- |
| Cellular | Close enough to a tower? Step outside buildings |
| Wi-Fi | Near the AP? Interference? Congestion? |
| Congested Wi-Fi | Change AP channel / band and retest |

### Liquid Damage

Phones and liquids do not mix. Techs look for an **LCI** (Liquid Contact Indicator) in charge or SIM areas — it changes color when wet.

If liquid gets on the device:

1. **Power off** — do not charge
2. Remove case
3. Remove cards / battery if removable
4. Air dry; prefer **desiccant** packs over rice
5. Leave alone about **24 hours** — no heat/oven, no charging, minimal handling
6. Then try power-on; service if it fails

**Rice myth:** Rice mostly just keeps people from touching the phone. Desiccant absorbs moisture better.

### Overheating

Passive cooling only goes so far.

Triggers:

- Hot rooms / **direct sun** (dashboard)
- Charging while under heavy CPU use
- Power-hungry apps

Actions:

- Check battery report for hot apps; close unused apps
- Get out of sunlight
- Let the device cool; auto-shutdown is protection

### Frozen / Unresponsive Black Screen

Force restart (vendor-specific):

| Platform | Typical idea |
| --- | --- |
| Apple | Power off/on; or hold power + home/volume (model-dependent) ~10 seconds |
| Android | Varies widely — battery remove (if possible) or power + volume combos |

Always check the device’s official reset steps.

### Damaged Charge / Data Port

Rough cable handling can damage the USB/Lightning/USB-C port.

Symptoms: intermittent or no charging/data.

Ports are often **not modular** — repair may mean replacing the **system board**.

### Malware

Unusual apps, unexpected data use, or abnormal CPU/battery drain can mean malware.

Run reputable mobile anti-malware / antivirus and remove suspects.

### Cursor Drift / Ghost Touches

Screen acts like it is being touched with no contact.

Usually a **digitizer / display** fault — not malware.

| Step | Note |
| --- | --- |
| Calibration app (older devices) | Retrain touch mapping |
| If drift continues | Replace display / digitizer |

### Apps Will Not Install

| Check | Why |
| --- | --- |
| Free storage | Most common cause |
| Network bandwidth | Large apps need a solid connection |
| Compatibility | OS / device support |
| Store authentication | Username, password, MFA |

### Stylus Issues

Modern styluses are often **active** (need power) and may use **Bluetooth**.

| Check | Action |
| --- | --- |
| Stylus battery | Recharge |
| Bluetooth pairing | Pair again |
| Physical damage / tip | Inspect; replace tip if worn |
| Still failing | Reset tablet and/or stylus; power cycle |

### Slow / Stuttering Device

| Check | Note |
| --- | --- |
| OS and app updates | Fix bugs and improve performance |
| Free storage | Low space can slow or force restarts |
| Storage hardware wear | Slow reads/writes feel like “app problems” |
| Background apps | Close heavy CPU/RAM users |
| Aging hardware | Newest apps may need a newer device |

## Side-by-Side Comparison

| Symptom | First useful direction |
| --- | --- |
| Fast battery drain | Signal searching, radios, battery report |
| Case swelling | Stop use; replace battery (fire risk) |
| Cracked glass | Backup; replace display; avoid cuts |
| No charge | Debris → cable → adapter → outlet |
| Weak signal | Location, Airplane Mode, Wi-Fi channel |
| Got wet | Power off; dry with desiccant; wait |
| Overheat / auto-off | Sun, heavy apps, charging under load |
| Ghost touches | Digitizer; calibrate or replace screen |
| App won’t install | Storage, network, compatibility, login |
| Dead stylus | Charge, pair, tip, reset |

## Key Terms

| Term | Meaning |
| --- | --- |
| Battery health | OS report of capacity / replace guidance |
| Swollen battery | Battery inflated with gas — unsafe |
| Digitizer | Touch-sensing layer of the screen |
| Cursor drift | Ghost input without touch |
| LCI | Liquid Contact Indicator |
| Desiccant | Moisture-absorbing packets (better than rice) |
| Airplane Mode | Disables radios (stops constant tower search) |
| Active stylus | Powered stylus, often Bluetooth-paired |
| Force restart | Hardware key combo to reboot a frozen device |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Battery dies in weak coverage | Constant signal search; Airplane Mode |
| Phone puffed open | Swollen battery — power off, replace |
| Will not charge | Port debris / bad cable |
| Dropped in water | Power off; no charge; desiccant; wait |
| Rice | Myth for absorption; isolation is the real gain |
| Overheats on dashboard | Heat + load; remove from sun |
| Ghost taps | Digitizer / cursor drift |
| App install fails | Storage space first |
| Stylus dead after travel | Charge + Bluetooth pair |
| Slow phone, almost full | Free storage / updates |

## Common Mix-Ups

### Keep using a swollen battery “carefully”

No. Power off and replace. Fire risk.

### Rice dries phones best

Desiccant is better; the main win is not powering a wet phone.

### Ghost touches = malware

Usually digitizer/display hardware.

### Broken glass only

Usually the whole display assembly.

### Charge port “just dirty forever”

Clear debris first, but physical damage may need board replacement.

## Quick Review

| Topic | Remember |
| --- | --- |
| Drain | Radios + signal hunting + hungry apps |
| Swollen | Stop, replace, do not puncture |
| Charge path | Port → cable → adapter → outlet |
| Liquid | Off, dry, desiccant, wait ~24h |
| Heat | Sun and heavy apps; auto-off protects hardware |
| Touch issues | Digitizer; calibrate or replace |
| Install fails | Space, network, compatibility, auth |
| Stylus | Battery, Bluetooth, tip |
| Slow | Updates, storage, background load, age |

---

## Continue Learning

- Previous Topic: [Troubleshooting Display Issues](troubleshooting-display-issues.md)
- Next Topic: [Troubleshooting Networks](troubleshooting-networks.md)
- Related: [Troubleshooting Hardware](troubleshooting-hardware.md)
- Back to [Domain 5 — Hardware and Network Troubleshooting](README.md)
