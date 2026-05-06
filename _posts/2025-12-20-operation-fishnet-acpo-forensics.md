---
layout: post
title: "Operation FishNet – ACPO digital forensic investigation"
tags:
  - dfir
  - forensics
  - volatility
  - acpo
---

### Brief
Operation FishNet was a live‑forensic dig during the final semester of my degree. Two Windows machines seized in a cyber‑crime investigation needed a chain‑of‑custody compliant analysis that produced court‑ready evidence for an ACPO‑compliant report. My role was to extract, analyse and document every artifact while preserving evidence integrity.

### Approach
The investigation workflow followed the ACPO‑2012 chain of custody checklist:
1. **Acquisition** – used FTK Imager 4.7.1 to capture both the physical E01 disk images and the live‑memory dumps (RAW).
2. **Hash verification** – calculated MD5 and SHA256 for each artefact, logged in a secure audit trail.
3. **Analysis** – employed Volatility 2.6 to enumerate processes (`pslist`), locate hidden malware (`malfind`), and network sockets (`netscan`). The DarkComet RAT was identified through its characteristic PID‑58 service and a distinct registry hive modification.
4. **Evidence tabulation** – each discoverable artefact was numbered, the provenance recorded in a PDF filing system, and duplicated onto secure storage.
5. **Reporting** – drafted the ACPO‑compliant report, aligning findings with the standard’s six pillars: chain of custody, provenance, authenticity, integrity and admissibility.

### Results
The operation produced **50+** audit‑ready exhibits, including:
- **DarkComet RAT** – confirmed via hash and binary memory snapshot.
- **Email evidence** – verified through Thunderbird logs, matched to suspect communication.
- **MD5 evidence** – disallowed (genuine images) on Device 2 and recognised as legitimate on Device 1.

All findings were cross‑validated by the proprietary hyper‑visor forensic toolkit and presented in a court‑tolerant PDF suitable for the prosecutor’s office. The investigation itself was highlighted in the department’s annual best‑practice showcase.

### Tools
- Autopsy 4.21.0 – forensic case management.
- FTK Imager 4.7.1 – evidence acquisition.
- Volatility 2.6 – memory live‑analysis.
- RegRipper 3.0 – registry history extraction.
- Registry Explorer – quick visualisation of suspect keys.

### Repo
https://github.com/CodeEvent/Operation‑FishNet
