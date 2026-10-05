# Physical Security

CompTIA A+ Core 2 — 220-1202  
Objective 2.1 — Summarize various security measures and their purposes

## What You Need to Know

By the end of this lesson, you should understand:

- How **bollards** and **barricades** stop vehicles and guide people
- What an **access control vestibule** does between the outside and a secure area
- How **badge readers** work (magnetic stripe, **RFID**, **NFC**)
- What **CCTV**, motion detection, and alarms are for
- Door locks: key, **PIN**, token, and **biometrics**
- Why equipment racks are locked but still get airflow
- What a **security guard**, **ID badge**, **access list**, and **audit trail** add
- How a **fence** (and sometimes razor wire) protects a perimeter

## What Is It?

**Physical security** is the set of barriers, locks, cameras, alarms, and people that stop someone from walking up to equipment they should not touch. Software passwords do not help if a stranger can open the rack.

## Why Does It Matter?

Servers, switches, and user data live in real rooms. A help-desk technician is often the person who:

- Badges into a building or data center
- Notices a door propped open
- Explains why a cabinet stays locked
- Knows which control matches an exam scenario (vestibule, bollard, fence, guard, camera)

## Real-World Analogy

Think of a bank branch:

| Bank control | IT equivalent |
| --- | --- |
| Concrete posts in the drive lane | Bollards / barricades |
| The small locked room before the vault | Access control vestibule |
| Key card at the employee door | Badge reader (RFID or NFC) |
| Cameras over the lobby | CCTV |
| Silent alarm under the counter | Duress button |
| Locked teller drawers | Locked equipment racks |
| Person at the desk checking IDs | Security guard and access list |
| Wall around the property | Fence |

## How It Works

### Bollards and Barricades

**Bollards** and **barricades** are steel or concrete barriers outside an entrance. They stop cars and trucks. People can still walk through the gaps, so foot traffic is funneled to one controlled point. That keeps vehicles out of pedestrian areas.

Shapes depend on the site:

| Type | What it does |
| --- | --- |
| Steel posts | Block vehicles at a doorway or walkway |
| Large round concrete barriers | Heavy vehicle stop |
| Canal or moat | A natural water barrier around a building |

### Access Control Vestibule

An **access control vestibule** is a small locked room between the outside world and the protected area (common at a data center). A guard or receptionist checks ID and badges before anyone goes farther.

Doors are set so two paths are not open at once:

| Setup | What happens |
| --- | --- |
| Doors start unlocked | Opening one door locks the others. One person or one group moves through at a time. |
| Doors start locked | An access card opens one door. The other doors stay locked until that door closes. |
| Two-door room | One door in, one door out. While one is open, the other stays locked. |

From the outside you often see a card reader, then a reception desk, then a second door the guard unlocks.

### Badge Readers

Most sites no longer hand out a metal key for every room. An **access card** talks to a **badge reader**.

| Reader | How you use it |
| --- | --- |
| Magnetic stripe | Older style. You swipe the card. |
| RFID | A chip and a loop antenna inside the card. Hold it near the reader. |
| NFC | Same idea: bring the badge close. No swipe. |

Readers open locked doors. They can also clock people in and out, or record that a guard completed a patrol round.

### Video Surveillance (CCTV)

**CCTV** means **closed-circuit television**: cameras that show what is happening without a person standing in that spot. Cameras around a site are networked back to one recording station, so one operator can watch many locations.

Modern cameras can:

- Tell vehicle types apart
- Read license plates
- Use infrared (and similar night vision) when it is dark
- Raise an alarm on the console when they see motion

### Alarms and Sensors

| Control | What triggers it |
| --- | --- |
| Circuit sensor | A door, window, or fence opens, closes, or moves |
| Motion sensor | Movement in an area, even if nobody is watching the screen |
| Duress button | A person under threat pushes a hidden button (often under a desk) |

The alert goes to the security team. You do not have to be looking at that camera at that second.

### Door Locks

| Lock | How access is proved |
| --- | --- |
| Conventional lock and key | A physical key. A **deadbolt** adds a second, stronger bolt. |
| Electronic lock | A **PIN** (personal identification number) on a keypad |
| Token lock | The **RFID** chip in a badge |
| Biometric lock | Fingerprint, handprint, or retina scan |

High-security doors stack factors. Example: scan the badge, enter a PIN, then use a fingerprint. Each factor checks a different thing: something you **have**, something you **know**, and something you **are**.

### Equipment Locks

Inside a data center, different teams share the room. Cabinets still need their own locks.

Typical rack setup:

1. Racks sit side by side so nobody can pull a side panel and reach in.
2. Front and back doors lock.
3. Openings at the top and bottom (or perforated / glass doors) let cool air through.
4. Only someone with the key opens the door.

### Guards, Badges, and Access Lists

A **security guard** sits at reception and may patrol. The guard checks identification and either allows or denies entry.

