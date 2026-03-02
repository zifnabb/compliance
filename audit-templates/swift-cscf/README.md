# SWIFT CSCF Compliance Template

A structured, editable template for organizing policy, evidence, and audit artifacts aligned to the **SWIFT Customer Security Controls Framework (CSCF)**.

## Source document

This template is derived from the CSCF document stored in this repo:

- `Source Docs/CSCF_v2026_20250701_compared_to_v2025.pdf` (dated 01 July 2025 in the document)

This template is **not** a substitute for the official SWIFT CSCF documentation, SWIFT guidance, or an external assessment.

## Directory structure

```
├── policies/           # Governance policies for CSCF compliance
├── procedures/         # Local procedures supporting CSCF controls (optional)
├── controls/           # CSCF control register (scope/status/evidence)
├── evidence/           # Evidence and records (dated, attributable)
├── templates/          # Reusable templates for audit/evidence capture
└── audits/             # Internal audit records and readiness checks
```

## Getting started

1. **Choose your architecture type(s)** in `controls/architecture-types.md`.
2. **Populate the control register** in `controls/cscf-controls.md` (owner, status, evidence links).
3. **Create an evidence index** in `evidence/README.md` and add evidence items per control.
4. **Run an internal readiness review** and record results under `audits/`.

## Suggested “minimum viable” evidence package

- Completed `controls/cscf-controls.md` with:
  - status per control,
  - owner per control,
  - evidence references per control (paths/links).
- A control-by-control evidence pack under `evidence/` (or a single index referencing your systems).
- An internal audit record under `audits/` describing:
  - scope,
  - assessment approach,
  - exceptions/compensating controls,
  - findings and remediation plan.

