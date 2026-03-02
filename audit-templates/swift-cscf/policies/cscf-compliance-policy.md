# CSCF Compliance Policy (SWIFT CSP)

**Document ID:** CSCF-POL-001  
**Version:** 1.0  
**Effective Date:** [DATE]  
**Owner:** [Owner]  
**Classification:** Internal

## 1. Purpose

This policy defines governance and minimum requirements for maintaining compliance with the SWIFT Customer Security Controls Framework (CSCF) as part of the Customer Security Programme (CSP).

## 2. Scope

This policy applies to:

- All SWIFT-related systems, components, and supporting infrastructure in scope for CSCF compliance.
- All personnel who administer, operate, support, or use SWIFT-related services in scope.
- All third parties providing outsourced or cloud services that affect in-scope components.

The applicable architecture type(s) shall be recorded in `controls/architecture-types.md`.

## 3. Roles and responsibilities

- **Executive sponsor:** accountable for resourcing and program oversight.
- **CSP/CSCF owner:** accountable for control register maintenance, attestation readiness, and remediation tracking.
- **System owners:** accountable for implementing and evidencing assigned controls.
- **Third-party/vendor owners:** accountable for supplier assurance and contract requirements where outsourcing applies.

## 4. Control management

1. The authoritative internal register is `controls/cscf-controls.md`.
2. Each control shall have:
   - an owner,
   - a status (Implemented / In Progress / Planned / Not Applicable),
   - evidence references in `evidence/` (or pointers to systems of record),
   - review cadence and last review date.
3. Controls marked **Not Applicable** must include a written justification referencing the selected architecture type(s) and scope.

## 5. Assessment and audit readiness

- Evidence shall be maintained as described in `evidence/README.md`.
- Internal readiness reviews shall be recorded under `audits/`.
- Where you rely on an independent audit/certification/assessment, record:
  - the assessment scope,
  - the date,
  - the assessor,
  - and which CSCF control(s) it supports.

Use `templates/control-assessment-record.md` to record consistent test steps and results.

## 6. Exceptions

Exceptions require:

- business justification,
- documented risk assessment and compensating controls,
- approval by the CSCF owner and executive sponsor (or delegated authority),
- an expiry date and review date,
- tracking in an exceptions log.

Use `templates/exception-record.md`.

## 7. Review

This policy shall be reviewed at least annually and when there are significant changes to:

- SWIFT-related architecture,
- outsourced services,
- threat landscape,
- or SWIFT CSCF requirements.

