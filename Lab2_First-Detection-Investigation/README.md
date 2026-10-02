# Lab 02 – Sysmon Integration with Wazuh

## Objective

The purpose of this lab was to improve endpoint visibility by installing Microsoft Sysmon on the Windows host and forwarding Sysmon events into Wazuh.

The goal was to collect detailed endpoint telemetry such as process creation, file creation, registry activity, network connections, and DNS queries for SOC investigation.

## Lab Environment

- Windows 11 endpoint
- Wazuh SIEM
- Wazuh Windows Agent
- Microsoft Sysmon
- PowerShell
- Windows Event Viewer
- Oracle VirtualBox

## Tools Used

- Wazuh
- Sysmon
- Windows Event Viewer
- PowerShell
- Oracle VirtualBox

## What is Sysmon?

Sysmon is a Microsoft Sysinternals tool that records detailed Windows system activity.

Examples of telemetry Sysmon can collect include:

- Process creation
- Network connections
- File creation
- Registry changes
- DNS queries
- Process hashes

This additional telemetry gives a SOC analyst more visibility than standard Windows logging alone.

## Tasks Completed

### 1. Downloaded Sysmon

Sysmon was downloaded from the official Microsoft Sysinternals website.

The files were extracted to the SOC lab directory.

Example files included:

```text
Sysmon.exe
Sysmon64.exe
Sysmon64a.exe
