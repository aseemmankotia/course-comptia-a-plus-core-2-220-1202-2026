# Answer Key — Practice Test 2

**Q1. Correct: B**

/MIR mirrors a directory tree, copying new/changed files and deleting files at the destination that no longer exist at the source, keeping both locations identical.

---

**Q2. Correct: D**

gpresult /r displays the Resultant Set of Policy (RSoP) summary, showing which GPOs and settings are currently applied to the logged-on user and the computer.

---

**Q3. Correct: A**

Disk Management allows a volume to be mounted to an empty NTFS folder (a mount point) instead of a drive letter, providing access to the new volume without requiring an available letter.

---

**Q4. Correct: A**

chmod 700 sets permissions to rwx (7) for the owner and 0 (no access) for both group and others, matching the requirement exactly.

---

**Q5. Correct: B**

Task Manager's Details tab includes a PID column, letting the technician match the suspicious PID to its process image name and take action such as ending the task.

---

**Q6. Correct: B**

exFAT supports files larger than 4GB and is natively readable and writable by both Windows and macOS without additional drivers, making it ideal for cross-platform removable media.

---

**Q7. Correct: C**

/MIR mirrors the source directory tree to the destination, copying new/changed files and purging files in the destination that no longer exist in the source, keeping both locations identical.

---

**Q8. Correct: D**

gpresult /r displays the Resultant Set of Policy (RSoP) summary, showing which GPOs are applied to the computer and user without modifying anything.

---

**Q9. Correct: D**

Converting a basic disk to a dynamic disk in Disk Management preserves all existing data and removes the MBR four-partition limit, allowing additional volumes to be created on the same physical disk.

---

**Q10. Correct: B**

exFAT supports files larger than 4 GB and is natively readable and writable by both current Windows and macOS without additional drivers, making it ideal for cross-platform large-file transfer.

---

**Q11. Correct: B**

top provides a continuously updating, real-time view of running processes along with CPU and memory usage, functioning like Windows Task Manager's live process view.

---

**Q12. Correct: C**

Time Machine is macOS's built-in backup feature that automatically creates hourly, daily, and weekly snapshots, allowing users to browse and restore previous versions of files.

---

**Q13. Correct: D**

The /E switch copies all subdirectories, including empty ones, and /R:1 /W:1 overrides robocopy's default behavior of retrying a failed file 1,000,000 times with a 30-second wait between attempts, so failures are skipped quickly instead of causing long hangs.

---

**Q14. Correct: B**

When a file is moved within the same NTFS volume, Windows simply updates the file's directory pointer instead of copying the data, so the file RETAINS its original NTFS permissions. Only copying a file, or moving it across different volumes, causes it to inherit the destination folder's permissions.

---

**Q15. Correct: B**

CompTIA's best-practice malware removal order is: 1) Investigate and verify symptoms, 2) Quarantine infected systems, 3) Disable System Restore in Windows, 4) Remediate infected systems, 5) Schedule scans and run updates, 6) Enable System Restore and create a restore point, 7) Educate the end user. Disabling System Restore comes immediately after quarantine so infected files aren't preserved in a restore point.

---

**Q16. Correct: C**

TACACS+ separates authentication, authorization, and accounting (AAA) into distinct processes and encrypts the entire packet payload, allowing administrators to define granular, command-level authorization for network device access — exactly the requirement described.

---

**Q17. Correct: D**

EFS encryption is tied to the user's personal encryption certificate and private key, which are stored in the user's profile. Deleting and recreating the account generates a brand-new SID and certificate, so the new profile no longer has the key needed to decrypt the file — this is why exporting/backing up the EFS certificate (or configuring a Data Recovery Agent) BEFORE such changes is a critical best practice.

---

**Q18. Correct: D**

WPA3 replaces WPA2's four-way handshake (vulnerable to offline dictionary/brute-force attacks against captured handshake data) with SAE, a Diffie-Hellman-based key exchange that provides forward secrecy and resists offline password-guessing attacks even if traffic is captured.

---

**Q19. Correct: A**

Degaussing works by disrupting the magnetic fields on platters in traditional HDDs; SSDs store data in NAND flash memory cells with no magnetic media, so degaussing has no effect on an SSD's data and should never be relied upon for SSD sanitization.

---

**Q20. Correct: C**

For network access, NTFS permissions from multiple groups combine to the most permissive (Read + Modify = Modify), and share permissions combine to the most permissive (Full Control + Full Control = Full Control). Then the more restrictive of the two combined results wins, so the effective permission is Modify.

---

**Q21. Correct: D**

EFS (Encrypting File System) is an NTFS-only feature. When an EFS-encrypted file is copied to a non-NTFS volume such as FAT32, Windows decrypts the file during the copy, and it lands on the destination in plaintext — a well-known EFS limitation and exam trap.

---

**Q22. Correct: A**

The correct malware remediation sequence is: investigate/verify symptoms, quarantine infected systems, disable System Restore, remediate infected systems (update anti-malware and remove malware, using Safe Mode or a preinstallation environment if needed), schedule scans and run updates, enable System Restore and create a restore point, and educate the end user. Disabling System Restore prevents the malware from being restored later.

---

**Q23. Correct: B**

TACACS+ encrypts the entire authentication packet (not just the password) and separates authentication, authorization, and accounting (AAA) into three distinct services, making it the preferred protocol for administrative access control on network devices such as routers and switches.

---

**Q24. Correct: D**

