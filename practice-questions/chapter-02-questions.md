## Chapter 2: Windows Command-Line Utilities for Diagnostics and Networking — Practice Questions

**Q1.** A user reports their laptop cannot reach any network resources after being moved to a new office with a different DHCP scope. Ipconfig shows an APIPA address (169.254.x.x). Which sequence of commands BEST resolves this?

A) ipconfig /release then ipconfig /renew
B) ipconfig /flushdns then ipconfig /all
C) netstat -an then ping 127.0.0.1
D) nslookup then ipconfig /displaydns

<details>
<summary>Answer</summary>

**Correct: A**

An APIPA address (169.254.x.x) means the client failed to reach a DHCP server. Releasing the old lease and forcing a new DHCP request (renew) is the correct fix so the client can obtain a valid address from the new scope.

**Why the others are wrong:**
- Flushing DNS clears the resolver cache but does nothing for a failed DHCP lease.
- netstat shows active connections/ports, not IP configuration issues, and pinging loopback only confirms the local stack works.
- nslookup queries DNS records; displaydns shows cached DNS entries — neither addresses the missing DHCP lease.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An administrator pushes a new Group Policy Object restricting USB storage devices. A technician on a domain-joined workstation needs the policy applied immediately without waiting for the next refresh cycle. Which command should be run?

A) gpresult /r
B) gpupdate /force
C) net use * /delete
D) sfc /scannow

<details>
<summary>Answer</summary>

**Correct: B**

gpupdate /force re-applies all Group Policy settings immediately, including ones that haven't changed, ensuring the new USB restriction takes effect right away.

**Why the others are wrong:**
- gpresult /r only displays which policies have been applied (Resultant Set of Policy); it does not push new settings.
- net use * /delete disconnects all mapped network drives and has nothing to do with Group Policy.
- sfc /scannow checks and repairs protected system files, unrelated to policy application.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A technician wants to confirm which Group Policy settings are currently applied to a user and computer, including which GPOs won and which were filtered out. Which command should be used?

A) gpupdate /force
B) netstat -b
C) gpresult /r
D) nslookup -type=all

<details>
<summary>Answer</summary>

**Correct: C**

gpresult /r generates a summary Resultant Set of Policy (RSoP) report showing applied GPOs for both computer and user, plus denied/filtered policies — exactly what's needed to verify policy application.

**Why the others are wrong:**
- gpupdate /force reapplies policy but does not report which ones are currently in effect.
- netstat -b lists executables associated with each connection, unrelated to Group Policy.
- nslookup -type=all queries DNS record types, not policy state.

</details>

---

**Q4.** A user's PC exhibits missing DLL errors and random application crashes, but Disk Management shows the drive is healthy with no bad sectors. Which command should be run FIRST?

A) sfc /scannow
B) chkdsk /f /r
C) robocopy C:\ D:\ /mir
D) gpupdate /force

<details>
<summary>Answer</summary>

**Correct: A**

Missing DLLs and app crashes with a healthy disk point to corrupted or missing protected system files. sfc /scannow scans and repairs Windows system files using the component store (WinSxS).

**Why the others are wrong:**
- chkdsk /f /r targets file system and physical disk sector errors, not corrupted system files — and the disk is already confirmed healthy.
- robocopy /mir mirrors a directory tree; it can destructively delete files at the destination and does not fix system files.
- gpupdate /force reapplies Group Policy, unrelated to file corruption.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A workstation is experiencing frequent 'Delayed Write Failed' errors and Event Viewer shows disk read errors. sfc /scannow completed with no integrity violations. Which command should be run next to check for and repair bad sectors?

A) sfc /scannow /offbootdir
B) netstat -an
C) chkdsk /f /r
D) net use Z: /delete

<details>
<summary>Answer</summary>

**Correct: C**

Disk read errors and delayed write failures indicate physical/logical disk problems. chkdsk /f fixes file system errors and /r locates bad sectors and recovers readable data, which is the appropriate escalation after sfc found no system file corruption.

**Why the others are wrong:**
- Re-running sfc with an offline boot directory switch doesn't address sector-level disk errors.
- netstat displays network connections, irrelevant to disk hardware issues.
- net use /delete just removes a mapped drive letter and has no diagnostic value here.

</details>

---

**Q6.** A technician needs to map network share \\FS01\Projects to drive letter P: from the command line for a user. Which command accomplishes this?

A) net use P: \\FS01\Projects
B) net use /delete P:
C) robocopy \\FS01\Projects P: /mir
D) netstat -r \\FS01\Projects P:

<details>
<summary>Answer</summary>

**Correct: A**

net use <drive letter> <UNC path> is the correct syntax to map a network share to a local drive letter.

**Why the others are wrong:**
- net use /delete P: disconnects a mapped drive rather than creating one.
- robocopy copies file contents between paths; it does not create a persistent mapped drive.
- netstat -r displays the routing table and has invalid syntax for this purpose.

</details>

---

**Q7.** A technician needs to copy an entire folder structure to a backup server, keeping the destination as an exact mirror (including deleting files at the destination that no longer exist at the source), and must be able to resume automatically if the connection drops. Which command and switch combination is BEST?

A) xcopy /s /e
B) robocopy source destination /mir /z
C) copy source destination /y
D) net use \\server\share /persistent:yes

<details>
<summary>Answer</summary>

**Correct: B**

robocopy /mir mirrors the source and destination (deleting orphaned files at destination), and /z enables restartable mode so interrupted copies resume rather than starting over — robocopy is specifically designed for resilient, large-scale copies.

**Why the others are wrong:**
- xcopy /s /e copies subdirectories including empty ones but does not mirror (won't delete extra destination files) and lacks restart capability.
- copy /y overwrites files without prompting but has no folder recursion, mirroring, or resiliency features.
- net use with /persistent:yes maps a network drive persistently; it does not copy files at all.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which statement BEST describes the difference between Command Prompt and PowerShell on Windows?

A) PowerShell can run legacy cmd commands and batch scripts, and adds cmdlets with object-based output and pipeline scripting; Command Prompt only runs traditional cmd commands and batch files.
B) Command Prompt supports cmdlets and object pipelines; PowerShell only supports plain text output.
C) Command Prompt and PowerShell are functionally identical, differing only in window color.
D) PowerShell requires elevation for every command, while Command Prompt never requires elevation.

<details>
<summary>Answer</summary>

**Correct: A**

PowerShell is a superset in practical terms — it can execute most cmd-style commands/batch files and adds cmdlets (Verb-Noun syntax) that output structured .NET objects, enabling powerful pipelining and scripting beyond what cmd offers.

**Why the others are wrong:**
- This reverses the actual relationship — cmdlets and object pipelines are PowerShell features, not Command Prompt features.
- The two shells differ significantly in scripting capability, command set, and output handling, not just appearance.
- Elevation requirements depend on the specific command/task (e.g., modifying system settings), not on which shell is used.

</details>

---

