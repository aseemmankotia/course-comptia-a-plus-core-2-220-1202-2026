## Chapter 9: Documentation, Ticketing, and Change Management — Practice Questions

**Q1.** A technician needs to update firmware on a production network switch during business hours. What should the technician do FIRST, before touching the device?

A) Submit a change request and get it approved through the change management process
B) Perform the update immediately since firmware updates are low risk
C) Notify the help desk after the update is complete
D) Create a backup of the switch configuration and proceed without approval

<details>
<summary>Answer</summary>

**Correct: A**

Any change to production systems, even one considered low risk, must go through the formal change management process for approval before implementation.

**Why the others are wrong:**
- No change is 'low risk enough' to skip approval — that determination is part of the risk analysis step, not the technician's judgment call
- Notifying after the fact violates the requirement that changes be approved BEFORE implementation
- Backing up config is good practice but does not replace the required approval step

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** During a change management review, a technician's request is rejected because it lacks a specific required element. The board states: 'If this change causes an outage, how do you undo it?' Which element was missing from the request?

A) Rollback plan
B) Scope of the change
C) Purpose of the change
D) Sandbox testing results

<details>
<summary>Answer</summary>

**Correct: A**

The rollback plan documents exactly how to reverse a change if it causes unintended issues — this is what the board's question is asking for.

**Why the others are wrong:**
- Scope defines what systems/users are affected, not how to undo the change
- Purpose explains why the change is needed, not how to reverse it
- Sandbox testing validates the change works, but doesn't itself address reversal

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A user calls the help desk reporting that their laptop will not connect to Wi-Fi. The technician logs the call. Which combination of fields is REQUIRED in a properly documented support ticket?

A) Issue description, category, priority, and resolution
B) User's home address and personal email
C) Only the issue description; other fields are optional
D) The technician's personal notes and lunch schedule

<details>
<summary>Answer</summary>

**Correct: A**

A complete ticket must capture the issue description, category (for routing/reporting), priority (for SLA/escalation), and resolution (for knowledge base and audit purposes).

**Why the others are wrong:**
- Personal address/email are not standard ticketing fields and are a privacy concern
- Category and priority are required for proper routing and SLA tracking, not optional
- Irrelevant personal information has no place in ticket documentation

</details>

---

**Q4.** A new hire on the help desk needs step-by-step instructions for resetting a user's password in Active Directory, including exact screens and click paths. Which document should they consult?

A) A knowledge base article / standard operating procedure (SOP)
B) A change management request form
C) An asset inventory list
D) A EULA

<details>
<summary>Answer</summary>

**Correct: A**

SOPs and KB articles provide standardized, repeatable step-by-step instructions for routine tasks like password resets.

**Why the others are wrong:**
- A change request form is used to propose and approve changes, not to document routine procedures
- Asset inventory tracks hardware/software ownership, not procedural steps
- A EULA is a software licensing agreement, unrelated to task instructions

</details>

---

**Q5.** An IT department is auditing laptops nearing the end of their support life. Which two pieces of information from the asset management system are MOST relevant to determine if a device should be replaced?

A) The employee's job title and desk location
B) The device's Wi-Fi SSID and password
C) The color and physical dimensions of the laptop
D) Purchase date and warranty expiration date

<details>
<summary>Answer</summary>

**Correct: D**

Purchase date and warranty expiration determine the device's age and whether it is still covered for repairs, directly informing replacement decisions in the procurement lifecycle.

**Why the others are wrong:**
- Job title/location are useful for asset assignment, not for lifecycle/replacement decisions
- Network credentials are unrelated to asset lifecycle tracking
- Physical attributes like color have no bearing on replacement timing

</details>

---

**Q6.** Place the change management process in the CORRECT order as tested on the exam.

A) Purpose of change, scope, risk analysis, sandbox testing, approval, implementation, rollback plan (if needed)
B) Implementation, approval, purpose, rollback plan
C) Rollback plan, sandbox testing, purpose, scope
D) Approval, purpose, scope, implementation

<details>
<summary>Answer</summary>

**Correct: A**

The standard change management flow starts by defining WHY (purpose) and WHAT (scope), assesses risk, validates in a sandbox, gets formal approval, then implements — with the rollback plan documented and ready before/during implementation in case it's needed.

**Why the others are wrong:**
- Implementation before approval and purpose skips required upfront steps entirely
- Starting with rollback plan before defining purpose/scope is out of sequence
- Approval must come after risk analysis and testing, not first

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A company receives a shipment of 50 new monitors. Per proper asset management procedure, what should be done immediately upon receipt, before the monitors are deployed to users?

A) Assign asset tags and record each unit in the inventory list
B) Deploy them to users first, then track them later if needed
C) Discard the original packaging and serial numbers
D) Wait until the warranty expires to log them

<details>
<summary>Answer</summary>

**Correct: A**

Asset tagging and inventory entry must occur at intake, establishing traceability (owner, location, warranty) for the entire lifecycle of the device.

**Why the others are wrong:**
- Deploying before tagging creates untracked assets, violating inventory procedure
- Serial numbers are needed for warranty claims and must be preserved, not discarded
- Logging must happen at procurement/receipt, not near warranty expiration

</details>

---

**Q8.** Which statement correctly differentiates an open source software license from a commercial EULA?

A) Open source licenses always prohibit modification of the source code, while commercial EULAs allow it
B) Open source licenses typically permit viewing/modifying source code and free redistribution, while commercial EULAs restrict use to licensed terms and usually prohibit source code access
C) A EULA only applies to open source software
D) There is no legal difference between the two license types

<details>
<summary>Answer</summary>

**Correct: B**

Open source licenses (e.g., GPL, MIT) grant rights to view, modify, and redistribute source code, while commercial EULAs govern use of proprietary software and generally restrict copying, modification, and source access.

**Why the others are wrong:**
- This reverses the actual relationship — open source generally allows modification, not prohibits it
- EULAs are associated with commercial/proprietary software, not open source
- The two license types have significantly different legal terms regarding modification and redistribution

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

