# Azure Account vs Tenant vs Subscription

## Introduction

In Microsoft Azure and Microsoft Entra ID, three important concepts are:

* Account (User)
* Tenant
* Subscription

These are separate concepts but work together in Azure environments.

---

# 1. Account / User

An account represents:

* A person
* An application
* A service

Example:

```text
john@example.com
```

It is used to:

* Login to Azure Portal
* Access resources
* Perform actions based on permissions

Authentication may include:

* Password
* MFA (Multi-Factor Authentication)

---

## Managed Identity

Applications also need identities.

Using a real user's credentials for applications is bad practice because:

* Password changes can break the app
* Disabled user accounts stop the app

### Solution:

Use **Managed Identity**

Azure automatically manages authentication for the application.

Benefits:

* More secure
* No hardcoded passwords
* Easier management

---

# 2. Tenant

A tenant represents:

* Organization
* Company
* Business

It contains:

* Users
* Groups
* Applications
* Policies

Example:

```text
company.onmicrosoft.com
```

You can also add custom domains like:

```text
company.com
```

---

## Important Notes

* Every Azure environment requires a tenant
* A domain can belong to only ONE tenant
* One tenant can contain many users

---

# 3. Subscription

A subscription is the:

# Billing arrangement in Azure

Examples:

* Free Trial
* Pay-As-You-Go
* Enterprise Agreement

Subscriptions are used to:

* Pay for Azure resources
* Manage costs
* Control resource usage

---

# Important Points

## A Tenant Can Exist Without a Subscription

But:

* You cannot create Azure resources

---

## A Tenant Can Have Multiple Subscriptions

Example:

```text
Dev Subscription
Test Subscription
Production Subscription
```

That is why Azure asks you to choose a subscription while creating resources.

---

# Relationship Between Them

```text
User → belongs to Tenant
Tenant → contains Subscription(s)
Subscription → pays for Azure resources
```

---

# Roles & Permissions

Users inside a tenant can have different roles:

Examples:

* Owner
* Contributor
* Reader

Azure also provides many fine-grained RBAC roles.

---

# Quick Summary

| Concept      | Meaning                       |
| ------------ | ----------------------------- |
| Account/User | Identity used to login        |
| Tenant       | Organization boundary         |
| Subscription | Billing/account for resources |

---

# Key Takeaways

✅ User = Person/Application identity
✅ Tenant = Organization in Azure
✅ Subscription = Billing model
✅ One tenant can have multiple subscriptions
✅ Managed Identity is used for applications
✅ RBAC controls permissions
