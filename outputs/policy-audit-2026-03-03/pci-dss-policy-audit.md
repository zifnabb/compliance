# PCI DSS Policy Audit (Documentation Mapping)

**Audit date:** 2026-03-03  
**Template audited:** `pci-dss-compliance-template/`  
**Business sources referenced:** `business/*.pdf`  
**PCI source:** `Source Docs/PCI-DSS-v4_0_1.pdf` (PCI DSS Requirements and Testing Procedures, v4.0.1, June 2024)

## Scope and method

This audit maps the **12 principal PCI DSS requirements** (v4.0.1) to the most relevant “business” policies/procedures where the requirement is covered in documentation.

- **Met (documented):** Business documentation clearly covers the requirement topic at a policy/procedure level.
- **Partial (documented):** Coverage exists, but is not explicitly PCI/CDE/account-data scoped (or relies on implied practices without a consolidated PCI scope statement).
- **Not evidenced:** No clear match found in `business/` documentation.

**Important limitation:** This is a **documentation mapping audit**, not a full PCI DSS assessment against the detailed testing procedures and scoping rules in the source standard. It does not validate operational effectiveness (for example, actual firewall rule reviews, actual vulnerability scans, actual access reviews performed, etc.).

## Business reference index (primary)

Where “Approved” exists in the PDF header, it is included below.

