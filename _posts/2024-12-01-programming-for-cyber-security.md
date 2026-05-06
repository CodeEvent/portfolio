---
layout: post
title: "Programming for Cyber Security - COMP08101"
tags: python security-tools
---

[View on GitHub](https://github.com/CodeEvent/Programming-for-Cyber-Security)

## Brief

COMP08101 Programming for Cyber Security at the University of the West of Scotland focused on building practical security tools in Python. The module was graded A2, First-class band (80-89%).

## Approach

### HTTP brute force tool

Built a Python script to perform dictionary-based brute force attacks against HTTP authentication endpoints. The tool handled session management, response code parsing, and timing controls.

### DNS enumeration pipeline

Developed a DNS enumeration pipeline that automated subdomain discovery through dictionary-based queries. The pipeline resolved DNS records, filtered live hosts, and produced structured output for further analysis.

### Defensive scripting patterns

Covered input validation, safe handling of external data, error handling that avoids information leakage, and logging practices that support incident investigation.

## Results

- Grade: A2, First-class band (80-89%)
- Working HTTP brute force and DNS enumeration tools

## Tools

Python 3, requests, socket, dns.resolver, argparse.
