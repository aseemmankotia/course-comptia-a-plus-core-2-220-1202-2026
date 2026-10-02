## Chapter 10 Cheat Sheet: Backup, Safety & Environmental Controls

### 3-2-1 Backup Rule
| Component | Requirement |
|---|---|
| 3 | Total copies of data (production + 2 backups) |
| 2 | Different media types (e.g., local disk + cloud, or NAS + tape) |
| 1 | Offsite copy (protects against fire/theft/site disaster) |

### Backup Type Comparison
| Type | Backup Speed | Storage Use | Restore Requirement | Restore Speed |
|---|---|---|---|---|
| Full | Slowest | Highest | Full backup only | Fastest |
| Incremental | Fastest | Lowest | Full + ALL incrementals since | Slowest |
| Differential | Medium (grows daily) | Medium (grows daily) | Full + latest differential only | Medium/Fast |

**Exam rule of thumb:** Incremental = fast backup, slow restore. Differential = balanced, simpler restore (2 sets).

### ESD Prevention
| Practice | Detail |
|---|---|
| ESD strap | ~1 megohm resistor; connects tech to ground |
| ESD mat | Grounds components/tools on workbench |
| Self-grounding | Touch unpainted metal chassis if no strap/mat available |
| Never | Wear ESD strap while servicing PSU or CRT (electrocution risk) |
| Storage | Anti-static bags for spare components |

### Electrical Safety
- Always power down AND unplug before opening a case or replacing internal components.
- Discharge PSU/CRT capacitors with a proper discharge tool before servicing — do NOT wear an ESD strap during this step.
- Avoid overloading a single circuit/power strip with high-draw devices (e.g., space heaters, multiple monitors) — fire hazard, not just performance issue.
- Use surge protectors/UPS appropriately; never daisy-chain multiple power strips.

### Personal Safety
- Lifting: bend at knees, keep back straight, lift with legs — never bend at the waist or twist while lifting.
- Cable management: route and secure cables to prevent tripping hazards.
- Know location of fire extinguisher (Class C for electrical fires) and emergency shutoff.

### Environmental Controls
| Control | Target/Requirement |
|---|---|
| Temperature | Stable, monitored range to prevent overheating |
| Humidity | ~40-60% RH — too low = ESD risk, too high = condensation/corrosion |
| SDS (Safety Data Sheet) | Required documentation for hazardous materials; must be accessible on-site |
| Battery/toner disposal | Recycle per local hazardous-waste regulations; never in regular trash |

### Account/Data Recovery Procedures
- Verify backup integrity regularly (test restores, not just backup completion).
- Document recovery steps and RTO/RPO expectations before an incident occurs.
- For account recovery: verify identity, use documented escalation/approval process, log all recovery actions for audit.
