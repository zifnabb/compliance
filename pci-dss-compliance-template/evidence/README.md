# Evidence (PCI DSS)

Evidence should be **dated**, **attributable**, and traceable to PCI DSS requirements and scope.

## Recommended structure

```
evidence/
  01-network-security/
  02-secure-configurations/
  03-protect-stored-account-data/
  04-encrypt-transmission/
  05-malware/
  06-secure-sdlc/
  07-access-need-to-know/
  08-authentication/
  09-physical-security/
  10-logging-monitoring/
  11-testing/
  12-program-governance/
```

## Minimum evidence set (guidance)

- PCI scope and CDE definition: `controls/scope-and-cde.md`
- Requirement register with links: `controls/pci-dss-requirements.md`
- Evidence items per requirement (policies, configs, reports, logs, tickets, scans, pen tests)
- Exception/compensating controls records (if any)
- Internal audit/readiness review report under `audits/`

