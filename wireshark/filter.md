# Wireshark ICMP Display Filters

This document contains the Wireshark display filters used during the ICMP traffic analysis lab.

## 1. Display All ICMP Traffic

```text
icmp.type == 8
icmp.type == 0
icmp.type == 3
ip.addr == 192.168.*.* && icmp
ip.src == 192.168.*.* && icmp.type == 8
ip.src == 192.168.*.* && icmp.type == 0
ip.addr == 192.168.*.* && ip.addr == 192.168.*.* && icmp
ip.dst == 192.168.*.* && icmp.type == 8
icmp.type == 8