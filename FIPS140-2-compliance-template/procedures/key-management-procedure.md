# Key Management Procedure (FIPS 140-2)

**Document ID:** FIPS-PROC-001  \
**Version:** 1.0  \
**Effective Date:** 2026-02-19  \
**Owner:** Terrence  \
**Classification:** Internal

## 1. Purpose

This procedure defines how cryptographic keys and other CSPs shall be generated, stored, distributed, used, rotated, and zeroized for the in-scope cryptographic module(s).

## 2. Scope

This procedure applies to:
- Keys and CSPs handled by the module within the defined boundary
- Supporting operational processes that interact with keys and CSPs (e.g., provisioning)

## 3. Inventory

An inventory of keys and CSPs shall be maintained using `templates/key-and-csp-inventory.md`.

## 4. Key Generation

- Key generation methods shall be documented per key type and use.
- Randomness sources and their use shall be documented where applicable to the module design.

## 5. Key Entry and Output

- Key entry and output methods shall be documented, including any wrapping, splitting, or key establishment mechanisms.
- Keys and CSPs shall not be output in plaintext unless required and justified for the design and target security level.

## 6. Key Storage and Protection

- Keys and CSPs shall be protected in storage according to their sensitivity and the target security level.
- Access to keys and CSPs shall be restricted to authorized roles and services.

## 7. Rotation and Revocation

- Rotation intervals and triggers shall be defined per key type.
- Revocation and replacement procedures shall be documented and tested.

## 8. Zeroization

- Zeroization mechanisms shall be documented per key/CSP type and storage location.
- Zeroization shall be verifiable (by test or inspection as appropriate) and evidence shall be retained.

## 9. Records

Key management evidence shall be stored under `evidence/key-management/`.

## 10. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-02-19 | Terrence | Initial release |