- `business/Information-Security-Policy.pdf` (v1.0, Approved: February 15, 2025, Classification: Internal)
- `business/Risk-Management-Policy.pdf` (v1.0, Approved: March 1, 2025, Classification: Internal)
- `business/Access-Control-Policy.pdf` (v1.0, Approved: April 26, 2025, Classification: Internal)
- `business/Acceptable-Use-Policy.pdf` (v1.0, Approved: February 25, 2025, Classification: Internal)
- `business/Data-Classification-and-Handling-Policy.pdf` (v1.0, Approved: March 15, 2025, Classification: Internal)
- `business/Data-Classification-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Encryption-and-Cryptography-Policy.pdf` (v1.0, Approved: February 23, 2025, Classification: Internal)
- `business/Encryption-Key-Management-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Restricted)
- `business/Logging-and-Monitoring-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Network-Security-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Physical-Security-Policy.pdf` (v1.0, Approved: October 28, 2025, Classification: Internal)
- `business/Anti-Malware-Policy.pdf` (v1.0, Approved: March 26, 2025, Classification: Internal)
- `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/System-Development-Lifecycle-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Change-Management-Policy.pdf` (v1.0, Approved: April 15, 2025, Classification: Internal)
- `business/Incident-Response-Policy.pdf` (v1.0, Approved: April 30, 2025, Classification: Internal)
- `business/Security-Awareness-Training-Policy.pdf` (v1.0, Approved: February 24, 2025, Classification: Internal)
- `business/Security-Awareness-Training-Delivery-and-Tracking-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Background-Check-Process-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Security-Onboarding-Checklist-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Security-Offboarding-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Vendor-Risk-Management-Policy.pdf` (v1.0, Approved: October 25, 2025, Classification: Internal)
- `business/Vendor-Onboarding-Security-Review-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Vendor-Performance-Monitoring-and-Review-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Vendor-Incident-Notification-Handling-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Backup-and-Recovery-Policy.pdf` (v1.0, Approved: April 28, 2025, Classification: Internal)
- `business/Business-Continuity-and-Disaster-Recovery-Policy.pdf` (v1.0, Approved: March 24, 2025, Classification: Internal)
- `business/Privacy-Policy.pdf` (v1.0, Approved: April 30, 2025, Classification: Public)

## Requirement-by-requirement mapping (principal requirements)

| PCI DSS requirement (v4.0.1 principal) | Status | Business references (where coverage is documented) |
|---|---|---|
| 1. Install and Maintain Network Security Controls | Met (documented) | `business/Network-Security-Policy.pdf` (boundary protection, segmentation concepts, secure remote connectivity); `business/Access-Control-Policy.pdf` (remote access, bastion/jump host concepts); `business/Logging-and-Monitoring-Policy.pdf` (monitoring/alerts) |
| 2. Apply Secure Configurations to All System Components | Met (documented) | `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (hardening standards/benchmarks + configuration reviews); `business/Change-Management-Policy.pdf` (controlled changes/testing/approvals); `business/Network-Security-Policy.pdf` (device/jump host hardening concepts); `business/Logging-and-Monitoring-Policy.pdf` (configuration monitoring and FIM baselines) |
| 3. Protect Stored Account Data | Partial (documented) | `business/Data-Classification-and-Handling-Policy.pdf` (storage, retention, disposal by classification); `business/Encryption-and-Cryptography-Policy.pdf` (data-at-rest encryption + key management principles); `business/Encryption-Key-Management-Procedure.pdf`; `business/Data-Disposal-and-Destruction-Procedure.pdf`; **Gap:** PCI DSS-specific “account data”/PAN handling, masking, and CDE-scoped retention requirements are not explicitly defined as a dedicated standard in this repo. |
| 4. Protect Cardholder Data with Strong Cryptography During Transmission Over Open, Public Networks | Partial (documented) | `business/Encryption-and-Cryptography-Policy.pdf` (TLS/HTTPS/VPN and secure transmission standards); `business/Network-Security-Policy.pdf` (secure connectivity); `business/Data-Classification-and-Handling-Policy.pdf` (transmission requirements); **Gap:** PCI-specific statement about cardholder data transmission scope and approved cryptographic configurations is not consolidated as a PCI/CDE artifact. |
| 5. Protect All Systems and Networks from Malicious Software | Met (documented) | `business/Anti-Malware-Policy.pdf`; `business/Logging-and-Monitoring-Policy.pdf` (alerting/logging); `business/Incident-Response-Policy.pdf` (malware incidents) |
| 6. Develop and Maintain Secure Systems and Software | Met (documented) | `business/System-Development-Lifecycle-Policy.pdf` (secure SDLC + security testing expectations); `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (vuln lifecycle, scanning, security testing including penetration testing concepts); `business/Change-Management-Policy.pdf` (controlled releases) |
| 7. Restrict Access to System Components and Cardholder Data by Business Need to Know | Met (documented) | `business/Access-Control-Policy.pdf` (least privilege/RBAC/need-to-know; privileged access governance; access reviews); `business/Data-Classification-and-Handling-Policy.pdf` (access controls by classification); onboarding/offboarding procedures for access lifecycle |
| 8. Identify Users and Authenticate Access to System Components | Met (documented) | `business/Access-Control-Policy.pdf` (authentication requirements, MFA, password controls, session controls); `business/Acceptable-Use-Policy.pdf` (credential responsibilities) |
| 9. Restrict Physical Access to Cardholder Data | Partial (documented) | `business/Physical-Security-Policy.pdf` (facility/equipment controls); `business/Access-Control-Policy.pdf` (physical access zones/visitor management concepts); **Gap:** explicit mapping of “cardholder data” storage locations (if any) to physical controls is not documented via a PCI scope/CDE artifact. |
| 10. Log and Monitor All Access to System Components and Cardholder Data | Partial (documented) | `business/Logging-and-Monitoring-Policy.pdf` (log sources, retention, integrity monitoring, alerting); `business/Access-Control-Policy.pdf` (privileged session logging/recording); **Gap:** CDE/account-data specific logging scope and review cadence is not declared as a PCI scoping statement in this repo. |
| 11. Test Security of Systems and Networks Regularly | Met (documented) | `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (vulnerability scanning frequency + penetration testing expectations); `business/System-Development-Lifecycle-Policy.pdf` (security testing throughout SDLC); `business/Change-Management-Policy.pdf` (testing requirements for changes) |
| 12. Support Information Security with Organizational Policies and Programs | Met (documented) | `business/Information-Security-Policy.pdf` (program governance, objectives, roles); `business/Risk-Management-Policy.pdf`; `business/Incident-Response-Policy.pdf`; `business/Security-Awareness-Training-Policy.pdf` (+ delivery/tracking procedure); `business/Vendor-Risk-Management-Policy.pdf` (supplier governance) |

