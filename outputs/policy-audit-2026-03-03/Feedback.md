# Feedback (for moving findings toward “Met”)

**Based on:** `outputs/policy-audit-2026-03-03/iso27001-policy-audit.md` and `outputs/policy-audit-2026-03-03/fips140-2-policy-audit.md`  
**Goal:** Add/clarify language in the **existing documents in this repo** so more sections can be assessed as “Met (documented)”.

---

## Highest-impact changes (do these first)

1. **Define ISMS scope/boundary explicitly** (currently “Not evidenced” in ISO template mapping).
2. **Make objectives measurable and consolidated** (ISO template expects measurable objectives; business docs have metrics scattered).
3. **Populate the ISO Annex A control register and risk register template with real values** (owners, status, evidence pointers).
4. **Fill missing approval metadata in several “Procedure” PDFs** (headers show `Approved:` blank).
5. **Create/clarify FIPS-specific items that are absent in business docs** (self-tests, module boundary, module-specific evidence governance).

---

## ISO 27001 template: additions/clarifications to get more “Met”

### 1) `iso27001-compliance-template/policies/isms-policy.md`

**What’s preventing “Met”:** Missing explicit ISMS boundary; objectives table is placeholder; approval table is blank.

**Additions/clarifications to make:**

- **§2.1 ISMS Boundary (make this explicit and auditable):**
  - Name the in-scope product/service (e.g., “DoBusiness Suite Platform”).
  - List in-scope locations, environments (prod/non-prod), and supporting functions (engineering, IT, support).
  - State in-scope information types (customer data, employee data, logs, backups).
  - State explicit exclusions (e.g., “customer-managed endpoints”, “third-party HR system” if applicable).
  - Reference the governing business policies that define scope elements:
    - `business/Information-Security-Policy.pdf` (Scope; systems/locations/personnel)
    - `business/Network-Security-Policy.pdf`, `business/Physical-Security-Policy.pdf`
    - `business/Vendor-Risk-Management-Policy.pdf` (for suppliers in scope)

- **§3.1 Measurable Objectives (replace placeholders with real targets and point to where measurement comes from):**
  - Use existing policy-defined metrics as the source of truth:
    - Vulnerability remediation / patch SLAs: `business/Vulnerability-Management-and-Patch-Management-Policy.pdf`
    - Change success rate / emergency change ratio: `business/Change-Management-Policy.pdf`
    - Training completion: `business/Security-Awareness-Training-Policy.pdf` + `business/Security-Awareness-Training-Delivery-and-Tracking-Procedure.pdf`
    - Logging/monitoring coverage + retention: `business/Logging-and-Monitoring-Policy.pdf`

- **§7 Continual Improvement (make it explicit rather than implied):**
  - Reference the specific mechanisms already present in business policies:
    - Post-incident review/lessons learned: `business/Incident-Response-Policy.pdf`
    - Vulnerability lifecycle + continuous improvement: `business/Vulnerability-Management-and-Patch-Management-Policy.pdf`
    - Policy review cadence: `business/Information-Security-Policy.pdf` (Policy Review and Updates)
  - Add a short list of required ISMS CI inputs (audit results, KPIs, incidents, risk register changes) and outputs (corrective actions, updates).

- **§9 Approval (make this passable):**
  - Populate role/name/date fields and align them to your governance model (CEO / CTO/CISO / Compliance).
  - If signatures aren’t practical in Markdown, state: “Approvals recorded in [system] and exported to `iso27001-compliance-template/evidence/approvals/`”.

### 2) `iso27001-compliance-template/controls/annex-a-controls.md`

**What’s preventing “Met”:** It’s a blank register (everything “Planned”, no owners/evidence).

**Additions/clarifications to make:**

- For each Annex A control you want to claim as **Implemented**, fill:
  - **Status:** Implemented
  - **Owner:** real role/person
  - **Evidence:** link to business documents in this repo (at minimum) and/or evidence folder paths
  - **Notes:** one-sentence implementation summary + where it is enforced

**Fast path to high “Met” coverage using existing business docs:**

