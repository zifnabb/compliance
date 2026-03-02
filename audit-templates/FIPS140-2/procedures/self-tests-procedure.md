# Self-Tests Procedure (FIPS 140-2)

**Document ID:** FIPS-PROC-002  \
**Version:** 1.0  \
**Effective Date:** 2026-02-19  \
**Owner:** Terrence  \
**Classification:** Internal

## 1. Purpose

This procedure defines how the cryptographic module's power-up and conditional self-tests shall be implemented, executed, monitored, and evidenced.

## 2. Scope

This procedure applies to the in-scope cryptographic module(s) and all deployment environments included in the validation boundary.

## 3. Power-Up Self-Tests

Power-up self-tests shall:
- Execute on initialization as required by the design
- Produce clear pass/fail behavior
- Prevent normal operation when required self-tests fail

## 4. Conditional Self-Tests

Conditional self-tests shall:
- Execute on defined triggering events (e.g., key generation, RNG use, firmware load), as applicable
- Produce clear pass/fail behavior and defined error states

## 5. Integrity Tests

Integrity mechanisms for in-scope firmware/software components shall be documented and tested. Evidence shall be retained under `evidence/self-tests/`.

## 6. Logging and Evidence

Self-test execution evidence shall be recorded using `templates/self-test-log.md`.

## 7. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-02-19 | Terrence | Initial release |
