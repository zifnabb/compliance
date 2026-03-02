# ISO 27001 Template Policy Audit (Documentation Mapping)

**Audit date:** 2026-03-03  
**Template audited:** `iso27001-compliance-template/`  
**Business sources referenced:** `business/*.pdf`

## Scope and method

This audit maps each section of the ISO 27001 template’s **policies and procedures** to the most relevant “business” policies/procedures where the requirement is covered in documentation.

- **Met (documented):** A business policy/procedure clearly covers the template requirement.
- **Partial (documented):** Coverage exists, but not as explicitly/cleanly as the template expects (e.g., covered across multiple docs, or missing ISMS-specific framing).
- **Not evidenced:** No clear match found in `business/` documentation (does not imply the control is not implemented operationally).

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
- `business/Backup-and-Recovery-Policy.pdf` (v1.0, Approved: April 28, 2025, Classification: Internal)
- `business/Data-Disposal-and-Destruction-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Network-Security-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Logging-and-Monitoring-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Physical-Security-Policy.pdf` (v1.0, Approved: October 28, 2025, Classification: Internal)
- `business/Incident-Response-Policy.pdf` (v1.0, Approved: April 30, 2025, Classification: Internal)
- `business/Vendor-Incident-Notification-Handling-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Change-Management-Policy.pdf` (v1.0, Approved: April 15, 2025, Classification: Internal)
- `business/System-Development-Lifecycle-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Security-Onboarding-Checklist-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Security-Offboarding-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Security-Awareness-Training-Policy.pdf` (v1.0, Approved: February 24, 2025, Classification: Internal)
- `business/Security-Awareness-Training-Delivery-and-Tracking-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Privacy-Policy.pdf` (v1.0, Approved: April 30, 2025, Classification: Public)
- `business/Vendor-Risk-Management-Policy.pdf` (v1.0, Approved: October 25, 2025, Classification: Internal)
- `business/Vendor-Onboarding-Security-Review-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)
- `business/Vendor-Performance-Monitoring-and-Review-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Internal)

## Template section-by-section mapping

### `iso27001-compliance-template/policies/information-security-policy.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Met (documented) | `business/Information-Security-Policy.pdf` (Purpose) |
| §2 Scope | Met (documented) | `business/Information-Security-Policy.pdf` (Scope) |
| §3.1 Access Control | Met (documented) | `business/Information-Security-Policy.pdf` (§9 Access Control); `business/Access-Control-Policy.pdf` (§4 Access Control Principles, §6 User Access Lifecycle, §7 Authentication, §9 Privileged Access Management); `business/Security-Onboarding-Checklist-Procedure.pdf`; `business/Security-Offboarding-Procedure.pdf` |
| §3.2 Data Classification | Met (documented) | `business/Information-Security-Policy.pdf` (asset/data classification references); `business/Data-Classification-and-Handling-Policy.pdf` (§4–§11); `business/Data-Classification-Procedure.pdf` |
| §3.3 Acceptable Use | Met (documented) | `business/Information-Security-Policy.pdf` (§8.3 Acceptable Use); `business/Acceptable-Use-Policy.pdf` |
| §3.4 Password and Authentication | Met (documented) | `business/Information-Security-Policy.pdf` (§9.3 Authentication); `business/Access-Control-Policy.pdf` (§7 Authentication incl. MFA); *(Template “Password Standards” is referenced by the business InfoSec policy but not present as a standalone document in this repo.)* |
| §3.5 Data Protection | Met (documented) | `business/Backup-and-Recovery-Policy.pdf` (Key Requirements; Recovery Testing Schedule); `business/Encryption-and-Cryptography-Policy.pdf` (data-at-rest/in-transit requirements; standards); `business/Encryption-Key-Management-Procedure.pdf`; `business/Data-Disposal-and-Destruction-Procedure.pdf`; `business/Data-Classification-and-Handling-Policy.pdf` (§11 Data Retention and Disposal; §8 Data Storage; §9 Data Transmission); `business/Privacy-Policy.pdf` |
| §3.6 Network Security | Met (documented) | `business/Information-Security-Policy.pdf` (§13 Network Security / Segregation); `business/Network-Security-Policy.pdf`; `business/Logging-and-Monitoring-Policy.pdf`; `business/Vulnerability-Management-and-Patch-Management-Policy.pdf`; `business/Access-Control-Policy.pdf` (§10 Remote Access) |
| §3.7 Physical Security | Met (documented) | `business/Information-Security-Policy.pdf` (§11 Physical and Environmental Security); `business/Physical-Security-Policy.pdf` |
| §3.8 Incident Response | Met (documented) | `business/Information-Security-Policy.pdf` (§16 Information Security Incident Management); `business/Incident-Response-Policy.pdf`; `business/Vendor-Incident-Notification-Handling-Procedure.pdf` |
| §4.1 Monitoring | Met (documented) | `business/Logging-and-Monitoring-Policy.pdf`; `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (metrics/monitoring + exception monitoring); `business/Incident-Response-Policy.pdf` (testing/review + reporting/metrics, where applicable) |
| §4.2 Violations | Partial (documented) | `business/Acceptable-Use-Policy.pdf` (violations/acceptable use enforcement context); `business/Access-Control-Policy.pdf` (unauthorized access expectations); `business/Incident-Response-Policy.pdf` (policy violation classification); **Gap:** explicit cross-policy disciplinary process is not mapped to a single “Violations” section in the ISO template. |
| §5 Exceptions | Met (documented) | `business/Change-Management-Policy.pdf` (§16.3 Exception Process); `business/Incident-Response-Policy.pdf` (§19.3 Exception Process); `business/Encryption-Key-Management-Procedure.pdf` (§6 Exceptions and Escalations); `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (§10 Exception Handling) |
| §6 Review | Met (documented) | `business/Information-Security-Policy.pdf` (§19 Policy Review and Updates, includes review schedule and “Next Review Date”); many other business policies include “Policy Review and Updates” sections (example: `business/Change-Management-Policy.pdf` §16). |
| §7 Document Control | Met (documented) | Business PDFs include Document Control + Revision History sections (e.g., `business/Information-Security-Policy.pdf` “Document Control”). |

