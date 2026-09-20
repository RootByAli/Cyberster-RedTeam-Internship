# Week 04 — OWASP Top 10: Web Application Testing

## Overview
Covered OWASP Top 10 vulnerability testing against Metasploitable 2 / Mutillidae II. Burp Suite was used to intercept and manipulate HTTP traffic, with both manual and automated exploitation of common web vulnerabilities.

## Tools Used
- Burp Suite — HTTP proxy interception and manipulation
- SQLMap — automated SQL injection
- Manual testing — IDOR, XSS, LFI/RFI

## Key Findings
- SQL Injection exploited both manually and via SQLMap
- IDOR (Insecure Direct Object Reference) exploited via cookie manipulation
- Cross-Site Scripting (XSS) — both reflected and stored variants demonstrated
- Local/Remote File Inclusion (LFI/RFI) vulnerabilities tested
- Documented 20 screenshots across the session
