# Physical Access Security

CompTIA A+ Core 2 — 220-1202  
Objective 2.1 — Summarize various security measures and their purposes

## What You Need to Know

By the end of this lesson, you should understand:

- How a **key fob** uses the same RFID idea as a badge
- What a **smart card** stores (a signed **certificate**) and why a second factor is added
- How a **mobile digital key** lives on a phone
- Why a site still keeps **physical keys** in a checkout cabinet
- How **biometrics** turn a body feature into a stored model
- Which biometric methods are stronger, and why **voice** is weaker
- Why **lighting** helps cameras
- What a **magnetometer** can and cannot detect

## What Is It?

**Physical access security** is how a site decides that *you* may open a door, start a car, or log on to a laptop. The proof might be a fob, a card, a phone, a metal key, or a measurement of your body.

## Why Does It Matter?

The last lesson covered the building: bollards, vestibules, cameras, and guards. This lesson is the credential in your hand or on your body. Exam questions ask which control fits the clue: fob, smart card, phone key, retina, voice, lights, or a metal detector.

## Real-World Analogy

Think of getting into an apartment building:

| Method | What you present |
| --- | --- |
| Plastic tag on your key ring | Key fob |
| Work badge with a chip that proves who you are | Smart card |
| Phone app that unlocks the lobby | Mobile digital key |
| Numbered key you sign out from the office | Physical key cabinet |
| Finger or face at the door | Biometrics |
| Bright entry so the camera sees your face | Lighting |
| Walk-through frame at a courthouse | Magnetometer |

## How It Works

### Key Fob

A **key fob** is a small piece of plastic, usually on a keychain, with an **RFID** tag inside. You use it when access badges are not available.

Hold it near the sensor. The reader checks the tag and allows or denies the door. Functionally it matches a badge. The difference is the shape: a fob stays on a key ring, so it is easy to find.

### Smart Card

Many badges also have storage. That storage holds a **certificate**: a cryptographic ID that has been **digitally signed**. The system can check the signature and confirm the certificate belongs to that person.

A certificate alone is not the whole login. You scan the badge (which presents the certificate), then confirm you are the right holder:

| Second step | Example |
| --- | --- |
| Something you know | A PIN |
| Something you are | A biometric |

The reader might be:

- Built into a laptop (the laptop has to be purchased with that reader)
- Built into a door badge reader
- An external reader plugged in by USB

To sign in on that laptop, slide the card in, then complete the second step.

### Mobile Digital Key

A **mobile digital key** stores the key in the phone instead of on a separate badge or key ring. Phones already unlock cars, hotel rooms, office doors, and home locks.

The extra check is unlocking the phone first. Until the phone is unlocked, the digital key is not available to use.

### Physical Key Cabinet

Electronic locks are not always the right choice:

- They can cost too much for every door
- Some rooms should not depend on electronics
- A power loss must not trap people or block emergency access

Those doors use a normal key. The keys live in one cabinet. A person checks a key out and checks it back in. Keys are numbered so you take the one that matches the door.

A common rule: they hold your photo ID in the cabinet while you have the key. You get the ID back when you return the key.

### Biometrics

**Biometrics** measure a physical trait, turn it into a digital key, and store that key for the next time you authenticate.

A fingerprint scanner does **not** keep a picture of your fingerprint. It builds a **mathematical model** of the print and stores that model. Fingerprints are unique enough that an exact match to someone else is unusual. The model is also hard to edit into someone else’s print.

Not every scanner or setup is equally strong. The device and how the site deploys it both matter.

| Method | What it measures | How strong it is in practice |
| --- | --- | --- |
| Retina | Capillaries at the back of the eye | One of the most accurate |
| Fingerprint | A model of the print | Common on phones, laptops, and doors |
| Palm | Size and shape of the hand | Uses the whole hand, not one finger |
| Face (FRT) | A 3D map from many points on the face | About 1 in 1 million **false acceptance** |
| Voice | How you speak, after training phrases | Weaker; usually paired with another factor |

**Facial recognition (FRT)** uses a laser-dot projector. It marks many points and builds a 3D model. That model can unlock a phone or a data-center door. **False acceptance** means the system lets the wrong person in. A rate around 1 in 1 million is a strong result.

**Voice recognition** stores a model of your speaking style after you say several phrases. Later checks often use *different* phrases than the ones used in training. The model still decides whether the speaker is you. It is not the strongest biometric. Sites combine it with another factor. Your voice also changes when you are sick, so a voice check can fail even when you are the right person.

