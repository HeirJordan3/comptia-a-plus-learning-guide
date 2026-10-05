# Logical Security

CompTIA A+ Core 2 — 220-1202  
Objective 2.1 — Summarize various security measures and their purposes

## What You Need to Know

By the end of this lesson, you should understand:

- Why accounts get **least privilege** instead of administrator rights
- What **zero trust** changes about “inside” the network
- How an **access control list (ACL)** allows or denies traffic or file access
- The four common authentication factors
- Why **email**, **SMS**, and **phone calls** are weaker checks
- How an authenticator app and a hardware token create a one-time code
- The difference between **TOTP** and a plain **OTP**

## What Is It?

**Logical security** is the rules in software: who may sign in, what they may open, and which network traffic is allowed. Physical locks stop someone at the door. Logical controls stop them after they are on a computer or on the network.

## Why Does It Matter?

A stolen password or one infected PC should not open the whole company. Support tickets and exam questions both turn on the same ideas: give people only the access they need, do not trust a device just because it is inside the building, and ask for more than a password.

## Real-World Analogy

Think of a hospital:

| Hospital rule | IT equivalent |
| --- | --- |
| A nurse can open patient charts, not the pharmacy safe | Least privilege |
| Staff still badge in at every wing, not only the front door | Zero trust |
| A list of who may enter each room | Access control list |
| ID badge plus a keypad code | Multifactor authentication |
| A code on a keychain fob that changes by itself | Hardware token / TOTP |

## How It Works

### Least Privilege

Every workstation should not be an administrator. If malware or an attacker lands on an admin PC, they can reach far more of the network.

**Least privilege** means a person gets only the rights required for their job. Apps run with those same limited rights. People can still do their work. Malicious software cannot use a spare admin login it never received.

### Zero Trust

Older designs put the firewall at the edge and treated everything inside as safe. Once an attacker got in, the inside of the network was open.

**Zero trust** means no device is trusted because of where it sits. A laptop in the office is checked the same way as a laptop at home. Every user, device, and application authenticates.

Sites that adopt this add controls on the inside, not only at the border:

- Multifactor authentication
- Data encryption
- Tighter permissions
- Extra firewalls between internal systems
- Reporting and analytics on security events

### Access Control Lists

An **ACL** is a list of rules that **allow** or **deny**.

On a router, each rule can look at:

| Criteria | Example question |
| --- | --- |
| Source IP address | Where did this packet come from? |
| Destination IP address | Where is it going? |
| TCP or UDP port | Which service is it using? |
| Protocol | Is it ICMP, or something else? |

Rules can combine those checks. Each matching rule then has a disposition: allow this traffic, or deny it.

The same idea shows up on files. When you set rights on a Windows folder or permissions on a Linux file, you are editing an access control list: who may read, change, or run that object.

### Multifactor Authentication

A username and password are one check. **Multifactor authentication (MFA)** asks for proof from more than one category.

| Factor | What it means | Example in this lesson |
| --- | --- | --- |
| Something you know | A secret you remember | Password |
| Something you have | An object you carry | Phone app, hardware token, SMS, phone call |
| Something you are | Your body | Fingerprint or other biometric |
| Somewhere you are | Your location | GPS during login |

A strong login stacks categories. Password (know) plus a code from an app (have) plus GPS (somewhere) is three factors. Two passwords are still one category: something you know.

### Email as a Check

Many services use your email address during registration. They send a confirmation message. You click it to prove you can open that inbox.

Some services use that email step as the only way in: you enter the address, wait for the message, and the click lets you in. The same inbox is also used later to reset a password or approve a profile change.

### Authenticator Apps and Hardware Tokens

A common “something you have” is a code from an app. The app builds a new pseudorandom code on a device you carry. Opening the app usually requires you to unlock the phone first, which adds another check.

If you do not want the code on a phone, a **hardware token** on a keychain does the same job. You already keep track of your keys, so you keep track of the token.

### SMS and Phone Calls

**SMS** is a text message. During registration you give an email, a password, and a mobile number. At the next login you enter the username and password, then type the code from the text.

Text codes have a serious weakness. An attacker can social-engineer the phone company and move your number onto their phone. Texts then go to them. With your username and password, they finish the login.

A voice call that reads the code out loud has the same problem. Call forwarding sends the call to someone else. The number can also be added to the attacker’s phone. They hear the code. You do not.

### TOTP and OTP

**TOTP** is a **time-based one-time password**. The code on the screen changes about every 30 seconds, even if you are not looking at the app.

