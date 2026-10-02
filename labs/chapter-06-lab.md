# Chapter 6 Lab: Windows Security Settings: Permissions, UAC, BitLocker/EFS, and Data Destruction

**Estimated time:** 25 minutes

## Exercise

On a test VM, set conflicting NTFS and Share permissions on a folder, access it from a mapped network drive to observe the effective (most restrictive) permission, then enable BitLocker on the same volume

## Key takeaway

Master the NTFS-vs-share precedence rule and know exactly when BitLocker (whole-disk) beats EFS (file-level) for a given security requirement.
