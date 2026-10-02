## Chapter 1: Windows Editions, Features, and Core Administrative Tools — Practice Questions

**Q1.** A small business has 15 desktops running Windows 11 Home and wants to join them to an on-premises Active Directory domain. What is the BEST solution?

A) Use Settings > Accounts > Access work or school to join the domain
B) Upgrade the desktops to Windows 11 Pro
C) Install the Hyper-V feature on each desktop
D) Reinstall Windows 11 Home and enable Group Policy from Control Panel

<details>
<summary>Answer</summary>

**Correct: B**

Windows 11 Home cannot join a traditional AD domain — that capability starts at Pro. Upgrading the edition (via Settings > Activation using a Pro key, or a clean install) enables domain join, Group Policy, and BitLocker.

**Why the others are wrong:**
- Home's Accounts settings only support Azure AD 'work or school' add, not classic AD domain join — the option doesn't exist on Home
- Hyper-V is unrelated to domain join capability and also isn't available on Home
- gpedit.msc (Group Policy Editor) is not included in Home regardless of Control Panel access

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A CAD workstation requires the ReFS file system and needs to support 4 physical CPU sockets with up to 6TB of RAM. Which Windows edition should be installed?

A) Windows 11 Pro
B) Windows 11 Enterprise
C) Windows 11 Pro for Workstations
D) Windows 11 Home

<details>
<summary>Answer</summary>

**Correct: C**

Pro for Workstations is the only edition that adds ReFS support, persistent memory support, and raises hardware limits to 4 physical CPUs and 6TB RAM.

**Why the others are wrong:**
- Pro supports only 2 physical CPUs and up to 2TB RAM, and does not include ReFS
- Enterprise matches Pro's hardware limits (2 CPUs/2TB RAM) and is volume-license only — it does not add ReFS or the higher hardware ceiling
- Home is limited to 1 CPU and 128GB RAM and lacks ReFS entirely

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A technician wiped a 4TB drive and now needs to convert it from MBR to GPT before creating a new volume. Which tool provides a direct, single-purpose interface for this task?

A) Disk Management
B) Device Manager
C) Task Scheduler
D) Local Security Policy

<details>
<summary>Answer</summary>

**Correct: A**

Disk Management (diskmgmt.msc) is used to initialize disks, choose MBR/GPT, create partitions, format volumes, and assign drive letters or mount points.

**Why the others are wrong:**
- Device Manager manages hardware drivers and resources, not disk partitioning
- Task Scheduler automates programs/scripts on triggers and has no disk management function
- Local Security Policy configures password/audit/user rights policy, unrelated to disks

</details>

---

**Q4.** A technician troubleshooting a slow boot wants msconfig to display only non-Microsoft services so they can be safely disabled for testing. Which action accomplishes this?

A) On the General tab, select Diagnostic startup
B) On the Boot tab, enable Boot log
C) On the Startup tab, click Open Task Manager
D) On the Services tab, check 'Hide all Microsoft services'

<details>
<summary>Answer</summary>

**Correct: D**

The Services tab's 'Hide all Microsoft services' checkbox filters the list down to third-party services only, making it safe to disable them without risking core OS services.

**Why the others are wrong:**
- Diagnostic startup loads only basic devices/services automatically but does not give a filtered manual list to review
- Boot log records driver load info during startup to a text file — it doesn't filter the services list
- The Startup tab in modern msconfig only links out to Task Manager's Startup tab and has no service-hiding function

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which MMC snap-in is NOT available on a default installation of Windows 11 Home?

A) Device Manager (devmgmt.msc)
B) Disk Management (diskmgmt.msc)
C) Local Security Policy (secpol.msc)
D) Task Scheduler (taskschd.msc)

<details>
<summary>Answer</summary>

**Correct: C**

secpol.msc is removed from Windows Home editions along with gpedit.msc, since Home lacks the underlying Group Policy engine.

**Why the others are wrong:**
- Device Manager ships on all editions including Home
- Disk Management ships on all editions including Home
- Task Scheduler ships on all editions including Home

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A user reports an unfamiliar program launches every time they log in, but it does not appear in the Startup tab of Task Manager. Where should the technician look next to find what is triggering it?

A) Local Users and Groups
B) Device Manager
C) Task Scheduler
D) Local Security Policy

<details>
<summary>Answer</summary>

**Correct: C**

Task Manager's Startup tab only shows items in the Run registry keys and Startup folder. Logon-triggered scheduled tasks are configured in Task Scheduler and won't appear there.

**Why the others are wrong:**
- Local Users and Groups manages account/group membership, not what programs execute
- Device Manager manages hardware and drivers, not program execution triggers
- Local Security Policy manages permissions/policies, not startup execution

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which legacy Control Panel applet has NO equivalent page in the modern Settings app as of Windows 11?

A) Programs and Features
B) Power Options
C) Network and Sharing Center
D) Backup and Restore (Windows 7)

<details>
<summary>Answer</summary>

**Correct: D**

Backup and Restore (Windows 7) remains a Control Panel-only legacy tool; Settings > System > Backup uses File History/OneDrive instead and does not replicate this applet's functionality.

**Why the others are wrong:**
- Programs and Features maps to Settings > Apps > Installed apps
- Power Options maps to Settings > System > Power & battery
- Network and Sharing Center maps to Settings > Network & Internet

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** In Task Manager, which tab allows a technician to manually set a process's CPU affinity to limit it to specific cores?

A) Performance
B) Services
C) Details
D) Users

<details>
<summary>Answer</summary>

**Correct: C**

Right-clicking a process on the Details tab exposes 'Set affinity' and 'Set priority,' letting the technician restrict which CPU cores a process can use.

**Why the others are wrong:**
- Performance shows real-time graphs of CPU/RAM/disk/network usage, with no per-process controls
- Services lists Windows services and lets you start/stop them, but not set CPU affinity
- Users shows logged-on sessions and lets you disconnect/sign off users, not configure process affinity

</details>

---

