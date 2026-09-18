# Troubleshooting Printers

CompTIA A+ Core 1 — 220-1201  
Objective 5.6 — Given a scenario, troubleshoot common printer issues

## What You Need to Know

By the end of this lesson, you should understand how to approach:

- Isolating app vs driver vs OS vs hardware with test pages
- Bad output (streaks, fade, ghosting/speckling)
- Garbled prints (wrong driver / PDL mismatch)
- Paper jams, pickup rollers, and creased paper
- Stuck print queues and the spooler
- Grinding noises
- Finishing problems (staples, hole punch)
- Wrong page orientation
- Wrong paper tray / size mismatch
- Network printer connectivity and onboard print servers

## What Is It?

**Printer troubleshooting** separates software (app, driver, spooler) from the mechanical printer and from the network path — then fixes the layer that is actually broken.

## Why Does It Matter?

Printer tickets mix everything IT touches: Windows drivers, queues, paper path, toner, and Ethernet/Wi-Fi. Exam questions often hinge on:

- Which test page isolates the fault
- What a vertical line or ghost image means
- Spooler / queue behavior
- Tray and paper-size mismatches

## Real-World Analogy

Think of printing like a restaurant order:

- App = customer’s order
- Spooler = kitchen ticket rail
- Driver / PDL = language the kitchen understands (PCL vs PostScript)
- Printer hardware = the grill and conveyor
- Network = the delivery hallway
- OS test page = ordering the house special without the customer’s app
- Printer self-test = cooking without any kitchen tickets at all

## How It Works

### Isolate with Test Pages

| Test | What it includes | Pass means |
| --- | --- | --- |
| **OS / driver test page** (Windows Print Test Page) | OS + driver — not the app | Driver path works; page also lists printer/driver file details |
| **Printer self-test** | Hardware only | Printer mechanics/imaging work without OS/driver |

| Result | Suspect |
| --- | --- |
| Both pass, app fails | The **application** (try another app or update it) |
| Self-test fails | Hardware / consumables / internal fault |
| Self-test OK, OS test bad | Driver / OS / queue path |

### Bad Output Quality

| Symptom | Likely cause |
| --- | --- |
| Vertical line down the page (inkjet) | Dirty **print heads** — clean them |
| Vertical line down the page (laser) | Scratch on the **photosensitive drum** |
| Faded / hard to read | Low toner or ink |
| Ghosting / double image / speckles (laser) | Drum **not cleaning** properly — shadow of prior rotation |

### Garbled Prints

Garbage characters / scrambled layout often means:

- Wrong or corrupted **printer driver**
- Wrong printer model selected
- Wrong page description language (**PCL** vs **PostScript**)

Confirm with a printer self-test:

- Self-test good → driver/OS/app path
- Self-test also garbled → hardware

### Paper Path Problems

| Issue | Guidance |
| --- | --- |
| Paper jam | Do **not** rip paper — leave scraps inside. Open covers so mechanisms release, then remove carefully |
| No feed / multi-feed | Tray or worn/dirty **pickup rollers** — clean; maintenance kits often include replacements |
| Creased output (esp. laser) | Paper path problem or wrong **paper weight** — use manufacturer-recommended stock |

### Stuck Queue / Print Spooler

The **spooler** sits between apps and the printer. One corrupted job can freeze or crash it so nothing prints.

Windows notes from the transcript:

- Spooler may auto-restart on first/second failure, then stop until you intervene
- Check **Event Viewer → Windows Print Service**
- Delete or move the bad job; let the rest print; troubleshoot that job separately

### Grinding Noises

Printers click and whir — grinding is not normal.

Common checks:

- Paper jam
- Loose / poorly seated ink cartridge (carriage rubs)
- Failing mechanical part (may need specialist / teardown)

Always follow the printer’s service manual for noise troubleshooting.

### Finishing Issues

Many MFDs collate, staple, bind, or hole-punch.

| Problem | Check |
| --- | --- |
| Staple jam | Clear per documentation (varies by model) |
| Hole punch misaligned | Application settings + latest print driver |

