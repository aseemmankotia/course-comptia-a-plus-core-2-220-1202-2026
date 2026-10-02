## Chapter 11 Cheat Sheet: Incident Response, Regulated Data, Licensing, Scripting Risks

### Incident Response Order
1. **Preserve** device/data (don't power off unless instructed; stop using it)
2. **Report** through proper channels (supervisor/chain of command)
3. **Document** chain of custody
4. **Never** personally investigate, delete evidence, or confront the customer

### Chain of Custody Must Include
Who collected it | What was collected | When/where | Signatures of every handoff

### Regulated Data Categories
| Category | Governs | Keyword Trigger |
|---|---|---|
| PII | Any personally identifiable data | name, SSN, address |
| PHI | Health-related identifiable data (HIPAA) | diagnosis, treatment, medical record |
| PCI-DSS | Payment card data security standard | credit card, cardholder data |
| GDPR | EU residents' personal data (extraterritorial) | EU citizen/customer |

**GDPR fine:** up to €20M or 4% global revenue, whichever is higher.

### Licensing
| Term | Meaning |
|---|---|
| EULA | Legal terms of software use |
| DRM | Technical enforcement of license restrictions |
| Personal license | Single user/device |
| Enterprise/volume license | Many devices, centrally managed (e.g., KMS) |
| Open source (copyleft) | Source code open; derivatives must reuse same license |

### Remote Access Technologies
| Tech | Port | Encrypted? | Use |
|---|---|---|---|
| RDP | 3389 | Yes (modern versions) | Windows GUI remote access |
| VNC | 5900 | Often NOT by default | Cross-platform GUI access |
| SSH | 22 | Yes | CLI remote access (Linux) |
| Telnet | 23 | No (plaintext) | Legacy CLI — avoid |
| VPN | varies | Yes | Encrypts entire tunnel to network |
| RMM | varies | Vendor-dependent | Mass endpoint monitoring/management (MSPs) |

### Scripting File Types
| Ext | Language | Platform | Risk Note |
|---|---|---|---|
| .bat | Batch | Windows CMD | Simple automation, limited capability |
| .ps1 | PowerShell | Windows | Needs execution policy change to run |
| .sh | Shell | Linux/macOS | Requires execute permission (chmod +x) |
| .py | Python | Cross-platform | Needs interpreter installed |
| .vbs | VBScript | Windows (WSH) | Common phishing vector; being deprecated |
| .js | JavaScript | Browser/Node | Can run via browser or standalone engine; malware vector in attachments |

### Professionalism
- Stay within scope of the reported issue
- Never access, comment on, or copy unrelated personal files
- Use proper, non-judgmental communication with end users
- Always escalate legal/ethical concerns through official channels, not personally
