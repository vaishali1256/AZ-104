# Microsoft Entra ID Pricing & Licensing

## Introduction

Microsoft Entra ID offers multiple pricing tiers depending on the level of identity management, security, and governance features required.

When you create a new Microsoft Azure account, you automatically receive access to the **Free Tier** of Microsoft Entra ID.

As organizations grow, they may upgrade to:

* Entra ID Free
* Entra ID P1
* Entra ID P2

Each tier unlocks additional security and identity management capabilities.

The pricing and feature details discussed below are based on the uploaded course notes.

---

# Microsoft Entra ID Pricing Tiers

| Tier | Approximate Cost | Best For                       |
| ---- | ---------------- | ------------------------------ |
| Free | Included         | Small teams / learning         |
| P1   | ~$6/user/month   | Enterprise identity management |
| P2   | ~$9/user/month   | Advanced security & governance |

---

# 1. Microsoft Entra ID Free Tier

The free tier is included with services such as:

* Microsoft Azure
* Microsoft 365
* Dynamics 365
* Intune
* Power Platform

It allows organizations to:

* Create users and groups
* Use basic authentication
* Enable basic MFA
* Use Single Sign-On (SSO)

---

## Features Included in Free Tier

### Identity Management

* Unlimited users and groups (within Microsoft limits)
* Basic user/group management
* Cloud synchronization

### Authentication

* Multi-Factor Authentication (basic)
* Single Sign-On (SSO)
* Federation support

### Access Control

* Role-Based Access Control (RBAC)

---

## Limitations of Free Tier

### No SLA

There is no official Service Level Agreement (SLA).

Meaning:

* Microsoft does not financially guarantee uptime
* No compensation if service issues occur

### No Advanced Security Features

Not included:

* Conditional Access
* Identity Protection
* Advanced reporting
* Risk-based authentication
* AI-based threat detection

---

# 2. Microsoft Entra ID P1

## Cost

```text
~$6 per user/month
```

Organizations can assign P1 licenses only to selected users.

Example:

```text
1000 users total
100 users with P1
900 users on Free Tier
```

---

## Features Included in P1

### Conditional Access

Apply access rules based on:

* User location
* Device type
* Risk level
* Operating system

Example:

```text
If login outside Canada → Require MFA
```

---

### Dynamic Groups

Automatically add users to groups based on attributes.

Example:

```text
Department = HR
→ Automatically added to HR Group
```

---

### Self-Service Password Reset (SSPR)

Users can reset passwords themselves.

In hybrid environments:

```text
Cloud password reset
        ↓
Password Writeback
        ↓
On-Prem Active Directory
```

---

### Azure AD Connect Health

Monitoring for synchronization between:

* On-prem AD
* Entra ID

---

### Provisioning Features

Automated user provisioning for applications.

---

# 3. Microsoft Entra ID P2

## Cost

```text
~$9 per user/month
```

P2 includes everything in:

* Free Tier
* P1 Tier

PLUS advanced security and governance features.

---

# Advanced Security Features in P2

## Identity Protection

AI-based risk detection.

Example:

* Suspicious login attempts
* Impossible travel detection
* Credential stuffing attacks

---

## Risk-Based Conditional Access

Policies can automatically react to risky behavior.

Example:

```text
Risky sign-in detected
→ Block access
→ Require password reset
```

---

## Risky User Detection

Detects unusual account activity.

Example:

* User inactive for years suddenly logs in
* Multiple failed attempts from unknown locations

---

## Access Reviews

Users periodically confirm:

```text
"Do I still need this access?"
```

Helps reduce excessive permissions.

---

## Privileged Identity Management (PIM)

Controls privileged admin access.

Provides:

* Just-in-time access
* Time-limited admin permissions
* Approval workflows

---

# Conditional Access

One of the most important enterprise security features.

Conditional Access allows organizations to create:

```text
IF condition → THEN action
```

Example:

```text
IF login from unknown country
THEN require MFA
```

---

## Common Conditional Access Policies

### Location-Based Access

* Allow office locations
* Block risky countries

### Device Compliance

Require:

* Updated OS
* Managed device
* Antivirus enabled

### Application-Based Policies

Different security requirements for:

* Teams
* Outlook
* Azure Portal

---

# Cross-Tenant Synchronization

Advanced feature allowing synchronization between:

* Multiple organizations
* Multiple Entra tenants

Useful for:

* Mergers
* Partnerships
* B2B collaboration

---

# Identity Governance

Microsoft also provides advanced governance features.

Includes:

* Entitlement management
* Lifecycle workflows
* Access reviews
* Verified ID

Mostly used in enterprise compliance environments.

---

# MFA in Entra ID

Multi-Factor Authentication adds extra security beyond passwords.

Example:

```text
Password
+ OTP
+ Authenticator approval
```

MFA is available even in the free tier for basic scenarios.

---

# Real-World Example

## Small Startup

Uses:

* Free Tier
* Basic MFA
* SSO

---

## Medium Enterprise

Uses:

* P1
* Conditional Access
* Dynamic Groups
* Self-Service Password Reset

---

## Large Enterprise / Bank

Uses:

* P2
* Identity Protection
* Risk Detection
* Access Reviews
* PIM

---

# Important AZ-104 Exam Topics

Know these clearly:

## Free Tier

* Basic identity management
* No advanced security

## P1

* Conditional Access
* Dynamic Groups
* SSPR

## P2

* Identity Protection
* Risk Detection
* Access Reviews
* PIM

---

# Key Terms

## SLA

Service Level Agreement.

Microsoft guarantees uptime/service quality.

---

## RBAC

Role-Based Access Control.

Assign permissions using roles like:

* Owner
* Contributor
* Reader

---

## SSPR

Self-Service Password Reset.

---

## PIM

Privileged Identity Management.

---

# Summary

Microsoft Entra ID licensing provides different levels of:

* Identity management
* Security
* Governance

### Free Tier

Good for:

* Learning
* Small environments
* Basic authentication

### P1

Adds:

* Enterprise identity management
* Conditional access
* Automation features

### P2

Adds:

* Advanced security
* AI-based risk analysis
* Governance capabilities

---

# Final Takeaways

✅ Free Tier = Basic identity management
✅ P1 = Conditional Access + Enterprise features
✅ P2 = Advanced security + Governance
✅ MFA improves authentication security
✅ Conditional Access is a key enterprise feature
✅ PIM and Identity Protection are P2 features
