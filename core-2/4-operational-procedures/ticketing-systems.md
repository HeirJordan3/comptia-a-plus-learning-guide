# Ticketing Systems

CompTIA A+ Core 2 — 220-1202  
Objective 4.1 — Given a scenario, implement best practices associated with documentation and support systems

## What You Need to Know

By the end of this lesson, you should understand:

- Why organizations use ticketing systems
- The help desk’s role (intake, triage, assign, monitor)
- What to capture when creating a ticket
- Categories, severity/priority, and escalation
- Clear communication: description, progress notes, resolution
- Linking related tickets to find trends
- How tickets support reporting and handoffs

## What Is It?

A **ticketing system** is the shared tool IT uses to record, assign, track, and resolve support requests — so nothing relies on memory, sticky notes, or one person’s inbox.

## Why Does It Matter?

Without tickets:

- Problems get lost
- The wrong team gets the work
- Nobody knows status or history
- Managers cannot measure response or resolution time

With tickets, the help desk can triage, escalate, and prove what was done — and future techs can reuse past resolutions.

## Real-World Analogy

Think of a ticket like a hospital chart:

- Patient / contact = who needs help (and who to call)
- Chief complaint = problem description
- Department = category (network, login, hardware…)
- Urgency = severity / priority
- Progress notes = every step taken
- Discharge summary = resolution details
- Linked charts = other related cases that show a pattern

## How It Works

### What Ticketing Systems Do

| Capability | Benefit |
| --- | --- |
| Document issues | Full record of what happened |
| Assign work | Network issues → network team; server issues → server team |
| Guide resolution | Structured workflow from open to closed |
| Reporting | How fast issues are handled; volume by category |

### The Help Desk’s Role

The help desk usually owns the ticket queue. They:

1. Take intake (phone, email, text, portal)
2. **Triage** — what is urgent? what can wait? what stays at help desk vs handoff?
3. Use infrastructure knowledge to choose the next step
4. Create/assign the ticket
5. Monitor so the issue is handled on time

### Information Gathering (Ticket Creation)

Quality at intake drives speed of resolution.

| Capture | Why it matters |
| --- | --- |
| User / contact | Who has the problem; who to communicate with |
| Device | Laptop vs mouse (etc.) changes the fix |
| Problem description | Enough detail for next steps without a callback |
| Category | Routes work (network, authentication, hardware, onboarding…) |
| Severity / priority | Critical multi-user impact vs “within seven days” |
| Escalation need | Higher severity or specialist team when policy requires |

Confirm names and contact info — directories and AD sync can lag.

### Categories

Broad buckets that route and filter work, for example:

- Fix account / login problem
- Guest Wi-Fi
- New mobile device
- Hardware request
- Change request
- Onboarding
- Report a system problem
- Generic “get IT help”

Categories often map to specific owners or teams. Filters let you list all tickets of one type (e.g. guest Wi-Fi).

### Severity and Escalation

| Idea | Meaning |
| --- | --- |
| Severity / priority | Low → medium/high → critical / highest |
| Criteria | Who is affected, role, business impact, deadlines |
| Escalation | Hand off to a specialist or another team (network, Linux admin…) |

Same hardware issue might be **critical** for one department and **medium** for another — follow org policy.

Example: vendor needs guest Wi-Fi next week for a long-running fix → **highest** priority so it is done before they arrive.

### Clear, Concise Communication

Others will read this ticket. Keep:

| Field | Purpose |
| --- | --- |
| Problem description | Clear picture of the issue |
| Progress notes | What was tried, by whom, over days/weeks — detailed but scannable |
| Resolution details | Final fix so the next person can repeat it months later |

Also clarify **who the contact is** when someone calls on another user’s behalf.

### Contacts and Directories

Tickets usually pull users from a central directory (often **Active Directory**). Email/text intake may auto-fill from address or phone number. Always verify with the caller.

### Demo-Style Workflow (Typical Ticket)

1. Open a **service request** (not an outage or post-incident review, unless it is)
2. Choose request type (e.g. fix account problem)
3. Select who it is for (search “Dan…” → Daniel)
4. Summary: short title (e.g. problems logging into Intranet 01)
5. Description: details, screenshots, next-step notes
6. Create → review the new work item

Put recommendations in the description: call back, link to a larger event, or assign to another department.

### Progress Notes and Resolution

Solving the problem is not the end — **document the resolution**. Linked older tickets help when the same issue returns a year later.

### Linking Tickets and Trends

Related work items can show:

- Duplicates (another VPN outage report)
- Related projects (Sydney VPN upgrade)
- Recurring patterns (VPN access errors for 60 days)

Linking justifies bigger fixes (e.g. upgrade cost) and keeps teams aligned in one system.

## Side-by-Side Comparison

| Situation | Ticket approach |
| --- | --- |
| Login to intranet fails | Category: account/auth; capture user + server name |
| Vendor needs Wi-Fi next week | Guest Wi-Fi category; high priority before arrival |
| Many people hit Sydney VPN | Link tickets; may escalate severity / justify upgrade |
| Caller reports for a coworker | Record affected user + primary contact |
| Problem spans days | Progress notes from each tech |

## Key Terms

| Term | Meaning |
| --- | --- |
| Ticket | Recorded support request / work item |
| Help desk | Team that intakes, triages, and tracks tickets |
| Triage | Sorting by priority and who should handle it |
| Category / request type | Type of issue for routing and filtering |
| Severity / priority | How urgent the ticket is |
| Escalation | Raising severity or handing to another team |
| Progress notes | Ongoing troubleshooting log |
| Resolution details | Final fix documentation |
| Linked tickets | Related/duplicate items showing trends |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Lost requests / no history | Need a ticketing system |
| Who handles network vs server | Assign / escalate by category |
| “How fast do we resolve?” | Reports from the ticketing system |
| Incomplete first note | Poor intake slows resolution |
| Critical vs low | Severity based on impact and policy |
| Specialist team needed | Escalation |
| Same VPN issue for weeks | Link tickets; trend analysis |
| Clear handoff | Description + progress + resolution |

## Common Mix-Ups

### Ticket created = problem solved

No — track progress and write the resolution before closing.

### Severity = always “how mad the user is”

Use policy: scope, role, business impact, deadlines.

### Vague description is fine because you can call back

Good intake reduces callbacks and speeds handoffs.

### Categories are only for looks

They route work and enable filtering/reporting.

## Quick Review

| Topic | Remember |
| --- | --- |
| Purpose | Document, assign, resolve, report |
| Help desk | Intake → triage → assign → monitor |
| Intake | User, device, description, category, severity |
| Communicate | Clear description, progress notes, resolution |
| Escalate | Specialist team or higher severity per policy |
| Link | Duplicates and trends unlock better fixes |

---

## Continue Learning

- Next Topic: [Asset Management](asset-management.md)
- Related (Module 11): [Document Types](document-types.md)
- Back to [Domain 4 — Operational Procedures](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
