# Windows Command Line Tools

CompTIA A+ Core 2 — 220-1202  
Objective 1.5 — Given a scenario, use the appropriate Windows command-line tools

## What You Need to Know

By the end of this lesson, you should understand:

- Normal vs **elevated** Command Prompt
- How to get **help** and move around folders
- **chkdsk**, **format**, and **diskpart**
- **copy** vs **robocopy**
- **hostname**, **winver**, and **whoami**
- **gpupdate** and **gpresult**
- **sfc /scannow**

## What Is It?

The **Windows command line** (Command Prompt) is a text window where you type commands to inspect and change the computer. Search for **cmd**. Some commands need a normal prompt. Commands that change the system usually need **Run as administrator**.

## Why Does It Matter?

The command line is often faster than clicking through menus when you are:

- Checking a folder or copying files
- Repairing a file system
- Confirming which computer, Windows version, and user you are on
- Forcing Group Policy or repairing protected Windows files

Running the wrong command on the wrong machine — especially **format** — can erase data. Confirm the computer first.

## Real-World Analogy

Think of Command Prompt like a service elevator:

| Idea | Meaning |
| --- | --- |
| Normal prompt | You can look around and move boxes you already own |
| Elevated prompt | You have the building keys — you can change the structure |
| Current folder | The floor you are standing on |
| `cd` | Change floors |
| `hostname` | Read the name on the building before you cut power |

## How It Works

### Opening the Prompt

| Way | Result |
| --- | --- |
| Search **cmd** → Open | Normal rights |
| Run as administrator | Elevated prompt |
| Right-click Command Prompt → Run as administrator | Elevated prompt |
| **Ctrl+Shift+Enter** after selecting it | Elevated prompt |

You must be in the **Administrators** group to elevate. Normal rights cover most lookups. Changing OS configuration or repairing disks needs elevation.

The prompt shows your current folder, for example `C:\Users\alex`.

### Getting Help

| Command | What you get |
| --- | --- |
| `help` | List of commands at this prompt |
| `help dir` | Help for one command |
| `dir /?` | Same style of help, asked from the command itself |

**Ctrl+C** can stop a long listing.

### Looking at Files and Folders

**`dir`** lists files and directories in the current folder. You can also give a drive and path to list somewhere else. Directories are marked `DIR`.

Every command uses your **current working directory** unless you type a full path.

| Command | Action |
| --- | --- |
| `cd` or `chdir` | Change directory |
| `cd ..` | Go up one folder (`..` means the parent) |
| `md` or `mkdir` | Make a directory |
| `rd` or `rmdir` | Remove a directory |

`cd` accepts a folder name in the current location, or a full path. **Tab** can autocomplete a name. `md` and `rd` often return you to the prompt with no extra message — run `dir` to confirm.

