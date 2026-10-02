## Chapter 4: Security Measures, Wireless Protocols, and Authentication — Practice Questions

**Q1.** A data center wants to prevent an unauthorized person from following an authorized employee through a secure entrance. Which physical control BEST addresses this?

A) Mantrap
B) Cable lock
C) Badge reader
D) Biometric lock

<details>
<summary>Answer</summary>

**Correct: A**

A mantrap uses two interlocking doors so only one person (and one door) can pass at a time, directly preventing tailgating.

**Why the others are wrong:**
- Cable locks secure equipment from theft, not entry points.
- A badge reader authenticates entry but does not stop a second person from following through an open door.
- A biometric lock authenticates identity but, like a badge reader alone, doesn't physically prevent tailgating.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A network administrator needs to authenticate technicians logging into router and switch CLIs, and wants to log every individual command each technician issues for auditing. Which authentication protocol should be used?

A) TACACS+
B) RADIUS
C) Kerberos
D) LDAP

<details>
<summary>Answer</summary>

**Correct: A**

TACACS+ separates authentication, authorization, and accounting, and can authorize/log at the command level — ideal for network device administration.

**Why the others are wrong:**
- RADIUS is designed for network access authentication (VPN, Wi-Fi, 802.1X), not per-command authorization.
- Kerberos is a ticket-based authentication protocol used in Windows domains, not device admin AAA.
- LDAP is a directory access protocol, not an AAA authentication service.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A company is deploying new wireless access points and wants the strongest available encryption with protection against offline dictionary attacks on the pre-shared key. Which standard should be selected?

A) WPA3
B) WEP
C) WPA
D) WPA2

<details>
<summary>Answer</summary>

**Correct: A**

WPA3 replaces the WPA2 PSK exchange with SAE (Simultaneous Authentication of Equals), which resists offline dictionary attacks.

**Why the others are wrong:**
- WEP uses a broken RC4 cipher with static IVs and is crackable within minutes.
- WPA uses TKIP, which has known vulnerabilities and is deprecated.
- WPA2 (AES/CCMP) is strong but still vulnerable to offline dictionary attacks against a weak PSK — a weakness WPA3's SAE specifically fixes.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A user logs into a workstation with a fingerprint scan. Which MFA factor category does this represent?

A) Something you know
B) Something you have
C) Somewhere you are
D) Something you are

<details>
<summary>Answer</summary>

**Correct: D**

Fingerprints are biometric data, classified as 'something you are.'

**Why the others are wrong:**
- Something you know refers to passwords or PINs, not physical traits.
- Something you have refers to physical possessions like smart cards or hardware tokens.
- Somewhere you are refers to location-based authentication (e.g., GPS or IP geolocation), not biometrics.

</details>

---

**Q5.** During a security audit, a technician finds several unused switch ports still active and reachable on the production VLAN. What is the BEST hardening action?

A) Leave the ports active in case they're needed later
B) Change the VLAN on the unused ports to VLAN 1
C) Disable the unused ports and enable port security
D) Assign the unused ports a static IP address

<details>
<summary>Answer</summary>

**Correct: C**

Disabling unused ports (and enabling port security/802.1X) reduces the attack surface by preventing unauthorized devices from connecting.

**Why the others are wrong:**
- Leaving ports active unnecessarily exposes the network to rogue device connections.
- Moving ports to VLAN 1 (the default/native VLAN) is a common misconfiguration and security risk, not a fix.
- Assigning a static IP does nothing to prevent unauthorized physical connections.

</details>

---

**Q6.** A legacy IoT device only supports WEP encryption on its wireless interface. Which statement BEST describes the risk?

A) WEP is acceptable as long as a strong passphrase is used
B) WEP uses a weak RC4 cipher with reused IVs and can be cracked in minutes
C) WEP is secure but slower than WPA2
D) WEP only affects wired connections, not wireless

<details>
<summary>Answer</summary>

**Correct: B**

WEP's RC4 implementation reuses initialization vectors, making it crackable with widely available tools in minutes regardless of passphrase strength.

**Why the others are wrong:**
- Passphrase strength does not fix WEP's underlying cryptographic flaw.
- WEP is not merely slower — it is fundamentally broken cryptographically.
- WEP is a wireless (802.11) encryption standard; it has no wired application.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A company wants to restrict a file server so that the marketing team can only read files while the finance team has read/write access, and no one else can access the share. Which concept BEST describes this configuration?

A) Principle of least privilege via ACLs
B) Mandatory access control
C) Single sign-on
D) Network segmentation

<details>
<summary>Answer</summary>

**Correct: A**

Configuring ACLs to grant only the minimum required access per group (read for marketing, read/write for finance, none for others) is a textbook application of least privilege.

**Why the others are wrong:**
- Mandatory access control refers to system-enforced classification labels (e.g., government/military systems), not per-group file permissions.
- Single sign-on relates to authenticating once across multiple systems, not access levels.
- Network segmentation separates traffic into different network zones, not file-level permissions.

</details>

---

**Q8.** Which wireless encryption protocol should be avoided in new deployments due to known cryptographic weaknesses?

A) AES
B) TKIP
C) CCMP
D) GCMP

<details>
<summary>Answer</summary>

**Correct: B**

TKIP, used with WPA and legacy WEP-compatible modes, has known vulnerabilities and has been deprecated in favor of AES-based encryption.

**Why the others are wrong:**
- AES is the current strong encryption algorithm used by WPA2/WPA3.
- CCMP is the AES-based mode used by WPA2 and is considered secure.
- GCMP is the AES-based mode used by WPA3 and is considered secure.

</details>

---

