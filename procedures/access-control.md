# Access Control Procedure

**Document ID:** PROC-AC-001  
**Version:** 1.0  
**Effective Date:** [DATE]  
**Owner:** [IT Manager]  
**Classification:** Internal

## 1. Purpose

This procedure defines the processes for managing user access to information systems and data at [Organization Name].

## 2. Scope

This procedure applies to all systems, applications, and data repositories requiring access control.

## 3. Principles

- **Least Privilege:** Users receive minimum access required for their role
- **Need-to-Know:** Access granted only for legitimate business purposes
- **Segregation of Duties:** Critical functions separated to prevent fraud
- **Defense in Depth:** Multiple layers of access control

## 4. User Access Management

### 4.1 Access Request Process

**Step 1: Request Submission**
- User/Manager submits access request form
- Specify systems, access level, and business justification

**Step 2: Authorization**
- Data/System Owner reviews and approves request
- Manager confirms business need

**Step 3: Provisioning**
- IT implements approved access
- User notified of access grant

**Step 4: Documentation**
- Access recorded in access register
- Request form archived

### 4.2 New User Provisioning

| Task | Responsible | Timeline |
|------|-------------|----------|
| HR notification of new hire | HR | Start date - 5 days |
| Manager submits access request | Manager | Start date - 3 days |
| Owner approves access | Data Owner | Within 24 hours |
| IT provisions access | IT | By start date |
| User receives credentials | IT | Start date |
| Security awareness training | Security | Within 7 days |

### 4.3 Access Modification

Triggered by:
- Role change
- Department transfer
- Project assignment
- Promotion/demotion

**Process:**
1. Manager submits modification request
2. Old access reviewed for removal
3. New access approved by owner
4. Changes implemented
5. User notified

### 4.4 Access Revocation

**Termination (Voluntary/Involuntary):**

| Task | Responsible | Timeline |
|------|-------------|----------|
| HR notifies IT of termination | HR | Immediately |
| Disable all accounts | IT | Same day (involuntary: immediate) |
| Retrieve physical access badges | Facilities | Same day |
| Remove from distribution lists | IT | Within 24 hours |
| Archive user data | IT | Within 7 days |
| Delete accounts | IT | After retention period |

**Immediate Revocation Triggers:**
- Termination for cause
- Security incident involvement
- Policy violation
- Suspicious activity

## 5. Privileged Access Management

### 5.1 Privileged Account Types

- System administrators
- Database administrators
- Network administrators
- Security administrators
- Emergency/break-glass accounts

### 5.2 Controls

| Control | Requirement |
|---------|-------------|
| Approval | Information Security Manager/IT Manager approval required |
| Separation | Separate admin and regular accounts |
| MFA | Multi-factor authentication mandatory |
| Logging | All activity logged and monitored |
| Review | Quarterly access review |
| Password | Enhanced password requirements |
| Session | Automatic timeout after inactivity |

### 5.3 Break-Glass Accounts

- Used only in emergencies
- Sealed credentials in secure location
- Usage triggers immediate alert
- Post-use review required
- Password changed after each use

## 6. Authentication Requirements

### 6.1 Password Policy

| Requirement | Standard Users | Privileged Users |
|-------------|---------------|------------------|
| Minimum length | 12 characters | 16 characters |
| Complexity | 3 of 4 character types | 4 of 4 character types |
| Expiration | 90 days | 60 days |
| History | Last 12 passwords | Last 24 passwords |
| Lockout | 5 failed attempts | 3 failed attempts |

### 6.2 Multi-Factor Authentication

**Required for:**
- All remote access
- Privileged accounts
- Cloud services
- Financial systems
- Customer data access

**Accepted factors:**
- Hardware tokens
- Software authenticator apps
- Biometrics
- Smart cards

## 7. Access Reviews

### 7.1 Review Schedule

| Review Type | Frequency | Reviewer |
|-------------|-----------|----------|
| User access | Quarterly | Manager |
| Privileged access | Monthly | IT Manager/Information Security Manager |
| Service accounts | Quarterly | System Owner |
| Terminated users | Weekly | IT/HR |
| External access | Monthly | Information Security Manager |

### 7.2 Review Process

1. Generate access reports
2. Distribute to reviewers
3. Reviewers validate access appropriateness
4. Identify and remove excessive access
5. Document review completion
6. Report findings to management

## 8. Physical Access Control

### 8.1 Access Zones

| Zone | Access Level | Authentication |
|------|--------------|----------------|
| Public | All | None |
| General Office | Employees | Badge |
| Server Room | IT Staff | Badge + PIN |
| Data Center | Authorized IT | Badge + Biometric |

### 8.2 Visitor Management

- Sign in/out required
- Escort in secure areas
- Temporary badge issued
- Badge returned on exit
- Visitor log maintained

## 9. Remote Access

### 9.1 Requirements

- Approved VPN client
- MFA enabled
- Endpoint security verified
- Encrypted connection
- Session timeout configured

### 9.2 Restrictions

- No split tunneling
- Corporate data stays on corporate systems
- No access from public computers
- Automatic disconnect after inactivity

## 10. Roles and Responsibilities

| Role | Responsibility |
|------|----------------|
| HR | Notify IT of personnel changes |
| Manager | Request/approve team access |
| Data Owner | Approve access to owned data |
| IT | Provision and deprovision access |
| Security | Monitor and audit access |
| Users | Protect credentials, report issues |

## 11. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | [DATE] | [Author] | Initial release |
