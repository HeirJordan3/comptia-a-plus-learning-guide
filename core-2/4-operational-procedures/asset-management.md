# Asset Management

CompTIA A+ Core 2 — 220-1202  
Objective 4.1 — Given a scenario, implement best practices associated with documentation and support systems

## What You Need to Know

By the end of this lesson, you should understand:

- Why organizations track technology assets in one place
- What an **asset tag** is and how it ties to a database record
- What a **CMDB** (Configuration Management Database) is used for
- Who uses asset data (IT, finance, licensing)
- The **procurement life cycle** from request to payment

## What Is It?

**Asset management** is tracking an organization’s technology — phones, laptops, desktops, routers, switches, firewalls, modules, cards, and related software licenses — in a central system so support, finance, and purchasing all see the same truth.

## Why Does It Matter?

Without centralized tracking:

- Help desk guesses at make/model/warranty
- Finance cannot report spend or depreciation accurately
- Audits miss unused or missing devices
- License renewals surprise the budget

With it, a tech can pull a user’s full kit by name or tag and resolve issues faster — and the business can plan spending.

## Real-World Analogy

Think of company tech like a library of loaned tools:

- **Asset tag** = library barcode on the item
- **CMDB** = the catalog that says who has what, when it was bought, and what it costs to keep
- **Procurement life cycle** = request → approve → order → receive → pay

## How It Works

### What Gets Tracked

Almost anything IT owns or supports, for example:

- Mobile devices, laptops, desktops
- Network gear (routers, switches, firewalls)
- Modules and cards inside that gear
- Related purchase and support details

### Why a Central Database Helps

| Use | Benefit |
| --- | --- |
| Support | Pull make, model, components, purchase date when a user calls |
| Financial reports | Spend by category (tablets vs laptops) |
| Audits | Confirm devices are still in use |
| Taxes / depreciation | Know purchase date and how long the org has held the asset |

### Asset Tags

Physical label on the device — often org name, QR/barcode, and a unique number.

| In the real world | In the database |
| --- | --- |
| User reads the tag on the laptop | Tech searches that tag number |
| Tag is unique to that unit | Record shows exact hardware assigned |

Ask for the **asset tag / asset number** when the user calls — it removes guesswork.

### CMDB — Configuration Management Database

A **CMDB** is the centralized asset / configuration tracking system used across the organization — not only by the help desk.

| Team | How they use it |
| --- | --- |
| **IT / help desk** | Tie assets to people (laptop, phone, tablet per user) |
| **Finance** | Purchase dates, in-warranty vs out-of-warranty, maintenance vs replace budget |
| **Licensing** | Software license spend, renewal deadlines, renewal cost planning |

### Procurement Life Cycle

The path from “I need equipment” to “vendor is paid.”

| Step | Who / what | Purpose |
| --- | --- | --- |
| 1. Purchase request | End user (internal form) | Lists devices; budgeted or not; formal approvals / sign-offs |
| 2. Sourcing | Purchasing | Negotiate with suppliers — not always lowest price (terms, extra maintenance year, etc.) |
| 3. Purchase order (PO) | Purchasing → vendor | Official order |
| 4. Delivery | Vendor → org / user | Product arrives |
| 5. Invoice | Vendor → purchasing | Bill for what was shipped |
| 6. Payment | Accounting | Pay within the agreed time frame after invoice |

**Checks and balances:** right equipment, approved need, received goods, invoiced correctly, then paid.

## Side-by-Side Comparison

| Situation | Asset-management move |
| --- | --- |
| User: “My laptop is broken” | Ask for asset tag; open CMDB record |
| Manager asks laptop vs tablet spend | Run financial report from the database |
| Device might be unused | Audit against assigned / active assets |
| Warranty question | Check purchase date / warranty status in CMDB |
| New hire needs a laptop | Start procurement: request → approvals → PO → deploy → track |

## Key Terms

| Term | Meaning |
| --- | --- |
| Asset | Tracked technology item (hardware or related licensed software) |
| Asset tag | Physical ID (barcode/QR + number) on the device |
| CMDB | Configuration Management Database — central asset/config system |
| Depreciation | Loss of value over time for accounting/tax purposes |
| Procurement life cycle | Request → approve → purchase → receive → invoice → pay |
| Purchase order (PO) | Formal order sent to the vendor |
| Invoice | Vendor’s request for payment |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Central list of all IT gear | Asset management / CMDB |
| Sticker with barcode on a laptop | Asset tag |
| Help desk needs make/model/warranty fast | Look up asset in CMDB |
| Who owns which laptop? | Asset assigned to user in CMDB |
| In warranty vs replace budget | Finance use of purchase dates |
| Software renewal deadlines | Licensing team + CMDB |
| User form → PO → invoice → pay | Procurement life cycle |
| Cheapest vendor isn’t always chosen | Terms, maintenance, conditions matter |

## Common Mix-Ups

### CMDB is “only for the help desk”

IT, finance, and licensing all use it.

### Asset tag is just decoration

It is the key that links the physical device to the database record.

### Procurement = “buy the cheapest thing”

Purchasing weighs terms and maintenance, not price alone.

### Tracking stops after purchase

Assets stay in the CMDB for support, audits, warranty, and depreciation.

## Quick Review

| Topic | Remember |
| --- | --- |
| Goal | One central view of tech assets |
| Tag | Physical ID → database lookup |
| CMDB | Shared by IT, finance, licensing |
| Why | Support, spend reports, audits, depreciation, warranties, licenses |
| Buy path | Request → approve → PO → receive → invoice → pay |

---

## Continue Learning

- Previous Topic: [Ticketing Systems](ticketing-systems.md)
- Next Topic: [Document Types](document-types.md)
- Back to [Domain 4 — Operational Procedures](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
