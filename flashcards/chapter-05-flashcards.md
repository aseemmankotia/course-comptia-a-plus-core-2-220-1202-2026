## Chapter 5: Malware Types, Detection Tools, and Social Engineering — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Ransomware vs Rootkit — key behavior difference? | Ransomware encrypts files and demands payment (loud, immediately visible). Rootkit hides deep in the OS/kernel to stay undetected (silent, persistent). Exam tip: 'encrypts+demands' = ransomware; 'hides+persists' = rootkit. |
| 2 | Phishing vs Spear Phishing vs Whaling | Phishing = mass generic email. Spear phishing = targeted at a specific individual/group using personal details. Whaling = spear phishing aimed at executives/high-value targets. Exam tip: whale = big fish = big target (CEO/CFO). |
| 3 | Vishing definition | Voice phishing — social engineering conducted via phone call. Exam tip: 'V'ishing = 'V'oice. |
| 4 | Shoulder surfing vs Tailgating | Shoulder surfing = observing a screen/keystrokes to steal info. Tailgating = following an authorized person through a secured door without credentials. |
| 5 | Zero-day vulnerability | A vulnerability unknown to the vendor with no patch yet available. Exam tip: exploited before a fix exists — 'zero days' of protection time. |
| 6 | Keylogger primary symptom | Silently records keystrokes; symptom is compromised credentials/accounts without obvious system slowdown. Often bundled with trojans/spyware. |
| 7 | Zombie vs Botnet | Zombie = a single infected computer remotely controlled by an attacker. Botnet = a network of zombie computers controlled via a C2 server, often used for DDoS or spam. |
| 8 | Windows Defender: PowerShell command for a quick scan | Start-MpScan -ScanType QuickScan — Exam tip: full scan uses -ScanType FullScan. |
| 9 | Windows Defender: update virus definitions via CLI | Update-MpSignature (PowerShell) or MpCmdRun.exe -SignatureUpdate. Exam tip: know MpCmdRun.exe as the CLI utility name for Defender. |
| 10 | Rogue antivirus / scareware pop-up | A fake pop-up claims the system is infected and demands payment/download — the pop-up itself IS the malware. Exam tip: legitimate AV never demands payment through a browser pop-up. |
| 11 | Trojan vs Virus | Trojan disguises as legitimate software, requires the user to run it, and does NOT self-replicate. Virus attaches to files and self-replicates when the infected file is executed/shared. |
| 12 | Worm vs Virus | Worm self-replicates and spreads across networks WITHOUT needing a host file or user action. Virus requires a host file and user action (e.g., opening it) to spread. |
