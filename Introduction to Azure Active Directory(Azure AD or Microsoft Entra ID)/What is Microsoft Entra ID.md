# Microsoft Entra ID (Azure Active Directory)

## Introduction

Identity and Access Management (IAM) is one of the core pillars of cloud security.
In Microsoft Azure, the primary identity platform is **Microsoft Entra ID**.

Previously known as **Azure Active Directory (Azure AD)**, Microsoft renamed the service to **Microsoft Entra ID**.
You may still see both names used interchangeably across documentation, tutorials, and courses.

---

# What is Microsoft Entra ID?

Microsoft Entra ID is a **cloud-native identity and access management service** used to:

* Manage users and groups
* Authenticate users
* Control access to applications and resources
* Enable Single Sign-On (SSO)
* Secure identities using Multi-Factor Authentication (MFA)

It acts as the central identity provider for:

* Microsoft Azure
* Microsoft 365
* SaaS applications
* Custom cloud applications

---

# Identity Management

Identity management refers to:

* Creating user accounts
* Managing passwords
* Verifying identities
* Assigning permissions
* Securing authentication

Good identity management is a critical part of cloud security.

Example:

```text
User → Login → Authentication → Authorization → Access Granted
```

---

# Active Directory vs Entra ID

Microsoft Entra ID evolved from traditional **Microsoft Active Directory (AD)**.

## Microsoft Active Directory (On-Premises)

Traditional Active Directory is:

* Installed on company servers
* Used inside office networks
* Responsible for:

  * Users
  * Computers
  * Groups
  * Policies

### Protocols Used

* LDAP
* Kerberos

These protocols are mainly designed for internal/private networks.

---

## Microsoft Entra ID (Cloud)

Entra ID is the cloud version of identity management.

It is designed for:

* Internet-based authentication
* Cloud applications
* Remote users
* SaaS integrations

### Protocols Used

* OAuth
* SAML
* OpenID Connect

These are internet-friendly authentication protocols.

---

# Key Difference

| Active Directory                    | Entra ID                   |
| ----------------------------------- | -------------------------- |
| On-premises                         | Cloud-based                |
| Uses LDAP/Kerberos                  | Uses OAuth/SAML            |
| Requires servers/domain controllers | Fully managed by Microsoft |
| Best for internal networks          | Best for cloud & SaaS      |

---

# Hybrid Identity

Most organizations use a **Hybrid Identity** model.

Example:

```text
On-Prem AD  <---- Sync ---->  Microsoft Entra ID
```

This allows users to:

* Use same credentials everywhere
* Access both on-prem and cloud resources

---

# Authentication Protocols

## LDAP

Used for querying directory information in traditional AD.

## Kerberos

Authentication protocol used in Windows domains.

## OAuth

Used for secure authorization in cloud apps.

Example:

* Login with Microsoft
* Login with Google

## SAML

Used for Single Sign-On (SSO) between applications.

---

# Multi-Factor Authentication (MFA)

MFA adds an extra layer of security.

Instead of only:

```text
Username + Password
```

Users may also need:

* OTP
* Authenticator app approval
* Fingerprint
* Security key

Example:

```text
Password + Phone Verification
```

---

# Single Sign-On (SSO)

SSO allows users to:

* Login once
* Access multiple applications

Example:

```text
One Login → Teams + Outlook + OneDrive
```

---

# Managed Identity

Applications also need identities.

Using real user credentials for applications is bad practice because:

* Password changes break apps
* User accounts may get disabled

## Managed Identity

Azure can automatically create and manage identities for applications.

Benefits:

* No hardcoded passwords
* More secure
* Easier management

---

# Entra ID Integrations

Entra ID can integrate with:

* Microsoft 365
* OneDrive
* Dropbox
* SaaS applications
* Custom enterprise applications

It supports centralized authentication and authorization.

# Why Entra ID Matters

Entra ID is essential for:

* Cloud security
* Identity protection
* Secure remote access
* Enterprise authentication
* Zero Trust architecture

It is one of the most important services in Microsoft Azure.

---

# Summary

* Azure Active Directory is now called Microsoft Entra ID
* Entra ID is Microsoft's cloud identity platform
* Traditional Active Directory is on-premises
* Entra ID uses modern internet authentication protocols
* MFA and SSO are core security features
* Hybrid identity is common in enterprises
* Managed identities improve application security

---

# Key Takeaways

✅ Entra ID = Cloud Identity Provider
✅ Active Directory = On-Prem Identity System
✅ OAuth/SAML = Cloud Authentication Protocols
✅ LDAP/Kerberos = Traditional AD Protocols
✅ MFA improves security
✅ SSO improves user experience
✅ Hybrid Identity connects on-prem and cloud

