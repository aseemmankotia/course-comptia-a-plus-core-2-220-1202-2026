## Windows Edition Feature Matrix (Win10/11)

| Feature | Home | Pro | Enterprise | Pro for Workstations |
|---|---|---|---|---|
| BitLocker | No (Device Encryption only) | Yes | Yes | Yes |
| RDP Host (accept connections) | No (client only) | Yes | Yes | Yes |
| Group Policy Editor (gpedit.msc) | No | Yes | Yes | Yes |
| Domain Join | No | Yes | Yes | Yes |
| Hyper-V | No | Yes | Yes | Yes |
| Max CPU sockets | 1 | 2 | 2 | 4 |
| Max RAM | 128GB | 2TB | 2TB | 6TB |
| ReFS support | No | No | No | Yes |
| AppLocker / DirectAccess / Credential Guard | No | No | Yes | No |
| Licensing | Retail | Retail/Volume | Volume only | Retail/Volume |

## Control Panel → Settings App Mapping

| Control Panel Applet | Settings Equivalent |
|---|---|
| Programs and Features | Apps > Installed apps |
| Network and Sharing Center | Network & Internet |
| System | System > About |
| User Accounts | Accounts |
| Windows Defender Firewall | Privacy & Security > Windows Security > Firewall |
| Power Options | System > Power & battery |
| Ease of Access Center | Accessibility |
| **Backup and Restore (Win7)** | **No equivalent — Control Panel only** |
| **Mail (32-bit) applet** | **No equivalent — Control Panel only** |

## MMC Snap-ins (all inside Computer Management except noted)

| Tool | Command | Notes |
|---|---|---|
| Computer Management | compmgmt.msc | Container for Task Scheduler, Event Viewer, Shared Folders, Local Users/Groups, Device Manager, Disk Management, Services |
| Device Manager | devmgmt.msc | Available on all editions |
| Disk Management | diskmgmt.msc | Initialize, partition, format, assign drive letter/mount point |
| Services | services.msc | Start types: Automatic, Automatic (Delayed), Manual, Disabled |
| Task Scheduler | taskschd.msc | Triggers: logon, startup, schedule, event |
| Local Users and Groups | lusrmgr.msc | **Not on Home edition** |
| Local Security Policy | secpol.msc | **Not on Home edition** |

## Disk Partitioning Limits

| Style | Max Partitions | Max Size |
|---|---|---|
| MBR | 4 primary (or 3+extended) | 2TB per partition |
| GPT | 128 | Up to 256TB (NTFS practical limit) |

| File System | Max File Size | Notes |
|---|---|---|
| FAT32 | 4GB | Volume format limit ~32GB in Windows |
| exFAT | No practical limit | Used for flash/USB media |
| NTFS | 16TB default, up to 256TB | Default for Windows installs |

## msconfig Tabs

| Tab | Purpose |
|---|---|
| General | Normal / Diagnostic / Selective startup |
| Boot | Safe boot options, boot log, base video, timeout |
| Services | Hide all Microsoft services checkbox, enable/disable |
| Startup | Launches Task Manager's Startup tab (Win10/11) |
| Tools | Quick-launch shortcuts to admin tools (e.g., secpol, gpedit) |

## Task Manager Tabs

Processes (end task, resource usage) · Performance (real-time graphs) · App history · Startup (enable/disable/impact rating) · Users (sessions) · Details (priority, affinity, PID) · Services (start/stop, opens services.msc)
