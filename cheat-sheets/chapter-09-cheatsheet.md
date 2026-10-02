## Chapter 9 Cheat Sheet: Documentation, Ticketing, Change Management

### Ticketing System — Required Fields
| Field | Purpose |
|---|---|
| Issue description | What the user reported |
| Category | Type of issue (hardware/software/network) for routing |
| Priority | Urgency level, drives SLA/escalation |
| Resolution | How the issue was fixed — feeds the knowledge base |

### Change Management — Step Order (memorize sequence)
1. **Purpose of change** — why is this needed
2. **Scope** — what/who is affected
3. **Risk analysis** — what could go wrong, impact level
4. **Sandbox testing** — validate in isolated test environment
5. **Approval** — change board/manager sign-off
6. **Implementation** — execute the change
7. **Rollback plan** — documented BEFORE implementation, executed only if change fails

**Exam trap:** Rollback plan is prepared ahead of time, not created after something breaks. Missing rollback plan = most common wrong-answer trap in scenario questions.

### Knowledge Base / SOP vs. Change Request
| Document | Use Case |
|---|---|
| KB Article / SOP | Repeatable routine task (e.g., password reset, printer setup) |
| Change Request | Any modification to a production system requiring risk review and approval |

### Asset Management Lifecycle
Request → Purchase → **Receiving & Tagging** → Deployment → Maintenance → Retirement/Disposal

- **Asset tag**: assigned at intake, before deployment.
- **Inventory list**: tracks tag, owner, location, purchase date, warranty status.
- **Warranty tracking**: purchase date + warranty expiration = key data for replacement decisions.
- **Disposal**: must follow data destruction procedures (wipe/degauss/shred) — tested alongside data security domain.

### Software Licensing
| Type | Key Traits |
|---|---|
| EULA (commercial) | Restricts use to licensed terms; no source code access; per-seat/volume licensing common |
| Open Source | Source code viewable/modifiable; free redistribution (per license, e.g., GPL, MIT) |
| DRM | Technical restriction preventing unauthorized copying/use of licensed content |

**Exam trap:** Don't confuse DRM (a technical control) with EULA (a legal agreement) — questions test both terms separately.

### Quick Memory Trick
**"P-S-R-S-A-I-R"** — Purpose, Scope, Risk, Sandbox, Approval, Implementation, Rollback (ready) — say it like a chant to lock in the change management order.
