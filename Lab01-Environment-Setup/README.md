# Lab 01 – Wazuh SOC Environment Setup

## Objective

Build the foundation of a home SOC environment, deploy Wazuh, connect a Windows endpoint, and verify that the agent is communicating with the SIEM.

## Environment

- Windows 11 endpoint
- Wazuh virtual appliance
- Wazuh Windows agent
- Kali Linux VM
- Oracle VirtualBox
- Home lab network

## Tasks Completed

1. Deployed the Wazuh virtual appliance.
2. Verified the Wazuh server was reachable from the lab network.
3. Installed and configured the Wazuh agent on Windows.
4. Started the Wazuh agent service.
5. Confirmed the Windows endpoint appeared as active in Wazuh.
6. Documented the environment with screenshots.

## SOC Concepts Practiced

- SIEM architecture
- Endpoint agent deployment
- Log collection
- Agent-to-manager communication
- Basic SOC environment validation

## Evidence

See the [Screenshots](./Screenshots) folder for configuration and verification evidence.

## Result

The Windows endpoint successfully connected to Wazuh, establishing the monitoring foundation used in later detection and investigation labs.
