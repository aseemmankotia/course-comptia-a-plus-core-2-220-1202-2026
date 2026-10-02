## Chapter 7 Cheat Sheet: Windows Boot, Performance & App Troubleshooting

### BSOD Troubleshooting Workflow
1. Note stop code / driver filename on screen
2. Boot to Safe Mode if system won't boot normally
3. Check **Event Viewer > Windows Logs > System** (Error level, BugCheck events)
4. Check **Reliability Monitor** (`perfmon /rel`) for timeline correlation with recent updates/driver installs
5. Roll back driver in Device Manager, or uninstall recent update
6. If file corruption suspected: `sfc /scannow` → `DISM /Online /Cleanup-Image /RestoreHealth`

### Boot Failure Symptoms & Fixes
| Symptom | Likely Cause | Fix |
|---|---|---|
| "Boot Device Not Found" | Drive not detected by firmware | Check BIOS/UEFI boot order, cabling, drive health |
| Missing OS / "No bootable device" | Corrupt/missing BCD or boot sector | WinRE: `bootrec /fixmbr`, `/fixboot`, `/rebuildbcd` |
| Boot loop after update | Bad update | WinRE > Advanced Options > Uninstall Updates |
| Won't boot, no obvious error | Corrupt boot files | WinRE > Startup Repair |

### Key WinRE Command Prompt Tools
| Command | Purpose |
|---|---|
| `bootrec /fixmbr` | Repairs Master Boot Record |
| `bootrec /fixboot` | Writes new boot sector |
| `bootrec /rebuildbcd` | Rescans and rebuilds BCD |
| `sfc /scannow` | Repairs protected system files |
| `DISM /Online /Cleanup-Image /RestoreHealth` | Repairs component store used by SFC |
| `chkdsk /f /r` | Checks/repairs disk errors |

### Diagnosing Resource Bottlenecks
| Tool | Best For |
|---|---|
| Task Manager | Quick overview: CPU/RAM/Disk/Network per process, startup impact |
| Resource Monitor | Deep dive: per-thread, per-handle, per-connection detail |
| Reliability Monitor | Historical stability timeline, crash correlation |
| Event Viewer | Raw log detail (System/Application/Security logs) |

### Services Not Starting
- **Services.msc** > right-click service > Properties
  - **General tab**: Startup type (Automatic, Automatic Delayed, Manual, Disabled), Start/Stop buttons
  - **Dependencies tab**: shows required and dependent services
  - **Log On tab**: verify correct service account and permissions
- Common error "dependency service does not exist or marked for deletion" → check Dependencies tab, ensure dependent service isn't disabled

### Profile Issues
| Issue | Sign | Fix |
|---|---|---|
| Corrupted profile | Slow logon, missing settings, errors on load | Boot Safe Mode, back up data, delete/rebuild profile via System Properties > User Profiles |
| Temporary profile | "logged on with a temporary profile" banner, blank desktop | Rename corrupted key/folder in `HKLM\...\ProfileList` and matching `C:\Users\<name>.bak` folder, reboot |

### Safe Mode / WinRE Access
- Interrupt boot 3x → Automatic Repair → Advanced Options
- Settings > Update & Security > Recovery > Advanced startup > Restart now
- `msconfig` > Boot tab > Safe boot (for repeated Safe Mode access)

### WinRE Advanced Options Summary
| Option | Use Case |
|---|---|
| Startup Repair | Fix boot configuration automatically |
| System Restore | Revert system state to restore point |
| Uninstall Updates | Remove bad quality/feature update |
| Command Prompt | Manual bootrec/sfc/DISM commands |
| Safe Mode | Minimal driver boot for troubleshooting |
| Reset this PC | Last resort — reinstall OS, optionally keep files |

**Exam Note:** Always try the LEAST destructive fix first — Startup Repair/Uninstall Updates before System Restore before Reset this PC before full reinstall.