Certified data-wiping software overwrites the drive's data (often multiple passes with patterns of 0s, 1s, and random data) while leaving the drive mechanically intact and reusable, meeting both the security and reusability requirements.

---

**Q25. Correct: D**

Whaling is a highly targeted phishing attack aimed specifically at high-value individuals such as executives (CEO, CFO), often impersonating another executive and using researched, believable details to pressure a rushed, high-value action like a wire transfer — exactly what's described.

---

**Q26. Correct: A**

NTFS permissions from multiple group memberships are cumulative (Modify + Read = Modify), but when a resource is accessed over the network, the effective permission is the MOST RESTRICTIVE of the combined NTFS permission and the share permission. Here, combined NTFS = Modify, but Share = Read, so the effective access is Read.

---

**Q27. Correct: D**

CompTIA's official malware removal order is: 1) Identify/investigate symptoms, 2) Quarantine infected systems, 3) Disable System Restore, 4) Remediate infected systems (update anti-malware and scan), 5) Schedule scans and run updates, 6) Enable System Restore and create a restore point, 7) Educate the end user. Disabling System Restore comes immediately after quarantine so the malware isn't preserved in restore points.

---

**Q28. Correct: C**

Safe Mode loads only essential drivers, preventing the faulty third-party driver from loading and causing another crash. From Safe Mode, Event Viewer and Device Manager can be used to identify and roll back or remove the problematic driver referenced in the BSOD.

---

**Q29. Correct: A**

A service depending on another service that is disabled will fail to start because its dependency chain is broken. Setting the dependency service to Automatic and starting it resolves the root cause, allowing the dependent service to start normally afterward.

---

**Q30. Correct: A**

Recurring temporary profile issues are commonly caused by a corrupted entry under HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList, where Windows creates a duplicate SID key with a .bak suffix during a failed profile load. Renaming/removing the corrupted key and correcting the State value resolves the root cause that a simple profile deletion won't fix.

---

**Q31. Correct: C**

Repeated update failures often indicate corruption in the Windows component store or system files. DISM repairs the component store from Windows Update sources, and SFC then repairs system files using that repaired store, resolving most persistent update failures without a full OS reinstall.

---

**Q32. Correct: A**

Ransomware encrypts a victim's files and demands payment (often cryptocurrency) for the decryption key, exactly matching the symptoms of renamed/encrypted files and a ransom note.

---

**Q33. Correct: A**

Once symptoms are investigated and malware presence is confirmed, the very next step in the CompTIA-defined order is to quarantine the infected system (disconnect from the network/isolate it) to prevent further spread or data exfiltration before any remediation begins.

---

**Q34. Correct: C**

After remediation (update and scan) removes the initial threat, best practice is to schedule future automatic scans and confirm OS/application patching is current, hardening the system before restore points are re-enabled — this prevents reintroducing the same vulnerability.

---

**Q35. Correct: C**

When a boot failure occurs immediately after a specific update was applied, WinRE's Advanced Startup Options includes an 'Uninstall Updates' feature that removes the problematic update without touching user data or reinstalling the OS — the least destructive and most targeted fix.

---

**Q36. Correct: C**

Corrupted or duplicate user profiles causing a 'temporary profile' error are fixed by examining ProfileList, which stores SID-keyed profile entries (including any '.bak' duplicate keys) — renaming/removing the corrupt SID key and correcting the RefCount/State values resolves the mismatch so the correct profile loads.

---

**Q37. Correct: D**

A backout (rollback) plan defines exactly how to restore the previous configuration if a change fails. Without one, the technician had no defined method to quickly revert the switch, which is why the outage extended instead of being resolved rapidly.

---

**Q38. Correct: A**

Incremental backups only capture changes since the last backup, so they must be layered on top of the most recent full backup and applied in the order they were created — Monday's changes first, then Tuesday's — to correctly rebuild the data state.

---

**Q39. Correct: B**

First-response procedure requires preserving evidence and chain of custody by not altering the device further, then escalating to a supervisor, legal, or law enforcement as appropriate — the technician should never independently investigate or act on the finding.

---

**Q40. Correct: A**

Names combined with diagnosis and treatment information constitute Protected Health Information (PHI), which is governed in the U.S. by HIPAA, the regulation specifically covering healthcare data privacy and security.

---

**Q41. Correct: C**

VBScript (.vbs) files run natively through the Windows Script Host (wscript.exe/cscript.exe) without needing to be compiled, and attackers commonly disguise them with names like invoice.pdf.vbs so Windows' hidden file extension setting shows only 'invoice.pdf' to the user, tricking them into execution.

---

**Q42. Correct: C**

Class C extinguishers are rated for electrical fires involving energized equipment; they use a non-conductive agent, making them safe to use without risk of electric shock.

---

**Q43. Correct: B**

Formal change management always begins with a documented change request that includes purpose, scope, risk assessment, and a backback/rollback plan submitted to the change advisory board for approval before any work is scheduled or performed.

---

**Q44. Correct: B**

VBScript (.vbs) files are executed natively by the Windows Script Host without requiring elevation or an external interpreter, allowing them to run automatically upon opening — a characteristic frequently exploited in phishing/malware email attachments.

---

**Q45. Correct: A**

First-responder procedure requires preserving the evidence in its original state (chain of custody) and escalating through proper channels — a supervisor and potentially law enforcement — rather than taking unilateral action; this protects the technician legally and preserves evidence integrity.

---

