# Week 05 — Linux/Windows Privilege Escalation & Persistence

## Overview
Covered privilege escalation techniques on both Linux (Metasploitable 2) and Windows 7. Explored SUID/SGID binaries, writable cron jobs, token impersonation, and registry-based persistence, along with post-exploitation data collection.

## Tools Used
- Linux enumeration — SUID/SGID binaries, writable cron jobs
- Meterpreter — `getsystem` for Windows token impersonation
- Windows Event Log analysis (Event IDs 4624, 4672, 4688)

## Key Findings
- Achieved Linux privilege escalation via SUID binaries and writable cron jobs
- Windows privilege escalation via Meterpreter token impersonation
- Established registry-based persistence (Run keys, services)
- Simulated post-exploitation data collection and exfiltration
- Documented 22 screenshots across the session
