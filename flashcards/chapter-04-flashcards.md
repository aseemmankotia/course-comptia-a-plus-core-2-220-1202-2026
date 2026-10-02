## Chapter 4: Security Measures, Wireless Protocols, and Authentication — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | WPA3-Personal key exchange method? | SAE (Simultaneous Authentication of Equals) replaces WPA2's PSK exchange. Exam tip: SAE resists offline dictionary/brute-force attacks against weak passphrases. |
| 2 | TKIP vs AES for Wi-Fi encryption — which to choose? | AES/CCMP or AES/GCMP = current standard, strong. TKIP = deprecated, vulnerable, used with WEP/WPA1. Exam tip: never select TKIP for new deployments. |
| 3 | RADIUS default port(s) and transport protocol? | UDP 1812 (authentication) and 1813 (accounting); legacy ports 1645/1646. RADIUS encrypts only the password in the packet. Exam tip: RADIUS = network access (VPN, Wi-Fi, switch port 802.1X). |
| 4 | TACACS+ default port and transport protocol? | TCP port 49. Encrypts the entire packet body. Exam tip: TACACS+ = device administration (router/switch CLI), separates authentication, authorization, and accounting. |
| 5 | Three main MFA factor categories? | Something you know (password/PIN), something you have (token/smart card), something you are (biometric). Exam tip: true MFA requires two DIFFERENT categories, not two passwords. |
| 6 | What is a mantrap and what does it prevent? | A vestibule with two interlocking doors — only one opens at a time. Prevents tailgating/piggybacking into secure areas. Exam tip: mantrap = physical anti-tailgating control. |
| 7 | What does a cable lock protect against? | Physical theft of laptops/devices; low-cost deterrent. Exam tip: does NOT protect data on the device, only prevents removal of the hardware. |
| 8 | Principle of least privilege — definition? | Users and systems are granted only the minimum access necessary to perform their job function. Exam tip: implemented via ACLs and group-based permissions. |
| 9 | First step when hardening a newly installed network device? | Change default username/password immediately. Exam tip: default credentials are the #1 exploited misconfiguration tested on the exam. |
| 10 | Why disable unused switch ports? | Reduces attack surface and prevents rogue device connections. Exam tip: pair disabled/unused ports with 802.1X port-based authentication for active ports. |
| 11 | Common biometric authentication methods? | Fingerprint, facial recognition, retina/iris scan, voice recognition. Exam tip: biometrics = 'something you are'; evaluated by false-accept/false-reject rates. |
| 12 | Why is WEP considered insecure? | Uses a weak RC4 stream cipher with static/reused initialization vectors, crackable within minutes using freely available tools. Exam tip: WEP should never be selected; use WPA2 minimum, WPA3 preferred. |
