# Change Management Procedure

**Document ID:** PROC-CHG-001  
**Version:** 1.0  
**Effective Date:** [DATE]  
**Owner:** [IT Manager]  
**Classification:** Internal

## 1. Purpose

This procedure establishes the process for managing changes to information systems, infrastructure, and applications.

## 2. Scope

This procedure applies to all changes to production systems, networks, applications, and security configurations.

## 3. Change Categories

### 3.1 Standard Changes

- Pre-approved, low-risk changes
- Follow established procedure
- No CAB approval required
- Examples: password resets, software updates, user provisioning

### 3.2 Normal Changes

- Require formal approval process
- CAB review for significant changes
- Scheduled implementation
- Examples: new applications, configuration changes, patches

### 3.3 Emergency Changes

- Critical changes to restore service
- Expedited approval process
- Post-implementation review required
- Examples: security patches, outage fixes

## 4. Change Request Process

### 4.1 Step 1: Request Submission

**Requestor completes:**
- Change description
- Business justification
- Impact assessment
- Risk assessment
- Rollback plan
- Implementation schedule
- Testing requirements

### 4.2 Step 2: Initial Review

**Change Manager:**
- Validates completeness
- Assigns change category
- Assigns priority
- Routes for approval

### 4.3 Step 3: Impact Assessment

**Technical Teams assess:**
- Systems affected
- Dependencies
- Resource requirements
- Security implications
- Service impact
- Downtime required

### 4.4 Step 4: Approval

| Change Type | Approver |
|-------------|----------|
| Standard | Pre-approved |
| Normal (Low Risk) | Change Manager |
| Normal (Medium Risk) | CAB |
| Normal (High Risk) | CAB + Executive |
| Emergency | IT Manager (CAB retrospective) |

### 4.5 Step 5: Implementation

- Schedule implementation window
- Notify affected users
- Implement change per plan
- Execute testing
- Verify success criteria

### 4.6 Step 6: Post-Implementation Review

- Confirm change success
- Document actual vs. planned
- Update configuration records
- Close change request
- Capture lessons learned

## 5. Change Advisory Board (CAB)

### 5.1 Composition

- IT Manager (Chair)
- Information Security Manager
- Operations Lead
- Application Owners
- Infrastructure Lead
- Business Representatives (as needed)

### 5.2 Meeting Schedule

- Weekly CAB meetings
- Emergency CAB as needed
- Virtual attendance permitted

### 5.3 Responsibilities

- Review change requests
- Assess risks and impacts
- Approve or reject changes
- Prioritize change schedule
- Review failed changes

## 6. Risk Assessment

### 6.1 Risk Factors

| Factor | Low (1) | Medium (2) | High (3) |
|--------|---------|------------|----------|
| Impact scope | Single system | Multiple systems | Enterprise |
| Reversibility | Easy rollback | Complex rollback | Irreversible |
| Testing | Fully tested | Partially tested | Untested |
| Experience | Routine change | Some experience | First time |
| Timing | Off-hours | Business hours | Peak hours |

### 6.2 Risk Level Determination

| Total Score | Risk Level | Approval |
|-------------|------------|----------|
| 5-8 | Low | Change Manager |
| 9-12 | Medium | CAB |
| 13-15 | High | CAB + Executive |

## 7. Emergency Change Process

### 7.1 Criteria

Emergency changes are only for:
- Security vulnerabilities under active exploit
- System outages affecting business operations
- Regulatory compliance requirements
- Safety-critical issues

### 7.2 Process

1. IT Manager approval (verbal acceptable)
2. Implement change
3. Document change retrospectively
4. Submit for CAB review at next meeting
5. Update standard change library if applicable

## 8. Rollback Procedures

### 8.1 Rollback Criteria

- Change causes service degradation
- Unacceptable errors introduced
- Security vulnerabilities created
- Stakeholder requests rollback

### 8.2 Rollback Process

1. Decision made by Change Manager
2. Notify stakeholders
3. Execute rollback plan
4. Verify service restoration
5. Document incident
6. Conduct root cause analysis

## 9. Documentation Requirements

### 9.1 Change Request Record

- Unique change ID
- Description and justification
- Impact and risk assessment
- Approvals obtained
- Implementation plan
- Test results
- Rollback plan
- Post-implementation review

### 9.2 Retention

- Change records retained for 3 years
- Audit trail maintained
- Configuration updates documented

## 10. Metrics and Reporting

### 10.1 Key Metrics

| Metric | Target |
|--------|--------|
| Change success rate | > 95% |
| Emergency change ratio | < 10% |
| Changes causing incidents | < 5% |
| Unauthorized changes | 0 |

### 10.2 Reporting

- Weekly change summary
- Monthly metrics report
- Quarterly trend analysis

## 11. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [Author] | Initial release |
