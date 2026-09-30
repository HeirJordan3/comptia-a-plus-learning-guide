# Windows Network Technologies

CompTIA A+ Core 2 — 220-1202  
Objective 1.7 — Given a scenario, configure Microsoft Windows networking features on a client/desktop

## What You Need to Know

By the end of this lesson, you should understand:

- What a **Windows share** is and how to map it to a drive letter
- **Hidden shares** that end with `$`
- Where to see every share on a computer
- **Workgroups** vs **domains**
- Why a business uses **Active Directory**
- Which Windows editions can join a domain
- How to **share a printer**

## What Is It?

Windows networking lets computers use each other’s files, folders, and printers. A **share** is a resource you publish on the network. Computers are organized in a **workgroup** (each PC keeps its own accounts) or a **domain** (one central login for the organization).

## Why Does It Matter?

Help desk work constantly asks:

- How do I open a folder that lives on another PC?
- Why doesn’t this share show up in the list?
- Why does the same person need a different password on every home PC?
- Can this laptop join the company domain?
- How do I let the office print to the printer on this desk?

## Real-World Analogy

| Idea | Like |
| --- | --- |
| Share | A labeled cabinet other people can open over the network |
| Mapped drive | Giving that cabinet a short letter (H:, X:) on your computer |
| Hidden share (`$`) | A cabinet that is not on the directory, but opens if you know the exact name |
| Workgroup | A house where every room has its own lock and key |
| Domain | An office building with one badge that opens the doors you are allowed to use |

## How It Works

### Shares and Mapped Drives

A Windows share can be a file, a folder, a printer, or another resource on the network.

To use a share on another computer, **map a drive letter** to it:

| Method | How |
| --- | --- |
| File Explorer | Choose **Map network drive** |
| Command line | `net use` |

In the map-drive dialog you choose:

- The drive letter (many letters are free if X, Y, and Z are already used)
- The share, by browsing or by typing the folder path
- Whether to **reconnect at sign-in**
- Whether to connect with **different credentials** than the account you are using now

When you are done, disconnect that network drive from File Explorer.

### Hidden Shares

Put a **dollar sign** at the end of the share name to hide it from the normal browse list. **ADMIN$** is a share named ADMIN that does not appear in the user-interface list.

Hiding is not the same as locking. Anyone who knows the name can still try to open it. It only stays off the dropdown of available shares.

To see every share configured on this computer, including hidden ones, open **Computer Management → Shared Folders**.

### Workgroups

A **workgroup** is the usual home setup. Devices share one workgroup name, but each computer is standalone.

Each PC keeps its **own usernames and passwords**. The login that works for a printer on one PC can be different from the login for a shared folder on another PC. That gets hard to track as you add devices.

### Domains

A **domain** is the usual business setup. User accounts, computers, and resources are managed in one place. People remember **one** set of credentials instead of a different login for every PC.

IT can add or remove users and apply settings from that central point. That matters when there are hundreds or thousands of devices.

Check the current mode in **Settings → System → About**, or in the **System** Control Panel applet. It shows the device name and whether the PC is in a workgroup or a domain. Choose **Domain or workgroup** for details. **Change** lets you rename the PC or move it between a workgroup and a domain.

### Active Directory

Domain information lives in **Active Directory Domain Services**, a central database that can be distributed across servers on the network. You add and remove users there, and you push configuration to laptops with policy.

Active Directory needs a **server**. You normally see it in a business, not on a home network.

To join a PC to the domain:

| Requirement | Detail |
| --- | --- |
| Windows edition | **Pro**, or a higher edition. **Windows 10 Home** and **Windows 11 Home** cannot join Active Directory |
| Where | Settings → System → About, or Control Panel → System, then Domain or workgroup → Change |
| Credentials | A username and password that are allowed to add computers, plus the domain name |

After the PC joins, people sign in with **domain** credentials, not only a local account.

### Sharing a Printer

If a printer is physically connected to a Windows PC, you can share it with the network.

1. Open **Settings → Bluetooth & devices → Printers & scanners** (or the printer’s properties).
2. Open **Printer properties**.
3. On the **Sharing** tab, turn on sharing and set the share name.
4. Click **OK**.

Other people on the network can then connect to that printer.

## Side-by-Side Comparison

| Topic | Workgroup | Domain |
| --- | --- | --- |
| Typical place | Home | Business |
| Accounts | Separate on each PC | One central directory |
| Passwords | Can differ per device | One set of credentials |
| Who manages users | Each computer’s owner | IT, in Active Directory |
| Server required | No | Yes |
| Windows edition to join | Any edition can use a workgroup | Pro or higher to join Active Directory |

| Need | Where |
| --- | --- |
| Map a share | File Explorer or `net use` |
| Hide a share from the browse list | End the name with `$` |
| List every local share | Computer Management → Shared Folders |
| See workgroup or domain | Settings → System → About |
| Share the desk printer | Printer properties → Sharing |

## Key Terms

| Term | Meaning |
| --- | --- |
| Share | A file, folder, printer, or other resource published on the network |
| Mapped drive | A drive letter that points at a network share |
| Hidden share | A share whose name ends in `$` so it does not appear in the browse list |
| ADMIN$ | A common hidden administrative share |
| Workgroup | A named group of standalone PCs, each with its own accounts |
| Domain | A centrally managed group of users, computers, and resources |
| Active Directory Domain Services | The database that stores domain accounts and policy |
| Printer sharing | Publishing a local printer so other PCs can print to it |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Give a network folder a drive letter | Map a network drive, or `net use` |
| Share does not appear in the list, but the name works | Hidden share ending in `$` |
| See shares that the browse list hides | Computer Management → Shared Folders |
| Each PC has its own passwords | Workgroup |
| One login for every office PC | Domain |
| Home edition will not join the company network | Need Windows Pro or higher for Active Directory |
| Add users in one place for the whole company | Active Directory |
| Others need to print to the printer on this PC | Sharing tab in printer properties |

## Common Mix-Ups

### A dollar sign on a share name secures it

`$` only **hides** the share from the browse list. It does not stop someone who knows the name.

### A workgroup is a smaller domain

In a workgroup, every computer keeps its **own** accounts. A domain stores accounts in one directory.

### Any Windows 11 PC can join Active Directory

**Home** editions cannot. You need **Pro** or higher, plus an account that is allowed to join the domain.

### Active Directory is normal on a home network

It needs a domain server. Homes usually stay in a workgroup.

## Quick Review

| Topic | Remember |
| --- | --- |
| Share | Network access to a file, folder, or printer |
| Map | File Explorer or `net use`; optional reconnect and other credentials |
| Hide | Name ends with `$`; still reachable if you know it |
| Workgroup | Same group name, separate passwords |
| Domain | One credential store; central IT management |
| Join | Pro or better; domain name plus authorized credentials |
| Printer | Sharing tab → share name → OK |

---

## Continue Learning

- Previous Topic: [Windows Settings](windows-settings.md)
- Next Topic: [Configuring Windows Firewall](configuring-windows-firewall.md)
- Related: [The Windows Network Command Line](the-windows-network-command-line.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
