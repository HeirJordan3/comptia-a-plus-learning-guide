# Task Manager

CompTIA A+ Core 2 — 220-1202  
Objective 1.4 — Given a scenario, use the appropriate Microsoft Windows 10/11 features and tools

## What You Need to Know

By the end of this lesson, you should understand:

- How to open **Task Manager**
- What the **Services**, **Startup**, **Processes**, **Performance**, and **Users** tabs show
- How to start, stop, or restart a service
- How to disable startup apps when troubleshooting boot problems
- How to find which app is using the most CPU, memory, disk, or network
- How to see and disconnect users on a multi-user system

## What Is It?

**Task Manager** is a real-time Windows tool that shows how the operating system is performing right now — running programs, background work, hardware usage, startup apps, services, and who is connected.

## Why Does It Matter?

When a PC is slow, frozen, or acting strange at login, Task Manager is often the first place to look. It answers:

- What is running?
- What is using the most CPU, memory, disk, or network?
- What starts automatically?
- Which services can be restarted?
- Who else is connected to this computer?

## Real-World Analogy

Think of Task Manager like a restaurant manager’s board during a busy shift:

| Tab | Restaurant view |
| --- | --- |
| Processes | Every order currently in the kitchen |
| Performance | How hot the ovens are, and how full the fridges are, over the last minute |
| Startup | What the staff turns on automatically when the restaurant opens |
| Services | Background systems (water, power, POS) you can restart |
| Users | Everyone logged in or using the restaurant’s resources, even if they are not standing at the counter |

## How It Works

### Opening Task Manager

| Method | How |
| --- | --- |
| Security screen | **Ctrl+Alt+Delete** → Task Manager |
| Taskbar | Right-click the taskbar → Task Manager |
| Fast shortcut | **Ctrl+Shift+Esc** — Task Manager opens immediately |

### Services

The Services tab lists services running on the computer. You can also reach a fuller Services tool from Control Panel, but Task Manager is a quick front end.

From this tab you can:

- See services on this computer
- Right-click a service to **start**, **stop**, or **restart** it
- Open the Services applet for more options

### Startup

Many apps launch automatically when Windows starts. The Startup tab is where you manage that list.

When a problem happens during startup:

1. Disable one app, or disable several
2. Restart and test
3. Turn apps back on one at a time, or in groups
4. When the problem returns, you have found the startup app to leave disabled

Right-click an entry to **enable** or **disable** it for the next boot.

### Processes

The Processes tab is a live list of what is running now:

- Apps on the Windows desktop
- Background processes

Default columns typically include:

- CPU
- Memory
- Disk
- Network
- GPU
- Other metrics

You can rearrange columns, sort them, and right-click to add more metrics. Sorting is how you find the app using the most memory or the most network.

### Performance

The Performance tab shows hardware use as graphs, usually covering about the **last 60 seconds**.

Common graphs along the left side:

| Graph | What it tells you |
| --- | --- |
| CPU | Processor utilization |
| Memory | RAM in use |
| Disk | Storage activity |
| Network | Network activity |
| GPU | Graphics processor use (when the PC has one) |

Use this historical view to decide whether a problem looks like CPU, memory, disk, or network pressure.

### Users

Windows is a multi-user operating system. People can log on locally, and other people can use resources on this computer over the network. You might be the only person at the desk while many others are connected remotely.

The Users tab shows:

- Who is connected
- Which apps or resources they are using

From this view you can **disconnect** a user and remove their access.

## Side-by-Side Comparison

| You need to… | Use this tab |
| --- | --- |
| Restart a Windows service | Services |
| Stop an app from launching at boot | Startup |
| See what is running right now | Processes |
| Watch CPU or memory over the last minute | Performance |
| See who is logged on or using this PC | Users |
| Kick a remote user off | Users → disconnect |

## Key Terms

| Term | Meaning |
| --- | --- |
| Task Manager | Real-time Windows monitoring and control tool |
| Process | A program or background task currently running |
| Service | A Windows background component you can start, stop, or restart |
| Startup app | A program set to launch when Windows boots |
| Performance graph | A short history (about 60 seconds) of hardware use |
| Users tab | Shows local and network users connected to this computer |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Fastest way to open Task Manager | Ctrl+Shift+Esc |
| App slows the PC right after login | Startup tab — disable and retest |
| Which program is using the most RAM? | Processes — sort by Memory |
| CPU has been high for the last minute | Performance tab |
| Restart the print spooler from a quick view | Services tab — restart |
| Someone is connected over the network | Users tab — see or disconnect them |

## Common Mix-Ups

### Processes and Services are the same list

Processes are running apps and background tasks. Services are Windows service components you start, stop, or restart.

### Startup disable uninstalls the app

Disabling a startup item only stops it from launching at boot. The app is still installed.

### The Users tab only shows the person at the keyboard

It also shows people using this computer’s resources over the network.

## Quick Review

| Topic | Remember |
| --- | --- |
| Open it | Ctrl+Shift+Esc, Ctrl+Alt+Delete, or right-click the taskbar |
| Services | Start, stop, restart |
| Startup | Enable or disable boot apps to isolate login problems |
| Processes | Live apps plus CPU, memory, disk, network, GPU |
| Performance | Graphs for about the last 60 seconds |
| Users | Who is connected — and you can disconnect them |

---

## Continue Learning

- Next Topic: [The Microsoft Management Console](the-microsoft-management-console.md)
- Related: [The Windows Control Panel](the-windows-control-panel.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
