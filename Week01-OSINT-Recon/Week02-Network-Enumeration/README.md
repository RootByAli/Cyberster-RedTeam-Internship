# Week 02 — Network Enumeration & Vulnerability Assessment

## Overview
Covered active network enumeration and vulnerability assessment against Metasploitable 2 (192.168.56.101). Nmap was used extensively for port scanning, service version detection, and OS fingerprinting, alongside manual service probing.

## Tools Used
- Nmap — port scanning, service/version detection, OS fingerprinting
- Nikto — web vulnerability scanning
- netstat — local port/service enumeration
- ARP & IP neighbor tables — network topology mapping

## Key Findings
- Metasploitable 2 runs vsftpd 2.3.4 (backdoored), IRC UnrealIRCd, Samba 3.x, MySQL, PostgreSQL, Tomcat
- SSH configured with legacy RSA/DSA host keys
- netstat enumeration revealed 30+ open TCP/UDP listeners
- Full lab network topology mapped via ARP cache and neighbor discovery
- Documented 35 screenshots across the session
