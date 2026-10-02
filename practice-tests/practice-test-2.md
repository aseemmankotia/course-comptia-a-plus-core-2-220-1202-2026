# Practice Test 2: CompTIA A+ Core 2 (220-1202) Exam Prep Course

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-2.md`. Track results in `score-tracker.md`.

---

**Q1.** A technician needs to synchronize a folder structure from a file server to a backup server so that files deleted from the source are also removed from the destination during the copy job. Which robocopy switch accomplishes this?

A) /E
B) /MIR
C) /S
D) /COPYALL

---

**Q2.** A technician modified a Group Policy Object and now needs to verify exactly which policy settings are currently being applied to a specific user on a workstation, without forcing a new policy refresh. Which command should the technician run?

A) gpupdate /force
B) gpupdate /sync
C) chkdsk /r
D) gpresult /r

---

**Q3.** A Windows server has run out of available drive letters, but a new NTFS volume must be added and made accessible through an existing empty folder on the C: drive. Which Disk Management action should the technician perform?

A) Mount the new volume to an NTFS folder
B) Convert the disk to a dynamic disk
C) Extend the existing volume
D) Assign a new drive letter to the volume

---

**Q4.** A Linux administrator needs to give the file owner full read, write, and execute permissions while removing all permissions for the group and all other users. Which command accomplishes this?

A) chmod 700 report.sh
B) chmod 777 report.sh
C) chown 700 report.sh
D) chmod 070 report.sh

---

**Q5.** A technician runs netstat -ano on a Windows workstation and notices an ESTABLISHED connection to an unfamiliar external IP address on port 4444, associated with PID 6120. Which tool should the technician use next to identify the process image name behind that PID?

A) System Configuration (msconfig)
B) Task Manager's Details tab
C) Device Manager
D) Event Viewer

---

**Q6.** A user needs to store video files larger than 4GB on a USB flash drive that will be swapped between a Windows 11 workstation and a macOS system, with full native read/write access required on both platforms. Which file system should the technician choose when formatting the drive?

A) ext4
B) exFAT
C) NTFS
D) FAT32

---

**Q7.** A technician needs to synchronize a project folder to a backup server nightly. The backup must exactly mirror the source, including removing any files from the destination that were deleted from the source. Which robocopy switch accomplishes this?

A) /E
B) /Z
C) /MIR
D) /S

---

**Q8.** A network administrator wants to verify which Group Policy settings are currently applied to a user's workstation, including the resultant set of policy, without pushing any new policy changes. Which command should be run?

A) gpupdate /force
B) net accounts
C) secpol.msc
D) gpresult /r

---

**Q9.** A technician's Windows workstation has an MBR disk with four primary partitions already in use, all containing important data. The user needs a fifth volume on the same physical disk without losing any existing data. Which action should the technician take in Disk Management?

A) Delete one existing primary partition and create an extended partition with logical drives
B) Use Diskpart to extend the last partition to consume remaining space
C) Convert the disk from MBR to GPT
D) Convert the disk from basic to dynamic

---

**Q10.** A user needs to copy several 8 GB video files from a Windows 11 laptop to a USB flash drive, then read and write those same files on a macOS machine without installing any third-party drivers. Which file system should the flash drive be formatted with?

A) FAT32
B) exFAT
C) NTFS
D) HFS+

---

**Q11.** A technician troubleshooting a Linux server needs to continuously monitor which processes are consuming the most CPU and memory in real time, similar to using Task Manager's Performance tab on Windows. Which command should be used?

A) chmod
B) top
C) grep
D) ps aux

---

**Q12.** A macOS user accidentally overwrote an important document yesterday and wants to restore the version of the file as it existed two days ago using the built-in Apple backup utility. Which feature should be used?

A) Finder
B) Disk Utility
C) Time Machine
D) Migration Assistant

---

**Q13.** A technician must copy a folder tree—including empty subdirectories—to a new file server over a network connection known to drop packets intermittently. The technician wants the copy to skip a failed file quickly rather than hang for a long time retrying. Which command meets these requirements?

A) robocopy C:\Data \\Server\Data /S
B) xcopy C:\Data \\Server\Data /E /C
C) robocopy C:\Data \\Server\Data /E
D) robocopy C:\Data \\Server\Data /E /R:1 /W:1

---

**Q14.** A technician moves a file from a folder with NTFS permission 'Read Only' to a different folder on the SAME NTFS volume that has 'Full Control' permission assigned. After the move completes, what permission does the file have?

A) Full Control, because moved files always inherit the destination folder's permissions
B) Read Only, because moving a file within the same NTFS volume does not cause it to inherit new permissions
C) No permissions, because moving a file triggers an explicit Deny by default
D) Full Control minus Execute, because moved files receive the intersection of both permission sets

---

**Q15.** A technician has identified a malware infection and QUARANTINED the affected system according to CompTIA's malware removal best practices. What is the NEXT step in the recommended remediation process?

A) Remediate the infected systems by updating anti-malware software and scanning/removing malware
B) Disable System Restore in Windows
C) Re-enable System Restore and create a new restore point
D) Educate the end user about safe computing habits

---

**Q16.** A network administrator needs centralized authentication for administrators logging into routers and switches, along with the ability to authorize exactly which CLI commands each administrator is permitted to run. Which protocol BEST meets this requirement?

A) Kerberos
B) LDAP
C) TACACS+
D) RADIUS

---

**Q17.** A user encrypted a file with EFS on their Windows workstation. Later, the user's account profile became corrupted and was deleted and recreated by an administrator to resolve the issue. The user now attempts to open the previously encrypted file and receives an 'Access is denied' error. What is the MOST likely cause?

A) NTFS permissions on the folder were reset during profile recreation
B) BitLocker must be enabled before EFS-encrypted files can be opened
C) User Account Control (UAC) is blocking access to the encrypted file
D) The new user account does not possess the original EFS certificate and private key required to decrypt the file

---

**Q18.** Which of the following is a key security improvement that WPA3 provides over WPA2, specifically protecting against OFFLINE dictionary attacks against the pre-shared key?

A) TKIP integrity checking replacing CRC-32
B) Open System Authentication replacing shared-key authentication
C) AES-256 encryption replacing AES-128
D) SAE (Simultaneous Authentication of Equals) replacing the WPA2 four-way handshake

---

**Q19.** A company is decommissioning a batch of SSDs that contained sensitive financial data. Which data destruction method should be AVOIDED because it is INEFFECTIVE on solid-state drives?

A) Degaussing the drive
B) Physical shredding of the drive
C) Cryptographic erase (crypto-shred) of an encrypted drive
D) Manufacturer secure erase command

---

**Q20.** A user's account is a member of both the Sales group and the Managers group. On a file server, the Sales group has NTFS permission 'Read' and the Managers group has NTFS permission 'Modify' on a shared folder named Reports. The share permission for both groups on \\SERVER\Reports is set to 'Full Control'. When the user connects to \\SERVER\Reports over the network, what is the user's effective permission?

A) Read, because NTFS permissions always override share permissions
B) Full Control, because share permissions take precedence over NTFS when accessing remotely
C) Modify, because NTFS permissions combine to the most permissive (Modify), and comparing that to the combined share permission (Full Control) the more restrictive of the two applies
D) No Access, because conflicting group permissions always result in Deny

---

**Q21.** A technician encrypts a confidential file on a Windows 11 workstation using the built-in 'Encrypt contents to secure data' option (EFS) via file Properties > Advanced. The technician then copies the file onto a USB flash drive that is formatted with FAT32. What happens to the file's encryption status after the copy?

A) The file remains EFS-encrypted because EFS encryption travels with the file regardless of file system
B) The copy operation fails outright because EFS-encrypted files cannot be copied to removable media
C) The USB drive is automatically reformatted to NTFS to preserve the encryption
D) The file becomes unencrypted (plaintext) because FAT32 does not support the NTFS-based EFS feature

---

**Q22.** Following the standard CompTIA malware removal best-practice procedure, after a technician has identified and quarantined infected systems, which step should be performed NEXT, before remediating the infected system?

A) Disable System Restore in Windows
B) Educate the end user on how the infection occurred
C) Enable System Restore and create a new restore point
D) Schedule scans and run updates automatically

---

**Q23.** A network administrator manages authentication for administrative logins to dozens of routers and switches. The requirement is that the entire authentication packet, not just the password, must be encrypted, and that authentication, authorization, and accounting be handled as three separate, independently configurable services. Which protocol should the administrator implement?

A) RADIUS
B) TACACS+
C) Kerberos
D) LDAP

---

**Q24.** A company is retiring 40 hard drives that contain sensitive customer PII. The drives will be redeployed for internal, non-sensitive use within the company, so they must remain fully functional afterward. Which data destruction method BEST meets these requirements?

A) Physically shred the drives
B) Degauss the drives using a strong magnetic field
C) Drill holes through the platters
D) Use certified drive-wiping software to perform multiple overwrite passes

---

**Q25.** The CFO of a company receives an email that appears to come from the CEO's exact email address, requesting an urgent wire transfer to a new vendor account before end of day. The email uses correct company terminology and references a real ongoing project. Which social engineering attack does this scenario describe?

A) Vishing
B) Shoulder surfing
C) Tailgating
D) Whaling

---

**Q26.** A folder named Reports is shared with Share permission 'Everyone: Read'. NTFS permissions on the folder are set to 'Sales group: Modify' and 'Marketing group: Read'. A user who belongs to both the Sales and Marketing groups connects to the folder over the network. What is the user's effective permission?

A) Read, because the more restrictive share permission limits the combined NTFS permission when accessing over the network
B) Modify, because NTFS permissions always override share permissions
C) Full Control, because the permissions from both groups combine cumulatively
D) No access, because conflicting permissions from two different groups result in an implicit deny

---

**Q27.** A technician has already investigated symptoms and quarantined an infected workstation from the network, following CompTIA best-practice malware removal procedures. What is the correct NEXT step before remediating the system?

A) Educate the end user on how the infection occurred
B) Update anti-malware software and run a full scan
C) Schedule automatic scans and run Windows Updates
D) Disable System Restore in Windows

---

**Q28.** A user reports their laptop displayed a blue screen referencing a third-party driver file after installing a new printer, and the system now automatically reboots before the error can be read. Which troubleshooting step should the technician perform FIRST to safely diagnose the issue?

A) Reinstall Windows using the recovery partition
B) Run chkdsk /f /r on the system drive immediately
C) Boot into Safe Mode and check Device Manager and Event Viewer for the faulting driver
D) Replace the laptop's RAM modules

---

**Q29.** A critical Windows service fails to start and Event Viewer logs Error 1053: 'The service did not respond to the start or control request in a timely fashion.' The technician checks Services.msc and finds the service it depends on is set to Disabled. What is the MOST likely fix?

A) Set the dependent service's startup type to Automatic and start it, then start the original service
B) Increase the ServicesPipeTimeout registry value
C) Uninstall and reinstall the application associated with the service
D) Run System File Checker (sfc /scannow) to repair the service executable

---

**Q30.** A user logs into their Windows 11 workstation and sees the message 'You have been logged on with a temporary profile. You cannot access your files and files created in this profile will be deleted when you log off.' Simply deleting and recreating the user profile through System Properties has not fixed the issue on repeat logins. What should the technician check next?

A) The ProfileList registry key for a duplicate or corrupted SID entry ending in .bak
B) The user's password expiration policy in Local Security Policy
C) The NTFS permissions on the C:\Windows\System32 folder
D) The maximum profile size quota configured in Group Policy

---

**Q31.** Windows Update on a workstation repeatedly fails to install a cumulative update, showing the same error code after multiple restart attempts. A quick reboot did not fix it. Which sequence of actions is the BEST next troubleshooting approach?

A) Immediately reinstall Windows from a recovery image to guarantee update success
B) Perform a System Restore to a point before the update was ever offered
C) Run DISM /Online /Cleanup-Image /RestoreHealth, then run SFC /scannow, then retry Windows Update
D) Disable the Windows Update service entirely so the error stops appearing

---

**Q32.** A user reports that all of their personal documents now have a '.locked' file extension, and a text file on the desktop demands cryptocurrency payment to restore access. Which category of malware does this describe?

A) Ransomware
B) Rootkit
C) Keylogger
D) Trojan

---

**Q33.** A technician confirms that a Windows 11 laptop is displaying unauthorized pop-ups, a redirected browser homepage, and unusually high outbound network traffic, verifying that the machine is infected with adware and a possible bot client. Following the CompTIA best-practice malware removal procedure, what should the technician do NEXT?

A) Quarantine the infected system by disconnecting it from the network
B) Update the anti-malware definitions and run a full remediation scan
C) Educate the end user on how the infection likely occurred
D) Create a System Restore point to preserve the current state

---

**Q34.** A workstation was confirmed infected with ransomware. The technician has already quarantined the machine and disabled System Restore. Anti-malware definitions were then updated and a full scan removed the active threat. According to the correct malware removal procedure, what should the technician do NEXT, before re-enabling System Restore?

A) Re-enable System Restore immediately and create a new restore point
B) Educate the end user about phishing and safe browsing habits
C) Schedule regular anti-malware scans and ensure the OS and applications are fully updated
D) Reboot into Safe Mode and manually delete any remaining suspicious startup entries

---

**Q35.** A Windows 11 desktop enters an automatic repair loop immediately after a cumulative update failed to install correctly. Safe Mode is accessible, but normal boot fails every time. Which action should the technician attempt FIRST to resolve this with the least amount of data loss or rebuild effort?

A) Run 'Reset this PC' and choose the option to remove everything
B) Rebuild the BCD store using bootrec /rebuildbcd
C) Boot into WinRE and use Advanced Startup Options to uninstall the recent quality update
D) Run sfc /scannow from a standard Command Prompt in normal boot mode

---

**Q36.** A user logs into their Windows 10 workstation and receives a message stating they have been logged on with a temporary profile; none of their desktop customizations, pinned taskbar items, or saved files in Documents appear. A technician suspects profile corruption caused by a SID mismatch. Which registry path should the technician examine to correct the mismatched profile entries?

A) HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run
B) HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services
C) HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList
D) HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies

---

**Q37.** A network administrator submits a change request to upgrade firmware on the core switch during a scheduled maintenance window. The change advisory board reviews and approves the request, and documentation is filed correctly. During the upgrade, the switch loses connectivity to half the network and cannot be quickly returned to its previous working state, causing a prolonged outage. Which missing element of the change management process is the BEST explanation for the extended outage?

A) Risk analysis
B) Change request documentation
C) End-user acceptance
D) Backout plan

---

**Q38.** A file server crashes on Wednesday morning. The organization follows a Grandfather-Father-Son (GFS) rotation: a full backup runs on the last day of each month (Grandfather), a full backup runs every Friday (Father), and incremental backups run Monday through Thursday (Son). The most recent Friday full backup and the Monday and Tuesday incremental backups completed successfully, but Wednesday's incremental never finished due to the crash. Which restore approach correctly recovers data through Tuesday night?

A) Restore the Father (Friday) full backup, then apply the Monday and Tuesday incremental backups in chronological order
B) Restore only the most recent Grandfather (monthly) full backup
C) Restore only Tuesday's incremental backup
D) Restore the Father (Friday) full backup, then apply the incremental backups in reverse chronological order

---

**Q39.** While repairing a user's workstation, a technician discovers what appears to be illicit material stored on the device. Following standard incident response procedure for a suspected policy or legal violation, what should the technician do FIRST?

A) Continue the repair and document the finding in the ticket afterward
B) Preserve the current system state, stop using the device, and report the finding to the appropriate supervisor or authority
C) Immediately confront the user about the material
D) Delete the material to avoid company liability

---

**Q40.** A hospital's billing system stores patient names, diagnosis codes, and treatment history. Which classification applies to this data, and which regulation primarily governs its protection in the United States?

A) PHI, governed by HIPAA
B) PII, governed by GDPR
C) PCI, governed by PCI-DSS
D) PHI, governed by GDPR

---

**Q41.** A user opens an email attachment named invoice.vbs, and shortly afterward, files on the shared network drive are renamed with a .locked extension. Which characteristic of VBScript files makes them a common vector for this kind of attack?

A) VBScript files require administrator privileges to execute, ensuring the attack is logged before any damage occurs
B) VBScript files can only run inside a sandboxed browser environment, limiting any damage to interactive prompts
C) VBScript files can be disguised with a double extension to appear as a document and execute automatically through the Windows Script Host without requiring compilation
D) VBScript files are cryptographically signed by default, allowing them to bypass antivirus detection legitimately

---

**Q42.** While replacing a power supply, a technician notices smoke and small flames coming from the wall outlet wiring, and the equipment is still energized. Which class of fire extinguisher should the technician use?

A) Class A
B) Class B
C) Class C
D) Class D

---

**Q43.** A technician needs to apply a firmware update to a production database server that is currently in use by multiple departments. According to proper change management procedure, which action should the technician take FIRST?

A) Apply the update during the next scheduled maintenance window without further documentation
B) Submit a change request documenting the purpose, scope, risk analysis, and rollback plan for approval
C) Notify all end users that the server will be briefly unavailable
D) Test the update on the production server after hours since risk is considered low

---

**Q44.** An employee reports receiving an email with an attachment named "invoice.vbs" and asks IT whether it is safe to open. Which statement BEST describes the risk this file type poses on a Windows system?

A) It is a Bash shell script that only executes on Linux, so it poses no risk on a Windows machine
B) It is a Windows Script Host file that can execute automatically when opened and is a common vector for delivering malware
C) It is a Python script that requires a separate interpreter to be installed, so double-clicking it does nothing
D) It is a batch file that always requires administrator elevation before any code inside it can run

---

**Q45.** While repairing a customer's laptop, a technician discovers files that appear to be illicit or prohibited content stored on the drive. Which action should the technician take FIRST?

A) Preserve the device untouched, stop work on it, and report the finding to a supervisor following the organization's documented incident response procedure
B) Delete the files immediately and continue with the repair as scheduled
C) Confront the customer directly and demand an explanation before proceeding
D) Format the drive to remove the content and document the action taken afterward

---

