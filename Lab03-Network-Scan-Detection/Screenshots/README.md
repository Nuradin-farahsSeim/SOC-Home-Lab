# Lab 03 – Network Scan Detection and Windows Firewall Investigation

## Objective

The purpose of this lab was to simulate basic network reconnaissance from Kali Linux against a Windows endpoint, observe how Windows Firewall handled the traffic, and investigate the resulting network security events.

The lab focused on understanding how a SOC analyst can trace activity from a source system to firewall logs and Windows Security events.

## Lab Environment

- Windows 11 endpoint
- Kali Linux virtual machine
- Wazuh SIEM
- Wazuh Windows Agent
- Windows Defender Firewall
- PowerShell
- Nmap
- Oracle VirtualBox

## Network Information

The lab devices were connected to the same home network.

Example addresses used:

```text
Windows Endpoint: 192.168.0.149
Kali Linux:       192.168.0.195
Wazuh Server:     192.168.0.216
