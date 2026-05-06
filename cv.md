---
layout: page
title: cv
---

[Download PDF version](assets/cv/ErmandMani_CV.pdf)

## Professional Summary
BEng (Hons) Cyber Security graduate from the University of the West of Scotland with hands‑on experience across blockchain security, digital forensics, penetration testing, network security, and secure programming. Dissertation project SmartGuard, a Slither‑based DeFi fraud detection tool, was accepted for presentation at SIGiST 2026 in London, achieving 100 % precision, recall, and F1 against a 17‑contract evaluation dataset, with findings corroborated by a professional BlockSec audit. Actively seeking roles in SOC analysis, penetration testing, DFIR, application security, or blockchain security.

## Key Achievements
- SIGiST 2026 London: Research paper accepted for presentation
- SmartGuard: 100 % precision, recall, and F1 on 17‑contract blockchain dataset
- BlockSec STRATOS‑2024‑001: 2 of 12 HIGH‑severity audit findings independently corroborated
- Operation FishNet: ACPO‑compliant digital forensic investigation producing 50+ court‑ready exhibits
- Network Security (COMP10014): Grade A2, First‑class band (80‑89 %)
- Web Application Security: 89/100 across two penetration‑testing courseworks (45/50 and 44/50)

## Education
| Degree | Institution | Years | Additional 
|--------|-------------|-------|-------------
| BEng (Hons) Cyber Security | University of the West of Scotland | 2022‑2026 | Lanarkshire Campus, supervised by Dr. Althaff Irfan Cader Mohideen, Student ID: B00249469

### Modules
| Module | Grade |
|--------|-------|
| Honours Dissertation SmartGuard | First |
| Network Security COMP10014 | A2 |
| Web Application Security COMP09109 | 89/100 |
| Secure Programming COMP10068 | A2 |
| Programming for Cyber Security COMP08101 | A2 |

## Projects
### 1. SmartGuard (2025‑2026)
- Slither plugin with 3 custom detectors for DeFi fraud (unlimited minting, token name impersonation, unprotected critical functions). 17 contracts (7 fraudulent, 10 legitimate), 100 % precision/recall/F1, 0 false positives, 25 true positives. Corroborated 2 of 12 HIGH findings from BlockSec STRATOS‑2024‑001. SIGiST 2026 accepted. Stack: Python 3.10.11, Slither 0.11.5, Solidity 0.8.0, solc‑select.

### 2. Operation FishNet (Nov‑Dec 2025)
- ACPO 2012‑compliant forensic examination of two seized devices (E01 disk images, RAW memory dumps). DarkComet RAT identified via Volatility 2.6 (pslist, malfind, netscan). MD5 hash comparison confirmed illegal images on Device 2, zero on Device 1. Email evidence from Thunderbird. 50+ numbered exhibits, full chain of custody. Tools: Autopsy 4.21.0, FTK Imager 4.7.1, Volatility 2.6, RegRipper 3.0, Registry Explorer.

### 3. OWASP Pentest Suite (2024‑2025)
- Part A (45/50): broken access control, cryptographic failures, SQL injection auth bypass, security misconfiguration on Mutillidae II via Burp Suite.
- Part B (44/50): SQLi to extract TOTP secret and bypass 2FA on Juice Shop, stored and reflected XSS with session cookie theft on Mutillidae II, CSRF via image‑tag payload on Security Shepherd, OSSEC HIDS deployment. Tools: Burp Suite Community 2025.2.4, Kali Linux, OWASP Juice Shop, Mutillidae II, Security Shepherd, OSSEC v3.7.0.

### 4. Network Security Labs COMP10014 (2025‑2026)
- ARP poisoning and MITM with Ettercap, detection with Arpwatch. Snort IDS with custom rules, iptables TEE mirroring. GRE tunnelling with Linux kernel and OpenVSwitch. OpenVPN PKI with EasyRSA (CA, cert signing, DH params, SCP transfer). FreeRADIUS 3.0 AAA (client setup, user auth, AVPs, radclient testing). Grade: A2 First‑class.

### 5. SEI CERT C++ Remediation COMP10068 (2025‑2026)
- 5 noncompliant C++17 programs fixed against SEI CERT standard without modifying protected main(). Rules: DCL50‑CPP (C‑style variadic to template), STR50‑CPP (buffer over‑read fix), MEM51‑CPP (RAII via unique_ptr), MSC51‑CPP (std::random_device seeding), ERR55‑CPP (false noexcept removal). Rust Hangman with HashSet deduplication, ownership semantics, idiomatic patterns. Grade: A2 First‑class.

### 6. Programming for Cyber Security COMP08101 (2024‑2025)
- Python security tools, HTTP brute force, DNS pipeline. Grade: A2 First‑class band.

## Work Experience
Event Security and Staff Management, OVO Hydro, Glasgow, 2022‑Present. Managed security and staff across four hub zones (South, East, West, Hydro Club). Coordinated sign‑in, role slots, real‑time deployment. Built Excel staff planning workbooks and designed spec for React/Node.js/SQLite live staff management web app.

## Technical Skills
| Offensive Security | Digital Forensics | Network Security | SIEM and Monitoring | Blockchain Security | Languages | Platforms | Secure Coding |
|--------------------|------------------|-----------------|---------------------|--------------------|-----------|-----------|--------------|
| Burp Suite, Metasploit, Nmap, Ettercap, Wireshark, SQLi, XSS, CSRF, 2FA bypass | Autopsy 4.21, Volatility 2.6, FTK Imager, RegRipper 3.0, E01 imaging, ACPO 2012 | Snort IDS, OpenVPN 2.4, FreeRADIUS 3.0, GRE tunnelling, iptables, Arpwatch, Wireshark | Wazuh, OSSEC v3.7.0, Snort custom rules, log analysis, alert correlation | Slither 0.11.5, Solidity 0.8.0, DeFi taxonomy, taint analysis, smart contract AST | Python 3.10.11, Rust, C++17, Solidity, Bash, PowerShell | Kali Linux, Tails OS, Ubuntu 20.04, VirtualBox, Docker, Git | SEI CERT C++ (DCL50 STR50 MEM51 MSC51 ERR55), RAII, memory safety, type safety |

## Additional
- GitHub: github.com/CodeEvent
- SIGiST 2026 Speaker: London
- Website: ermand.uk
- Languages spoken: English (native), Italian (native)
