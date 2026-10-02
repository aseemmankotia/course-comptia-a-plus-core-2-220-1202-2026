## Chapter 7: Troubleshooting Windows Boot, Performance, and Application Issues — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | WinRE key combination to access Advanced Startup Options during boot | Hold Shift while clicking Restart, or interrupt boot 3 times to trigger Automatic Repair environment. Exam tip: F8 no longer works by default on modern Windows (fast startup disables it). |
| 2 | Command to rebuild the Boot Configuration Data (BCD) from WinRE Command Prompt | bootrec /rebuildbcd — scans for Windows installations and rebuilds BCD. Related: bootrec /fixmbr (repairs MBR) and bootrec /fixboot (writes new boot sector). |
| 3 | Command to check and repair protected system files | sfc /scannow — scans all protected system files, replaces corrupted ones from cache. Exam tip: run in elevated Command Prompt; if it can't fix files, follow with DISM. |
| 4 | DISM command to repair the Windows system image before running SFC | DISM /Online /Cleanup-Image /RestoreHealth — repairs the component store SFC pulls files from. Exam tip: run DISM first if SFC reports it 'could not fix some files.' |
| 5 | Where to view minidump-related BSOD crash events on a running Windows system | Event Viewer > Windows Logs > System, filtered for Error level events (e.g., Event ID 1001 BugCheck). Exam tip: Reliability Monitor gives a visual timeline; Event Viewer gives raw detail. |
| 6 | Tool that shows a historical stability index (1-10) graphing crashes over time | Reliability Monitor (perfmon /rel). Exam tip: use it to correlate a new problem's start date with a driver install or update. |
| 7 | Task Manager vs Resource Monitor — which shows per-thread/per-handle detail? | Resource Monitor. Task Manager shows overall process resource usage; Resource Monitor drills into threads, handles, and network connections per process. |
| 8 | Symptom: user logs in and sees 'You have been logged on with a temporary profile' — root cause? | Windows failed to load the existing user profile (registry ProfileList corruption or profile folder access issue). Fix: rename the .bak/corrupted profile key and folder, then reboot. |
| 9 | Service fails to start with 'dependency service does not exist' error — where to check? | Services.msc > right-click service > Properties > Dependencies tab. Shows required services and dependent services. |
| 10 | Which WinRE Advanced Option specifically removes a bad Windows Update without reinstalling the OS? | Uninstall Updates (choose Latest Quality Update or Latest Feature Update). Less destructive than System Restore or Reset this PC. |
| 11 | Difference between Startup Repair and System Restore in WinRE | Startup Repair automatically diagnoses/fixes boot files, BCD, and boot sector issues. System Restore reverts system files/settings/registry to an earlier restore point — does not fix boot files directly. |
| 12 | Safe Mode with Command Prompt vs Safe Mode vs Safe Mode with Networking | All three load minimal drivers/services. Safe Mode = GUI, no network. Safe Mode with Networking = GUI + network drivers. Safe Mode with Command Prompt = CLI only, no GUI shell (explorer.exe not loaded). |
