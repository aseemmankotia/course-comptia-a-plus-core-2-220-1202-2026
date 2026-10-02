## Chapter 11: Incident Response, Regulated Data, Licensing, and Scripting Risks — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Default RDP port number? | 3389 (TCP). Exam tip: VNC = 5900, SSH = 22, Telnet = 23. |
| 2 | GDPR maximum fine for non-compliance? | Up to €20 million or 4% of global annual revenue, whichever is higher. Exam tip: shows why GDPR scenarios matter even for non-EU companies. |
| 3 | PII vs PHI vs PCI vs GDPR — what's the difference? | PII = any personally identifiable info; PHI = health-specific identifiable info (HIPAA); PCI-DSS = standard for payment card data; GDPR = EU law protecting personal data of EU residents. Exam tip: match scenario keywords (medical=PHI, credit card=PCI, EU citizen=GDPR). |
| 4 | What must a chain-of-custody log document? | Who collected the evidence, what was collected, when/where, and every subsequent transfer with signatures and timestamps. Exam tip: an unbroken chain proves evidence integrity. |
| 5 | .ps1 file extension = ? | Windows PowerShell script. Exam tip: requires an execution policy change (e.g., Set-ExecutionPolicy) to run — a built-in defense against auto-run scripts. |
| 6 | .vbs file extension = ? (risk) | VBScript, run by Windows Script Host (wscript.exe/cscript.exe). Exam tip: common phishing/malware vector since it runs silently; Microsoft is phasing it out (disabled by default in newer Windows 11 builds). |
| 7 | .sh vs .bat vs .py — platform/use? | .sh = shell script (Linux/macOS); .bat = batch script (Windows CMD); .py = Python script (cross-platform, needs interpreter). Exam tip: know which OS runs which extension natively. |
| 8 | First-response steps for a discovered incident (e.g., illegal content, breach)? | 1) Preserve device/data 2) Report through proper channels (chain of command) 3) Document chain of custody 4) Never personally investigate further. Exam tip: preserve & report FIRST — order matters. |
| 9 | EULA vs DRM — difference? | EULA = legal agreement defining allowed software use (End User License Agreement); DRM = technical mechanism enforcing those restrictions (copy protection, activation). Exam tip: EULA is legal, DRM is technical. |
| 10 | Personal vs Enterprise (volume) licensing? | Personal license = single device/user, non-transferable; Enterprise/volume license = covers many devices under one organizational agreement, often managed via a license server (e.g., KMS). Exam tip: volume licensing centralizes activation/management. |
| 11 | RDP vs VNC vs SSH vs VPN — purpose? | RDP = remote GUI (Windows, port 3389); VNC = cross-platform remote GUI (port 5900, often unencrypted); SSH = encrypted remote CLI (port 22); VPN = encrypts the whole tunnel/connection to a network. Exam tip: VPN secures the connection; RDP/VNC/SSH access the remote system itself. |
| 12 | What is an RMM tool? | Remote Monitoring and Management software used by MSPs/IT to monitor, patch, and manage many endpoints remotely at scale. Exam tip: compromised RMM credentials give an attacker access to ALL managed endpoints at once — a major security risk. |