### `iso27001-compliance-template/policies/isms-policy.md`

This template is explicitly ISMS/ISO-scoped. The business documentation has strong general governance coverage, but does not appear to include a single, explicit “ISMS Policy” artifact.

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Partial (documented) | `business/Information-Security-Policy.pdf` (overall program purpose) |
| §2 Scope | Partial (documented) | `business/Information-Security-Policy.pdf` (Scope, Personnel/Assets/Systems/Locations); supporting scope is also present across policies (e.g., network/physical). |
| §2.1 ISMS Boundary | Not evidenced | No dedicated “ISMS boundary” statement found as a single, auditable statement in `business/` documentation. |
| §3 Information Security Objectives | Met (documented) | `business/Information-Security-Policy.pdf` (§4 Information Security Objectives) |
| §3.1 Measurable Objectives | Partial (documented) | `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (targets/metrics); `business/Logging-and-Monitoring-Policy.pdf` (requirements/monitoring); **Gap:** a consolidated ISMS objectives + measures table is not present. |
| §4 Leadership Commitment | Met (documented) | `business/Information-Security-Policy.pdf` (§5 Management Commitment) |
| §5 Roles and Responsibilities | Met (documented) | `business/Information-Security-Policy.pdf` (§6 Roles and Responsibilities) |
| §6 Risk Management | Met (documented) | `business/Risk-Management-Policy.pdf` (framework + exception process); `business/Information-Security-Policy.pdf` (§7 Risk Management) |
| §7 Continual Improvement | Partial (documented) | `business/Incident-Response-Policy.pdf` (lessons learned / continuous improvement expectations); `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (§4.3 Continuous Improvement). |
| §8 Document Control | Met (documented) | Document control exists across business PDFs (e.g., `business/Information-Security-Policy.pdf`). |
| §9 Approval | Partial (documented) | Business PDFs are approved at the policy level (header “Approved: …” where filled), but there is no single “ISMS policy approval” record. |

### `iso27001-compliance-template/policies/risk-management-policy.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Met (documented) | `business/Risk-Management-Policy.pdf` (Purpose) |
| §2 Scope | Met (documented) | `business/Risk-Management-Policy.pdf` (Scope) |
| §3 Risk Assessment Methodology | Met (documented) | `business/Risk-Management-Policy.pdf` (Framework/Lifecycle/Assessment criteria; identification sources and methods) |
| §4 Risk Treatment | Met (documented) | `business/Risk-Management-Policy.pdf` (treatment planning and controls assessment concepts) |
| §5 Risk Acceptance | Met (documented) | `business/Risk-Management-Policy.pdf` (§3.2 Risk Appetite; §16.3 Exception Process) |
| §6 Risk Monitoring | Met (documented) | `business/Risk-Management-Policy.pdf` (monitoring/review expectations; exception monitoring context) |
| §7 Roles and Responsibilities | Met (documented) | `business/Risk-Management-Policy.pdf` (§5 Roles and Responsibilities) |
| §8 Risk Register | Partial (documented) | `business/Risk-Management-Policy.pdf` requires/assumes a risk register; **Gap:** a filled risk register artifact is not present under `business/` or `iso27001-compliance-template/evidence/` in this repo. |
| §9 Document Control | Met (documented) | `business/Risk-Management-Policy.pdf` (Document Control / Revision History) |

