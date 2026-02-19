# FIPS 140-2 Compliance Template

A structured, editable template for preparing documentation and evidence for a FIPS 140-2 cryptographic module validation effort.

This template shall help you organize artifacts for a lab engagement and CMVP submission. It shall not replace the FIPS 140-2 standard, implementation guidance, or an accredited laboratory assessment.

## Getting Started

1. Define the cryptographic module boundary and the target **Security Level** (1-4).
2. Populate the requirement register in `controls/fips-140-2-requirements.md`.
3. Tailor policies and procedures under `policies/` and `procedures/` to match your design.
4. Collect dated, attributable evidence under `evidence/` using the templates under `templates/`.

## Directory Structure

```
├── policies/           # Governance policies for the crypto module program
├── procedures/         # Operational procedures (key management, CM, self-tests, etc.)
├── controls/           # FIPS 140-2 requirement register and tracking
├── evidence/           # Evidence and records (dated, attributable)
├── templates/          # Reusable templates for FIPS artifacts
└── audits/             # Internal reviews and readiness checks
```

## Core Artifacts (Typical)

- Module boundary description and diagram
- Roles, services, and authentication model
- Finite state model
- Key management specification (generation, storage, entry/exit, zeroization)
- Physical security model and operational environment description
- Self-tests and integrity checks (power-up and conditional)
- Configuration management and design assurance records
- Mitigation of other attacks (if applicable)
