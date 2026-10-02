## Chapter 3 Cheat Sheet — Installation, Networking, macOS/Linux

### File Systems
| FS | Max File Size | Security | Best Use |
|---|---|---|---|
| FAT32 | 4GB | None | Legacy compatibility, small USB drives |
| exFAT | No practical limit | None | Cross-platform USB/flash drives >32GB |
| NTFS | ~16TB | ACL permissions, EFS encryption, compression, quotas | Windows internal drives, BitLocker |

### Partition Styles
| Style | Max Partitions | Max Volume | Boot Mode |
|---|---|---|---|
| MBR | 4 primary (3+1 extended) | 2TB | Legacy BIOS |
| GPT | 128 (Windows) | 9.4ZB | UEFI (redundant partition table) |

### Boot Methods
- **USB**: bootable flash drive, fastest for single-machine installs
- **PXE**: requires PXE-capable NIC + DHCP + network boot server (WDS); used for mass imaging
- **Optical media**: DVD/CD, legacy method
- **External USB drive**: full OS image pre-loaded, used for recovery/deployment

### Upgrade vs Clean Install
- **Upgrade**: keeps apps/files/settings; requires compatible existing OS
- **Clean install**: wipes drive, requires backup first; use when changing architecture, fixing corruption, or repartitioning

### Workgroup vs Domain
| | Workgroup | Domain |
|---|---|---|
| Accounts | Local, per-PC | Centralized (AD) |
| Scale | ~20 PCs or fewer | Enterprise |
| Management | Manual per machine | Group Policy |

### Client Network Config
- **DHCP**: automatic IP/subnet/gateway/DNS, lease-based
- **Static**: manually set IP, subnet mask, gateway, DNS
- **VPN**: Settings > Network & Internet > VPN; protocols include L2TP/IPsec, SSTP, IKEv2
- **Proxy**: Settings > Network & Internet > Proxy; manual (address/port) or automatic (PAC script)

### macOS Essentials
- **Finder**: file management GUI
- **Time Machine**: incremental backup to external/network drive
- **Keychain**: stores saved passwords, Wi-Fi keys, certificates
- Terminal: `ls`, `cd`, `pwd`, `cp`, `mv`, `sudo`, `top`, `chmod`

### Linux Essentials
- `ls` – list files; `cd` – change directory
- `chmod [octal] file` – set permissions (r=4,w=2,x=1)
- `sudo` – elevate privileges for one command
- `apt` – Debian/Ubuntu package manager; `yum` – Red Hat/CentOS/Fedora package manager
- Filesystem layout: `/` root, `/home` user data, `/etc` config files, `/var` logs/variable data, `/bin` binaries, `/boot` boot files, `/mnt`/`/media` mount points
