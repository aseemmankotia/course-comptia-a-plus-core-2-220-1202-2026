# Answer Key — Practice Test 1

**Q1. Correct: D**

netstat -ano lists all active TCP/UDP connections and listening ports along with the owning process ID, allowing the technician to correlate suspicious connections to a specific process.

---

**Q2. Correct: B**

exFAT supports individual files larger than 4GB and is natively readable and writable by both Windows and macOS without additional drivers.

---

**Q3. Correct: B**

A domain uses a central server (domain controller) running Active Directory Domain Services to manage user accounts and enforce Group Policy across all joined computers, providing single sign-on.

---

**Q4. Correct: D**

Activity Monitor is the built-in macOS utility that displays CPU, memory, disk, and network usage per process and allows the technician to force quit unresponsive or resource-heavy processes.

---

**Q5. Correct: B**

Disk Management's Extend Volume feature can only grow a partition into unallocated space that is contiguous and immediately follows it. If another partition sits between C: and the unallocated space at the end of the disk, Extend Volume will be unavailable until that partition is deleted, shrunk, or moved.

---

**Q6. Correct: A**

gpresult /r displays a Resultant Set of Policy (RSoP) summary, listing the GPOs currently applied to the computer and the user, which helps verify whether the expected policies took effect.

---

**Q7. Correct: D**

Robocopy (Robust File Copy) is designed for large-scale file transfers, supports automatic retry on network failure, can resume interrupted copies, and mirrors directory structures with logging — exactly the resiliency needed here.

---

**Q8. Correct: B**

Windows Pro supports domain join, Group Policy, and BitLocker without requiring volume licensing agreements, making it the correct fit for a small business with these needs.

---

**Q9. Correct: C**

exFAT has no 4GB file size limit, is natively supported for both read and write on modern Windows and macOS without extra drivers, making it ideal for cross-platform removable media.

---

**Q10. Correct: C**

sfc /scannow (System File Checker) scans protected Windows system files, verifies them against a cached copy, and automatically repairs or replaces corrupted or missing files.

---

**Q11. Correct: B**

nslookup queries DNS servers directly to resolve a hostname to an IP address; if it fails to resolve the name while the IP works fine, this confirms a DNS resolution problem, which matches the symptoms described.

---

**Q12. Correct: B**

Activity Monitor is the built-in macOS graphical utility that displays real-time CPU, memory, disk, network, and energy usage for running processes — functionally equivalent to Windows Task Manager.

---

**Q13. Correct: C**

sfc /scannow scans all protected system files and replaces corrupted or missing ones with a cached correct version, which directly addresses corrupted DLL/system file errors without touching the disk's file system structure or user data.

---

**Q14. Correct: D**

The malware removal best practice order is: 1) Investigate and verify malware symptoms, 2) Quarantine infected systems, 3) Disable System Restore in Windows, 4) Remediate infected systems (update anti-malware and scan/remove), 5) Schedule scans and run updates, 6) Enable System Restore and create a restore point, 7) Educate the end user. After verifying symptoms, quarantining the system comes next to prevent further spread.

---

**Q15. Correct: B**

Vishing (voice phishing) is a social engineering attack conducted over a phone call, where the attacker impersonates a trusted entity (like IT support) to trick the victim into revealing sensitive information such as a password.

---

**Q16. Correct: D**

WPA3-Enterprise uses 802.1X authentication with a RADIUS server, allowing individual user authentication with domain credentials, combined with the strongest current wireless encryption (192-bit security suite in enterprise mode), satisfying both the centralized authentication and strongest-encryption requirements.

---

**Q17. Correct: C**

Copying a file, whether within the same volume or to a different volume, always causes the file to inherit the NTFS permissions of the destination folder. Only a MOVE within the same NTFS volume retains the original permissions; a COPY operation never retains source permissions.

---

**Q18. Correct: D**

Physical destruction, such as shredding, is the most reliable method for ensuring data on an SSD is unrecoverable. SSDs use flash memory and wear-leveling algorithms that can leave data remnants in reserved or remapped blocks even after overwrite attempts, making software-based erasure unreliable.

---

**Q19. Correct: D**

A fingerprint scan is a biometric authentication method, which falls under the 'something you are' factor category since it relies on a unique physical characteristic of the individual.

---

**Q20. Correct: B**

After investigating and verifying symptoms, step 2 of the malware removal process is to quarantine the infected system by disconnecting it from the network to prevent lateral spread and further encryption.

---

**Q21. Correct: A**

Tailgating (piggybacking) occurs when an unauthorized person follows an authorized employee through a secured physical entry point without proper credentials.

---

**Q22. Correct: D**

When accessing a resource across the network, the effective permission is the most restrictive combination of the share permission and the NTFS permission. Here, Share=Read and NTFS=Modify, so the effective access is Read.

---

**Q23. Correct: A**

WPA3 replaces the WPA2 PSK exchange with SAE (also known as Dragonfly handshake), which prevents offline dictionary attacks by requiring interactive attempts against the live access point rather than allowing captured handshake data to be brute-forced offline.

---

**Q24. Correct: B**

SSDs store data on flash memory rather than magnetic platters, so degaussing has no effect. CompTIA recommends using the drive's cryptographic/secure erase function combined with physical destruction (shredding) to guarantee data cannot be recovered.

