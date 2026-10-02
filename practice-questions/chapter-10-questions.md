## Chapter 10: Backup Strategies, Safety Procedures, and Environmental Controls — Practice Questions

**Q1.** A company's disaster recovery policy must ensure data survives a fire at the primary office. Which configuration BEST satisfies the 3-2-1 backup rule?

A) Three copies of data on three different external HDDs, all stored in the server room
B) Two copies on internal RAID drives and one copy on tape stored in the same room
C) Three copies of the same data saved into three different folders on one NAS device
D) One production copy, one backup copy on a local NAS, and one backup copy on cloud storage in a different region

<details>
<summary>Answer</summary>

**Correct: D**

This gives 3 total copies (production, NAS, cloud), 2 different media types (local disk/NAS and cloud), and 1 copy offsite (cloud, different region) — satisfying all three parts of the 3-2-1 rule.

**Why the others are wrong:**
- All copies are the same media type and same physical location — a fire destroys everything, violating the offsite requirement.
- Only 2 real copies exist and neither is offsite; RAID protects against drive failure, not site disasters.
- Same device and same media type in the same location — one hardware failure or fire destroys all three 'copies'.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An administrator performs a full backup every Sunday and needs the fewest backup sets possible to restore data after a Wednesday failure. Which backup type should run Monday through Saturday?

A) Incremental
B) Snapshot only
C) Mirror
D) Differential

<details>
<summary>Answer</summary>

**Correct: D**

Differential backups only require the last full backup plus the single most recent differential to restore — exactly two sets, minimizing restore complexity.

**Why the others are wrong:**
- Incremental restore requires the full backup plus every incremental since, meaning more sets to apply as the week progresses.
- Snapshots are point-in-time images typically used for VMs, not the standard full/incremental/differential comparison tested here.
- 'Mirror' is not one of the three core backup types tested on 220-1202 (full, incremental, differential).

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** Which statement BEST describes the trade-off between incremental and differential backups?

A) Incremental backups take longer to restore but differential backups take longer to run and use more storage over the backup cycle
B) Incremental and differential backups have identical restore times and storage requirements
C) Differential backups can only be performed on tape media
D) Incremental backups always require more storage than a full backup

<details>
<summary>Answer</summary>

**Correct: A**

Incremental backups are small and fast to create but restore requires applying the full backup plus every incremental in sequence, increasing restore time. Differentials grow larger each day until the next full backup, taking longer to run, but restore only needs the full plus the latest differential — faster restore.

**Why the others are wrong:**
- They have distinctly different restore times and storage growth patterns — this is the core exam distinction.
- Differential backups work on any media type, not just tape.
- Incremental backups only capture changes since the last backup, so they use far less storage than a full backup.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A technician needs to open a desktop case but has no ESD strap or mat available. What should be done FIRST before touching internal components?

A) Begin work immediately since the case is unplugged from the wall
B) Put on rubber gloves to insulate hands from static
C) Touch an unpainted metal part of the case chassis to discharge static from the body
D) Place removed components on a carpeted surface

<details>
<summary>Answer</summary>

**Correct: C**

Touching bare, unpainted metal on the chassis safely discharges static built up on the technician's body to ground before handling sensitive components.

**Why the others are wrong:**
- Unplugging the PC removes power but does NOT remove static charge already stored on the technician's body — a classic exam trap.
- Rubber gloves are insulators, which trap static charge rather than dissipate it, increasing ESD risk.
- Carpet generates and holds static electricity, making ESD damage more likely, not less.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which practice is correct when servicing a power supply unit or CRT monitor?

A) Wear an ESD strap at all times for consistency across all repairs
B) Discharge stored capacitor charge using a proper tool, and do NOT wear an ESD strap while working inside these components
C) Keep the ESD strap connected to ground while working, then remove it only after finishing
D) Immediately touch internal capacitors with bare hands after unplugging the unit

<details>
<summary>Answer</summary>

**Correct: B**

PSUs and CRTs can retain lethal high-voltage charge in capacitors even when unplugged. An ESD strap creates a direct path for that current through the technician's body, so it must be removed, and capacitors should be discharged with an insulated, purpose-built tool before servicing.

**Why the others are wrong:**
- Wearing an ESD strap on high-voltage components creates an electrocution hazard rather than protecting equipment.
- Keeping the strap connected during high-voltage work is the exact scenario that causes serious injury.
- Bare-hand contact with charged capacitors can deliver a dangerous or fatal shock even after the unit is unplugged.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A technician wants to plug a UPS, a second monitor, and a space heater into a power strip that already has two desktop computers connected. What is the PRIMARY safety concern?

A) Increased risk of ESD damage to the connected devices
B) Radio frequency interference affecting the monitors
C) Circuit overload creating a potential fire hazard
D) Voltage drop causing intermittent blue screens

<details>
<summary>Answer</summary>

**Correct: C**

Adding multiple high-draw devices, especially a space heater, to a single power strip/circuit can exceed the circuit's amperage rating, causing overheating and fire risk.

**Why the others are wrong:**
- Power strip loading has no relationship to electrostatic discharge risk.
- RFI is not the primary hazard of circuit loading; it's a separate, unrelated concern.
- Voltage drop from overloading could theoretically cause instability, but the safety-critical concern tested here is fire risk from overload.

</details>

---

**Q7.** What is the correct technique for lifting heavy server equipment to avoid personal injury?

A) Bend at the waist and keep the legs straight while lifting with the back
B) Twist the torso while lifting to distribute the weight evenly
C) Lift quickly in one motion to minimize time spent under load
D) Bend at the knees, keep the back straight, and lift using the legs

<details>
<summary>Answer</summary>

**Correct: D**

Bending the knees and keeping the back straight transfers lifting force to the stronger leg muscles, reducing risk of back injury.

**Why the others are wrong:**
- Bending at the waist and lifting with the back is the exact technique that causes back injuries.
- Twisting while under load significantly increases the risk of spinal injury.
- Lifting quickly increases strain and injury risk rather than reducing it; a controlled, steady lift is correct.

</details>

---

**Q8.** Which statement about environmental humidity control in a server room is correct for exam purposes?

A) Relative humidity should be maintained in a moderate range, roughly 40-60%, to avoid both ESD and condensation/corrosion
B) Humidity should be kept as close to 0% as possible to eliminate all moisture risk
C) Humidity should be maintained at 90% or higher to prevent static buildup
D) Humidity control is unnecessary as long as ESD mats are used on all workbenches

<details>
<summary>Answer</summary>

**Correct: A**

A moderate relative humidity range (roughly 40-60%) balances two risks: humidity too low increases static electricity/ESD risk, while humidity too high causes condensation and corrosion on components.

**Why the others are wrong:**
- Extremely low humidity actually increases static buildup, raising ESD risk rather than eliminating it.
- Very high humidity causes condensation and corrosion damage to hardware.
- ESD mats address localized static discharge but do not address condensation, corrosion, or overall environmental risk in the room.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

