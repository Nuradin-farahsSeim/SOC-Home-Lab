# Lab 01 – Wazuh SOC Environment Setup

## Objective

The purpose of this lab was to build the foundation of a home SOC environment using Wazuh, Windows, Kali Linux, and Oracle VirtualBox.

The main goal was to create a working SIEM environment, connect a Windows endpoint to Wazuh, and confirm that security events and alerts were being received successfully.

## Lab Environment

- Windows 11 host
- Oracle VirtualBox
- Kali Linux virtual machine
- Wazuh virtual appliance
- Home router/network
- Wazuh Windows Agent

## Network Setup

The lab devices were connected to the same home network.

Example lab structure:

```text
Home Router
   |
   |-- Windows Host
   |     |
   |     |-- Wazuh Agent
   |
   |-- Kali Linux VM
   |
   |-- Wazuh Server VM
