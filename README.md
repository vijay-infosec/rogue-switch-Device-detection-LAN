# rogue-switch-Device-detection-LAN
Detects rogue switches and devices in LANs using Layer 2 behaviour analysis, ARP integrity checks, STP protection, MAC control enforcement, and lightweight ML-based anomaly detection. Demonstrates ARP spoofing, STP manipulation, and MAC flooding with validated results.

**Overview**

This repository provides the implementation details, detection logic, and supporting materials for identifying rogue switches and rogue devices in wired LAN environments. The project evaluates Layer 2 attacks and presents practical mitigation using standard switch security features and anomaly-based analysis. Full technical depth is available in the published paper.

Contents
paper/              → Published ECCWS 2025 paper, citation files
implementation/     → Detection rules, attack scenarios, config notes
results/            → Logs, switch outputs, packet captures, ML metrics

**Focus Areas**

Rogue switch insertion detection

ARP spoofing prevention (DAI)

STP root manipulation containment (Root Guard)

MAC flooding control (Port Security, Sticky MAC)

ML-based anomaly scoring for Layer 2 deviations

**Tools & Environment**

GNS3 (Cisco IOS switches)

Wireshark

Ettercap / Macof

Windows & Kali Linux hosts

Python (data processing & ML)

**Publication**

Published in ECCWS 2025
DOI: https://doi.org/10.34190/eccws.24.1.3705
