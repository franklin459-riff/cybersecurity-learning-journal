# Domain 01 – Security Principles

> **Certification:** ISC2 Certified in Cybersecurity (CC)

---

# Learning Objectives

This document covers the core security principles required for ISC2 CC Domain 1. The focus is not only on passing the exam but also on understanding how these concepts are applied in enterprise environments.

---

# CIA Triad

The CIA Triad is the foundation of Information Security.

## Confidentiality

Ensures that information is accessible only to authorized individuals.

### Examples

* Encryption
* Multi-Factor Authentication (MFA)
* File Permissions
* Access Control Lists (ACLs)

### Enterprise Example

Only the Endpoint Security team can modify CrowdStrike policies.

---

## Integrity

Ensures information cannot be modified without authorization.

### Examples

* Hashing
* Digital Signatures
* Checksums

### Enterprise Example

If malware modifies a Windows system file, Integrity has been compromised.

---

## Availability

Ensures systems and data remain accessible when required.

### Examples

* Backups
* RAID
* Load Balancers
* UPS
* High Availability Clusters

### Enterprise Example

If the CrowdStrike console becomes unavailable during an incident, Availability has been impacted.

---

# Threat, Vulnerability and Risk

These three concepts work together.

## Threat

Anything capable of causing harm.

Examples:

* Hackers
* Malware
* Insider Threats
* Fire
* Flood

---

## Vulnerability

A weakness that can be exploited.

Examples:

* Weak Password
* Missing Patch
* Open RDP Port
* Misconfigured Firewall

---

## Risk

The likelihood that a threat successfully exploits a vulnerability.

Simple formula:

Threat + Vulnerability = Risk

### Example

Threat:
Attacker

Vulnerability:
Unpatched VPN

Risk:
Unauthorized access to the corporate network.

---

# Security Governance

Governance defines how security is managed across an organization.

It includes:

* Policies
* Standards
* Procedures
* Roles & Responsibilities
* Compliance

Important takeaway:

> Governance defines the direction. Security teams implement it.

---

# Security Controls

Security controls reduce risk.

## Administrative Controls

Examples:

* Policies
* Security Awareness Training
* Background Verification

---

## Technical Controls

Examples:

* Firewalls
* MFA
* CrowdStrike
* Encryption
* EDR

---

## Physical Controls

Examples:

* CCTV
* Security Guards
* Smart Card Access
* Biometric Doors

---

# Due Care vs Due Diligence

## Due Care

Taking reasonable security measures.

Example:

Deploying CrowdStrike across the enterprise.

---

## Due Diligence

Continuously verifying those controls remain effective.

Example:

Monitoring sensor health every week and remediating non-compliant devices.

---

# Data Classification

Information should be classified according to business impact.

Typical classifications:

* Public
* Internal
* Confidential
* Restricted

Higher classifications require stronger security controls.

---

# Least Privilege

Users should receive only the permissions required to perform their job.

This minimizes the impact of compromised accounts.

---

# Need to Know

Users should access only the information necessary for their responsibilities.

Difference:

* Least Privilege → What actions can a user perform?
* Need to Know → What information can a user access?

---

# Separation of Duties

Critical business functions should be divided between multiple individuals.

Example:

* Employee A creates a payment request.
* Employee B approves it.
* Employee C releases the payment.

Purpose:

Reduce fraud and human error.

---

# Defense in Depth

No single security control should be trusted completely.

Multiple layers should work together.

Example:

* BitLocker
* Windows Password
* MFA
* EDR
* Firewall
* VPN

---

# Zero Trust

Core Principle:

> Never Trust. Always Verify.

Every access request should be evaluated continuously using multiple signals.

Examples of signals:

* Identity
* MFA
* Device Compliance
* Sign-in Risk
* Device Registration
* Location
* IP Reputation

---

# Authentication, Authorization and Accounting (AAA)

## Authentication

Verifies identity.

Examples:

* Password
* Fingerprint
* Smart Card
* MFA

Question answered:

Who are you?

---

## Authorization

Determines what a user is allowed to access.

Question answered:

What are you allowed to do?

---

## Accounting

Records user activity.

Examples:

* Event Logs
* SIEM
* Audit Logs
* Azure Sign-in Logs

Question answered:

What did you do?

---

# Authentication Factors

## Something You Know

* Password
* PIN

## Something You Have

* Smart Card
* Hardware Token
* Mobile Phone

## Something You Are

* Fingerprint
* Face Recognition
* Iris Scan

---

# Access Control Models

## DAC (Discretionary Access Control)

The resource owner decides who receives access.

Example:

Google Drive sharing.

---

## MAC (Mandatory Access Control)

Access is determined by system-enforced classifications.

Commonly used in Government and Military environments.

---

## RBAC (Role-Based Access Control)

Permissions are assigned to job roles rather than individuals.

Example:

Security Architect role automatically receives predefined permissions.

---

## ABAC (Attribute-Based Access Control)

Access decisions are made using multiple attributes.

Examples:

* User Role
* Device Compliance
* Location
* Time
* Sign-in Risk

---

# Important Realization

One of the biggest lessons learned today:

> Technology does not define security.

> Security Policy defines security.

Technology simply enforces those policies.

This explains why two organizations using Microsoft Entra can have completely different access experiences.

---

# Personal Notes

Key observations from today's discussion:

* RBAC and ABAC complement each other rather than replace one another.
* Country restrictions alone are not sufficient because VPNs can change the apparent source IP.
* Modern Zero Trust solutions evaluate multiple signals instead of relying on a single condition.
* Every security control has limitations. Security improves by combining multiple independent controls (Defense in Depth).

---

# Common Interview Questions

* Explain the CIA Triad with real-world examples.
* What is the difference between Risk, Threat and Vulnerability?
* Explain Due Care and Due Diligence.
* Difference between Least Privilege and Need to Know.
* Explain Defense in Depth.
* What is Zero Trust?
* Explain AAA.
* Compare DAC, MAC, RBAC and ABAC.

---

# Revision Checklist

* [x] CIA Triad
* [x] Threat, Vulnerability and Risk
* [x] Governance
* [x] Security Controls
* [x] Due Care vs Due Diligence
* [x] Data Classification
* [x] Least Privilege
* [x] Need to Know
* [x] Separation of Duties
* [x] Defense in Depth
* [x] Zero Trust
* [x] Authentication, Authorization and Accounting
* [x] Authentication Factors
* [x] Access Control Models

# Questions I Asked During This Session

1. If all ABAC attributes pass except one (for example, location), can access still be denied?
   - Yes. The Security Architect defines the policy. Technology enforces it.

2. If I connect to an Indian VPN before signing in, can I bypass location restrictions?
   - Sometimes. It depends on the organization's Conditional Access policies and what other signals Microsoft Entra evaluates.

3. Isn't relying on location alone a security gap?
   - Yes. This is why Zero Trust uses multiple signals such as MFA, device compliance, sign-in risk and identity.