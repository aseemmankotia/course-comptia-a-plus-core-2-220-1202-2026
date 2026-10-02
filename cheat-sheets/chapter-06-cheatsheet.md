# Chapter 6 Cheat Sheet: Windows Security Settings

## NTFS Permissions (granular, local + network)
| Permission | Capability |
|---|---|
| Read | View file/folder contents |
| Read & Execute | Read + run executables |
| Write | Create/modify files |
| Modify | Read & Execute + Write + Delete |
| Full Control | Modify + change permissions + take ownership |

## Share Permissions (network only, coarse)
| Permission | Capability |
|---|---|
| Read | View/open files over network |
| Change | Read + edit/delete over network |
| Full Control | Change + modify permissions |

## Combined Permission Rule
**Network access = MOST RESTRICTIVE of (NTFS permission) vs (Share permission).**
Local access = NTFS permission only (Share permission ignored).

## Copy/Move Inheritance Rules
| Action | Same Volume | Different Volume |
|---|---|---|
| Copy | Inherits destination permissions | Inherits destination permissions |
| Move | Retains original permissions | Inherits destination permissions (treated as copy) |

## UAC Levels (high to low)
1. Always notify (prompts for user AND program changes, dims desktop)
2. Notify only for app changes (DEFAULT, dims desktop)
3. Notify only for app changes (no dim)
4. Never notify (not recommended)

Standard account = always prompted for admin credentials on elevation.
Administrator account = simple consent prompt (Yes/No), no credentials needed.

## BitLocker vs EFS
| Feature | BitLocker | EFS |
|---|---|---|
| Scope | Whole volume | Individual file/folder |
| Key storage | TPM 1.2+/2.0 or USB key | User certificate/private key |
| Protects against | Physical theft, offline access | Other local users on shared PC |
| Filesystem requirement | Any (volume-level) | NTFS only |
| Recovery | Recovery key | Exported certificate/key backup |

## Windows Defender Firewall Profiles
- **Domain** – AD-managed network, moderate rules
- **Private** – trusted home/work network, moderate rules, discovery enabled
- **Public** – untrusted network (coffee shop, airport), most restrictive, discovery disabled

## SOHO Hardening Checklist (priority order)
1. Change default admin username/password
2. Update firmware
3. Enable WPA2/WPA3 encryption
4. Disable WPS
5. Disable SSID broadcast (minor obscurity only)
6. Enable MAC filtering (weak, bypassable control)
7. Disable unused ports/UPnP

## Data Destruction Methods
| Method | Works On | Notes |
|---|---|---|
| Standard Format | HDD/SSD | Data recoverable with tools — NOT secure |
| Low-level Format/Wipe | HDD | Overwrites data (multiple passes historically referenced, e.g. DoD 5220.22-M) |
| Degaussing | HDD/tape ONLY | Ineffective on SSD (no magnetic storage) |
| ATA Secure Erase / Crypto-Erase | SSD | Recommended secure method for SSDs |
| Physical Destruction (shred/drill) | Any | Most certain method; irreversible |
| Certificate of Destruction | Any | Compliance/audit documentation |

**Exam Gotchas:**
- Network share access = most restrictive wins (not additive).
- Same-volume MOVE is the one case that keeps original permissions.
- Degaussing ≠ effective for SSDs.
- BitLocker ≠ file-level; EFS ≠ whole-disk.
