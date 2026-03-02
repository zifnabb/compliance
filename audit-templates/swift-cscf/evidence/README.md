# Evidence (CSCF)

Evidence should be **dated**, **attributable**, and **traceable to a CSCF control**.

## Recommended structure

Create subfolders per control, for example:

```
evidence/
  1.1-swift-environment-protection/
  1.2-os-privileged-account-control/
  4.2-mfa/
  6.4-logging-and-monitoring/
  ...
```

## Evidence checklist (per control)

- Policy/procedure reference(s)
- System configuration or screenshots (redacted as needed)
- Reports (e.g., patch status, vulnerability scans, access reviews)
- Logs or monitoring exports (summaries preferred; retain raw logs in system of record)
- Tickets/change records showing implementation
- Exception record (if applicable)

## Evidence index (optional but recommended)

Maintain an index file (or spreadsheet) mapping:

- control ID → evidence items → location → date → owner.

The simplest approach is to use one `templates/control-assessment-record.md` per control and link it from `controls/cscf-controls.md`.

