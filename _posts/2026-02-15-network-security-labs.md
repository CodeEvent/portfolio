---
layout: post
title: "Network Security Labs - COMP10014"
tags: network-security ids vpn radius
---

[View on GitHub](https://github.com/CodeEvent/Network-Security)

## Brief

COMP10014 Network Security at the University of the West of Scotland covered five core areas of network defence through hands-on lab exercises. Each lab built on the previous one, progressing from attack techniques through detection, tunnelling, encryption, and authentication. The module was graded A2, First-class band (80-89%).

## Approach

### ARP poisoning and MITM

Using Ettercap to execute ARP poisoning against a target on the local network segment, intercepting HTTP traffic via tcpdump. Detection was handled by Arpwatch, which generated flip-flop alerts when MAC-to-IP bindings changed unexpectedly.

### Snort IDS deployment

Deployed Snort with custom rule sets to detect specific attack signatures. Configured traffic mirroring via iptables TEE to redirect copies of live traffic to the Snort sensor, transitioning the deployment from a host-based IDS to a network-based IDS.

### GRE tunnelling

Configured Generic Routing Encapsulation tunnels using the Linux kernel and OpenVSwitch. Analysed Layer 2 and Layer 3 encapsulation behaviour in Wireshark.

### OpenVPN PKI

Deployed a full OpenVPN Public Key Infrastructure using EasyRSA. This included Certificate Authority creation, server and client certificate signing, Diffie-Hellman parameter generation, and secure credential transfer via SCP.

### FreeRADIUS AAA

Configured FreeRADIUS 3.0 as an Authentication, Authorisation, and Accounting server. Set up client devices, user authentication entries, Attribute Value Pairs for access policies, and validated the configuration using radclient test queries.

## Results

- Grade: A2, First-class band (80-89%)
- Five distinct lab areas completed with full documentation

## Tools

Ettercap, tcpdump, Arpwatch, Snort IDS, iptables, OpenVSwitch, Wireshark, OpenVPN 2.4, EasyRSA, FreeRADIUS 3.0.