### `iso27001-compliance-template/procedures/access-control.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Met (documented) | `business/Access-Control-Policy.pdf` (Purpose) |
| §2 Scope | Met (documented) | `business/Access-Control-Policy.pdf` (Scope) |
| §3 Principles | Met (documented) | `business/Access-Control-Policy.pdf` (§4 Access Control Principles) |
| §4 User Access Management | Met (documented) | `business/Access-Control-Policy.pdf` (§6 User Access Lifecycle); `business/Security-Onboarding-Checklist-Procedure.pdf`; `business/Security-Offboarding-Procedure.pdf` |
| §5 Privileged Access Management | Met (documented) | `business/Access-Control-Policy.pdf` (§9 Privileged Access Management; includes approvals, session monitoring, break-glass) |
| §6 Authentication Requirements | Met (documented) | `business/Access-Control-Policy.pdf` (§7 Authentication, incl. MFA) |
| §7 Access Reviews | Met (documented) | `business/Access-Control-Policy.pdf` (Privileged access reviews; access lifecycle controls) |
| §8 Physical Access Control | Partial (documented) | `business/Physical-Security-Policy.pdf`; **Gap:** visitor management + access zones are covered physically, but not presented as a single procedure aligned to the template’s structure. |
| §9 Remote Access | Met (documented) | `business/Access-Control-Policy.pdf` (§10 Remote Access) |
| §10 Roles and Responsibilities | Met (documented) | `business/Access-Control-Policy.pdf` (Roles and Responsibilities) |
| §11 Document Control | Met (documented) | `business/Access-Control-Policy.pdf` (Document Control / Revision History) |

### `iso27001-compliance-template/procedures/change-management.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Met (documented) | `business/Change-Management-Policy.pdf` (Purpose) |
| §2 Scope | Met (documented) | `business/Change-Management-Policy.pdf` (Scope) |
| §3 Change Categories | Met (documented) | `business/Change-Management-Policy.pdf` (§6 Change Categories) |
| §4 Change Request Process | Met (documented) | `business/Change-Management-Policy.pdf` (§7 Change Request Process; §8 Assessment and Planning; §9 Approval; §10 Testing; §11 Implementation) |
| §5 CAB | Met (documented) | `business/Change-Management-Policy.pdf` (CAB concepts appear as governance/approval body; also references to version control exist) |
| §6 Risk Assessment | Met (documented) | `business/Change-Management-Policy.pdf` (§8.1 Risk Assessment) |
| §7 Emergency Change Process | Met (documented) | `business/Change-Management-Policy.pdf` (§12 Emergency Changes) |
| §8 Rollback Procedures | Met (documented) | `business/Change-Management-Policy.pdf` (Rollback planning/process sections) |
| §9 Documentation Requirements | Met (documented) | `business/Change-Management-Policy.pdf` (documentation/retention expectations; version control references) |
| §10 Metrics and Reporting | Met (documented) | `business/Change-Management-Policy.pdf` (metrics/reporting) |
| §11 Document Control | Met (documented) | `business/Change-Management-Policy.pdf` (Document Control / Revision History) |

### `iso27001-compliance-template/procedures/incident-response.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Met (documented) | `business/Incident-Response-Policy.pdf` (Purpose) |
| §2 Scope | Met (documented) | `business/Incident-Response-Policy.pdf` (Scope) |
| §3 Definitions | Met (documented) | `business/Incident-Response-Policy.pdf` (Definitions / terms) |
| §4 Classification | Met (documented) | `business/Incident-Response-Policy.pdf` (severity levels / classification criteria) |
| §5 Response Process | Met (documented) | `business/Incident-Response-Policy.pdf` (phases/process) |
| §6 Documentation Requirements | Met (documented) | `business/Incident-Response-Policy.pdf` (report contents, evidence handling/chain of custody concepts) |
| §7 Communication | Met (documented) | `business/Incident-Response-Policy.pdf` (internal/external notification); `business/Vendor-Incident-Notification-Handling-Procedure.pdf` |
| §8 Roles and Responsibilities | Met (documented) | `business/Incident-Response-Policy.pdf` (roles) |
| §9 Testing and Maintenance | Met (documented) | `business/Incident-Response-Policy.pdf` (testing cadence, review/update) |
| §10 Document Control | Met (documented) | `business/Incident-Response-Policy.pdf` (Document Control / Revision History) |

### `iso27001-compliance-template/controls/annex-a-controls.md`

**Status:** Not evidenced (register is a blank template with placeholder owners/evidence/statuses).  
While many Annex A topics are covered by `business/` policies, the template register itself is not populated with:

- implemented/planned status per control,
- owners,
- evidence links.

### `iso27001-compliance-template/templates/risk-register.md`

**Status:** Not evidenced (template exists, but no completed risk register evidence is present in this repo).  
Relevant business policy foundation exists in `business/Risk-Management-Policy.pdf`.

