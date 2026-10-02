## Chapter 5: Malware Types, Detection Tools, and Social Engineering — Practice Questions

**Q1.** A user reports that all their files have been renamed with a .locked extension and a full-screen message demands Bitcoin payment within 72 hours to restore access. Which type of malware is this?

A) Rootkit
B) Ransomware
C) Worm
D) Spyware

<details>
<summary>Answer</summary>

**Correct: B**

Ransomware encrypts victim files and demands payment for the decryption key — the ransom note and file encryption are the defining, immediately visible symptoms.

**Why the others are wrong:**
- Rootkit: hides deep in the OS/kernel and avoids detection; it does not encrypt files or demand payment.
- Worm: self-replicates across networks to spread, but doesn't inherently encrypt files or demand ransom.
- Spyware: silently collects user data/activity; it does not lock files or display ransom demands.

</details>

---

**Q2.** A network administrator notices a workstation is being remotely controlled, silently sending spam emails without the user's knowledge, and repeatedly contacting an unfamiliar external IP address. This workstation is best described as:

A) A zombie
B) A zero-day host
C) A rogue antivirus system
D) A tailgating victim

<details>
<summary>Answer</summary>

**Correct: A**

A 'zombie' is an individual infected machine under remote attacker control, typically part of a larger botnet communicating with a C2 (command-and-control) server — matching the described symptoms exactly.

**Why the others are wrong:**
- Zero-day host: describes a system vulnerable to an unpatched exploit, not a term for a remotely controlled infected machine.
- Rogue antivirus: refers to fake AV/scareware pop-ups tricking users into payment, unrelated to C2 communication.
- Tailgating victim: a physical security social engineering term, unrelated to malware infection.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An employee receives an email that appears to come from the company's CEO, addressed specifically to the CFO by name, referencing a confidential upcoming merger, and requesting an urgent wire transfer. Which type of attack is this?

A) Phishing
B) Spear phishing
C) Vishing
D) Whaling

<details>
<summary>Answer</summary>

**Correct: D**

Whaling is spear phishing specifically targeted at high-value/executive individuals (like a CFO), using personalized, business-relevant details to increase credibility.

**Why the others are wrong:**
- Phishing: describes generic, mass-distributed emails, not a personalized attack against a specific executive.
- Spear phishing: correctly describes targeted attacks in general, but this scenario targets an executive specifically, making 'whaling' the more precise answer.
- Vishing: refers to voice/phone-based social engineering, but this attack was delivered via email.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which built-in Windows tool provides real-time malware protection and is included at no additional cost on supported Windows 10 and 11 editions?

A) Microsoft Defender Antivirus (Windows Defender)
B) Malwarebytes
C) Norton 360
D) McAfee LiveSafe

<details>
<summary>Answer</summary>

**Correct: A**

Microsoft Defender Antivirus ships built into Windows 10/11 and provides real-time protection, cloud-delivered protection, and scanning at no extra charge.

**Why the others are wrong:**
- Malwarebytes: a third-party tool, not built into Windows.
- Norton 360: a paid third-party security suite requiring separate licensing.
- McAfee LiveSafe: a paid third-party product, sometimes preinstalled by OEMs but not a native Windows component.

</details>

---

**Q5.** A technician suspects a system is infected with a rootkit that hides from normal OS-level antivirus scans. Which approach is BEST suited to detect it?

A) Run Microsoft Defender Offline (boot-time scan)
B) Run a Quick Scan from within the running Windows session
C) Review running processes in Task Manager
D) Check for pending Windows Updates

<details>
<summary>Answer</summary>

**Correct: A**

Rootkits hide from tools running under the infected OS. Microsoft Defender Offline reboots the machine into a clean pre-boot environment, scanning before the rootkit can conceal itself.

**Why the others are wrong:**
- Quick Scan while OS is running: the rootkit can actively hide from scans made from within the compromised OS.
- Task Manager: rootkits are specifically designed to hide their processes from tools like Task Manager.
- Checking Windows Updates: unrelated to detecting active rootkit infections.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which PowerShell cmdlet initiates a full system scan using Microsoft Defender Antivirus?

A) Start-MpScan -ScanType QuickScan
B) Start-MpScan -ScanType FullScan
C) Update-MpSignature
D) Get-MpThreat

<details>
<summary>Answer</summary>

**Correct: B**

The -ScanType FullScan parameter tells Start-MpScan to scan the entire system, including all files and running processes.

**Why the others are wrong:**
- QuickScan: scans only common malware locations, not a full system scan.
- Update-MpSignature: updates virus definitions, doesn't perform a scan.
- Get-MpThreat: retrieves detected threat history, doesn't initiate a scan.

</details>

---

**Q7.** An employee walks closely behind a coworker through a badge-secured door without swiping their own access card. This is an example of:

A) Shoulder surfing
B) Tailgating
C) Dumpster diving
D) Vishing

<details>
<summary>Answer</summary>

**Correct: B**

Tailgating is gaining unauthorized physical access by following an authorized person through a secured entry point.

**Why the others are wrong:**
- Shoulder surfing: observing someone's screen or keystrokes to steal information, not a physical entry technique.
- Dumpster diving: searching discarded trash for sensitive data, unrelated to physical access.
- Vishing: phone-based social engineering, unrelated to physical building access.

</details>

---

**Q8.** Which term describes a vulnerability that attackers exploit before the software vendor is aware of it or has released a patch?

A) Non-compliant system
B) Rootkit
C) Zero-day
D) Botnet

<details>
<summary>Answer</summary>

**Correct: C**

A zero-day vulnerability is unknown to the vendor and has 'zero days' of available patch time before it's exploited.

**Why the others are wrong:**
- Non-compliant system: a device violating organizational security policy (e.g., missing patches), a different concept.
- Rootkit: a type of malware focused on hiding its presence, not a vulnerability classification.
- Botnet: a network of compromised (zombie) devices controlled by an attacker, unrelated to patch timing.

</details>

---