---

**Q25. Correct: D**

A remote wipe issued through the MDM console immediately removes or protects corporate data already stored on the lost device, which is the primary security purpose of MDM enrollment.

---

**Q26. Correct: C**

WPA3 provides the strongest current wireless encryption standard (SAE replacing PSK vulnerabilities) and, when paired with RADIUS (802.1X enterprise authentication), allows centralized user credential validation against an authentication server, which is the industry-standard combination tested on the exam for enterprise wireless security.

---

**Q27. Correct: B**

The CompTIA-recommended order is: 1) Investigate/identify symptoms, 2) Quarantine the infected system, 3) Disable System Restore, 4) Remediate (update and scan), 5) Schedule scans and run updates, 6) Re-enable System Restore and create a restore point, 7) Educate the end user. Quarantine (disconnect from the network) is step 2 and comes immediately after identification.

---

**Q28. Correct: A**

Since the BSOD started immediately after a driver update and references the video driver, the least invasive and most direct fix is booting into Safe Mode (which loads minimal drivers) and rolling back the driver to the previous working version using Device Manager.

---

**Q29. Correct: C**

Resource Monitor provides granular, real-time detail on CPU, memory, disk, and network activity per process, including exactly which files are being read from or written to, making it the correct tool for diagnosing a specific process's disk I/O behavior.

---

**Q30. Correct: D**

System Restore is configured and disabled from the System Protection tab, accessed via System Properties (right-click This PC > Properties > Advanced system settings > System Protection), where the technician can select the drive and click Configure to turn protection off.

---

**Q31. Correct: A**

Settings resetting every session and only affecting one user account is the classic symptom of a corrupted user profile, causing Windows to load a temporary profile. The fix is to back up the user's data, then delete the corrupted profile and create a new local profile, restoring the data into it.

---

**Q32. Correct: C**

Per the CompTIA-recommended sequence, after remediation (updating anti-malware software and scanning/removing malware), the next step is to schedule scans and run updates to ensure ongoing protection, followed later by re-enabling System Restore and educating the end user.

---

**Q33. Correct: A**

The correct malware remediation order is: investigate/identify, quarantine, disable System Restore, remediate (update anti-malware definitions and scan), schedule scans/updates, re-enable System Restore, then educate the user. After disabling System Restore, the very next step is updating and running the anti-malware scan.

---

**Q34. Correct: A**

A BSOD referencing a specific driver file (nvlddmkm.sys is the NVIDIA display driver) immediately following a driver update strongly indicates a faulty or incompatible driver. Booting into Safe Mode and rolling back the driver is the fastest, least destructive fix.

---

**Q35. Correct: C**

Error 1053 commonly points to a problem with the account the service logs on as, or with a dependent service that isn't running. Checking the Log On tab and dependencies in Services.msc is the standard first diagnostic step for this specific error.

---

**Q36. Correct: D**

When Windows cannot load a user's registry hive (ntuser.dat) or the profile folder is damaged, it falls back to creating a temporary profile so the user can still log in, but with no access to their original files or settings. This is the classic symptom of a corrupted local user profile.

---

**Q37. Correct: A**

Standard change management requires a formal change request approved by a change advisory board (or manager) before implementation, and it must document the purpose, scope of change, risk analysis, plan for change, backout/rollback plan, and end-user acceptance before work begins.

---

**Q38. Correct: A**

Because PHI (protected health information) was potentially exposed, the first step in incident response is to report and document the incident to the compliance/security officer so a formal chain-of-custody investigation and any required regulatory breach notification (e.g., HIPAA) can begin.

---

**Q39. Correct: C**

Grandfather-Father-Son (GFS) is a tape rotation strategy that maintains daily (son), weekly (father), and monthly (grandfather) backup sets, exactly matching the tiered retention described and minimizing total media used.

---

**Q40. Correct: A**

RemoteSigned allows locally created scripts to run without a digital signature while requiring that any scripts downloaded from the internet (remote) be digitally signed by a trusted publisher, which is the recommended balanced security setting for this scenario.

---

**Q41. Correct: C**

A standard retail EULA grants rights to install the software on a limited number of devices (often just one), and using a single license across multiple machines without a volume or multi-seat license violates the licensing terms, regardless of DRM enforcement.

---

**Q42. Correct: A**

Grounding yourself with an anti-static wrist strap attached to the chassis equalizes electrical potential between you and the components, preventing an electrostatic discharge that could damage sensitive parts like the motherboard or expansion cards.

---

**Q43. Correct: A**

A change request is the formal document submitted through change management that includes the purpose of the change, scope, risk analysis, rollback plan, and requires approval from a change advisory board before implementation on production systems.

---

**Q44. Correct: B**

VBScript (.vbs) files are interpreted and executed directly by the Windows Script Host, requiring no compilation, which is why they are a common vector for email-based malware — double-clicking or auto-executing the attachment runs the script immediately with the user's permissions.

---

**Q45. Correct: C**

PHI (Protected Health Information) specifically covers patient treatment records, diagnoses, and health-related insurance claim data, and is governed under regulations such as HIPAA in healthcare environments.

---

