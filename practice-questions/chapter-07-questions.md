## Chapter 7: Troubleshooting Windows Boot, Performance, and Application Issues — Practice Questions

**Q1.** A technician installs a new video card driver, and on next boot the computer displays a BSOD referencing the display driver file. The system boots fine when the display adapter falls back to the default driver. Which action should the technician take FIRST to resolve this?

A) Boot into Safe Mode and roll back the driver in Device Manager
B) Perform a clean install of Windows
C) Run Startup Repair from WinRE
D) Replace the video card with new hardware

<details>
<summary>Answer</summary>

**Correct: A**

A BSOD tied to a specific driver file after an update is a classic driver conflict; Safe Mode loads minimal drivers, allowing Device Manager rollback without triggering the faulty driver.

**Why the others are wrong:**
- A clean install is destructive and unnecessary for a known driver-specific fault
- Startup Repair targets boot configuration/file corruption, not driver conflicts
- Hardware replacement is not indicated since the error is software/driver-based, not a hardware failure

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A desktop displays 'Boot Device Not Found' immediately after POST, and no OS selection menu appears. The user says nothing was changed recently. Which is the BEST first troubleshooting step?

A) Reinstall Windows from recovery media
B) Run bootrec /rebuildbcd from WinRE
C) Check BIOS/UEFI boot order and verify the drive is detected
D) Replace the motherboard

<details>
<summary>Answer</summary>

**Correct: C**

Boot Device Not Found is a firmware-level message indicating the BIOS/UEFI cannot detect a bootable drive; confirming the drive is recognized and boot order is correct is the least invasive first step.

**Why the others are wrong:**
- Reinstalling is premature before confirming the drive is even detected
- bootrec assumes the drive is detected and Windows partitions exist, which hasn't been confirmed yet
- Motherboard replacement is an extreme, unsupported first action

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A service configured to start automatically fails with the error 'The dependency service does not exist or has been marked for deletion.' Where should the technician check to identify the required dependency?

A) Task Manager Startup tab
B) Event Viewer Security log
C) Services.msc, Dependencies tab of the failing service's Properties
D) Device Manager

<details>
<summary>Answer</summary>

**Correct: C**

The Dependencies tab in a service's Properties dialog lists which services it depends on and which depend on it, directly identifying the missing dependency.

**Why the others are wrong:**
- Task Manager's Startup tab manages login apps, not Windows services
- The Security log tracks auditing events, not service dependency configuration
- Device Manager manages hardware drivers, not Windows services

</details>

---

**Q4.** A user reports intermittent system freezes over the past week. Which built-in tool provides a timeline view correlating application crashes, Windows updates, and hardware failures to help pinpoint when the problem started?

A) Resource Monitor
B) Task Manager
C) Reliability Monitor
D) Performance Monitor

<details>
<summary>Answer</summary>

**Correct: C**

Reliability Monitor displays a chronological stability index graph with icons for application failures, Windows failures, and miscellaneous failures, ideal for correlating a problem's onset with recent changes.

**Why the others are wrong:**
- Resource Monitor shows real-time resource usage, not historical stability trends
- Task Manager shows current running processes and resource use, not a historical timeline
- Performance Monitor tracks performance counters over time but doesn't summarize stability events in an easy timeline

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A user's CPU usage sits at 100% even when no applications are open. Which tool BEST identifies exactly which process and thread is consuming the CPU cycles?

A) Event Viewer
B) System Configuration (msconfig)
C) Resource Monitor
D) Disk Management

<details>
<summary>Answer</summary>

**Correct: C**

Resource Monitor provides granular per-process, per-thread CPU, disk, network, and memory data, useful for pinpointing the exact source of resource bottlenecks beyond what Task Manager shows.

**Why the others are wrong:**
- Event Viewer logs system/application events, not live resource consumption
- msconfig controls startup and boot options, not real-time resource monitoring
- Disk Management manages partitions and volumes, unrelated to CPU diagnostics

</details>

---

**Q6.** A user logs in and finds a plain desktop background, missing personal files, and default settings, despite normal login credentials. Windows shows 'You have been logged on with a temporary profile.' What is the recommended fix?

A) Reinstall Windows
B) Restore from a system image backup
C) Run chkdsk /f on the system drive
D) Log off, rename the corrupted profile folder and matching registry key, then restart

<details>
<summary>Answer</summary>

**Correct: D**

A temporary profile indicates Windows failed to load the real user profile due to registry or file corruption; renaming the corrupted profile folder and correcting the ProfileList registry key (removing the .bak suffix conflict) resolves this without a full rebuild.

**Why the others are wrong:**
- Reinstalling Windows is unnecessary for a single corrupted user profile
- A full system restore is overkill and may lose unrelated recent data
- chkdsk checks disk integrity, not profile/registry corruption

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** After a failed Windows Update leaves the system unable to boot normally, which WinRE option is specifically designed to remove the problematic update and revert the OS?

A) Startup Repair
B) System Restore
C) Uninstall Updates
D) Reset this PC

<details>
<summary>Answer</summary>

**Correct: C**

WinRE's 'Uninstall Updates' option under Advanced Options is purpose-built to remove the latest quality or feature update causing boot failure.

**Why the others are wrong:**
- Startup Repair fixes boot configuration issues but doesn't specifically target update rollback
- System Restore reverts to a restore point but may not exist or may remove more changes than necessary
- Reset this PC is a much more drastic option that reinstalls Windows and can remove apps/data

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the primary functional difference between booting into 'Safe Mode' versus 'Safe Mode with Networking'?

A) Safe Mode with Networking loads all third-party drivers, while Safe Mode does not
B) Safe Mode with Networking additionally loads network drivers and services needed for internet/network access
C) Safe Mode disables the mouse and keyboard, while Safe Mode with Networking enables them
D) Safe Mode with Networking boots into the full GUI, while Safe Mode boots into a command prompt only

<details>
<summary>Answer</summary>

**Correct: B**

Both modes load only essential drivers and services; Safe Mode with Networking adds the network drivers/services on top of the standard Safe Mode minimal environment.

**Why the others are wrong:**
- Neither Safe Mode variant loads third-party or non-essential drivers
- Both Safe Mode variants support mouse and keyboard input
- Both boot into the GUI; a separate option, Safe Mode with Command Prompt, provides CLI-only access

</details>

---

