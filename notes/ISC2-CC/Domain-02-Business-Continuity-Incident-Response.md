# Domain 02 – Business Continuity, Disaster Recovery and Incident Response

> Certification: ISC2 Certified in Cybersecurity (CC)

---

# Business Continuity (BC)

Business Continuity focuses on maintaining critical business operations during a disruption.

Goal:

> Keep the business running.

Examples:

* Alternate work locations
* Manual business processes
* Redundant systems
* Alternate communication channels

Enterprise Example:

If Microsoft Entra becomes unavailable, critical business operations should continue through predefined contingency processes.

---

# Disaster Recovery (DR)

Disaster Recovery focuses on restoring IT systems and infrastructure after a disruption.

Goal:

> Restore technology services.

Examples:

* Restoring servers
* Recovering databases
* Restoring applications from backups
* Rebuilding infrastructure

Enterprise Example:

Recovering a failed Active Directory server from backup.

---

# Business Continuity vs Disaster Recovery

Business Continuity:

* Focuses on business operations
* Concerned with keeping the organization functioning

Disaster Recovery:

* Focuses on technology recovery
* Concerned with restoring systems and services

---

# Business Impact Analysis (BIA)

A Business Impact Analysis identifies:

* Critical business functions
* Potential impacts of disruption
* Recovery priorities
* Recovery objectives

Purpose:

Determine what must be restored first.

---

# Recovery Time Objective (RTO)

Defines the maximum acceptable downtime.

Question Answered:

> How long can the service remain unavailable?

Example:

RTO = 2 hours

The service must be restored within 2 hours.

---

# Recovery Point Objective (RPO)

Defines the maximum acceptable data loss.

Question Answered:

> How much data can be lost?

Example:

Backups occur every 4 hours.

Maximum possible data loss = 4 hours.

RPO = 4 hours.

---

# Backup Types

## Full Backup

Backs up all selected data.

Advantages:

* Fast recovery
* Simple restoration

Disadvantages:

* Requires more storage
* Longer backup duration

---

## Incremental Backup

Backs up changes since the last backup.

Advantages:

* Smallest storage requirement
* Fast backup process

Disadvantages:

* More complex restoration

---

## Differential Backup

Backs up changes since the last full backup.

Advantages:

* Faster restoration than incremental

Disadvantages:

* Consumes more storage than incremental

---

# Alternate Recovery Sites

## Cold Site

* Empty facility
* Minimal equipment
* Lowest cost
* Longest recovery time

---

## Warm Site

* Partial infrastructure available
* Some restoration required
* Moderate cost

---

## Hot Site

* Fully operational duplicate environment
* Fastest recovery
* Highest cost

---

# Redundancy

Redundancy eliminates single points of failure.

Examples:

* Dual ISPs
* Multiple Firewalls
* Multiple Domain Controllers
* RAID Storage

Purpose:

Improve availability and resilience.

---

# Incident Response Lifecycle

1. Preparation
2. Detection and Analysis
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

---

## Preparation

Activities performed before incidents occur.

Examples:

* Security awareness training
* Incident response procedures
* Monitoring tools
* Playbooks

---

## Detection and Analysis

Identify and investigate suspicious activity.

Examples:

* EDR alerts
* SIEM alerts
* Log analysis

---

## Containment

Limit the spread of the incident.

Examples:

* Isolate compromised endpoint
* Disable compromised account
* Block malicious IP address

---

## Eradication

Remove the root cause.

Examples:

* Remove malware
* Patch vulnerabilities
* Remove malicious accounts

---

## Recovery

Restore normal operations.

Examples:

* Reconnect isolated systems
* Restore services
* Monitor for recurrence

---

## Lessons Learned

Review the incident and improve processes.

Questions:

* What worked well?
* What failed?
* What should be improved?

---

# Key Exam Distinctions

RTO = Downtime

RPO = Data Loss

Containment = Stop the spread

Eradication = Remove the cause

Recovery = Restore operations

Lessons Learned = Improve for next time

---

# Personal Notes

Key lessons from today's session:

* RPO relates to acceptable data loss, not downtime.
* Incremental backups generally use the least storage.
* Hot sites provide the fastest recovery but are the most expensive.
* Most Incident Response questions can be solved by identifying the current phase of the lifecycle.

---

# Revision Checklist

* [x] Business Continuity
* [x] Disaster Recovery
* [x] Business Impact Analysis
* [x] RTO
* [x] RPO
* [x] Backup Types
* [x] Hot / Warm / Cold Sites
* [x] Redundancy
* [x] Incident Response Lifecycle
