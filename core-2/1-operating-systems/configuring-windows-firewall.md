# Configuring Windows Firewall

CompTIA A+ Core 2 — 220-1202  
Objective 1.7 — Given a scenario, configure Microsoft Windows networking features on a client/desktop

## What You Need to Know

By the end of this lesson, you should understand:

- What **Windows Defender Firewall** is and why it stays on
- **Domain**, **private**, and **public** profiles
- Broad settings: block all incoming, and notify when a new app is blocked
- **Windows Defender Firewall with Advanced Security**
- How to create an inbound rule by program, port, predefined rule, or custom rule

## What Is It?

**Windows Defender Firewall** is the personal firewall built into Windows. It decides which network traffic is allowed to reach the PC and which traffic the PC may send. It is meant to stay **enabled**.

## Why Does It Matter?

A PC on a coffee-shop network should not use the same rules as a PC on the company domain. Firewall settings are where you:

- Temporarily turn the firewall off while you test a connection
- Block unexpected inbound connections
- Allow one app or one port
- Build a custom rule, such as blocking unencrypted web traffic on TCP port 80

Changing these settings requires **elevated** (administrator) rights.

## Real-World Analogy

Think of the firewall as a building receptionist with three rulebooks:

| Profile | Building |
| --- | --- |
| Domain | The company office |
| Private | A trusted home or small office |
| Public / guest | A coffee shop or hotel |

Advanced Security is the full policy binder: who may come in, who may go out, and a log of what was blocked.

## How It Works

### Where to Open It

- Control Panel → **Windows Defender Firewall**
- Search for Windows Defender Firewall

The main page shows separate status for:

- Domain networks
- Private networks
- Guest or public networks

Each profile can have its own settings. The page also shows whether the firewall is on, whether it blocks connections that are not on the allow list, which network you are on now, and whether it notifies you when it blocks a new app.

### Broad Settings for Each Profile

For a private network, a public network, or both, you can:

| Setting | Effect |
| --- | --- |
| Turn Windows Firewall on | The profile filters traffic |
| Block all incoming connections | Blocks inbound traffic **even if** you previously allowed it — use this when you do not want anyone connecting in |
| Notify when a new app is blocked | Windows tells you instead of blocking silently |

Turn the firewall off only for a short troubleshooting test, then turn it back on. That change needs administrator rights.

### More Precise Rules

Broad on/off settings are not always enough. You can allow inbound traffic for:

- One **application** (a specific program)
- One **port number**, when you do not want to name an executable

Windows also includes a long list of **predefined** apps and features you can enable or disable depending on the network. If none of those fit, build your own exception.

### Advanced Security

**Windows Defender Firewall with Advanced Security** is the administrator view. Open it from the left side of the firewall page.

| Section | What it holds |
| --- | --- |
| Inbound rules | Traffic coming **into** this PC |
| Outbound rules | Traffic leaving this PC |
| Connection security rules | Extra requirements for how connections are protected |
| Monitoring | What the firewall is doing |

### Creating an Inbound Rule

Right-click **Inbound Rules** → **New Rule**. Choose a rule type:

| Type | Use it when |
| --- | --- |
| Program | The rule applies to one application, or to all programs |
| Port | The rule applies to a TCP or UDP port |
| Predefined | You want a rule Windows already includes |
| Custom | You need program, port, and address choices together |

Example: block unencrypted web traffic **into** this PC on **TCP port 80**.

1. Choose **Custom**.
2. **Program:** leave it set so the rule applies to all programs.
3. **Protocol and ports:** TCP, local port **80** (a specific port, not all ports). Remote port can be **any**.
4. **Scope:** which IP addresses. **Any** local address and **any** remote address, or name specific addresses.
5. **Action:**
   - Allow the connection
   - Allow the connection if it is secure
   - **Block the connection** (this example)
6. **Profile:** Domain, Private, and/or Public. Leave all checked to apply everywhere.
7. **Name:** for example, `Block Unencrypted Web Traffic`, then Finish.

That rule blocks inbound TCP port 80, the non-encrypted form of web traffic, on the profiles you selected.

## Side-by-Side Comparison

| Goal | Where |
| --- | --- |
| Different rules at home vs at a cafe | Private profile vs public profile |
| Stop every inbound connection while traveling | Block all incoming connections |
| Let one app accept connections | Allow rule for that program |
| Let one port through without naming an app | Port rule |
| Block TCP 80 from anywhere | Custom inbound rule: TCP, local port 80, Block |
| See outbound rules and monitoring | Windows Defender Firewall with Advanced Security |
| Turn the firewall off to test | Firewall settings — needs administrator rights; turn it back on |

## Key Terms

| Term | Meaning |
| --- | --- |
| Windows Defender Firewall | Built-in Windows personal firewall |
| Profile | A rule set for domain, private, or public networks |
| Inbound rule | Controls traffic coming into the PC |
| Outbound rule | Controls traffic leaving the PC |
| Predefined rule | A rule Windows already includes for a known app or feature |
| Custom rule | A rule you build with your own program, port, and address choices |
| Port 80 | TCP port used for unencrypted web traffic |
| Elevated rights | Administrator permission required to change the firewall |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Firewall that ships with Windows | Windows Defender Firewall |
| Stricter rules on public Wi-Fi than at home | Separate public and private profiles |
| Domain-joined PC has another rule set | Domain profile |
| Block everything inbound, even previous allows | Block all incoming connections |
| Allow one executable | Program rule |
| Allow or block a TCP/UDP number | Port rule |
| Block unencrypted web inbound | Inbound TCP port 80, action Block |
| Need outbound rules or monitoring | Firewall with Advanced Security |
| Cannot turn the firewall off | Need an elevated account |

## Common Mix-Ups

### Turning the firewall off is a normal fix

It is a **temporary** troubleshooting step. Leave Windows Defender Firewall enabled for normal use.

### One firewall setting covers every network

Domain, private, and public profiles can each have different rules.

### “Block all incoming” still honors your allow list

That option blocks incoming connections **including** ones you explicitly allowed.

### Port 80 is secure web traffic

Port 80 is **unencrypted** web traffic. Encrypted web traffic uses a different port.

### Any user can create firewall rules

Changing the firewall requires **administrator** rights.

## Quick Review

| Topic | Remember |
| --- | --- |
| Product | Windows Defender Firewall — leave it on |
| Profiles | Domain, private, public/guest |
| Broad options | On/off, block all incoming, notify on new apps |
| Precision | Program, port, predefined, or custom |
| Advanced | Inbound, outbound, connection security, monitoring |
| Example rule | Custom inbound block, TCP local port 80, all profiles |

---

## Continue Learning

- Previous Topic: [Windows Network Technologies](windows-network-technologies.md)
- Next Topic: [Windows IP Address Configuration](windows-ip-address-configuration.md)
- Related: [The Windows Control Panel](the-windows-control-panel.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