Setup stores the same secret on the phone and on the authentication server. Both sides use the time of day, so both compute the same code at the same moment. You type your username, your password, and the code showing right then.

Google Authenticator uses TOTP. The same method shows up with Facebook, Microsoft, and many other services.

A plain **OTP** (one-time password) is used when syncing to the clock is not practical. The app or hardware token gives you a code. You use it once, discard it, and the next login uses the next code in the list. Each code is different, so guessing the next one is not realistic. Phone apps and keychain tokens both work this way.

| | TOTP | OTP |
| --- | --- | --- |
| What changes the code | The clock (about every 30 seconds) | The next unused code in the list |
| What both sides share | A secret, plus the current time | A secret list of codes |
| Where it runs | Phone app or similar | Phone app or hardware token |

## Side-by-Side Comparison

| Control | Question it answers |
| --- | --- |
| Least privilege | What is the smallest set of rights that still lets this person work? |
| Zero trust | Did we authenticate this user and device, even inside the office? |
| ACL | Does this packet, or this person, get an allow or a deny? |
| MFA | Did they prove more than one factor? |
| TOTP | Does the code match what the server expects at this minute? |

## Key Terms

| Term | Meaning |
| --- | --- |
| Least privilege | Only the rights needed to do the job |
| Zero trust | Nothing is trusted just because it is inside the network |
| ACL | A list of allow or deny rules for traffic or for files |
| Disposition | The allow or deny result when a rule matches |
| MFA | Login that requires more than one factor category |
| Something you know | A remembered secret, such as a password |
| Something you have | A phone, app, or hardware token you carry |
| Something you are | A biometric, such as a fingerprint |
| Somewhere you are | Location, such as GPS at login |
| Hardware token | A keychain device that shows a login code |
| SMS | A text message carrying a login code |
| TOTP | A one-time code that changes on a timer, about every 30 seconds |
| OTP | A one-time code you use once, then replace with the next code |
| Secret key | The shared value the phone and the server use to compute the same TOTP |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Users are not domain admins | Least privilege |
| Malware on one PC should not own the network | Limited rights on that account and its apps |
| The firewall is only at the edge | The weakness zero trust is meant to fix |
| Every user and device authenticates, inside or outside | Zero trust |
| Internal firewalls, encryption, MFA, and security logs | Controls added for zero trust |
| Router allows or blocks by IP, port, or protocol | Network ACL |
| Windows or Linux file permissions | An ACL on the file or folder |
| Password plus a phone code | MFA: know + have |
| App also checks GPS | Somewhere you are |
| Fingerprint | Something you are |
| Click a link sent to your inbox | Email confirmation |
| Code in a text message | SMS |
| Attacker convinces the carrier to move the number | SMS or call factor stolen |
| Call forwarding steals the spoken code | Voice-call factor |
| Code changes every 30 seconds | TOTP |
| Google Authenticator, Facebook, Microsoft app codes | TOTP |
| Use a code once, then the next code in the list | OTP |
| Same secret on the phone and the server, synced to the clock | How TOTP stays in step |

## Common Mix-Ups

### Two passwords count as multifactor

Both are **something you know**. MFA needs a second category, such as a code you have or a biometric you are.

### Zero trust means the internal network is blocked

People still work inside the building. Zero trust means that location is not proof. The user, the device, and the app still authenticate.

### An ACL is only a router feature

Routers use ACLs for packets. Windows rights and Linux permissions are ACLs for files and folders.

### SMS is as strong as an authenticator app

A text or a phone call follows the **phone number**. That number can be moved or forwarded. An app code from TOTP is tied to a secret on that device and the current time.

### TOTP and OTP are the same timer

**TOTP** changes because the clock changed. A plain **OTP** changes because you already used the previous code.

## Quick Review

| Topic | Remember |
| --- | --- |
| Least privilege | Minimum rights for the job; apps stay limited too |
| Zero trust | Inside is not “already safe” |
| ACL | Allow or deny by IP, port, protocol, or by file rights |
| Factors | Know, have, are, somewhere you are |
| Email | Proves you can open that inbox; also used for resets |
| SMS / phone call | Easy to redirect by moving or forwarding the number |
| TOTP | Shared secret + time; new code about every 30 seconds |
| OTP | Next code in the list; use it once |

---

## Continue Learning

- Previous Topic: [Physical Access Security](physical-access-security.md)
- Next Topic: [Authentication and Access](authentication-and-access.md)
- Back to [Domain 2 — Security](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