- Policies / governance (A.5): map heavily to `business/Information-Security-Policy.pdf`, `business/Risk-Management-Policy.pdf`, `business/Vendor-Risk-Management-Policy.pdf`, `business/Privacy-Policy.pdf`.
- People controls (A.6): map to `business/Background-Check-Process-Procedure.pdf`, `business/Security-Awareness-Training-Policy.pdf`, `business/Employee-Code-of-Conduct.pdf`, onboarding/offboarding procedures.
- Physical (A.7): map to `business/Physical-Security-Policy.pdf`.
- Technological (A.8): map to `business/Access-Control-Policy.pdf`, `business/Network-Security-Policy.pdf`, `business/Logging-and-Monitoring-Policy.pdf`, `business/Vulnerability-Management-and-Patch-Management-Policy.pdf`, `business/Backup-and-Recovery-Policy.pdf`, `business/Anti-Malware-Policy.pdf`, `business/Encryption-and-Cryptography-Policy.pdf`.

### 3) `iso27001-compliance-template/templates/risk-register.md`

**What’s preventing “Met”:** Template exists but there’s no completed risk register artifact.

**Additions/clarifications to make:**

- Create a filled risk register file under `iso27001-compliance-template/evidence/` (or alongside template if you prefer) and:
  - Reference `business/Risk-Management-Policy.pdf` as the methodology.
  - Add owners, likelihood/impact, treatment, due dates, residual risk, and review date fields.
  - Cross-link to implementing policies for treatments (e.g., vuln mgmt policy for patching, access control policy for IAM risks).

### 4) `iso27001-compliance-template/policies/information-security-policy.md`

**What’s preventing “Met”:** Mostly OK, but it uses generic placeholders and lacks direct mapping to your existing business policy set.

**Additions/clarifications to make:**

- Replace `[Organization Name]` with the business entity name used in PDFs (“DoBusiness Suite Platform / Custom Business SaaS Inc.” as appropriate).
- Add a short “Related policies” section (or expand Notes) that explicitly names the authoritative `business/*.pdf` documents for each subsection:
  - Access Control → `business/Access-Control-Policy.pdf`
  - Data Classification → `business/Data-Classification-and-Handling-Policy.pdf` (+ procedure)
  - Acceptable Use → `business/Acceptable-Use-Policy.pdf`
  - Crypto → `business/Encryption-and-Cryptography-Policy.pdf` (+ key mgmt procedure)
  - Incident response → `business/Incident-Response-Policy.pdf`
  - Monitoring → `business/Logging-and-Monitoring-Policy.pdf`

### 5) “Violations / disciplinary process” clarity (ISO template §4.2)

**What’s preventing “Met”:** The ISO template expects explicit consequences; business coverage is distributed.

**Additions/clarifications to make (choose one path):**

- **Path A (lowest effort):** Add a short “Violations and enforcement” section to `iso27001-compliance-template/policies/information-security-policy.md` that points to:
  - `business/Employee-Code-of-Conduct.pdf` (disciplinary expectations)
  - `business/Acceptable-Use-Policy.pdf` (acceptable use violations)
  - `business/Access-Control-Policy.pdf` (unauthorized access)

- **Path B (cleaner governance):** Add a single “Policy Compliance & Enforcement Standard” document under `iso27001-compliance-template/policies/` that consolidates violations, sanctions, exception handling, and reporting. (Still “within provided docs” in the repo.)

---

## FIPS 140-2 template: additions/clarifications to get more “Met”

### 1) `FIPS140-2-compliance-template/policies/cryptographic-module-security-policy.md`

**What’s preventing “Met”:** It’s module-program specific, but business docs are general org security/crypto docs; the missing piece is explicit module boundary + program governance linkage.

**Additions/clarifications to make:**

- Replace `[Organization Name]` and add:
  - **Named module(s)** in scope (exact name/version)
  - **Target FIPS level** (e.g., Level 1/2/3/4) and intended operational environment type
  - **Module boundary definition pointer** (e.g., “See `evidence/module-spec/` module specification”)
  - Explicit statement that `business/Encryption-and-Cryptography-Policy.pdf` is the org-level policy and this FIPS policy is the validation-program overlay.

### 2) `FIPS140-2-compliance-template/procedures/configuration-management-procedure.md`

**What’s preventing “Met”:** Business change mgmt is strong, but FIPS expects build/release provenance, baselines, and evidence handling.

**Additions/clarifications to make:**

