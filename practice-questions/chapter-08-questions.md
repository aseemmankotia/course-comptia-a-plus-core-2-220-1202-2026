## Chapter 8: Malware Removal Best Practices and Mobile OS Troubleshooting — Practice Questions

**Q1.** A technician confirms a workstation is infected with ransomware that is actively encrypting files on a mapped network share. According to CompTIA's malware removal best practices, what should the technician do IMMEDIATELY after verifying the symptoms?

A) Disconnect the system from the network to quarantine it
B) Disable System Restore on the infected machine
C) Run a full anti-malware scan with updated definitions
D) Educate the end user on how the infection occurred

<details>
<summary>Answer</summary>

**Correct: A**

Step 2 of the process is quarantine — disconnect the infected system from the network (unplug Ethernet/disable Wi-Fi) to stop the ransomware from spreading to shares and other hosts before any remediation begins.

**Why the others are wrong:**
- Disabling System Restore is Step 3, which happens only after the system is quarantined, otherwise the malware could keep spreading during the delay
- Scanning (remediation) is Step 4 and must not occur before quarantine, or the malware can keep propagating over the network during the scan
- User education is the final step (Step 7), performed after the system is fully cleaned

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** Which of the following correctly lists the CompTIA seven-step malware removal process in order?

A) Quarantine, Investigate, Disable System Restore, Remediate, Schedule scans/updates, Re-enable System Restore, Educate user
B) Investigate and verify, Disable System Restore, Quarantine, Remediate, Educate user, Schedule scans/updates, Re-enable System Restore
C) Investigate and verify, Quarantine, Disable System Restore, Remediate, Schedule scans/updates, Re-enable System Restore, Educate user
D) Investigate and verify, Quarantine, Remediate, Disable System Restore, Re-enable System Restore, Schedule scans/updates, Educate user

<details>
<summary>Answer</summary>

**Correct: C**

The official order is: 1) Investigate and verify malware symptoms, 2) Quarantine infected systems, 3) Disable System Restore, 4) Remediate infected systems, 5) Schedule scans and run updates, 6) Enable System Restore and create a restore point, 7) Educate the end user.

**Why the others are wrong:**
- This starts with Quarantine before Investigate, which is reversed — you must verify the infection first
- This disables System Restore before quarantining the system, which is out of sequence
- This puts Remediate before Disable System Restore and Educate before Schedule scans, both out of the correct sequence

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A technician has finished remediating a malware infection, updated anti-malware definitions, and run a clean full scan. What should be done NEXT, before considering the job complete?

A) Immediately re-enable System Restore and create a new restore point
B) Reboot into Safe Mode and run a second scan before doing anything else
C) Format the drive and reinstall the operating system as a precaution
D) Schedule scans and run updates, then re-enable System Restore and create a restore point

<details>
<summary>Answer</summary>

**Correct: D**

Step 5 (schedule scans and run updates) comes right after remediation and before Step 6 (re-enable System Restore and create a restore point) — you don't want to snapshot restore points until the ongoing protection schedule is configured and the system is confirmed clean.

**Why the others are wrong:**
- Re-enabling System Restore before scheduling scans/updates skips Step 5, which is out of order per the seven-step process
- A second Safe Mode scan isn't part of the defined seven-step sequence at this point and isn't required if remediation already succeeded
- Reformatting isn't part of the seven-step process and is an overreaction once a clean scan has already been confirmed

</details>

---

**Q4.** Why must System Restore be disabled during Step 3 of the malware removal process, before remediation begins?

A) System Restore consumes too much CPU and slows down anti-malware scans
B) System Restore automatically deletes infected files, interfering with forensic evidence
C) Anti-malware software cannot run while System Restore is active
D) Malware can be backed up into existing restore points and reintroduced later if the system is rolled back

<details>
<summary>Answer</summary>

**Correct: D**

Windows System Restore snapshots system files, and an infected restore point can reinfect the system if a user or process ever rolls back to it. Disabling it before remediation and clearing existing points prevents this reinfection vector.

**Why the others are wrong:**
- CPU usage isn't the reason System Restore is disabled during malware removal — it's about reinfection risk
- System Restore doesn't delete files or interfere with evidence collection; it snapshots system state
- Anti-malware tools run fine with System Restore enabled — this isn't a technical conflict, it's a reinfection prevention step

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A user reports their Android phone's battery drains from 100% to 20% within two hours despite minimal use, and the device feels warm even when idle. Which troubleshooting step should the technician perform FIRST?

A) Replace the battery immediately
B) Check battery usage statistics in settings to identify which app is consuming the most power
C) Perform a factory reset on the device
D) Disable the mobile data connection permanently

<details>
<summary>Answer</summary>

**Correct: B**

Checking the battery usage screen identifies the specific app or process causing excessive drain (e.g., a rogue background app or malware), which is the least invasive and most diagnostic first step before taking corrective action.

**Why the others are wrong:**
- Replacing the battery is costly and premature without first diagnosing whether a software issue is the cause
- A factory reset is a valid remediation but should not be the first troubleshooting step — it's disruptive and should follow diagnosis
- Permanently disabling mobile data doesn't fix the underlying drain and removes needed functionality

</details>

---

**Q6.** A company laptop is confirmed infected with malware. The technician disconnects it from the network and disables System Restore. Which action correctly represents Step 4, Remediation?

A) Educate the user on safe browsing habits
B) Create a system restore point to preserve the current state
C) Update anti-malware signatures and run a full system scan to remove the malware
D) Configure Windows Update to run automatically going forward

<details>
<summary>Answer</summary>

**Correct: C**

Remediation (Step 4) means updating the anti-malware software's definitions and running a full scan to identify and remove the malicious software from the system.

**Why the others are wrong:**
- User education is Step 7, done at the end of the process, not during remediation
- Creating a restore point happens in Step 6, after remediation is confirmed successful — not during it
- Scheduling automatic updates is part of Step 5, which follows remediation

</details>

---

**Q7.** A user's smartphone shows an unusually high amount of cellular data usage even though the user reports not streaming video or downloading large files. What is the MOST likely cause the technician should investigate?

A) The phone's screen brightness is set too high
B) The phone's touchscreen digitizer is malfunctioning
C) A malicious or misconfigured app is running in the background and transmitting data without user awareness
D) The battery is nearing end of life

<details>
<summary>Answer</summary>

**Correct: C**

Unauthorized/unexpected data usage is a classic symptom of malware or a misbehaving app performing background data transmission (e.g., adware, spyware, or a sync loop), and the technician should review app permissions and data usage per app.

**Why the others are wrong:**
- Screen brightness affects battery life, not cellular data consumption
- A malfunctioning touchscreen would cause input problems, not elevated data usage
- Battery age affects charge capacity, not data transmission over the cellular network

</details>

---

**Q8.** What is the purpose of Step 7, 'Educate the end user,' in the malware removal process?

A) To document the incident for compliance auditors only
B) To train the user how to disable System Restore themselves
C) To have the user sign a waiver releasing IT from liability
D) To inform the user of safe practices (e.g., avoiding suspicious links/attachments) to prevent future infections

<details>
<summary>Answer</summary>

**Correct: D**

Educating the end user closes the loop by teaching prevention — safe browsing, recognizing phishing, avoiding untrusted downloads — reducing the likelihood of reinfection.

**Why the others are wrong:**
- While documentation is good practice generally, it is not the defined purpose of Step 7 in the seven-step process
- Teaching users to disable System Restore is a technician-level task, not an end-user education topic, and isn't the goal here
- Liability waivers are not part of the CompTIA-defined remediation process

</details>

---