### Lighting

Dark areas are easier to hide in. More **lighting** makes a space safer and gives security cameras a usable picture. If the goal is video, the light has to be strong enough to read a license plate or see a face clearly enough for facial recognition.

### Magnetometer

A **magnetometer** is the walk-through metal detector at a secure entrance. The scan is **passive**: you walk through, and the frame looks for metal on you.

It cannot see what is not metal. A ceramic weapon does not set it off.

## Side-by-Side Comparison

| Credential | You carry | Extra check |
| --- | --- | --- |
| Key fob | RFID tag on a keychain | The reader’s allow list |
| Smart card | Signed certificate in the badge | PIN or biometric |
| Mobile digital key | The key inside the phone | Unlock the phone first |
| Metal key | A numbered key from the cabinet | ID left behind until the key returns |
| Biometric | Nothing separate; it is your body | Quality of the scanner and the method |

## Key Terms

| Term | Meaning |
| --- | --- |
| Key fob | A keychain token with an RFID tag inside |
| Smart card | A badge that stores a digitally signed certificate |
| Certificate | A cryptographic ID the system can verify |
| Mobile digital key | A door, car, or building key stored on a phone |
| Key cabinet | A locked set of numbered physical keys checked out and back in |
| Biometrics | A body measurement stored as a digital key |
| Mathematical model | The stored form of a fingerprint; not a photo of the print |
| Retina scanner | Reads capillaries at the back of the eye |
| Palm print | Size and shape of the hand |
| FRT | Facial recognition technology; a 3D map of the face |
| False acceptance | The system allows someone who is not the enrolled person |
| Voice recognition | A model of how you speak; weaker, and affected by illness |
| Lighting | Illumination that makes an area safer and cameras more useful |
| Magnetometer | A passive walk-through metal detector |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Plastic tag on a key ring, tap to enter | Key fob (RFID) |
| Badge stores a signed certificate | Smart card |
| Slide a card into the laptop, then enter a PIN | Smart card plus a second factor |
| USB device reads the badge | External smart-card reader |
| Unlock the office with a phone | Mobile digital key |
| Must unlock the phone before the key works | Second factor on the phone |
| Electronic lock is too costly, or power might fail | Physical key |
| Leave your license until you bring the key back | Key cabinet checkout |
| Stored fingerprint is not a picture | Mathematical model |
| Capillaries in the eye | Retina scan; very accurate |
| Whole hand, not one finger | Palm print |
| Laser dots build a 3D face | Facial recognition (FRT) |
| Wrong person accepted about once per million | Strong false-acceptance rate for face |
| Speak phrases; voice changes when sick | Voice recognition; pair it with another factor |
| Cameras cannot read plates at night | Add lighting |
| Walk through; it finds metal only | Magnetometer |
| Ceramic knife not detected | Magnetometer ignores non-metal |

## Common Mix-Ups

### A key fob is a different technology from a badge

Both use **RFID**. A fob is the keychain form you get when badges are not issued. You still hold it near the reader.

### The system keeps a photo of your fingerprint

It keeps a **mathematical model** of the print. That model is the key it compares later.

### Every biometric is equally strong

A **retina** scan and a 3D **face** map are much stronger than **voice**. Voice is usually combined with another factor, and illness can change a voice enough to fail the check.

### A phone key is secure because the key is hidden in an app

The extra security in this design is that you **unlock the phone** before the key can be used.

### A magnetometer replaces a bag search

It only reports **metal**. Ceramic and other non-metal objects walk through.

### Lights are only for comfort

For security, light is what lets a camera read a plate or a face. A dark lot makes the other controls weaker.

## Quick Review

| Topic | Remember |
| --- | --- |
| Key fob | RFID on a keychain; same tap as a badge |
| Smart card | Signed certificate, then PIN or biometric |
| Phone | Mobile digital key; unlock the phone first |
| Metal keys | Numbered cabinet; ID stays until the key returns |
| Fingerprint | Model, not a picture |
| Strongest in this lesson | Retina; face is about 1 in 1 million false acceptance |
| Weakest in this lesson | Voice; combine it, and it fails when you are sick |
| Cameras | Need enough light for plates and faces |
| Magnetometer | Passive metal check only |

---

## Continue Learning

- Previous Topic: [Physical Security](physical-security.md)
- Next Topic: [Logical Security](logical-security.md)
- Back to [Domain 2 — Security](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