Employees wear an **ID badge** (photo and name, usually on a lanyard) everywhere in the building. Visitors get a badge too. Some sites take a photo and print a temporary badge on arrival.

Some facilities require **pre-registration**. The guard checks an **access list**: the names allowed in that day. A name on the list speeds entry.

That process is an **audit trail**. The site records who came in, where they went, and when they left. People do not walk in and out with no record.

### Fences

A **fence** is the perimeter. It keeps people from crossing a boundary.

| Feature | Purpose |
| --- | --- |
| Transparent or opaque | See through it, or hide what is inside |
| Heavy metal | Hard to break |
| Tall | Hard to climb |
| Razor wire (extreme sites) | Extra deterrent along the top |

## Side-by-Side Comparison

| Control | Stops | Does not replace |
| --- | --- | --- |
| Bollard | Vehicles | A person on foot |
| Vestibule | Two doors open at once; unknown visitors | A camera record by itself |
| Badge reader | People without a valid card | A lost card that was never disabled |
| CCTV | “Nobody was watching” | A lock on the door |
| Motion / door alarm | Silent entry | Identifying who it was |
| Guard + access list | Unlisted visitors | A locked rack inside the room |
| Fence | Casual perimeter crossing | The door at the building |

## Key Terms

| Term | Meaning |
| --- | --- |
| Bollard | A post or barrier that blocks vehicles |
| Barricade | A barrier that blocks or channels access |
| Access control vestibule | A small room between outside and a secure area; one path open at a time |
| Badge reader | A device that reads an access card |
| RFID | A chip plus antenna in a card; works when held near the reader |
| NFC | Close-range badge or phone tap on a reader |
| CCTV | Closed-circuit television; cameras recorded to a central station |
| Motion sensor | Alerts when something moves |
| Duress button | A hidden alarm a person presses when they feel unsafe |
| Deadbolt | An extra physical bolt on a keyed door |
| PIN | A number you type on an electronic lock |
| Biometrics | Fingerprint, handprint, or retina used as proof of identity |
| Security guard | A person who checks IDs and patrols |
| ID badge | Photo and name worn in the building |
| Access list | Names pre-approved to enter that day |
| Audit trail | A record of who entered, where they went, and when they left |
| Fence | A perimeter barrier; may include razor wire |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Stop cars, let people walk through | Bollards / barricades |
| Water around the building | Moat or canal as a barrier |
| Small room; one door locks when the other opens | Access control vestibule |
| Swipe a stripe | Older magnetic badge reader |
| Tap a card; chip and antenna inside | RFID (or NFC) |
| Many cameras, one recording desk | CCTV |
| Camera sees in the dark | Infrared |
| Door or window opens and security is notified | Circuit alarm |
| Something moves and security is notified | Motion sensor |
| Button under the desk | Duress alarm |
| Key plus a second bolt | Conventional lock and deadbolt |
| Type a number on the door | Electronic lock, PIN |
| Finger, hand, or eye | Biometrics |
| Badge, then PIN, then fingerprint | Multiple factors |
| Rack doors locked; air still flows | Equipment lock with vents or perforated doors |
| Person checks your ID at the desk | Security guard |
| Photo on a lanyard | ID badge |
| Name must be on today’s list | Access list / pre-registration |
| Time in, where they went, time out | Audit trail |
| Tall metal barrier, maybe razor wire | Fence |

## Common Mix-Ups

### A vestibule is just a lobby

A lobby is a waiting area. An **access control vestibule** is built so you cannot hold both doors open and walk straight through. Someone checks who is moving.

### RFID and a metal key do the same job

A metal key opens a conventional lock. **RFID** is the chip inside a badge that a reader detects up close. You can still have both on the same door.

### CCTV locks the building

Cameras **record and alert**. They do not stop a person the way a lock, bollard, or guard does.

### Locking a rack means sealing it airtight

Front and back doors lock. Tops, bottoms, or perforated doors stay open enough for **cooling**.

### An access list is the same as a badge

The **access list** is who is allowed in today. The **badge** is what that person carries. The **audit trail** is the record after they enter.

## Quick Review

| Topic | Remember |
| --- | --- |
| Vehicles | Bollards, barricades, sometimes a moat |
| People flow | Vestibule: one path at a time, then a guard |
| Cards | Magnetic swipe, or RFID/NFC tap |
| Eyes | CCTV to one station; infrared at night |
| Alerts | Door/window/fence circuit, motion, duress button |
| Doors | Key, PIN, token, biometrics; stack them when risk is high |
| Gear | Lock rack doors; keep airflow |
| People process | Guard, badge, access list, audit trail |
| Perimeter | Tall fence; razor wire only on extreme sites |

---

## Continue Learning

- Previous Topic: [Cloud Productivity Tools](../1-operating-systems/cloud-productivity-tools.md)
- Next Topic: [Physical Access Security](physical-access-security.md)
- Back to [Domain 2 — Security](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
