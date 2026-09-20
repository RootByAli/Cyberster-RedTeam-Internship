# Week 09 — Payload Delivery, Evasion & C2 Frameworks

## Overview
Focused on payload creation, antivirus/AMSI evasion, and Command & Control (C2) framework deployment. Generated encoded Meterpreter payloads, bypassed AMSI to run offensive PowerShell tooling, and deployed a full C2 framework with multiple listener types.

## Tools Used
- `msfvenom` / `msfpc` — staged payload generation (EXE, DLL, VBA macro)
- AMSI bypass (.NET reflection) — enable unrestricted PowerShell tooling
- Sliver C2 — HTTP and mTLS listeners
- `regsvr32` (Squiblydoo) — SCT scriptlet payload delivery
- `certutil` — payload delivery via LOLBin

## Key Findings
- Generated staged Meterpreter reverse TCP payloads with `msfvenom`
- Applied XOR encoding (`x64/xor_dynamic`, 5 iterations) to evade signature-based detection
- Bypassed AMSI via .NET reflection, enabling `Invoke-Mimikatz` execution
- Deployed Sliver C2 with HTTP (port 80) and mTLS (port 8443/8888) listeners
- Delivered payloads via `certutil` LOLBin and Squiblydoo SCT scriptlet technique
- Documented 12 screenshots across the session