Paths use a **backslash** (`\`) between the drive and each folder:

`C:\Users\alex\Documents`

**C:** is usually the Windows system drive. File Explorer’s Local Disk (C:) is the same tree you see at the prompt.

### Check Disk (`chkdsk`)

A file system such as **NTFS** can get out of sync with the files on the drive after a power loss or a disk problem. **chkdsk** compares the index to the files.

| Switch | What it does |
| --- | --- |
| `chkdsk /f` | Fix file-system problems |
| `chkdsk /r` | Sector-by-sector check, recover readable data, **and** do the `/f` fixes |

`/r` takes much longer because it tests the whole drive. Both need an **administrator** prompt.

If the volume is in use, Windows cannot check it now. It offers to run the scan at the **next restart**. During boot you see a scanning and repairing progress display, then Windows continues to start.

### Format

**format** initializes a partition with a file system so it can store files. Example: `format K:` formats the volume whose letter is K.

If you do not name a file system, this command **defaults to FAT32**. It reports the size and the result when it finishes.

Format **erases the partition**. Run it only as an administrator, only on the correct drive, and only when you have a backup.

### DiskPart

**diskpart** is the command-line tool for listing and working with disks, partitions, and volumes. It must run elevated. If you start it from a normal prompt, User Account Control asks for approval and opens an administrator window.

Useful list commands:

- `list disk`
- `list partition`
- `list volume`
- `list vdisk`

A typical `list volume` view might show an optical drive, the **C:** NTFS boot volume, a hidden recovery partition, and a small system partition. You can also format or inspect partitions from here — the same caution as `format` applies.

### Copy and Robocopy

**copy** duplicates a file. You name the source, then the destination.

| Switch | Meaning |
| --- | --- |
| `/v` | Verify the new file was written correctly |
| `/y` | Overwrite the destination **without asking** |

If the destination file already exists, copy asks before it overwrites unless you used `/y`. That matters in a batch file that runs when nobody is there to press Y. Answer carefully: Yes overwrites that file; All overwrites every file in that command.

**robocopy** (robust copy) has many more options. Run `robocopy /?` to see them. Useful ones:

- Copy or skip subdirectories
- **Throttle** bandwidth so a large copy does not fill a slow link
- **Retry** if the network drops, then continue

### Know Which Window You Are In

Several prompts can be open at once. Confirm the machine before you restart it or change it.

| Command | Tells you |
| --- | --- |
| `hostname` | Windows device name |
| `winver` | A dialog with the Windows version (for example Windows 11), version number, and licensing details |
| `whoami` | Computer and user you are logged on as |
| `whoami /all` | User, SID, groups, and privileges |

If a command fails unexpectedly, `whoami` often shows you are not the account you thought you were.

### Group Policy

**Active Directory** is the central database of users and devices. **Group Policy** pushes settings to those computers and users. Policies often apply at logon. To apply them now:

| Command | Use |
| --- | --- |
| `gpupdate /force` | Force a Group Policy refresh on this computer or user |
| `gpresult /r` | Show the **resultant set of policy** (what is actually applied) |

`gpresult /r` can show the domain, the logged-on user, the computer name, whether it is a workstation, the Windows version, the local profile, when policy was last applied, which Group Policy objects applied, and the user’s security groups. After `gpupdate /force`, run `gpresult /r` again to confirm a new policy (for example a desktop-background policy) is listed.

### System File Checker

Core Windows files can be changed by a third-party app, an update, or malware. **SFC** (System File Checker) compares important Windows files to known-good copies.

`sfc /scannow` scans and can repair corrupt protected files. It can take a while. A typical success line says Windows Resource Protection found corrupt files and repaired them. Details go in **cbs.log**, and the tool tells you where that log is.

## Side-by-Side Comparison

| Need | Command |
| --- | --- |
| See files here | `dir` |
| Move up one folder | `cd ..` |
| Make or remove a folder | `md` / `rd` |
| Fix NTFS inconsistencies | `chkdsk /f` (admin; may wait for reboot) |
| Test every sector and fix the file system | `chkdsk /r` |
| Wipe and prepare a partition | `format` — backup first |
| List volumes | `diskpart` → `list volume` |
| Copy one file and skip the overwrite prompt | `copy /y` |
| Copy with retry and bandwidth limits | `robocopy` |
| Confirm the PC name before a reboot | `hostname` |
| Confirm Windows 10 vs 11 | `winver` |
| Confirm the logged-on user and groups | `whoami /all` |
| Push Group Policy now | `gpupdate /force` |
| See which policies applied | `gpresult /r` |
| Repair protected system files | `sfc /scannow` |

## Key Terms

| Term | Meaning |
| --- | --- |
| Command Prompt | The `cmd` window |
| Elevated prompt | Command Prompt running as administrator |
| Working directory | The folder commands use unless you type a full path |
| `..` | The parent folder |
| chkdsk | Check Disk — file system (and optionally sector) repair |
| format | Erase and initialize a partition with a file system |
| diskpart | Disk, partition, and volume tool |
| copy / robocopy | Simple copy vs robust copy |
| hostname | This computer’s name |
| winver | Windows version dialog |
| whoami | Current user and security context |
| gpupdate / gpresult | Refresh Group Policy / show what applied |
| RSOP | Resultant set of policy |
| sfc | System File Checker |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Command fails until you use Run as administrator | Needs an elevated prompt |
| `help dir` and `dir /?` | Two ways to read a command’s help |
| `cd ..` | Move to the parent folder |
| Volume is in use; check at next boot | `chkdsk` on the system drive |
| `/r` vs `/f` | `/r` includes the `/f` fixes and scans sectors |
| Format with no file system named | Defaults to FAT32 |
| Do not prompt when overwriting | `copy /y` |
| Large copy over a slow WAN | `robocopy` throttle and retry |
| “Am I on the right server?” | `hostname` |
| Which Windows build before installing an app | `winver` |
| Policy should apply without logoff | `gpupdate /force` |
| Which GPOs are on this PC | `gpresult /r` |
| Core OS files were changed | `sfc /scannow` |

## Common Mix-Ups

### Any Command Prompt can repair the disk

**chkdsk**, **format**, **diskpart**, and **sfc** need administrator rights.

### `/r` is a lighter check than `/f`

`/r` does the `/f` repair **and** a full sector scan, so it takes longer.

### Defrag and format are the same idea

Format **erases** the volume and builds a file system. It is not a cleanup.

### Startup apps and Group Policy both “refresh themselves”

Group Policy often waits for logon. `gpupdate /force` applies it now. `gpresult /r` shows what landed.

### copy and robocopy are identical

`copy` is the simple file copy. `robocopy` adds retries, subdirectory control, and bandwidth limits.

## Quick Review

| Topic | Remember |
| --- | --- |
| Prompt | `cmd`; elevate with Run as administrator or Ctrl+Shift+Enter |
| Help | `help`, `help command`, or `command /?` |
| Navigate | `dir`, `cd`, `cd ..`, `md`, `rd`; `\` in paths |
| Disks | `chkdsk /f` or `/r`; `format` erases; `diskpart` lists volumes |
| Files | `copy /v /y`; `robocopy` for tough copies |
| Identity | `hostname`, `winver`, `whoami /all` |
| Policy | `gpupdate /force`, then `gpresult /r` |
| System files | `sfc /scannow`; read `cbs.log` |

---

## Continue Learning

- Previous Topic: [Additional Windows Tools](additional-windows-tools.md)
- Next Topic: [The Windows Network Command Line](the-windows-network-command-line.md)
- Related: [The Microsoft Management Console](the-microsoft-management-console.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
