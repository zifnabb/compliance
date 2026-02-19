# FIPS 140-2 Requirement Register

**Document ID:** FIPS-CTL-001  \
**Version:** 1.0  \
**Last Updated:** 2026-02-19  \
**Owner:** Terrence  \
**Classification:** Internal

## Overview

This register tracks readiness for FIPS 140-2 validation. Each area shall have an owner, implementation notes, and evidence references. Entries shall be refined as the module design and lab feedback evolve.

## Status Legend

| Status | Meaning |
|--------|---------|
| Implemented | Requirement is implemented and evidenced |
| In Progress | Implementation or evidence collection is underway |
| Planned | Work is scheduled but not started |
| Not Applicable | Not applicable to the module scope/level (justify) |

## 1. Cryptographic Module Specification

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/module-spec/`  \
- **Notes:** Module description, boundary definition, approved modes, ports/interfaces, and architecture shall be documented.

## 2. Cryptographic Module Ports and Interfaces

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/ports-interfaces/`  \
- **Notes:** Logical/physical interfaces, data/control/status/output separation, and interface documentation shall be maintained.

## 3. Roles, Services, and Authentication

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/roles-services/`  \
- **Notes:** Operator roles, services, and authentication mechanisms and strength shall be defined and evidenced.

## 4. Finite State Model

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/state-model/`  \
- **Notes:** A finite state model for the module shall be documented and consistent with the design.

## 5. Physical Security

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/physical-security/`  \
- **Notes:** The physical embodiment, tamper-evidence/tamper-response features (as required), and operational guidance shall be documented.

## 6. Operational Environment

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/operational-environment/`  \
- **Notes:** The operational environment type and associated controls shall be documented.

## 7. Cryptographic Key Management

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/key-management/`  \
- **Notes:** Keys and CSPs shall have documented lifecycle handling (generation, entry/exit, storage, use, and zeroization).

## 8. EMI/EMC

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/emi-emc/`  \
- **Notes:** EMI/EMC requirements shall be addressed per the target security level and module type.

## 9. Self-Tests

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/self-tests/`  \
- **Notes:** Power-up and conditional self-tests and integrity checks shall be defined, implemented, and logged.

## 10. Design Assurance (Configuration Management)

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/configuration-management/`  \
- **Notes:** Configuration management, versioning, change control, and reproducible build/firmware provenance shall be maintained.

## 11. Mitigation of Other Attacks

- **Status:** Planned  \
- **Owner:** [Owner]  \
- **Evidence:** `evidence/other-attacks/`  \
- **Notes:** If claimed, mitigations (e.g., timing or power analysis) shall be described and evidenced.

## Summary

| Area | Status | Primary Evidence Location |
|------|--------|---------------------------|
| 1. Module Spec | Planned | `evidence/module-spec/` |
| 2. Ports/Interfaces | Planned | `evidence/ports-interfaces/` |
| 3. Roles/Services/Auth | Planned | `evidence/roles-services/` |
| 4. State Model | Planned | `evidence/state-model/` |
| 5. Physical Security | Planned | `evidence/physical-security/` |
| 6. Operational Environment | Planned | `evidence/operational-environment/` |
| 7. Key Management | Planned | `evidence/key-management/` |
| 8. EMI/EMC | Planned | `evidence/emi-emc/` |
| 9. Self-Tests | Planned | `evidence/self-tests/` |
| 10. Configuration Management | Planned | `evidence/configuration-management/` |
| 11. Other Attacks | Planned | `evidence/other-attacks/` |
