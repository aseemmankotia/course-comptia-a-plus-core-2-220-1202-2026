## Chapter 1: Windows Editions, Features, and Core Administrative Tools — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Windows 11 Home vs Pro: BitLocker drive encryption? | Home = No (Device Encryption on supported hardware only). Pro/Enterprise/Education/Pro for Workstations = Yes, full BitLocker. Exam tip: BitLocker requires Pro or higher. |
| 2 | Which Windows editions can act as an RDP HOST (accept incoming Remote Desktop connections)? | Pro, Enterprise, Education, Pro for Workstations. Home can only be an RDP CLIENT, never a host. |
| 3 | Max physical CPU sockets: Home / Pro / Pro for Workstations | Home = 1, Pro/Enterprise/Education = 2, Pro for Workstations = 4. Exam tests these exact numbers. |
| 4 | Max RAM supported: Home / Pro / Pro for Workstations (64-bit) | Home = 128GB, Pro/Enterprise/Education = 2TB, Pro for Workstations = 6TB. |
| 5 | Which edition adds ReFS file system support? | Windows Pro for Workstations only (also adds persistent memory support and Storage Spaces Direct-related features). |
| 6 | gpedit.msc and secpol.msc — which editions include them? | Pro, Enterprise, Education, Pro for Workstations. NOT included on Home (no Group Policy engine on Home). |
| 7 | MMC snap-in to convert a disk between MBR and GPT? | Disk Management (diskmgmt.msc). Requires the disk to have no volumes/be unallocated to change partition style safely. |
| 8 | MBR partition limits | Max 4 primary partitions (or 3 primary + 1 extended with logical drives), max partition size 2TB. Exam tip: choose GPT for drives over 2TB or UEFI boot. |
| 9 | msconfig Services tab — key checkbox for safe troubleshooting? | 'Hide all Microsoft services' — filters to third-party services only so you don't accidentally disable a core OS service. |
| 10 | Control Panel > Programs and Features → Settings app equivalent? | Settings > Apps > Installed apps (Windows 11) / Apps & Features (Windows 10). |
| 11 | Task Manager tab to view/change a process's priority and CPU affinity? | Details tab — right-click a process for 'Set priority' and 'Set affinity'. |
| 12 | Local Users and Groups vs Local Security Policy — purpose difference | Local Users and Groups (lusrmgr.msc) manages account/group membership. Local Security Policy (secpol.msc) manages password policy, account lockout policy, and user rights assignment. Neither is available on Home edition. |
