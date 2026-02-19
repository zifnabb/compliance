# Cryptographic Module Security Policy (FIPS 140-2)

**Document ID:** FIPS-POL-001  \
**Version:** 1.0  \
**Effective Date:** 2026-02-19  \
**Owner:** Terrence  \
**Classification:** Internal

## 1. Purpose

This policy defines governance, security objectives, and minimum requirements for [Organization Name]'s cryptographic module validation program aligned to FIPS 140-2.

## 2. Scope

This policy applies to:
- The cryptographic module(s) in scope for validation
- All personnel who design, build, test, release, operate, or support the module(s)
- All assets and processes supporting module development and validation evidence

## 3. Objectives

[Organization Name] shall:
- Define and maintain a clear cryptographic module boundary
- Implement approved cryptographic algorithms and modes as required
- Protect cryptographic keys and CSPs throughout their lifecycle
- Maintain reliable self-tests and integrity mechanisms
- Maintain design assurance and configuration management suitable for validation

## 4. Roles and Responsibilities

- **Program Owner:** Shall own validation scope, target security level, and lab engagement.
- **Engineering Owner:** Shall implement and maintain technical controls and module documentation.
- **Security/Compliance Owner:** Shall maintain this repository, evidence quality, and review cadence.

## 5. Evidence and Records

Validation-related evidence shall be:
- Dated and attributable (who/what/when)
- Stored under `evidence/` with consistent naming
- Protected from unauthorized modification where feasible

## 6. Review

This policy shall be reviewed at least annually and whenever the module boundary, target security level, or major release changes.

## 7. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-02-19 | Terrence | Initial release |
