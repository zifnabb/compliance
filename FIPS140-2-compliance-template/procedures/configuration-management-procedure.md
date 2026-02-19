# Configuration Management Procedure (FIPS 140-2)

**Document ID:** FIPS-PROC-003  \
**Version:** 1.0  \
**Effective Date:** 2026-02-19  \
**Owner:** Terrence  \
**Classification:** Internal

## 1. Purpose

This procedure defines how the cryptographic module's source, build inputs, releases, and validation evidence shall be controlled to support FIPS 140-2 design assurance expectations.

## 2. Scope

This procedure applies to:
- Source code and build configuration within the module boundary
- Tooling and build inputs required to reproduce releases
- Released binaries/firmware and their provenance
- Documentation and evidence used for validation

## 3. Versioning and Baselines

- Each release candidate shall have a unique version identifier.
- A baseline shall capture source revision, build configuration, dependencies, and build environment identifiers.

## 4. Change Control

- Changes shall be requested, reviewed, approved, implemented, and recorded.
- Security-impacting changes shall include a risk assessment and testing evidence.

Template: `templates/change-record.md`

## 5. Build and Release Evidence

- Build steps and outputs shall be recorded for each release candidate.
- Checksums and signatures shall be generated and stored where applicable.

Evidence location: `evidence/configuration-management/`

## 6. Access Control

Access to repositories, build systems, and release keys shall be restricted to authorized roles and recorded.

## 7. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-02-19 | Terrence | Initial release |
