# Week 07 — Active Directory Enumeration & Kerberos Attacks

## Overview
Introduced Active Directory offensive techniques. PowerView was used to enumerate domain objects, BloodHound mapped attack paths, and two classic Kerberos attacks (AS-REP Roasting and Kerberoasting) were executed to extract crackable credential hashes.

## Tools Used
- PowerView — AD enumeration (users, groups, computers, domain controllers)
- SharpHound / BloodHound — attack path collection and analysis
- Impacket (`GetNPUsers`) — AS-REP Roasting
- `Invoke-Kerberoast` — Kerberoasting

## Key Findings
- Enumerated full AD environment (users, groups, computers, DCs) using PowerView
- Collected BloodHound data via SharpHound for attack path analysis
- AS-REP Roasted the `testuser` account (configured without Kerberos pre-authentication)
- Kerberoasted `svcaccount`, extracting a crackable TGS hash
- Documented 10 screenshots across the session
