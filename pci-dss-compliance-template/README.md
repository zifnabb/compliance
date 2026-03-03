# PCI DSS Compliance Template

A structured, editable template for organizing policy, evidence, and audit artifacts aligned to **PCI DSS v4.0.1**.

## Source document

This template is derived from the PCI DSS document stored in this repo:

- `Source Docs/PCI-DSS-v4_0_1.pdf` (PCI DSS Requirements and Testing Procedures, Version 4.0.1, June 2024)

This template is **not** a substitute for the official PCI DSS standard, official PCI SSC guidance, or a QSA-led assessment.

## Directory structure

```
├── policies/           # Governance policies for PCI DSS compliance
├── procedures/         # Local procedures supporting PCI DSS requirements (optional)
├── controls/           # PCI DSS requirement register (scope/status/evidence)
├── evidence/           # Evidence and records (dated, attributable)
├── templates/          # Reusable templates for audit/evidence capture
└── audits/             # Internal audit records and readiness checks
```

## Getting started

1. Define PCI DSS **scope** and your **Cardholder Data Environment (CDE)** in `controls/scope-and-cde.md`.
2. Populate the requirement register in `controls/pci-dss-requirements.md` with owners, status, and evidence references.
3. Build an evidence pack under `evidence/` (or link to systems of record).
4. Run an internal readiness review and store results under `audits/`.

