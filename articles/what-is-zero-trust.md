# What is Zero Trust?

## Introduction

Traditional security models assumed that users and devices inside the corporate network could be trusted. Once authenticated, users often received broad access to systems and data.

Modern organizations have moved away from this approach.

Zero Trust is a security model based on a simple principle:

> Never Trust. Always Verify.

Every access request should be continuously evaluated, regardless of whether it originates from inside or outside the network.

---

## Why Zero Trust Exists

Modern organizations face several challenges:

* Remote work
* Cloud applications
* Personal devices
* Insider threats
* Credential theft
* Sophisticated phishing attacks

A user connecting from the corporate network is not automatically trustworthy.

Attackers frequently gain access using legitimate credentials, making identity-based security more important than network location.

---

## Core Principles of Zero Trust

### Verify Explicitly

Every access request should be validated using multiple signals.

Examples:

* User identity
* Multi-Factor Authentication (MFA)
* Device compliance
* Location
* Sign-in risk
* Application sensitivity

---

### Use Least Privilege

Users should receive only the permissions necessary to perform their job.

Benefits:

* Reduces attack surface
* Limits damage from compromised accounts
* Prevents unnecessary access

---

### Assume Breach

Organizations should operate under the assumption that attackers may already be present within the environment.

Security controls should focus on:

* Detection
* Containment
* Monitoring
* Rapid response

---

## Common Zero Trust Signals

Modern access decisions may evaluate:

| Signal              | Example                    |
| ------------------- | -------------------------- |
| Identity            | Valid user account         |
| MFA                 | Authenticator approval     |
| Device Compliance   | Managed and patched device |
| Location            | Approved country           |
| Risk Score          | Low sign-in risk           |
| Device Registration | Corporate-owned device     |

Access may be denied if any required condition is not met.

---

## Real-World Example

Consider a Finance employee attempting to access Microsoft 365.

Access is granted only when:

* User belongs to Finance
* MFA is successful
* Device is compliant
* Sign-in risk is low
* Connection originates from an approved location

If one condition fails, access can be blocked.

This demonstrates how Zero Trust evaluates multiple security signals before making an access decision.

---

## Zero Trust and Conditional Access

Microsoft Entra Conditional Access is a common implementation of Zero Trust principles.

Conditional Access policies can evaluate:

* User groups
* Device compliance
* Location
* Risk levels
* Authentication strength

This allows organizations to enforce dynamic security decisions instead of relying on static rules.

---

## Benefits of Zero Trust

* Improved security posture
* Reduced impact of compromised credentials
* Better visibility into access requests
* Stronger protection for cloud applications
* Reduced insider threat risk

---

## Challenges

* Initial implementation complexity
* Increased planning requirements
* Legacy application limitations
* User adoption considerations

Despite these challenges, Zero Trust has become a foundational security model for modern enterprises.

---

## Key Takeaways

* Zero Trust does not automatically trust users or devices.
* Every access request must be verified.
* Multiple signals are evaluated before granting access.
* Least Privilege and Assume Breach are core principles.
* Modern platforms such as Microsoft Entra help organizations implement Zero Trust controls.

Zero Trust is not a single product. It is a security strategy that combines identity, device, application, and risk-based controls to make access decisions.
