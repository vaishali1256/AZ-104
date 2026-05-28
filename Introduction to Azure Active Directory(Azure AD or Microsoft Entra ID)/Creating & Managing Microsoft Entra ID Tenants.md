# Creating & Managing Microsoft Entra ID Tenants

## Important Update

Previously, users could create unlimited Azure Active Directory tenants for free.

Now:

* Azure Active Directory is renamed to **Microsoft Entra ID**
* Microsoft has added restrictions on tenant creation
* Some users may not be able to create new tenants

---

# Tenant Creation Changes

## Earlier

Users with:

* Free Azure account
* Pay-as-you-go account

could create multiple Entra ID tenants easily.

---

## Now

Creating a new Microsoft Entra ID tenant may require:

* Microsoft 365 subscription
* Enterprise licensing
* Paid Microsoft services

Some users may only see:

```text id="g5fd1m"
B2C Tenant Creation
```

instead of standard Entra ID tenant creation.

---

# What is a B2C Tenant?

B2C = Business to Consumer

Used for:

* Customer-facing applications
* Social login integrations

Users can sign in using:

* Google
* Microsoft
* LinkedIn
* Facebook

Not the primary focus for AZ-104.

---

# Why Create Your Own Tenant?

If you use your company's tenant:

* You may only be a normal user
* You may not have admin privileges

Creating your own tenant allows you to:

* Become Global Administrator
* Create users/groups
* Test configurations
* Practice P1/P2 features

---

# Steps to Create a New Tenant

## Step 1

Open:

```text id="38p2g2"
Microsoft Entra ID
```

---

## Step 2

Go to:

```text id="w5w1ih"
Manage Tenants
→ Create
```

---

## Step 3

Choose:

```text id="x92s9s"
Microsoft Entra ID
```

---

## Step 4

Provide:

* Organization Name
* Unique Domain Name
* Region/Country

Example:

```text id="9f3c1j"
mycompany.onmicrosoft.com
```

---

## Step 5

Complete CAPTCHA and create tenant.

---

# Important Notes

## Domain Name Must Be Unique

Example:

```text id="r8o7ul"
company.onmicrosoft.com
```

cannot already exist.

---

## Region Selection

Choose the correct region for:

* Compliance
* Data residency
* Legal requirements

Example:

* European companies may prefer EU regions

---

# After Tenant Creation

You are automatically:

# Global Administrator

This is the highest built-in role in Entra ID.

---

# Global Administrator Permissions

Can:

* Create users
* Create groups
* Assign roles
* Configure policies
* Manage applications

Every tenant must have at least:

```text id="e6qzt5"
1 Global Administrator
```

---

# Tenant Overview

After creation, the tenant contains:

* One user (you)
* No groups
* No applications
* No devices

Initially:

```text id="i6uv2m"
License = Free Tier
```

---

# Tenant ID

Each tenant has a unique:

# Tenant ID

Used in:

* PowerShell
* Azure CLI
* Scripts
* Automation

---

# Switching Between Tenants

You can switch tenants using:

## Method 1

```text id="cb9r7s"
Manage Tenants → Switch
```

---

## Method 2

Use profile icon:

```text id="v2cfv5"
Profile → Switch Directory
```

Useful when:

* Managing multiple organizations
* Different admin roles per tenant

---

# Azure AD Free vs Premium

Free tier has limitations.

Some advanced features require:

* P1
* P2

---

# Free Tier Limitations

Cannot access:

* Custom Roles
* Advanced MFA
* Identity Protection
* AI-based threat detection

---

# P1 & P2 Trial

Microsoft provides:

```text id="xqb83u"
30-day free trial
```

for premium features.

Can be activated from:

```text id="mmsd0o"
Roles & Administrators
→ Get Free Trial
```

---

# P2 Features

Premium P2 includes:

* Conditional Access
* Custom Roles
* Risk Detection
* Identity Protection
* Access Reviews
* AI-based security

---

# Important Trial Note

Free trial can only be used:

```text id="u2h1cw"
ONCE
```

After that:

* You must purchase a license

---

# Purchasing P2

Can be purchased through:

```text id="k1c2iq"
Microsoft Admin Center
→ Billing
→ Purchase Services
```

---

# Real-World Scenario

A company may have:

```text id="vltp2l"
Production Tenant
Development Tenant
Testing Tenant
```

Admins can switch between them easily.

---

# Key Concepts

| Concept              | Meaning                    |
| -------------------- | -------------------------- |
| Tenant               | Organization boundary      |
| Global Administrator | Highest admin role         |
| B2C Tenant           | Customer identity platform |
| Tenant ID            | Unique tenant identifier   |
| P1/P2                | Premium Entra features     |

---

# Key Takeaways

✅ Entra ID tenant creation rules have changed
✅ Some accounts cannot create standard tenants
✅ Global Administrator has full control
✅ Multiple tenants can be managed from one account
✅ Free tier has limited features
✅ P1/P2 unlock advanced identity & security features
✅ Tenant switching is simple in Azure Portal
