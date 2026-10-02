## Chapter 3: Installing Windows, Client Networking, and macOS/Linux Basics — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | FAT32 maximum single file size? | 4GB. Max volume size is 2TB (up to 8TB per spec, but Windows format tool limits to 32GB). Exam tip: FAT32 has no native permissions/encryption. |
| 2 | exFAT single file size limit? | No practical 4GB limit — designed for large files on flash media. No journaling, no built-in permissions/encryption. Exam tip: best choice for cross-platform USB drives >32GB. |
| 3 | NTFS max file size and key security features? | Max file size ~16TB (practical limit). Supports NTFS permissions (ACLs), EFS encryption, compression, and disk quotas. Exam tip: required for BitLocker and file-level security. |
| 4 | MBR partition limits | Max 4 primary partitions (or 3 primary + 1 extended). Max volume size 2TB. Requires legacy BIOS boot mode. Exam tip: use for older/legacy systems. |
| 5 | GPT partition limits | Up to 128 partitions in Windows. Max volume size 9.4ZB. Requires UEFI for native boot. Exam tip: GPT stores a backup partition table for redundancy, MBR does not. |
| 6 | Workgroup vs Domain — key difference? | Workgroup: peer-to-peer, local user accounts, recommended for small networks (~20 PCs or fewer). Domain: centralized authentication via Active Directory, requires a domain controller, supports Group Policy. |
| 7 | chmod 755 meaning? | Owner=rwx(7), Group=r-x(5), Others=r-x(5). Exam tip: memorize r=4, w=2, x=1 and add digits per user class. |
| 8 | What does 'sudo' do in Linux? | Executes a single command with elevated (root) privileges. Exam tip: required before commands that modify system files or install packages. |
| 9 | apt vs yum — when to use each? | apt = package manager for Debian/Ubuntu-based distros. yum = package manager for Red Hat/CentOS/Fedora-based distros. Exam tip: matching the manager to the distro family is heavily tested. |
| 10 | PXE boot requirements? | NIC with PXE support, a DHCP server, and a network boot/imaging server (e.g., WDS). Exam tip: used for imaging many machines simultaneously without physical media. |
| 11 | macOS Time Machine — what is it? | Built-in backup utility requiring an external or network drive; performs incremental backups. Exam tip: distinguish from Migration Assistant, which transfers data between Macs, not ongoing backup. |
| 12 | macOS Keychain — what does it store? | Saved passwords, Wi-Fi network keys, and certificates, accessible via Keychain Access. Exam tip: don't confuse with FileVault, which encrypts the entire disk. |
