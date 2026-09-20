# Week 12 — Final Capstone: Boardroom Report

## Overview
The final week compiled all 11 weeks of lab work into a single, professional Capstone Red Team Engagement Report — structured as a real-world client deliverable, including a pre-engagement scope document, weekly evidence, a full Cyber Kill Chain walkthrough, post-engagement cleanup steps, and a boardroom-style executive summary.

## Engagement Objectives (Flags) — All 8 Achieved
| Flag | Objective | Status |
|---|---|---|
| FLAG-01 | Gain initial SYSTEM-level access to Windows 7 target | ✅ |
| FLAG-02 | Achieve remote code execution via a known CVE | ✅ |
| FLAG-03 | Dump and crack at least one password hash | ✅ |
| FLAG-04 | Escalate privileges to local administrator/SYSTEM | ✅ |
| FLAG-05 | Enumerate Active Directory and identify Domain Admins | ✅ |
| FLAG-06 | Achieve full Domain Administrator compromise | ✅ |
| FLAG-07 | Establish persistence on a compromised host | ✅ |
| FLAG-08 | Deploy simulated phishing infrastructure | ✅ |

## Key Findings by Severity
| Severity | Count | Examples |
|---|---|---|
| CRITICAL | 3 | MS17-010 RCE, DCSync, Golden Ticket forgery |
| HIGH | 8 | Kerberoasting, AS-REP Roasting, ACL misconfig, LLMNR poisoning, AMSI bypass, C2 implant, hash dumping, Pass-the-Hash |
| MEDIUM | 3 | WMI persistence, security log tampering, phishing infrastructure |

## MITRE ATT&CK Coverage
Techniques mapped across all major tactics: Reconnaissance, Initial Access, Execution, Persistence, Privilege Escalation, Defense Evasion, Credential Access, Discovery, Lateral Movement, Command & Control, and Impact.

## Top Recommendations Delivered
- **Critical:** Patch MS17-010 immediately; disable SMBv1 domain-wide
- **Critical:** Rotate the krbtgt password twice to invalidate forged Golden Tickets
- **High:** Enforce strong service account passwords; audit unnecessary SPNs
- **High:** Tighten AD ACLs; remove GenericAll/WriteDACL from non-Tier-0 accounts
- **High:** Disable LLMNR/NBT-NS via Group Policy; enforce SMB signing
- **Medium:** Centralize logging to a SIEM; roll out phishing-resistant MFA (FIDO2)

## Full Report
The complete 87-page Capstone Red Team Engagement Report — including the pre-engagement scope, all weekly evidence, the full kill chain execution, post-engagement cleanup checklist, and the boardroom executive summary — is available in [`Capstone-Report/`](../Capstone-Report).
