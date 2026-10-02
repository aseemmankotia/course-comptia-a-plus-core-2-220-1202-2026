## Chapter 6: Windows Security Settings: Permissions, UAC, BitLocker/EFS, and Data Destruction — Practice Questions

**Q1.** A user's account has NTFS Modify permission on a local folder called Reports. The folder is shared over the network with Share permission set to Read. When the user accesses the folder through the network share, what is their effective permission?

A) Modify, because NTFS permissions always override share permissions
B) Read, because the most restrictive permission between NTFS and Share applies
C) Full Control, because permissions are combined additively
D) Read & Execute, because that is the default fallback permission

<details>
<summary>Answer</summary>

**Correct: B**

When a resource is accessed over the network, Windows evaluates both the NTFS permission and the Share permission, then applies whichever is MORE RESTRICTIVE. Modify (NTFS) vs Read (Share) → Read wins.

**Why the others are wrong:**
- NTFS permissions only take sole precedence when the file is accessed locally, not over the network share.
- Permissions are never combined additively; the more restrictive of the two always wins for network access.
- Read & Execute is not a valid fallback rule — the actual rule is 'most restrictive of NTFS and Share' applies.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A technician moves a file from D:\Finance (NTFS, Modify permission inherited) to E:\Archive (NTFS, Read-only permission inherited) using drag-and-drop in File Explorer. Both D: and E: are separate volumes. What permission will the file have in E:\Archive?

A) Modify, because moving a file always retains its original permissions
B) Full Control, because cross-volume moves reset to the highest available permission
C) The file will retain no permissions and require manual reassignment
D) Read-only, because moving across volumes is treated as a copy, inheriting the destination folder's permissions

<details>
<summary>Answer</summary>

**Correct: D**

Moving a file BETWEEN different volumes is actually performed as a copy-then-delete operation internally, so the file inherits the permissions of the destination folder — Read-only in this case.

**Why the others are wrong:**
- Permissions are only retained when moving within the SAME volume, not across volumes.
- Cross-volume moves inherit the destination folder's existing permissions, not the highest possible permission.
- The file does inherit permissions automatically from the destination folder — no manual reassignment is needed.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A company laptop is used by a single employee and contains sensitive client files stored locally. The laptop was stolen from the employee's car. The company's primary concern is that the entire drive's contents — OS, apps, and data — remain unreadable to the thief. Which technology should have been implemented to best address this?

A) EFS applied to the sensitive files only
B) NTFS permissions restricting access to the Administrator account
C) BitLocker Drive Encryption on the entire volume
D) Windows Defender Firewall with inbound rules blocking all traffic

<details>
<summary>Answer</summary>

**Correct: C**

BitLocker encrypts the entire volume, including the OS and all files, protecting against offline attacks like removing the drive and reading it on another machine — exactly the scenario of a stolen laptop.

**Why the others are wrong:**
- EFS only encrypts specific files/folders tied to a user account; it does not protect the OS or unencrypted files on the same drive.
- NTFS permissions can be bypassed entirely if the drive is removed and mounted on another system as a non-restricted user.
- A firewall only controls network traffic; it does nothing to protect data at rest on a stolen physical drive.

</details>

---

**Q4.** An organization is decommissioning several failed solid-state drives (SSDs) that contained financial records. Which data destruction method is INEFFECTIVE for SSDs and should NOT be relied upon?

A) Physical shredding
B) Secure erase using the drive's built-in ATA Secure Erase command
C) Degaussing
D) Manufacturer-certified crypto-erase

<details>
<summary>Answer</summary>

**Correct: C**

Degaussing works by disrupting magnetic domains and is only effective on magnetic storage media such as HDDs and tapes. SSDs store data using flash memory cells with no magnetic properties, so degaussing has no effect on them.

**Why the others are wrong:**
- Physical shredding destroys the physical media and works on any storage type, including SSDs.
- ATA Secure Erase is a supported, effective method specifically designed for SSDs.
- Crypto-erase (destroying the encryption key) is an effective and recommended method for SSDs.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A help desk technician needs to configure a workstation so that a standard user account receives a UAC prompt requiring an administrator's credentials before installing any new software, while minimizing unnecessary interruptions during normal file browsing. Which UAC configuration achieves this?

A) Never notify
B) Always notify
C) Notify me only when apps try to make changes to my computer (default)
D) Disable UAC entirely and rely on antivirus software

<details>
<summary>Answer</summary>

**Correct: C**

The default UAC level prompts only when a program (not the user) attempts to make system changes, such as installing software — matching the requirement while avoiding prompts for routine tasks like browsing files.

**Why the others are wrong:**
- Never notify disables prompts entirely, which fails to meet the requirement of prompting before installations.
- Always notify prompts for both user actions and program actions, causing more interruptions than necessary during normal use.
- Disabling UAC removes a core security control and is never the correct configuration recommendation.

</details>

---

**Q6.** Which Windows Defender Firewall network profile should be applied when a laptop connects to a coffee shop's Wi-Fi hotspot to ensure the most restrictive default rules are enforced?

A) Domain profile
B) Private profile
C) Guest profile
D) Public profile

<details>
<summary>Answer</summary>

**Correct: D**

The Public profile applies the most restrictive default firewall rules, blocking most inbound connections and disabling network discovery — appropriate for untrusted networks like public Wi-Fi.

**Why the others are wrong:**
- The Domain profile is used only when the machine is joined to and authenticated against an Active Directory domain network.
- The Private profile is meant for trusted home or work networks and allows more permissive settings like network discovery.
- 'Guest profile' is not one of the three Windows Defender Firewall network location profiles.

</details>

---

**Q7.** During a SOHO router hardening review, a technician finds that the router still uses its factory default administrator username and password, has WPS enabled, and broadcasts its default SSID. Which single action provides the GREATEST immediate reduction in risk?

A) Disabling SSID broadcast
B) Changing the default administrator credentials
C) Enabling MAC address filtering
D) Updating the router firmware

<details>
<summary>Answer</summary>

**Correct: B**

Default admin credentials are publicly documented and are the first thing attackers try; leaving them unchanged allows complete control of the router. This is consistently identified as the highest-priority hardening step.

**Why the others are wrong:**
- Disabling SSID broadcast provides only minor obscurity and does not stop determined attackers from discovering the network.
- MAC filtering can be bypassed by spoofing an allowed MAC address and is considered a weak, secondary control.
- Firmware updates are important for patching vulnerabilities but do not address the immediate risk of unchanged default credentials.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the key difference between the NTFS Full Control permission and the NTFS Modify permission?

A) Modify allows changing file ownership and permissions, while Full Control does not
B) There is no difference; they grant identical access
C) Modify is only available on FAT32 volumes, while Full Control is NTFS-only
D) Full Control includes the ability to change permissions and take ownership, which Modify does not allow

<details>
<summary>Answer</summary>

**Correct: D**

Full Control includes all Modify capabilities (read, write, execute, delete) PLUS the ability to change permissions and take ownership of the file or folder — capabilities Modify does not grant.

**Why the others are wrong:**
- This reverses the actual relationship — changing ownership/permissions is a Full Control capability, not Modify.
- The two permissions are distinctly different, with Full Control being a superset of Modify.
- Neither permission is exclusive to FAT32; in fact, FAT32 does not support NTFS-style granular permissions at all.

</details>

---

