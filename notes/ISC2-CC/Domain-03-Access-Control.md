# Domain 03 – Access Control Concepts

> Certification: ISC2 Certified in Cybersecurity (CC)

---

# Identification, Authentication, Authorization and Accountability

These concepts describe how users interact with systems securely.

---

## Identification

A user claims an identity.

Question Answered:

> Who are you?

Examples:

* Username
* Employee ID
* Email Address

Example:

Username: franky

The user has claimed an identity but has not yet proven it.

---

## Authentication

Authentication verifies a claimed identity.

Question Answered:

> Can you prove who you are?

Examples:

* Password
* PIN
* Fingerprint
* Smart Card
* MFA

Enterprise Example:

A user signs into Microsoft 365 using a password and Microsoft Authenticator.

---

## Authorization

Authorization determines what an authenticated user is allowed to do.

Question Answered:

> What are you allowed to access?

Examples:

* Read-only access
* Administrator access
* Application permissions
* Folder permissions

Enterprise Example:

An Endpoint Engineer can view CrowdStrike dashboards but may not have permission to modify policies.

---

## Accountability

Accountability records and tracks user actions.

Question Answered:

> What did you do?

Examples:

* Audit Logs
* SIEM Events
* Sign-in Logs
* Security Logs

Purpose:

Provide traceability and support investigations.

---

# Authentication Factors

Authentication factors are grouped into categories.

---

## Something You Know

Examples:

* Password
* PIN
* Passphrase
* Security Question

---

## Something You Have

Examples:

* Mobile Authenticator
* Smart Card
* Hardware Token
* Security Key

---

## Something You Are

Examples:

* Fingerprint
* Face Recognition
* Iris Scan
* Retina Scan

---

## Something You Do

Examples:

* Typing Pattern
* Signature Dynamics

Less common but still valid authentication factors.

---

# Multi-Factor Authentication (MFA)

MFA requires two or more different authentication factors.

Valid Example:

* Password
* Authenticator App

Something You Know + Something You Have

---

Invalid Example:

* Password
* Security Question

Both belong to the same factor category.

This is not MFA.

---

# Least Privilege

Users should receive only the permissions required to perform their jobs.

Purpose:

Reduce risk if an account becomes compromised.

Example:

A Helpdesk Engineer can reset passwords but cannot modify firewall rules.

---

# Need-to-Know

Users should access only the information necessary for their responsibilities.

Purpose:

Protect sensitive information.

Example:

HR staff can access employee records but should not automatically access merger documentation.

---

# Difference Between Least Privilege and Need-to-Know

Least Privilege:

* Focuses on permissions
* What actions can a user perform?

Need-to-Know:

* Focuses on information
* What information should a user access?

---

# Separation of Duties

Critical tasks should be divided among multiple individuals.

Purpose:

Prevent fraud, abuse and human error.

Example:

* Employee A creates a payment request
* Employee B approves it
* Employee C releases payment

---

# Privileged Accounts

Privileged accounts have elevated permissions.

Examples:

* Domain Administrator
* Root Account
* Local Administrator
* Global Administrator

These accounts require stronger security controls and monitoring.

---

# Access Control Models

Access Control Models define how permissions are assigned and enforced.

---

## DAC (Discretionary Access Control)

The owner of the resource decides who receives access.

Examples:

* Google Drive Sharing
* Personal File Sharing

Characteristics:

* Flexible
* User-controlled

---

## MAC (Mandatory Access Control)

Access is enforced by system-defined classifications.

Examples:

* Government Systems
* Military Environments

Common Classifications:

* Confidential
* Secret
* Top Secret

Characteristics:

* Highly restrictive
* Users cannot override permissions

---

## RBAC (Role-Based Access Control)

Permissions are assigned based on job roles.

Examples:

* HR Role
* Finance Role
* Security Architect Role

Characteristics:

* Simple administration
* Common in enterprise environments

---

## ABAC (Attribute-Based Access Control)

Access decisions are based on multiple attributes.

Examples:

* User Role
* Device Compliance
* Location
* Time of Day
* Sign-in Risk

Enterprise Example:

Allow access only if:

* User belongs to Finance
* Device is compliant
* Sign-in Risk is low
* User is connecting from an approved country

Characteristics:

* Dynamic
* Highly flexible

---

# Real-World Observation

Modern organizations often combine RBAC and ABAC.

Example:

RBAC grants Finance users access to an application.

ABAC evaluates additional conditions such as:

* MFA
* Device Compliance
* Location
* Risk Score

Access is granted only when both requirements are satisfied.

---

# Common Exam Traps

Password + Security Question

* Not MFA
* Both are Something You Know

---

Fingerprint

* Authentication
* Not Identification

---

Relying only on country restrictions is weak security.

Modern Zero Trust solutions evaluate multiple signals.

---

# Revision Checklist

* [x] Identification
* [x] Authentication
* [x] Authorization
* [x] Accountability
* [x] Authentication Factors
* [x] MFA
* [x] Least Privilege
* [x] Need-to-Know
* [x] Separation of Duties
* [x] Privileged Accounts
* [x] DAC
* [x] MAC
* [x] RBAC
* [x] ABAC
