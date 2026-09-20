# Week 08 — AD Domain Dominance & Advanced Persistence

## Overview
Represented full domain compromise. Captured NTLMv2 hashes via network poisoning, cracked them, abused AD ACL misconfigurations to escalate rights, and forged a Golden Ticket using the krbtgt hash.

## Tools Used
- Responder — LLMNR/NBT-NS/mDNS poisoning
- Metasploit (`server/capture/smb`) — NTLMv2 hash capture
- Hashcat (mode 5600) — NetNTLMv2 cracking
- `Get-ObjectAcl` / `Add-DomainObjectAcl` — ACL enumeration & abuse
- Impacket (`secretsdump`, `lookupsid`, `ticketer`) — credential extraction & Golden Ticket forgery
- Mimikatz — DCSync attempt

## Key Findings
- Captured NTLMv2 hashes via Responder (LLMNR/NBT-NS poisoning) on eth0
- Cracked captured hashes using Hashcat mode 5600 with rockyou.txt
- Discovered GenericAll ACL misconfiguration on `svcaccount` and `testuser`
- Escalated to DCSync rights via `Add-DomainObjectAcl`
- Extracted the full NTDS.dit domain credential database via `impacket-secretsdump`
- Forged a Golden Ticket using the krbtgt NTLM hash via `impacket-ticketer`
- Documented 13 screenshots across the session
