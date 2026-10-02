## Chapter 4 Cheat Sheet — Security, Wireless Protocols & Authentication

### Wireless Encryption Comparison
| Standard | Cipher | Status |
|---|---|---|
| WEP | RC4 (static IV) | Broken — never use |
| WPA | TKIP | Deprecated — vulnerable |
| WPA2 | AES (CCMP) | Secure, but PSK vulnerable to offline dictionary attacks |
| WPA3 | AES (GCMP), SAE key exchange | Current standard — resists offline dictionary attacks |

**Rule of thumb:** AES/CCMP/GCMP = good. TKIP/RC4 = avoid.

### RADIUS vs TACACS+
| Feature | RADIUS | TACACS+ |
|---|---|---|
| Transport | UDP | TCP |
| Port(s) | 1812/1813 (legacy 1645/1646) | 49 |
| Encryption | Password only | Entire packet |
| AAA | Combines auth+authz | Separates auth, authz, accounting |
| Best use case | Network access (VPN, Wi-Fi, 802.1X) | Device administration (router/switch CLI, per-command logging) |
| Vendor | Open standard | Cisco proprietary |

### MFA Factor Categories
- **Something you know** — password, PIN, security question
- **Something you have** — smart card, hardware token, authenticator app
- **Something you are** — fingerprint, facial recognition, iris scan
- (Extended) Somewhere you are (geolocation), something you do (behavioral)

**Exam trap:** Two passwords ≠ MFA. Requires two *different* categories.

### Physical Security Controls
| Control | Purpose |
|---|---|
| Badge reader | Authenticates identity at entry point |
| Mantrap | Prevents tailgating — only one door open at a time |
| Cable lock | Deters physical theft of hardware |
| Biometric lock | Identity-based physical access control |

### Logical Security
- **ACLs** — restrict access at network/file level by user/group
- **Principle of least privilege** — grant only the minimum access required for the job function

### Device Hardening Checklist
1. Change default usernames/passwords immediately
2. Disable unused ports and services
3. Apply firmware/software updates from official vendor sources
4. Enable port security / 802.1X on active switch ports
5. Disable unnecessary protocols (e.g., Telnet — use SSH instead)

### Biometric Methods
Fingerprint, facial recognition, retina/iris scan, voice recognition — all fall under "something you are." Evaluated by false-accept rate (FAR) and false-reject rate (FRR).

### Common Exam Traps
- Choosing WPA2 when WPA3 is explicitly required for dictionary-attack resistance
- Confusing RADIUS (network access) with TACACS+ (device admin/command authorization)
- Assuming two knowledge factors (two passwords) qualify as MFA
- Selecting TKIP because it "sounds newer" than AES — TKIP is deprecated
- Forgetting that cable locks protect hardware, not data
