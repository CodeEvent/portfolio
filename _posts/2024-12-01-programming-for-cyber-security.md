---
layout: post
title: "Programming for Cyber Security - COMP08101"
tags: python security-tools
---

[View on GitHub](https://github.com/CodeEvent/Programming-for-Cyber-Security)

## Brief

COMP08101 Programming for Cyber Security at the University of the West of Scotland focused on building practical security tools in Python. The module covered offensive scripting techniques including HTTP brute force attacks and DNS enumeration, alongside defensive scripting patterns. The module was graded A2, First-class band (80-89%).

## Approach

### HTTP brute force tool

Built a Python script to perform dictionary-based brute force attacks against HTTP authentication endpoints. The tool handled session management, response code parsing, and timing controls to avoid trivial rate-limit detection. The exercise demonstrated how weak credentials are exploited in practice and why account lockout policies matter.

### DNS enumeration pipeline

Developed a DNS enumeration pipeline that automated subdomain discovery through dictionary-based queries. The pipeline resolved DNS records, filtered live hosts, and produced structured output for further analysis. This type of reconnaissance is a standard first step in penetration testing engagements.

### Defensive scripting patterns

Alongside the offensive tools, the module covered defensive scripting: input validation, safe handling of external data, error handling that avoids information leakage, and logging practices that support incident investigation without exposing sensitive data.

## Results

- Grade: A2, First-class band (80-89%)
- Working HTTP brute force and DNS enumeration tools
- Understanding of both offensive application and defensive countermeasures

## Tools

Python 3, requests, socket, dns.resolver, argparse.
