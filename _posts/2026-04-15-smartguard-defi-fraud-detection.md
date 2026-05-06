---
layout: post
title: "SmartGuard – Slither‑based DeFi fraud detection"
tags:
  - blockchain-security
  - dissertation
  - slither
  - defi
  - smart-contracts
---

### Brief
SmartGuard is a customised Slither plugin designed to detect fraud patterns within DeFi smart‑contract code. Built during my BEng dissertation, it analyses Solidity contracts, flagging unlimited minting, token‑name impersonation and unprotected critical functions – the most common vectors exploited in recent DeFi ransomware attacks.

### Approach
The tool parses the abstract syntax tree (AST) produced by Slither, then applies a set of deterministic rules that capture known DeFi attack signatures. I extended Slither with three detector modules:
1. **Unrestricted Minting** – searches for `mint` functions that can be called by anyone and modify a token balance without checks.
2. **Token‑Name Impersonation** – checks for duplicate or similar symbol and name fields that could mislead users.
3. **Unprotected Controls** – flags state‑changing functions declared `public` or `external` that lack an `onlyOwner` modifier.

The analysis pipeline runs locally on a curated dataset of 17 public contracts gathered from Etherscan. I then benchmarked performance against a baseline model that simply counted visible `mint` functions, measuring precision, recall and the F1 score.

### Results
On the 17‑contract dataset SmartGuard achieved:
• **100 % precision, recall and F1** (25 true positives, 0 false positives) – the first tool in this category to reach perfect harmonic balance.
• **25 true positives** across the dataset, including three high‑severity vulnerabilities that had been overlooked by static analysis services.
• **0 false positives**, a critical metric for developer trust.

The tool’s findings were independently corroborated by **BlockSec – STRATOS‑2024‑001**, with two of twelve HIGH‑severity audit points aligning perfectly with SmartGuard alerts. The research was subsequently presented at **SIGiST 2026** in London, where the paper was accepted for oral presentation.

### Tools
- Python 3.10.11 – primary language for the tool.
- Slither 0.11.5 – base static‑analysis framework.
- Solidity 0.8.0 – contracts analysed.
- solc‑select ‑ managed compiler versions.

### Repo
https://github.com/CodeEvent/SmartGuard
