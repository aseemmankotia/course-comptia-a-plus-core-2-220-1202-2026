## Chapter 11: Incident Response, Regulated Data, Licensing, and Scripting Risks — Practice Questions

**Q1.** A technician discovers what appears to be illegal content on a customer's computer during a repair. What should the technician do FIRST?

A) Delete the illegal content immediately
B) Continue the repair and say nothing
C) Confront the customer directly about the content
D) Preserve the device without further use and report through proper channels

<details>
<summary>Answer</summary>

**Correct: D**

First response requires preserving the device/data and reporting through the established chain of command (supervisor, legal, or designated authority) — not personal investigation.

**Why the others are wrong:**
- Deleting evidence is illegal and destroys the chain of custody
- Failing to report violates policy and possibly the law
- Confronting the customer is unprofessional and outside the technician's authority

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** Which piece of information is REQUIRED on a chain-of-custody form when evidence is transferred from a technician to a forensics investigator?

A) List of antivirus software installed on the device
B) Date, time, and signatures of who released and received the evidence
C) List of all applications installed on the device
D) Serial number of the technician's employee badge only

<details>
<summary>Answer</summary>

**Correct: B**

Chain of custody must show an unbroken, timestamped, signed trail of every person who possessed the evidence to prove it wasn't tampered with.

**Why the others are wrong:**
- AV software list is irrelevant to custody tracking
- Installed application list doesn't establish possession or integrity
- A badge number alone doesn't document the transfer event

</details>

---

**Q3.** A US-based company processes payment card transactions for customers located in the European Union. Which regulation requires the company to protect the personal data of those EU customers regardless of where the company is physically located?

A) PCI-DSS
B) HIPAA
C) FERPA
D) GDPR

<details>
<summary>Answer</summary>

**Correct: D**

GDPR has extraterritorial reach — it protects personal data of EU residents no matter where the processing company is based.

**Why the others are wrong:**
- PCI-DSS is a payment card data security standard, not a general personal-data privacy law
- HIPAA only governs protected health information within the US
- FERPA only governs US student education records

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** An email attachment named 'invoice.vbs' arrives unexpectedly. Which statement describes the GREATEST security concern with this file?

A) VBScript is fully deprecated and cannot run on any modern Windows system
B) .vbs files only run on Linux, so this poses low risk on Windows
C) .vbs files require compilation before execution, giving time for detection
D) VBScript files can execute automatically via Windows Script Host without the user seeing the code first

<details>
<summary>Answer</summary>

**Correct: D**

VBScript is interpreted and executed silently by wscript.exe/cscript.exe with no visible code review, making it a classic phishing/malware delivery vector.

**Why the others are wrong:**
- Microsoft is deprecating VBScript but many systems still support it as of 2026, especially without the latest updates
- .vbs is a Windows Script Host format, not native to Linux
- .vbs is interpreted, not compiled — it runs immediately with no compile step

</details>

---

**Q5.** A patient's medical record includes their name, diagnosis, and treatment history. Under which data category does this record fall?

A) PII
B) PHI
C) PCI
D) GDPR

<details>
<summary>Answer</summary>

**Correct: B**

Health-specific identifiable information (diagnosis, treatment tied to identity) is classified as PHI and is protected under HIPAA.

**Why the others are wrong:**
- PII is the broader category; PHI is the more specific, correct classification for medical data
- PCI applies only to payment card data
- GDPR is a regulation/law, not a data category name

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which remote access technology encrypts traffic by default and is commonly used to run command-line administration on Linux servers over TCP port 22?

A) RDP
B) SSH
C) VNC
D) Telnet

<details>
<summary>Answer</summary>

**Correct: B**

SSH provides encrypted command-line remote access by default on port 22, standard for Linux administration.

**Why the others are wrong:**
- RDP uses port 3389 and provides GUI access, primarily for Windows
- VNC (port 5900) is often unencrypted by default
- Telnet (port 23) transmits data in plaintext

</details>

---

**Q7.** Which licensing model allows an organization to inspect, modify, and redistribute a program's source code, provided redistributed modifications remain under the same license terms?

A) Enterprise license agreement
B) Personal use license
C) Open source (copyleft) license
D) DRM-protected license

<details>
<summary>Answer</summary>

**Correct: C**

Copyleft open source licenses (e.g., GPL) grant source code access and modification rights with the requirement that derivative works remain under the same license.

**Why the others are wrong:**
- Enterprise/volume licenses are typically proprietary and don't grant source code rights
- Personal licenses restrict use to a single user/device with no source access
- DRM technically restricts copying and access — the opposite of open modification

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** While repairing a customer's laptop, a technician notices personal photos on the desktop unrelated to the reported issue. What is the BEST course of action?

A) Open the photos to confirm they aren't malware
B) Delete the photos to free up disk space
C) Copy the photos to a USB drive in case they are needed as evidence later
D) Avoid accessing or commenting on personal files and only address the reported issue

<details>
<summary>Answer</summary>

**Correct: D**

Professionalism and customer privacy require technicians to stay within the scope of the reported issue and not access unrelated personal data.

**Why the others are wrong:**
- Opening unrelated personal files is a privacy violation outside the scope of the task
- Deleting customer data without authorization is unprofessional and potentially damaging
- Copying personal data without cause or authorization is a serious privacy/ethics violation

</details>

---

