# Cyberster Red Team Internship — Batch 02

## Overview
This repository documents a 12-week, hands-on Red Team internship completed at **Cyberster** (June – September 2026), under the mentorship of **Umar Niaz**. The engagement simulated a full offensive security assessment against a self-built home-lab Active Directory environment — progressing from passive reconnaissance to complete domain compromise.

All activity was performed in an isolated, authorized VirtualBox lab for educational purposes only. No real-world or production systems were targeted at any point.

## Lab Environment
| Host | Role |
|---|---|
| DC01 (Windows Server 2022) | Domain Controller |
| Windows 7 Workstation | Domain-joined target |
| Metasploitable 2 | Intentionally vulnerable Linux host |
| Kali Linux | Attacker platform |

Network: `192.168.56.0/24` (VirtualBox Host-Only)

## Weekly Breakdown

| Week | Focus |
|---|---|
| 01 | Passive OSINT & Subdomain Enumeration |
| 02 | Network Enumeration & Vulnerability Assessment |
| 03 | Endpoint Enumeration, CVE Exploitation & Web Auditing |
| 04 | OWASP Top 10 — Web Application Testing |
| 05 | Linux/Windows Privilege Escalation & Persistence |
| 06 | Post-Exploitation — Pivoting, Credential Dumping, Lateral Movement |
| 07 | Active Directory Enumeration & Kerberos Attacks |
| 08 | AD Domain Dominance & Advanced Persistence |
| 09 | Payload Delivery, Evasion & C2 Frameworks |
| 10 | Phishing Infrastructure (GoPhish) & Social Engineering |
| 11 | Domain Compromise & Golden Ticket Attack |
| 12 | Final Capstone — Boardroom Report |

Each week's folder contains a short write-up, the tools/techniques used, and supporting screenshots.

## Engagement Outcome
All 8 engagement objectives were achieved, including:
- Initial access via **MS17-010 (EternalBlue)**
- Full **domain compromise** via DCSync and a forged **Golden Ticket**
- Credential capture via **LLMNR/NBT-NS poisoning** and **Kerberoasting/AS-REP Roasting**
- **C2 deployment** (Sliver) with AMSI bypass and payload evasion
- Simulated **phishing infrastructure** via GoPhish

Findings were rated by severity (3 Critical, 8 High, 3 Medium) and mapped to the **MITRE ATT&CK** framework, with a full remediation plan delivered in the capstone report.

## Tools & Techniques Used
`Nmap` `Burp Suite` `SQLMap` `Metasploit` `Impacket` `PowerView` `BloodHound/SharpHound` `Mimikatz` `Responder` `Hashcat` `John the Ripper` `Sliver C2` `GoPhish` `msfvenom` `Subfinder/Amass` `FFUF/Gobuster` `WPScan`

## Full Report
The complete Capstone Red Team Engagement Report (86 pages — pre-engagement scope, weekly evidence, kill chain mapping, and boardroom-style executive summary) is available here: [`Capstone-Report/`](./Capstone-Report)

## About Me
Cybersecurity student and aspiring penetration tester, currently working toward Security+ → eJPT → OSCP.
GitHub: [RootByAli](https://github.com/RootByAli)
