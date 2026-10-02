# Practice Test 1: CompTIA A+ Core 2 (220-1202) Exam Prep Course

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-1.md`. Track results in `score-tracker.md`.

---

**Q1.** A technician suspects a Windows 11 workstation has malware communicating with an external server. Which command should the technician run to view all active TCP connections along with the process ID (PID) using each connection?

A) ipconfig /all
B) nslookup
C) chkdsk /f
D) netstat -ano

---

**Q2.** A user needs to store a single 12GB video file on a USB flash drive that will be moved back and forth between a Windows 11 PC and a macOS computer, with both systems needing full read/write access. Which file system should the technician use to format the drive?

A) FAT32
B) exFAT
C) NTFS
D) ext4

---

**Q3.** A small office with five Windows 11 Pro computers wants centralized user account management, Group Policy enforcement, and a single sign-on experience across all the machines. Which network configuration should be implemented?

A) Workgroup
B) Domain
C) HomeGroup
D) Peer-to-peer VPN

---

**Q4.** A technician is troubleshooting a MacBook Pro that is showing high CPU usage from an unidentified background process. Which built-in macOS utility should the technician use to identify and force quit the process?

A) Task Manager
B) System Configuration
C) Terminal Monitor
D) Activity Monitor

---

**Q5.** A technician wants to increase the size of the NTFS-formatted C: drive on a Windows 11 workstation. Disk Management shows unallocated space at the end of the physical disk, but the Extend Volume option is grayed out for C:. Which is the MOST likely reason?

A) The C: drive is formatted as FAT32
B) Another partition exists between C: and the unallocated space
C) The disk has not been converted to GPT
D) The workstation needs to be restarted

---

**Q6.** A network administrator suspects a Group Policy Object (GPO) has not been applied correctly to a domain-joined Windows 10 workstation. Which command should be used to generate a report showing which Group Policy settings are currently applied to the computer and the logged-in user?

A) gpresult /r
B) gpupdate /force
C) net use
D) robocopy

---

**Q7.** A technician must copy a 200GB folder structure containing thousands of files from an old file server to a new one overnight. The network connection is unreliable, and the technician needs the copy to automatically resume and skip files that are already successfully copied if the connection drops. Which tool should be used?

A) xcopy
B) net use
C) copy
D) robocopy

---

**Q8.** A small business owner wants new desktops to join the company's Active Directory domain and use BitLocker drive encryption, but does not want to pay for volume licensing associated with Enterprise edition. Which Windows edition should be installed?

A) Windows Home
B) Windows Pro
C) Windows Enterprise
D) Windows Education

---

**Q9.** A user needs a USB flash drive that can store individual video files larger than 4GB and be readable/writable on both a Windows 11 laptop and a macOS device without installing extra drivers. Which file system should the drive be formatted with?

A) FAT32
B) NTFS
C) exFAT
D) ext4

---

**Q10.** After removing malware from a Windows 11 workstation, the technician notices several core Windows system files appear to be missing or corrupted, causing intermittent application crashes. Which command should be run to scan and repair the protected system files?

A) chkdsk /r
B) gpupdate /force
C) sfc /scannow
D) diskpart

---

**Q11.** A user reports that they cannot open the company website by typing its name (www.company.com) in a browser, but can reach the same site successfully by entering its IP address directly. Which command should the technician run FIRST to confirm whether the issue is DNS-related?

A) ipconfig /release
B) nslookup www.company.com
C) netstat -an
D) tracert www.company.com

---

**Q12.** A technician is helping a user on a macOS laptop who wants to view real-time CPU, memory, and energy usage of running processes, similar to Task Manager on Windows. Which built-in macOS utility should the technician open?

A) Terminal
B) Activity Monitor
C) Disk Utility
D) System Preferences

---

**Q13.** A user reports that several Windows system programs are crashing intermittently and error messages reference missing or corrupted DLL files. No recent hardware changes were made, and the hard drive passes a health check. Which command should the technician run FIRST to attempt to repair the issue?

A) chkdsk /r
B) diskpart clean
C) sfc /scannow
D) robocopy /mir

---

**Q14.** A technician has verified that a Windows workstation is infected with malware and confirmed the symptoms. According to CompTIA's malware removal best practice procedure, what is the NEXT step the technician should perform?

A) Disable System Restore
B) Remediate the infected system
C) Schedule scans and run updates
D) Quarantine the infected system

---

**Q15.** An employee receives a phone call from someone claiming to be from the IT help desk. The caller states there is an urgent problem with the employee's account and asks the employee to read back their password over the phone to 'verify' it. Which type of social engineering attack does this describe?

A) Phishing
B) Vishing
C) Whaling
D) Shoulder surfing

---

**Q16.** A company is deploying a new wireless access point in its corporate office. Employees must authenticate using their individual domain credentials against a centralized authentication server, and the company wants the strongest available wireless encryption standard. Which configuration BEST meets these requirements?

A) WPA2-Personal
B) WEP
C) WPA3-Personal
D) WPA3-Enterprise

---

**Q17.** A file located in Folder A on an NTFS volume has explicit NTFS permissions of 'Deny: Everyone - Write.' A technician copies this file into Folder B, which resides on the same NTFS volume but has different permissions. What permissions will the copied file have in Folder B?

A) The file retains its original NTFS permissions from Folder A
B) The file merges the permissions of both Folder A and Folder B
C) The file inherits the permissions of Folder B
D) The file becomes owned by the Everyone group with Full Control

---

**Q18.** An organization is decommissioning several failed SSDs that contained highly sensitive financial data. The security policy requires that data be rendered completely unrecoverable before disposal. Which method BEST meets this requirement for SSDs specifically?

A) Degaussing the drive
B) Performing a single-pass low-level format
C) Overwriting the drive three times with zeros
D) Physically shredding the drive

---

**Q19.** A company is implementing multifactor authentication (MFA) for remote VPN access. Which of the following authentication methods represents the 'something you are' factor?

A) A PIN entered on a keypad
B) A smart card inserted into a reader
C) An answer to a security question
D) A fingerprint scan

---

**Q20.** A technician receives a call from a user whose workstation displays a ransom note demanding payment, and encrypted files are confirmed. The technician verifies this is ransomware. According to CompTIA's best-practice malware removal procedure, what should the technician do NEXT?

A) Disable System Restore
B) Isolate the infected system from the network
C) Run a full antivirus scan and remove the malware
D) Educate the end user on prevention

---

**Q21.** An employee holds the secured server room door open for a person carrying boxes who claims to be a new hire but is not wearing a visible badge. This scenario describes which type of attack?

A) Tailgating
B) Phishing
C) Whaling
D) Shoulder surfing

---

**Q22.** A network share named \\SERVER\Data has share permissions set to Read for the Sales group. The underlying NTFS permissions on the same folder grant the Sales group Modify. When a Sales group member accesses the folder over the network, what is their effective permission?

A) Modify
B) Full Control
C) No access
D) Read

---

**Q23.** Which feature of WPA3 protects against the offline dictionary and brute-force attacks that were possible against WPA2's four-way handshake?

A) SAE (Simultaneous Authentication of Equals)
B) TKIP encryption
C) WEP fallback compatibility
D) Open System Authentication

---

**Q24.** A company is decommissioning several solid-state drives (SSDs) that contained sensitive financial data. Which method should be used to ensure the data cannot be recovered?

A) Degaussing
B) Secure erase using the drive's built-in cryptographic erase, followed by physical shredding
C) Low-level formatting
D) Quick format

---

**Q25.** An employee reports that their company-owned smartphone, enrolled in the organization's MDM solution, has been lost. Which action should the administrator take FIRST to protect corporate data on the device?

A) Reset the employee's email password
B) File a police report
C) Disable the employee's VPN account
D) Initiate a remote wipe through the MDM console

---

**Q26.** A technician needs to configure a wireless network for a small business that requires the strongest available encryption and authentication for user credentials against a centralized server. Which combination BEST meets this requirement?

A) WEP with a shared passphrase
B) WPA2-Personal with AES
C) WPA3 with RADIUS authentication
D) WPA3 with TACACS+ authentication

---

**Q27.** A technician confirms a workstation has ransomware and has already completed step 1 (investigate and identify symptoms) of the standard malware removal process. Which step should the technician perform NEXT?

A) Schedule scans and run updates
B) Quarantine the infected system
C) Disable System Restore in Windows
D) Remediate the infected system

---

**Q28.** A user reports a Blue Screen of Death (BSOD) with a stop code referencing a video driver, occurring only since a new graphics card driver was installed yesterday. What should the technician do FIRST to resolve this?

A) Boot into Safe Mode and roll back the video driver
B) Reformat the drive and reinstall Windows
C) Run chkdsk /r on the system drive
D) Reseat the RAM modules

---

**Q29.** Task Manager shows one background process consuming a large percentage of disk resources, but the technician needs to see the exact files being read and written by that process in real time to determine the root cause. Which built-in Windows tool should be used?

A) Disk Defragmenter
B) Event Viewer
C) Resource Monitor
D) System Configuration (msconfig)

---

**Q30.** As part of the malware remediation process, a technician needs to disable System Restore on a Windows 11 workstation before scanning. Where should the technician go to do this?

A) Local Group Policy Editor > Windows Update settings
B) Control Panel > Programs and Features
C) Task Scheduler > Task Scheduler Library
D) System Properties > System Protection tab

---

**Q31.** A user logs into their Windows workstation and finds the desktop background reset to default, no saved shortcuts, and any personalization changes disappear after they log off. Other users on the same machine are unaffected. What is the MOST likely cause and correct fix?

A) The user's profile is corrupted and Windows is loading a temporary profile; back up the user's data and create a new profile
B) Windows Update failed to install; run Windows Update troubleshooter
C) Malware has infected the system; disable System Restore and run a full scan
D) The hard drive is failing; run chkdsk and replace the drive if errors are found

---

**Q32.** A technician has already updated the anti-malware definitions and completed a full scan and removal of the infection (remediation step) as part of the standard malware removal process. Which step comes NEXT?

A) Educate the end user
B) Disable System Restore in Windows
C) Schedule scans and run updates
D) Quarantine the infected system

---

**Q33.** A technician has identified malware on a workstation, quarantined the system by disconnecting it from the network, and disabled System Restore. According to CompTIA best practice procedures, what should the technician do NEXT?

A) Update anti-malware software and scan the system
B) Educate the end user on how to avoid future infections
C) Re-enable System Restore and create a new restore point
D) Schedule automatic scans and run Windows Update

---

**Q34.** A user installed a new video card driver, and now the computer displays a blue screen of death referencing 'nvlddmkm.sys' every time Windows boots. Which of the following is the BEST first troubleshooting step?

A) Boot into Safe Mode and roll back the video driver
B) Reinstall Windows using an in-place upgrade
C) Replace the video card with a different manufacturer's model
D) Run chkdsk /f on the system drive

---

**Q35.** A Windows 11 workstation's Print Spooler service fails to start, and Event Viewer logs error 1053: 'The service did not respond to the start or control request in a timely fashion.' Which of the following is the BEST first step to resolve this issue?

A) Uninstall and reinstall the printer driver
B) Run System File Checker (sfc /scannow)
C) Verify the service's Log On As account and check dependent services in Services.msc
D) Disable the Windows Firewall

---

**Q36.** A user logs into Windows and receives a temporary profile instead of their normal profile, losing access to their desktop icons, files, and settings. Which of the following is the MOST likely cause?

A) The user's account has exceeded its storage quota
B) The computer is not joined to the domain
C) A recent Windows Update failed to install correctly
D) The user's local user profile has become corrupted

---

**Q37.** A technician plans to install a critical driver update on 50 production workstations during business hours next Monday. According to standard change management procedures, which document MUST be completed and approved BEFORE the technician begins the installation?

A) A change request that includes scope, risk analysis, rollback plan, and end-user acceptance
B) An incident report describing the current driver version
C) A knowledge base article documenting the driver's release notes
D) An asset inventory update listing the affected workstations

---

**Q38.** An employee's laptop is stolen from their car. The laptop contains unencrypted files with patient health records. Which action should the technician take FIRST according to proper incident response procedures?

A) Report the incident to the compliance/security officer for a formal investigation
B) Wipe the employee's domain account to prevent further access
C) Reimage a replacement laptop and reassign it to the employee
D) Purchase a new backup laptop with full-disk encryption enabled

---

**Q39.** A company wants a backup rotation scheme that keeps daily backups for two weeks, weekly backups for a month, and monthly backups for a year, minimizing the number of tapes needed while maintaining long-term recovery points. Which backup rotation scheme BEST fits this requirement?

A) Incremental-only backup scheme
B) Full backup every night with no rotation
C) Grandfather-Father-Son (GFS) rotation
D) Differential backup with a single retained copy

---

**Q40.** A technician downloads a PowerShell script from an internal repository but running it returns an error stating that script execution is disabled on the system. Which command should the technician run in an elevated PowerShell session to allow locally created and signed remote scripts to run?

A) Set-ExecutionPolicy RemoteSigned
B) Set-ExecutionPolicy Unrestricted
C) Enable-PSRemoting -Force
D) Set-ExecutionPolicy Bypass

---

**Q41.** A small business purchases a single retail copy of productivity software and installs it on five employee computers, believing this is allowed because they own the physical installation disc. Which licensing concept explains why this violates the software agreement?

A) Digital Rights Management (DRM) restricts the number of installs automatically
B) Open-source licensing requires attribution for each installed copy
C) The End User License Agreement (EULA) typically permits installation on only one device per license unless a volume/multi-seat license is purchased
D) Personal-use licenses automatically convert to enterprise licenses after three installations

---

**Q42.** A technician is about to open a desktop computer case to replace a failing power supply. Which action should be performed FIRST to protect the components from electrostatic discharge?

A) Ground yourself using an anti-static wrist strap connected to the chassis before touching internal components
B) Place the computer on a carpeted surface to insulate it from the floor
C) Turn on the room's air conditioning to increase static buildup control
D) Wear rubber-soled shoes to prevent any electrical contact with the case

---

**Q43.** A technician wants to upgrade the firmware on a critical file server that is currently in production. Before making the change, which document must be submitted and approved to minimize business impact and ensure proper rollback planning?

A) A change request
B) An incident report
C) A knowledge base article
D) An asset inventory update

---

**Q44.** A user reports that a script with a .vbs extension arrived as an unexpected email attachment and executed automatically, deleting several files on their system. Which characteristic of this file type made it a significant risk on this Windows system?

A) VBScript files can only run inside a sandboxed browser environment
B) VBScript files can be executed natively by the Windows Script Host without user compilation
C) VBScript files require administrator credentials to execute
D) VBScript files can only modify files within the user's Documents folder

---

**Q45.** A healthcare clinic's IT technician is troubleshooting a workstation that stores patient treatment records, diagnosis codes, and insurance claim numbers. Which classification of regulated data applies to this information?

A) PCI
B) GDPR
C) PHI
D) DRM

---

