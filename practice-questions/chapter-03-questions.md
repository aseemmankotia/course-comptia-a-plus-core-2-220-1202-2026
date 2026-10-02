## Chapter 3: Installing Windows, Client Networking, and macOS/Linux Basics — Practice Questions

**Q1.** A technician is deploying a new desktop with no optical drive and no network configured yet. The Windows ISO has already been written to a bootable flash drive. Which boot method should the technician use to start the installation?

A) PXE network boot
B) Optical media boot
C) External USB-attached hard drive boot
D) USB boot

<details>
<summary>Answer</summary>

**Correct: D**

The ISO is already on a flash drive and no network is configured, so booting directly from the USB drive is the only available and correct option.

**Why the others are wrong:**
- PXE requires a configured network, DHCP, and a boot server, none of which exist yet.
- There is no optical drive present on this machine.
- The image is on a USB flash drive, not an external USB hard drive with the OS pre-installed.

</details>

---

**Q2.** A remote employee needs to securely access internal file shares over the public internet using an encrypted tunnel to the corporate network. Which Windows feature should be configured on the laptop?

A) VPN connection
B) Proxy settings
C) Windows Firewall inbound rule
D) Homegroup sharing

<details>
<summary>Answer</summary>

**Correct: A**

A VPN connection creates an encrypted tunnel between the client and the corporate network, allowing secure remote access to internal resources.

**Why the others are wrong:**
- A proxy only routes/filters web traffic and does not provide an encrypted tunnel to internal resources.
- An inbound firewall rule controls traffic reaching the local machine, not remote network access.
- Homegroup was a Windows feature for local peer sharing and was removed from modern Windows; it does not provide remote WAN access.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A small office with 8 computers has no server and wants each user to log in with a local account while sharing a printer and a folder among the PCs. Which network model should be configured?

A) Active Directory domain
B) Cloud tenant (Azure AD/Entra ID)
C) RADIUS-authenticated network
D) Workgroup

<details>
<summary>Answer</summary>

**Correct: D**

A workgroup is a peer-to-peer model using local accounts on each machine, recommended for small networks (roughly up to 20 PCs) without centralized management.

**Why the others are wrong:**
- A domain requires a domain controller running Active Directory, which this office does not have.
- A cloud tenant requires an Entra ID subscription and internet-based identity management, unnecessary for 8 local PCs.
- RADIUS is used for centralized authentication on network devices/VPNs, not simple local file/printer sharing.

</details>

---

**Q4.** A user needs a file system for a USB flash drive that will store individual video files larger than 4GB and be readable on both Windows and macOS without installing extra drivers. Which file system should be used?

A) FAT32
B) NTFS
C) ext4
D) exFAT

<details>
<summary>Answer</summary>

**Correct: D**

exFAT has no practical 4GB file size limit, is natively readable/writable on both Windows and macOS, and is designed for flash media.

**Why the others are wrong:**
- FAT32 caps individual file size at 4GB, which fails for large video files.
- NTFS is writable on Windows but macOS only mounts it read-only by default without third-party drivers.
- ext4 is a Linux file system not natively supported by Windows or macOS.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A technician is partitioning a new SSD for a UEFI-based system that will require more than four partitions on a single drive. Which partition style should be selected?

A) MBR
B) APFS
C) exFAT
D) GPT

<details>
<summary>Answer</summary>

**Correct: D**

GPT supports up to 128 partitions in Windows and is required for native UEFI boot, satisfying both requirements.

**Why the others are wrong:**
- MBR is limited to four primary partitions (or three primary plus one extended) and pairs with legacy BIOS boot.
- APFS is a macOS file system, not a Windows-compatible partition style.
- exFAT is a file system, not a partition style/scheme.

</details>

---

**Q6.** A technician configures a workstation with a static IP address instead of DHCP. Which set of settings MUST be entered manually for the workstation to communicate on the network and internet correctly?

A) IP address and MAC address only
B) IP address, subnet mask, default gateway, and DNS server
C) Hostname and workgroup name only
D) Subnet mask and DHCP lease time

<details>
<summary>Answer</summary>

**Correct: B**

Static configuration requires the IP address, subnet mask, default gateway, and DNS server to be entered manually since DHCP will not supply them.

**Why the others are wrong:**
- The MAC address is burned into the NIC and is never manually assigned as part of IP configuration.
- Hostname and workgroup name do not provide network connectivity or routing information.
- DHCP lease time is irrelevant once a static address is configured, since DHCP is not being used.

</details>

---

**Q7.** On a Linux system, a technician runs 'chmod 755 script.sh'. What permissions does this assign?

A) Owner: read/write, Group: read, Others: none
B) Owner: read/write/execute, Group: read/execute, Others: read/execute
C) Owner: full control, Group: none, Others: read only
D) Owner: read only, Group: read/write, Others: execute

<details>
<summary>Answer</summary>

**Correct: B**

755 in octal notation translates to rwx (7) for owner, r-x (5) for group, and r-x (5) for others.

**Why the others are wrong:**
- This describes 640, not 755.
- This describes something closer to 704, not 755, and doesn't match the actual digit-to-permission mapping.
- This does not correspond to any correct decoding of the digits 7, 5, 5.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which statement correctly describes a key functional difference between NTFS and FAT32?

A) FAT32 supports file-level encryption while NTFS does not
B) NTFS supports file/folder permissions and encryption (EFS); FAT32 does not support either
C) FAT32 supports larger single file sizes than NTFS
D) NTFS cannot be used on internal hard drives, only external drives

<details>
<summary>Answer</summary>

**Correct: B**

NTFS supports NTFS permissions (ACLs), Encrypting File System (EFS), compression, and quotas; FAT32 lacks native security features entirely.

**Why the others are wrong:**
- FAT32 has no built-in encryption at all — this is reversed.
- FAT32 caps files at 4GB while NTFS supports files up to 16TB or more, so this is reversed.
- NTFS is the default and most common file system for internal Windows system drives.

</details>

---

