# Week 10 — Phishing Infrastructure (GoPhish) & Social Engineering

## Overview
Covered offensive phishing infrastructure deployment and social engineering payload creation. Built a cloned Microsoft 365 login page with GoPhish and explored multiple alternate payload delivery mechanisms for social engineering campaigns.

## Tools Used
- GoPhish — phishing campaign platform (email templates, landing pages, SMTP profiles)
- `msfvenom` — VBA macro payload generation
- HTML Smuggling — base64-encoded payload delivery via JavaScript Blob
- WMI MOF persistence — `mofcomp`

## Key Findings
- Deployed GoPhish with a spoofed "M365 Security Alert" email template
- Cloned a Microsoft 365 login page as a phishing landing page via GoPhish site import
- Configured an SMTP sending profile for simulated campaign delivery
- Prepared malicious LNK file concept (PowerShell IEX download cradle)
- Built a VBA macro payload and an HTML smuggling payload for delivery testing
- Documented WMI persistence via MOF file compiled with `mofcomp`
- Researched SPF/DKIM/DMARC concepts relevant to domain spoofing and typosquatting
- Documented 18 screenshots across the session
