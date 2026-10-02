## Chapter 5 Cheat Sheet: Malware, Social Engineering & Detection

### Malware Types — Quick ID
| Type | Self-Replicates? | Needs Host/User Action? | Key Symptom |
|---|---|---|---|
| Virus | Yes | Yes (host file + user runs it) | File corruption, spreads via sharing |
| Worm | Yes | No | Rapid network spread, no user action needed |
| Trojan | No | Yes (disguised as legit app) | Unexpected behavior after install |
| Ransomware | No | Varies | Files encrypted, ransom note |
| Rootkit | No | No (hides post-infection) | No visible symptoms; hides from OS-level scans |
| Keylogger | No | Varies | Compromised credentials, no slowdown |
| Spyware | No | Varies | Unwanted tracking, popups, browser changes |
| Botnet/Zombie | No (member of network) | No | High outbound traffic, remote control |

### Social Engineering — Quick ID
| Attack | Vector | Target Scope |
|---|---|---|
| Phishing | Email | Mass/generic |
| Spear Phishing | Email | Specific individual/group |
| Whaling | Email | Executives/high-value (CEO/CFO) |
| Vishing | Phone call | Any target |
| Shoulder Surfing | Physical observation | Screen/keystrokes |
| Tailgating | Physical entry | Following authorized person |
| Dumpster Diving | Physical trash search | Discarded documents |

### Detection & Response
- **Rootkits**: require offline/boot-time scans (Microsoft Defender Offline) since they hide from the running OS.
- **Rogue AV/Scareware**: fake pop-up claims infection, demands payment — legitimate AV never asks for payment via browser pop-up.
- **Zero-day**: vulnerability with no patch yet; exploited before vendor awareness.
- **Non-compliant system**: violates security policy (e.g., missing patches, disabled AV).

### Windows Defender (Microsoft Defender Antivirus) Commands
| Task | PowerShell Command |
|---|---|
| Quick scan | `Start-MpScan -ScanType QuickScan` |
| Full scan | `Start-MpScan -ScanType FullScan` |
| Update signatures | `Update-MpSignature` |
| View detected threats | `Get-MpThreat` |
| CLI alternative | `MpCmdRun.exe -Scan -ScanType 2` (full scan) |

### Exam Traps
- Confusing **spear phishing** (targeted individual) with **whaling** (targeted executive) — whaling is a *subset* of spear phishing.
- Assuming rootkits are 'loud' like ransomware — they are designed to be silent and undetected.
- Believing quick/full scans from within Windows can catch rootkits — they often cannot; offline scan is required.
- Mistaking a zombie for malware itself — a zombie is an infected *host*, not the malware.
