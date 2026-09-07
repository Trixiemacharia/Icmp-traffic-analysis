# ICMP Traffic Analysis

A hands-on SOC/Blue Team lab focused on analyzing ICMP traffic using Kali Linux, tcpdump, Wireshark, UFW and Splunk.

## Objective

The objective of this lab is to understand ICMP packet structure, analyze normal ICMP communication, identify different ICMP message types, and investigate potential ICMP-based reconnaissance.

## Lab Environment

- Main Kali Linux — `192.168.*.*`
- Kali Linux VM — `192.168.*.*`
- Packet Capture — tcpdump
- Packet Analysis — Wireshark
- Firewall — UFW
- SIEM — Splunk

## ICMP Concepts

Important ICMP message types investigated:

| Type | Description |
|------|-------------|
| 0 | Echo Reply |
| 3 | Destination Unreachable |
| 8 | Echo Request |
| 11 | Time Exceeded |

### Wireshark Filters

```text
icmp.type == 8
icmp.type == 0
icmp.type == 3