# Week 11 — Domain Compromise & Golden Ticket Attack

## Overview
Represented the culmination of the full domain attack chain. Re-exploited EternalBlue for SYSTEM access, extracted domain-wide credentials, and used a forged Golden Ticket to authenticate as Domain Administrator.

## Tools Used
- Metasploit (`ms17_010_eternalblue`) — SYSTEM-level exploitation
- Meterpreter (`hashdump`) — local NTLM hash extraction
- Impacket (`psexec`, `wmiexec`, `secretsdump`, `lookupsid`, `ticketer`) — lateral movement, credential extraction, and ticket forgery
- Kerberos (`KRB5CCNAME`) — ticket-based authentication

## Key Findings
- Re-exploited MS17-010 (EternalBlue) to obtain a SYSTEM Meterpreter session on the Windows 7 workstation
- Extracted local NTLM hashes for Administrator, ali, Guest, and HomeGroupUser via `hashdump`
- Performed Pass-the-Hash lateral movement using `impacket-psexec`
- Extracted the full domain credential database (NTDS.dit) via `impacket-secretsdump`
- Enumerated all domain SIDs using `impacket-lookupsid`
- Forged a Golden Ticket with the krbtgt hash via `impacket-ticketer`, authenticating as Domain Administrator
- Documented 12 screenshots across the session
