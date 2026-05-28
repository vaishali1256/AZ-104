# Custom Domains in Microsoft Entra ID

## Introduction

When creating a Microsoft Entra ID tenant, Azure automatically assigns a default domain name.

Example:

```text id="xq6msp"
mycompany.onmicrosoft.com
```

This domain becomes part of:

* Usernames
* Authentication
* Identity management

---

# Why Custom Domains Are Needed

By default, users would look like:

```text id="n4p0q7"
john@mycompany.onmicrosoft.com
```

But organizations usually want professional usernames such as:

```text id="5zq5qi"
john@example.com
```

To achieve this, we add a:

# Custom Domain

---

# Default Domain vs Custom Domain

| Type           | Example                 |
| -------------- | ----------------------- |
| Default Domain | company.onmicrosoft.com |
| Custom Domain  | company.com             |

---

# Adding a Custom Domain

Go to:

```text id="7r7h4x"
Entra ID
→ Manage
→ Custom Domain Names
→ Add Custom Domain
```

Example:

```text id="vqg8ij"
example.com
```

---

# Domain Verification

Microsoft must verify that you actually own the domain.

Verification is done using:

* TXT Record (most common)
* MX Record

---

# TXT Record Verification

Microsoft provides a TXT record like:

```text id="3q3gxu"
MS=ms12345678
```

You must add it to your domain’s DNS settings.

---

# DNS Registrar

The TXT record is added where the domain is managed.

Examples:

* Namecheap
* GoDaddy
* Cloudflare

---

# Verification Steps

## Step 1

Add custom domain in Entra ID.

Example:

```text id="vqg8ij"
example.com
```

---

## Step 2

Microsoft generates TXT record.

Example:

```text id="3q3gxu"
MS=ms12345678
```

---

## Step 3

Add TXT record in DNS manager.

Example:

```text id="h6a8z0"
Type: TXT
Host: @
Value: MS=ms12345678
```

---

## Step 4

Microsoft checks DNS records.

If record exists:

```text id="7kk6nn"
Domain Verified ✅
```

---

# DNS Propagation

DNS changes may take time to update globally.

This is called:

# DNS Propagation

Can take:

* Minutes
* Hours
* Sometimes 24 hours

---

# Making the Domain Primary

After verification, the custom domain can be set as:

# Primary Domain

Then new users will use:

```text id="5zq5qi"
john@example.com
```

instead of:

```text id="n4p0q7"
john@mycompany.onmicrosoft.com
```

---

# Adding Users with Custom Domain

After verification:

```text id="9z4z4d"
Users
→ New User
```

You can now create users like:

```text id="5zq5qi"
john@example.com
```

---

# Important Notes

## Domain Must Be Unique

A domain can belong to only:

```text id="khhj0i"
ONE Entra ID tenant
```

---

## You Must Own the Domain

Only domain owners can update DNS records.

---

## Why Verification Is Important

Prevents fake ownership claims.

Example:

* Someone cannot claim microsoft.com without verification.

---

# Real-World Example

## Company Domain

```text id="vqg8ij"
example.com
```

---

## Default Tenant Domain

```text id="n4p0q7"
example.onmicrosoft.com
```

---

## After Custom Domain Setup

Users can sign in as:

```text id="5zq5qi"
john@example.com
```

---

# Key Concepts

| Concept         | Meaning                             |
| --------------- | ----------------------------------- |
| Default Domain  | Automatically assigned by Microsoft |
| Custom Domain   | Organization’s real domain          |
| TXT Record      | DNS verification record             |
| DNS Propagation | Time taken for DNS updates          |
| Primary Domain  | Default sign-in domain              |

---

# Key Takeaways

✅ Entra ID assigns a default onmicrosoft.com domain
✅ Organizations can add custom domains
✅ DNS TXT records are used for verification
✅ Only domain owners can verify domains
✅ Custom domains create professional user identities
✅ A domain can belong to only one tenant