### Page Orientation

Portrait prints as landscape (or reverse) = setting mismatch.

Check in order:

1. Application print dialog
2. Driver defaults
3. Update/reinstall driver if needed
4. Printer’s own default orientation (affects later jobs)

### Paper Trays and Size

Multi-tray printers need the job’s paper size to match the selected tray.

| Check | Why |
| --- | --- |
| Driver tray list vs physical trays | Admin should confirm they match |
| Letter vs legal (etc.) | Wrong size → printer “paper mismatch” messages |
| Driver tray properties | Configure what size/media each tray holds |

### Network Printers

Treat them like any network device:

1. Wired vs wireless? (cable vs RF interference)
2. Verify IP, subnet mask, gateway, DNS
3. Check onboard **print server** (web UI — stop/start, manage jobs)
4. Confirm Ethernet **link lights** / activity

## Side-by-Side Comparison

| Symptom | First useful direction |
| --- | --- |
| Don’t know where fault is | OS test page + printer self-test |
| Vertical black line | Inkjet: clean heads; laser: scratched drum |
| Ghost / shadow images | Laser drum cleaning failure |
| Fade | Ink/toner low |
| Garbled text | Driver / wrong PDL; confirm with self-test |
| Jobs pile up, nothing prints | Spooler / corrupt job |
| Grind / scrape | Jam or unseated cartridge |
| Wrong orientation | App → driver → printer defaults |
| Paper mismatch alert | Tray size vs job size |
| Networked printer offline | IP config, link, print server |

## Key Terms

| Term | Meaning |
| --- | --- |
| Print test page | OS/driver output without an app |
| Self-test / printer test | Hardware-only print |
| Photosensitive drum | Laser imaging cylinder — scratches leave lines |
| Ghosting | Faint repeat of prior image from poor drum cleaning |
| PDL | Page description language (e.g. PCL, PostScript) |
| Pickup rollers | Feed paper from the tray |
| Print spooler | Service that queues and sends jobs |
| Finishing | Collate, staple, bind, hole punch |
| Print server (on printer) | Embedded service managing network jobs |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Vertical line, laser | Scratched drum |
| Vertical line, inkjet | Dirty print heads |
| Ghost images | Cleaning failure on drum |
| Garbled print | Wrong/bad driver or PDL |
| Queue stuck for everyone | Spooler / one bad job |
| Multi-feed or no feed | Pickup rollers |
| Creases | Path or wrong paper weight |
| Landscape when portrait chosen | Driver/app/printer orientation |
| Paper size error on panel | Tray mismatch |
| Printer unreachable on LAN | IP / link / print server |

## Common Mix-Ups

### Always blame the printer first

Use self-test vs OS test vs app to isolate.

### Yank jammed paper hard

Rips leave scraps that cause more jams.

### Ghosting = low toner

Ghosting is usually cleaning/drum, not empty toner (fade is low toner/ink).

### Garbled = always hardware

Often wrong driver or PCL/PostScript mismatch.

### Spooler “just broken forever”

Often one corrupt job — clear it and restart the service.

## Quick Review

| Topic | Remember |
| --- | --- |
| Isolate | Printer test vs OS test vs app |
| Lines | Inkjet heads vs laser drum |
| Ghost / fade | Cleaning vs low ink/toner |
| Garbled | Driver / PDL |
| Paper | Don’t tear; rollers; weight |
| Queue | Spooler + Event Viewer |
| Noise | Jam / cartridge seat / part |
| Finish | Staple jam; driver for punches |
| Orientation / trays | App, driver, printer, size match |
| Network | Same as any host + print server |

---

## Continue Learning

- Previous Topic: [Troubleshooting Networks](troubleshooting-networks.md)
- Related: [Multifunction Devices](../3-hardware/multifunction-devices.md)
- Related: [Laser Printer Maintenance](../3-hardware/laser-printer-maintenance.md)
- Back to [Domain 5 — Hardware and Network Troubleshooting](README.md)
- Back to [Core 1](../README.md)
