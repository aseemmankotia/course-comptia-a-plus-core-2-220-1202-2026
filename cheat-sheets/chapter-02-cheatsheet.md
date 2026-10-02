## Chapter 2 Cheat Sheet: CLI Diagnostics & Networking

### Network Diagnostic Commands
| Command | Purpose | Key Switches |
|---|---|---|
| `ipconfig` | Show basic IP config | `/all` full details, `/release` drop lease, `/renew` get new lease, `/flushdns` clear DNS cache |
| `ping` | Test reachability/latency | `-t` continuous, `-n <count>` set count, `-4`/`-6` force protocol |
| `netstat` | Show connections/ports | `-a` all, `-n` numeric (no DNS), `-b` show owning executable, `-o` show PID |
| `nslookup` | Query DNS records | Interactive mode; `-type=MX` for mail records |

### ipconfig Lease Workflow
1. `ipconfig /release` → adapter shows 0.0.0.0
2. `ipconfig /renew` → requests fresh DHCP lease
**Exam trap:** APIPA address (169.254.x.x) = DHCP unreachable, NOT a DNS problem.

### Disk & System Integrity
| Command | Fixes | Requires |
|---|---|---|
| `sfc /scannow` | Corrupted/missing protected system files | Elevation |
| `chkdsk /f` | Logical file system errors | Elevation; may need reboot on system drive |
| `chkdsk /f /r` | File system errors + bad sector scan/recovery | Elevation; longest run time |
**Rule of thumb:** App crashes / missing DLLs → `sfc`. Disk errors / bad sectors / delayed write failures → `chkdsk`.

### Group Policy Commands
| Command | Purpose |
|---|---|
| `gpupdate /force` | Re-applies ALL GPOs immediately |
| `gpresult /r` | Reports which GPOs are currently applied (RSoP) — diagnostic only |
**Exam trap:** `gpresult` does NOT change anything; `gpupdate` does not report current state.

### File & Drive Management
| Command | Purpose |
|---|---|
| `net use Z: \\Server\Share` | Map network drive |
| `net use Z: /delete` | Disconnect mapped drive |
| `net use * /delete` | Disconnect ALL mapped drives |
| `robocopy src dst /mir` | Mirror folders (deletes extra dest files!) |
| `robocopy src dst /z` | Restartable copy mode |

### Shell Comparison
| Shell | Type | Scripting |
|---|---|---|
| Command Prompt | Legacy shell | Batch files (.bat) only |
| PowerShell | Cmdlet-based shell | Object pipelines, .ps1 scripts, can run cmd commands too |
| Windows Terminal | Host application (not a shell) | Runs cmd, PowerShell, WSL in tabs |

### Elevation
Run as Administrator required for: `sfc /scannow`, `chkdsk /f` (system drive), `diskpart`, most Group Policy and system-level changes. Use right-click → Run as administrator, or `Ctrl+Shift+Enter` from Start search.
