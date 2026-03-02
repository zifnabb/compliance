# SWIFT CSCF Policy Audit (Documentation Mapping)

**Audit date:** 2026-03-03  
**Template audited:** `swift-cscf-compliance-template/`  
**Business sources referenced:** `business/*.pdf`  
**CSCF source:** `Source Docs/CSCF_v2026_20250701_compared_to_v2025.pdf`

## Scope and method

This audit maps each SWIFT CSCF control in `swift-cscf-compliance-template/controls/cscf-controls.md` to the most relevant “business” policies/procedures where the requirement is covered in documentation.

- **Met (documented):** Business documentation clearly covers the control topic.
- **Partial (documented):** Coverage exists, but is not SWIFT-environment-specific (or is spread across multiple documents without an explicit “SWIFT scope/boundary” statement).
- **Not evidenced:** No clear match found in `business/` documentation.

**Architecture applicability note:** CSCF controls apply differently by architecture type (A1/A2/A3/A4/B). The business documentation in this repo does not explicitly declare which CSCF architecture type(s) are in scope; where a control is architecture-specific (e.g., 1.5 applies to A4 only), this audit treats it as **scope-dependent** and recommends documenting applicability explicitly in `swift-cscf-compliance-template/controls/architecture-types.md`.

## Business reference index (primary)

Where “Approved” exists in the PDF header, it is included below.

- `business/Information-Security-Policy.pdf` (v1.0, Approved: February 15, 2025, Classification: Internal)
- `business/Access-Control-Policy.pdf` (v1.0, Approved: April 26, 2025, Classification: Internal)
- `business/Acceptable-Use-Policy.pdf` (v1.0, Approved: February 25, 2025, Classification: Internal)
- `business/Network-Security-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Logging-and-Monitoring-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Anti-Malware-Policy.pdf` (v1.0, Approved: March 26, 2025, Classification: Internal)
- `business/Encryption-and-Cryptography-Policy.pdf` (v1.0, Approved: February 23, 2025, Classification: Internal)
- `business/Encryption-Key-Management-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Restricted)
- `business/Data-Classification-and-Handling-Policy.pdf` (v1.0, Approved: March 15, 2025, Classification: Internal)
- `business/Data-Classification-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Incident-Response-Policy.pdf` (v1.0, Approved: April 30, 2025, Classification: Internal)
- `business/Security-Awareness-Training-Policy.pdf` (v1.0, Approved: February 24, 2025, Classification: Internal)
- `business/Security-Awareness-Training-Delivery-and-Tracking-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Background-Check-Process-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Physical-Security-Policy.pdf` (v1.0, Approved: October 28, 2025, Classification: Internal)
- `business/Vendor-Risk-Management-Policy.pdf` (v1.0, Approved: October 25, 2025, Classification: Internal)
- `business/Vendor-Onboarding-Security-Review-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Vendor-Performance-Monitoring-and-Review-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Vendor-Incident-Notification-Handling-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Change-Management-Policy.pdf` (v1.0, Approved: April 15, 2025, Classification: Internal)
- `business/System-Development-Lifecycle-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)

## Control-by-control mapping

### 1 Restrict Internet Access and Protect Critical Systems from General IT Environment

