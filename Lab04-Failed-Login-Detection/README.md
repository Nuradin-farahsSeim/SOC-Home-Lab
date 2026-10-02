# Lab 04 – Failed Login Detection and Investigation with Wazuh

## Objective

The purpose of this lab was to generate intentional failed Windows login attempts, verify that Windows recorded the activity, and investigate the resulting authentication alerts in Wazuh.

The goal was to practice SOC triage and learn how to read failed-login events using Windows Security logs and Wazuh Threat Hunting.

## Lab Environment

- Windows 11 endpoint
- Wazuh SIEM
- Wazuh Windows Agent
- PowerShell
- Windows Security Event Logs
- Oracle VirtualBox

## Tools Used

- Wazuh
- PowerShell
- Windows Event Viewer
- Windows Security Auditing

## Key Event ID

```text
4625