- Add explicit baseline contents (commit hash, build container image digest, dependency lockfiles, compiler versions, build flags).
- Add a requirement to store release artifacts + checksums/signatures in `FIPS140-2-compliance-template/evidence/configuration-management/`.
- Cross-reference:
  - `business/Change-Management-Policy.pdf` (approval/testing)
  - `business/System-Development-Lifecycle-Policy.pdf` (SDLC governance)
  - `business/Access-Control-Policy.pdf` (access restrictions for repos/build keys)

### 3) `FIPS140-2-compliance-template/procedures/key-management-procedure.md`

**What’s preventing “Met”:** Business key mgmt exists; the missing piece is FIPS/module framing (entry/output, CSP handling in-module, zeroization evidence).

**Additions/clarifications to make:**

- Add a table that maps **key/CSP types** → **storage location** → **entry/output method** → **zeroization mechanism** → **evidence artifact**.
- Add explicit “zeroization verification” expectation (test case IDs / inspection evidence).
- Cross-reference:
  - `business/Encryption-and-Cryptography-Policy.pdf`
  - `business/Encryption-Key-Management-Procedure.pdf`

### 4) `FIPS140-2-compliance-template/procedures/self-tests-procedure.md`

**What’s preventing “Met”:** No corresponding business document; the template itself exists and can be made auditable by making it module-specific.

**Additions/clarifications to make:**

- List required self-tests for the actual module design (power-up + conditional) and:
  - triggering conditions,
  - pass/fail behavior (including “no crypto operations until self-tests pass” if applicable),
  - logging requirements,
  - where logs are stored (`evidence/self-tests/`).
- Map integrity tests to your runtime (binary signing, hash checks, FIM interaction) and connect to:
  - `business/Logging-and-Monitoring-Policy.pdf` (FIM concepts)
  - `business/System-Development-Lifecycle-Policy.pdf` (testing requirements)

### 5) `FIPS140-2-compliance-template/controls/fips-140-2-requirements.md`

**What’s preventing “Met”:** Everything is “Planned”, and evidence folders aren’t populated.

**Additions/clarifications to make (documentation-only improvements):**

- Change each section’s **Status/Owner** from placeholders to real values.
- For each requirement area, add at least:
  - a link to the specific template artifact you will produce (e.g., module spec, ports/interfaces, FSM),
  - the primary related business policies (crypto, key mgmt, change mgmt, access control, logging).
- Add a “Minimum evidence set for readiness review” subsection per area (1–3 bullets).

---

## Governance hygiene that will improve audit outcomes quickly

### A) Fill blank `Approved:` headers in procedure PDFs

The following have `Approved:` blank in their PDF header (as extracted from text in this repo):

- `business/Background-Check-Process-Procedure.pdf`
- `business/Data-Classification-Procedure.pdf`
- `business/Data-Disposal-and-Destruction-Procedure.pdf`
- `business/Data-Residency-Verification-Procedure.pdf`
- `business/Encryption-Key-Management-Procedure.pdf`
- `business/Security-Awareness-Training-Delivery-and-Tracking-Procedure.pdf`
- `business/Security-Offboarding-Procedure.pdf`
- `business/Security-Onboarding-Checklist-Procedure.pdf`
- `business/Vendor-Incident-Notification-Handling-Procedure.pdf`
- `business/Vendor-Onboarding-Security-Review-Procedure.pdf`
- `business/Vendor-Performance-Monitoring-and-Review-Procedure.pdf`

**Clarification to add (minimum):** approver role + approval date + next review date. This alone often moves “Partial” to “Met” for governance checks.

### B) Align names and cross-references

- Standardize on one organization name string across templates (ISO/FIPS) and match what business PDFs use.
- Where a business policy says “see X policy/procedure”, ensure X exists in the repo under the referenced name (example: business InfoSec policy references “Password Standards” but no standalone document is present here).

---

## Optional (but high leverage) additions within existing repo documents

If your auditors expect “single-source-of-truth” mapping rather than distributed references:

- Add `iso27001-compliance-template/policies/document-hierarchy.md` that states which docs are authoritative (business vs ISO templates) and how conflicts are resolved.
- Add a one-page “Scope Statement” under `iso27001-compliance-template/policies/` and reference it from ISMS policy and Annex A register.