| Control | Type | Status | Business references (where coverage is documented) |
|---|---|---|---|
| 1.1 Swift Environment Protection | Mandatory | Partial (documented) | `business/Network-Security-Policy.pdf` (segmentation/DMZ/boundary protection concepts); `business/Access-Control-Policy.pdf` (remote access controls; bastion/jump host concepts); **Gap:** no explicit statement defining a “SWIFT environment” boundary and required isolation level. |
| 1.2 Operating System Privileged Account Control | Mandatory | Met (documented) | `business/Access-Control-Policy.pdf` (privileged access management; session controls/recording; approvals and reviews); `business/Logging-and-Monitoring-Policy.pdf` (monitoring and alerting) |
| 1.3 Virtualisation or Cloud Platform Protection | Mandatory | Met (documented) | `business/Network-Security-Policy.pdf` (architecture controls; segmentation; boundary protection); `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (hardening standards + scanning); `business/Access-Control-Policy.pdf` (privileged access restrictions) |
| 1.4 Restriction of Internet Access | Mandatory | Met (documented) | `business/Network-Security-Policy.pdf` (internet boundary controls/DMZ; controlled connectivity; firewall concepts); `business/Access-Control-Policy.pdf` (remote access restrictions); `business/Acceptable-Use-Policy.pdf` (internet usage rules) |
| 1.5 Customer Environment Protection | Mandatory | Not evidenced (scope-dependent) | Applies to CSCF architecture A4 only. Business policies cover customer data protection generally (`business/Data-Classification-and-Handling-Policy.pdf`, `business/Access-Control-Policy.pdf`) but do not explicitly document CSCF A4 “customer environment” requirements. |

### 2 Reduce Attack Surface and Vulnerabilities

| Control | Type | Status | Business references (where coverage is documented) |
|---|---|---|---|
| 2.1 Internal Data Flow Security | Mandatory | Met (documented) | `business/Network-Security-Policy.pdf` (segmentation/controlled flows); `business/Encryption-and-Cryptography-Policy.pdf` (data-in-transit requirements); `business/Data-Classification-and-Handling-Policy.pdf` (transmission handling by classification) |
| 2.2 Security Updates | Mandatory | Met (documented) | `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (patch management lifecycle; prioritization); `business/Change-Management-Policy.pdf` (change control/testing); `business/System-Development-Lifecycle-Policy.pdf` (release/testing gates) |
| 2.3 System Hardening | Mandatory | Met (documented) | `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (hardening standards/benchmarks); `business/Anti-Malware-Policy.pdf` (hardening concepts and baselines); `business/Network-Security-Policy.pdf` (device/jump host hardening concepts) |
| 2.4A Back Office Data Flow Security | Advisory | Met (documented) | `business/Network-Security-Policy.pdf` (segmentation; controlled inter-segment connectivity); `business/Access-Control-Policy.pdf` (least privilege; segregation of duties); `business/Encryption-and-Cryptography-Policy.pdf` (secure protocols; encryption in transit) |
| 2.5A External Transmission Data Protection | Advisory | Met (documented) | `business/Encryption-and-Cryptography-Policy.pdf` (TLS/HTTPS/VPN requirements); `business/Data-Classification-and-Handling-Policy.pdf` (transmission requirements); `business/Network-Security-Policy.pdf` (secure connectivity/boundary) |
| 2.6 Operator Session Confidentiality and Integrity | Mandatory | Met (documented) | `business/Access-Control-Policy.pdf` (session management, timeouts, workstation locking, privileged session logging/recording); `business/Acceptable-Use-Policy.pdf` (user responsibilities) |
| 2.7 Vulnerability Scanning | Mandatory | Met (documented) | `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (systematic scanning frequency/scope); `business/Logging-and-Monitoring-Policy.pdf` (monitoring/reporting support) |
| 2.8 Outsourced Critical Activity Protection | Mandatory | Met (documented) | `business/Vendor-Risk-Management-Policy.pdf` (due diligence/contractual requirements/monitoring); `business/Vendor-Onboarding-Security-Review-Procedure.pdf`; `business/Vendor-Performance-Monitoring-and-Review-Procedure.pdf`; `business/Vendor-Incident-Notification-Handling-Procedure.pdf` |
| 2.9 Transaction Business Controls | Mandatory | Met (documented) | `business/Access-Control-Policy.pdf` (segregation of duties for financial transactions; approval constraints); `business/Logging-and-Monitoring-Policy.pdf` (transaction logs retention); `business/Incident-Response-Policy.pdf` (fraud/suspicious transaction considerations) |
| 2.10 Application Hardening | Mandatory | Met (documented) | `business/System-Development-Lifecycle-Policy.pdf` (security testing: SAST/DAST/pen testing concepts; secure SDLC); `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (application scanning/testing expectations) |
| 2.11A RMA Business Controls | Advisory | Partial (documented) | Business documentation covers access control and privileged access generally (`business/Access-Control-Policy.pdf`) and vendor identity considerations (`business/Vendor-Risk-Management-Policy.pdf`), but does not explicitly reference SWIFT RMA-specific business controls. |

### 3 Physically Secure the Environment

| Control | Type | Status | Business references (where coverage is documented) |
|---|---|---|---|
| 3.1 Physical Security | Mandatory | Met (documented) | `business/Physical-Security-Policy.pdf` (facility/equipment protection); `business/Information-Security-Policy.pdf` (physical/environmental security governance) |

### 4 Prevent Compromise of Credentials

| Control | Type | Status | Business references (where coverage is documented) |
|---|---|---|---|
| 4.1 Password Policy | Mandatory | Met (documented) | `business/Access-Control-Policy.pdf` (authentication requirements incl. password controls); `business/Acceptable-Use-Policy.pdf` (credential handling responsibilities) |
| 4.2 Multi-Factor Authentication | Mandatory | Met (documented) | `business/Access-Control-Policy.pdf` (MFA requirements and accepted factors; remote access and privileged access) |

### 5 Manage Identities and Separate Privileges

| Control | Type | Status | Business references (where coverage is documented) |
|---|---|---|---|
| 5.1 Logical Access Control | Mandatory | Met (documented) | `business/Access-Control-Policy.pdf` (least privilege/RBAC/need-to-know; approvals; access lifecycle; access reviews) |
| 5.2 Token Management | Mandatory | Partial (documented) | `business/Access-Control-Policy.pdf` (MFA tokens; credential protections); `business/Encryption-Key-Management-Procedure.pdf` (hardware security tokens for key management); **Gap:** no single “token management” standard written in SWIFT terms (token issuance, custody, loss/compromise response) across SWIFT operator/admin use cases. |
| 5.3A Staff Screening Process | Advisory | Met (documented) | `business/Background-Check-Process-Procedure.pdf` (background check levels incl. enhanced checks for privileged access); `business/Security-Onboarding-Checklist-Procedure.pdf` (background checks before onboarding); `business/Access-Control-Policy.pdf` (background check verification for privileged access) |
| 5.4 Password Repository Protection | Mandatory | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (vault-protected configurations; restricted vault passwords); `business/Access-Control-Policy.pdf` (prohibits secrets in source repositories; controlled access) |

### 6 Detect Anomalous Activity to Systems or Transaction Records

| Control | Type | Status | Business references (where coverage is documented) |
|---|---|---|---|
| 6.1 Malware Protection | Mandatory | Met (documented) | `business/Anti-Malware-Policy.pdf`; `business/Incident-Response-Policy.pdf` (malware incidents); `business/Logging-and-Monitoring-Policy.pdf` (alerting and monitoring) |
| 6.2 Software Integrity | Mandatory | Met (documented) | `business/Logging-and-Monitoring-Policy.pdf` (file integrity monitoring with cryptographic hashing/baselines); `business/Change-Management-Policy.pdf` (authorized change tracking) |
| 6.3 Database Integrity | Mandatory | Partial (documented) | `business/Logging-and-Monitoring-Policy.pdf` (integrity/anti-tampering expectations for logs; monitoring); `business/System-Development-Lifecycle-Policy.pdf` (testing/quality); **Gap:** database-specific integrity controls are not consolidated as a distinct “database integrity” standard (tamper detection, privileged DB changes monitoring, transaction record integrity controls) in a single business document. |
| 6.4 Logging and Monitoring | Mandatory | Met (documented) | `business/Logging-and-Monitoring-Policy.pdf` (log sources/retention/alerting; includes transaction log retention); `business/Incident-Response-Policy.pdf` (use of logs in detection/response) |
| 6.5A Intrusion Detection | Advisory | Met (documented) | `business/Network-Security-Policy.pdf` (IDS/IPS concepts); `business/Logging-and-Monitoring-Policy.pdf` (centralized monitoring and alert handling); `business/Incident-Response-Policy.pdf` (intrusion incidents) |

### 7 Plan for Incident Response and Information Sharing

| Control | Type | Status | Business references (where coverage is documented) |
|---|---|---|---|
| 7.1 Cyber Incident Response Planning | Mandatory | Met (documented) | `business/Incident-Response-Policy.pdf`; `business/Vendor-Incident-Notification-Handling-Procedure.pdf` |
| 7.2 Security Training and Awareness | Mandatory | Met (documented) | `business/Security-Awareness-Training-Policy.pdf`; `business/Security-Awareness-Training-Delivery-and-Tracking-Procedure.pdf` |
| 7.3A Penetration Testing | Advisory | Met (documented) | `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (penetration testing expectations); `business/System-Development-Lifecycle-Policy.pdf` (security testing incl. pen testing); `business/Vendor-Risk-Management-Policy.pdf` (vendor audits/pen tests concepts) |
| 7.4A Scenario-based Risk Assessment | Advisory | Partial (documented) | `business/Risk-Management-Policy.pdf` (risk assessment framework); `business/Incident-Response-Policy.pdf` (tabletops/testing concepts); **Gap:** explicit scenario-based risk assessment artifacts and a repeatable scenario library are not provided as a documented business process/artifact in this repo. |

