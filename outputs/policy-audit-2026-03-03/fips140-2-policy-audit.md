# FIPS 140-2 Template Policy/Procedure Audit (Documentation Mapping)

**Audit date:** 2026-03-03  
**Template audited:** `FIPS140-2-compliance-template/`  
**Business sources referenced:** `business/*.pdf`

## Scope and method

This audit maps each section of the FIPS 140-2 template’s **policy and procedures** to the most relevant “business” policies/procedures where similar governance and operational expectations are documented.

- **Met (documented):** A business policy/procedure clearly covers the template requirement in a way that would reasonably support a crypto module program.
- **Partial (documented):** Coverage exists, but is not FIPS/module-specific (e.g., organization-wide policy rather than a cryptographic module validation program artifact).
- **Not evidenced:** No clear match found in `business/` documentation.

## Business reference index (primary)

- `business/Encryption-and-Cryptography-Policy.pdf` (v1.0, Approved: February 23, 2025, Classification: Internal)
- `business/Encryption-Key-Management-Procedure.pdf` (v1.0, Approved: *(blank in header)*, Classification: Restricted)
- `business/Change-Management-Policy.pdf` (v1.0, Approved: April 15, 2025, Classification: Internal)
- `business/System-Development-Lifecycle-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Access-Control-Policy.pdf` (v1.0, Approved: April 26, 2025, Classification: Internal)
- `business/Logging-and-Monitoring-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Vulnerability-Management-and-Patch-Management-Policy.pdf` (v1.0, Approved: October 29, 2025, Classification: Internal)
- `business/Information-Security-Policy.pdf` (v1.0, Approved: February 15, 2025, Classification: Internal)

## Template section-by-section mapping

### `FIPS140-2-compliance-template/policies/cryptographic-module-security-policy.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Partial (documented) | `business/Encryption-and-Cryptography-Policy.pdf` (organization-wide crypto principles/standards); `business/Information-Security-Policy.pdf` (overall security governance) |
| §2 Scope | Partial (documented) | `business/Encryption-and-Cryptography-Policy.pdf` (scope covers information types/systems/crypto operations); **Gap:** no explicit “cryptographic module boundary” scope. |
| §3 Objectives | Partial (documented) | `business/Encryption-and-Cryptography-Policy.pdf` (encryption requirements + standards); `business/Encryption-Key-Management-Procedure.pdf` (key lifecycle); **Gap:** FIPS validation program objectives (module boundary, lab engagement, target security level) are not explicitly documented in business policies. |
| §4 Roles and Responsibilities | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (roles/responsibilities); `business/Information-Security-Policy.pdf` (security roles). |
| §5 Evidence and Records | Partial (documented) | `business/Change-Management-Policy.pdf` (change records/retention expectations); `business/Logging-and-Monitoring-Policy.pdf` (logging/retention); **Gap:** explicit “FIPS validation evidence repository” governance. |
| §6 Review | Met (documented) | Business policies generally include review/update sections (e.g., `business/Information-Security-Policy.pdf` §19 Policy Review and Updates). |
| §7 Document Control | Met (documented) | Business PDFs include document control and revision history sections. |

### `FIPS140-2-compliance-template/procedures/configuration-management-procedure.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Met (documented) | `business/Change-Management-Policy.pdf` (change governance for systems/config); `business/System-Development-Lifecycle-Policy.pdf` (development lifecycle controls) |
| §2 Scope | Met (documented) | `business/Change-Management-Policy.pdf` (scope covers production systems, applications, security configurations) |
| §3 Versioning and Baselines | Met (documented) | `business/Change-Management-Policy.pdf` (§4.4 Version Control; references to Git) |
| §4 Change Control | Met (documented) | `business/Change-Management-Policy.pdf` (§7–§11 change request through post-implementation review; approvals; testing; documentation) |
| §5 Build and Release Evidence | Partial (documented) | `business/System-Development-Lifecycle-Policy.pdf` (development phases and governance); `business/Change-Management-Policy.pdf` (testing/approvals/records); **Gap:** explicit build reproducibility + signed release artifact provenance per crypto module. |
| §6 Access Control | Met (documented) | `business/Access-Control-Policy.pdf` (least privilege, privileged access, authentication/MFA); `business/Change-Management-Policy.pdf` (segregation of duties expectations) |
| §7 Document Control | Met (documented) | Document control exists across business PDFs. |

### `FIPS140-2-compliance-template/procedures/key-management-procedure.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (Purpose and Scope) |
| §2 Scope | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (Scope) |
| §3 Inventory | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (§5 Documentation Requirements / Key Inventory) |
| §4 Key Generation | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (§4.1 Key Generation); `business/Encryption-and-Cryptography-Policy.pdf` (approved standards) |
| §5 Key Entry and Output | Partial (documented) | `business/Encryption-Key-Management-Procedure.pdf` (key distribution and handling); **Gap:** module boundary-specific entry/output mechanisms (wrapping, splitting, establishment) aren’t framed in FIPS terms. |
| §6 Key Storage and Protection | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (§4.2 Key Storage); `business/Encryption-and-Cryptography-Policy.pdf` (key protection principles) |
| §7 Rotation and Revocation | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (§4.4 Rotation; compromise response); `business/Encryption-and-Cryptography-Policy.pdf` (rotation standards) |
| §8 Zeroization | Partial (documented) | `business/Encryption-Key-Management-Procedure.pdf` (§4.6 Key Destruction); **Gap:** explicit “zeroization verifiable by test/inspection” evidence expectations for in-module CSPs. |
| §9 Records | Met (documented) | `business/Encryption-Key-Management-Procedure.pdf` (§5 Documentation Requirements incl. logs/records; exceptions/escalations) |
| §10 Document Control | Met (documented) | Document control exists in the business procedure PDF. |

### `FIPS140-2-compliance-template/procedures/self-tests-procedure.md`

| Template section | Status | Business references (where coverage is documented) |
|---|---|---|
| §1 Purpose | Not evidenced | No business document found that defines cryptographic module power-up/conditional self-tests as required for FIPS validation. |
| §2 Scope | Not evidenced | — |
| §3 Power-Up Self-Tests | Not evidenced | — |
| §4 Conditional Self-Tests | Not evidenced | — |
| §5 Integrity Tests | Partial (documented) | `business/Logging-and-Monitoring-Policy.pdf` (file integrity monitoring concepts); `business/System-Development-Lifecycle-Policy.pdf` (testing expectations). **Gap:** FIPS self-test requirements and pass/fail behavior are not documented. |
| §6 Logging and Evidence | Partial (documented) | `business/Logging-and-Monitoring-Policy.pdf` (logging/retention); **Gap:** self-test specific log and evidence trail. |
| §7 Document Control | Met (documented) | Document control exists across business PDFs. |

### `FIPS140-2-compliance-template/controls/fips-140-2-requirements.md`

**Status:** Not evidenced as implemented (the register entries are marked “Planned” and point to evidence folders that are not populated here).  
Business documentation that can contribute to readiness (governance-level) includes:

- `business/Encryption-and-Cryptography-Policy.pdf`
- `business/Encryption-Key-Management-Procedure.pdf`
- `business/Change-Management-Policy.pdf`
- `business/Access-Control-Policy.pdf`
- `business/Logging-and-Monitoring-Policy.pdf`

However, FIPS 140-2 validation typically requires module-specific technical artifacts and evidence (module boundary/spec, ports & interfaces, FSM, self-test evidence, operational environment constraints, etc.) that are not present under `FIPS140-2-compliance-template/evidence/` in this repo.

