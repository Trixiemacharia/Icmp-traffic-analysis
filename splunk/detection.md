# ICMP Detection & Investigation

This document contains the detection and investigation techniques used during the ICMP traffic analysis lab.

## Lab Environment

| Component | Details |
|---|---|
| Main Kali Linux | `192.168.*.*` |
| Kali Linux VM | `192.168.*.*` |
| Packet Capture | tcpdump |
| Packet Analysis | Wireshark |
| Firewall | UFW |
| SIEM | Splunk |
| Splunk Receiver | `192.168.*.*:9997` |
| UFW Log | `/var/log/ufw.log` |

---

## 1. Detection Objective

The objective is to identify potentially suspicious ICMP activity that may indicate:

- Host discovery
- ICMP reconnaissance
- Excessive ICMP activity
- Unusual communication patterns
- Potentially unreachable or misconfigured hosts

ICMP is commonly used for legitimate network troubleshooting, so the presence of ICMP traffic alone is **not considered malicious**.

The investigation therefore focuses on the behavior and pattern of the traffic.

---

# 2. Wireshark-Based Detection

Before using Splunk, the PCAP files are analyzed in Wireshark.

### All ICMP Traffic

```text
icmp