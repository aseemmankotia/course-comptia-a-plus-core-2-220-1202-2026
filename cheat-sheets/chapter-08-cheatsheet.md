## Chapter 8 Cheat Sheet: Malware Removal & Mobile OS Troubleshooting

### The 7-Step Malware Removal Process (MEMORIZE ORDER)

| Step | Action | Key Detail |
|---|---|---|
| 1 | Investigate and verify malware symptoms | Rule out hardware/driver causes first |
| 2 | Quarantine the infected system | Disconnect network cable / disable Wi-Fi |
| 3 | Disable System Restore (Windows) | Prevents malware from being saved to a restore point |
| 4 | Remediate the infected system | Update anti-malware signatures, run full scan |
| 5 | Schedule scans and run updates | Set up recurring protection, OS/AV updates |
| 6 | Re-enable System Restore & create a restore point | Only after confirmed clean |
| 7 | Educate the end user | Safe browsing, phishing awareness, prevent recurrence |

**Memory trick:** "I Quit Dieting, Remembering Scheduled Restore Education" = Investigate, Quarantine, Disable, Remediate, Schedule, Restore(enable), Educate.

### Exam Traps
- Disabling System Restore happens **before** remediation, never after.
- Re-enabling System Restore + creating a restore point is **Step 6**, not Step 4 or 5.
- Quarantine (Step 2) always precedes disabling System Restore (Step 3) — don't touch settings on a machine still connected to the network.
- Step 5 (scheduling scans/updates) comes before Step 6 (re-enable restore) — commonly swapped on exam.

### Key Windows Commands

| Task | Command / Location |
|---|---|
| Disable System Restore | Control Panel > System Protection > Configure > Disable, or `Disable-ComputerRestore -Drive 'C:\'` |
| Enable System Restore | Control Panel > System Protection > Configure > Turn on protection, or `Enable-ComputerRestore -Drive 'C:\'` |
| Create restore point | System Protection > Create, or `Checkpoint-Computer -Description 'name'` |

### Common Mobile OS Issues & First Troubleshooting Step

| Symptom | First Action |
|---|---|
| App crashes | Force-stop and reopen; clear cache/data |
| Battery drain | Check per-app battery usage stats |
| Unresponsive touchscreen | Reboot; check for stuck app or screen protector interference |
| Unauthorized data usage | Check Settings > Data Usage per app; look for rogue/adware app |

### Quick Reference: Why Order Matters
- **Quarantine before Disable Restore:** stop spread first, then adjust local settings safely.
- **Disable before Remediate:** avoid saving infected state to a restore point during cleanup.
- **Schedule before Re-enable:** ensure ongoing protection is active before snapshotting the clean state.
- **Educate last:** only makes sense once the system is fully clean and stable.
