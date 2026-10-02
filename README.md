# SOC Home Lab

Hands-on blue-team and SOC analyst portfolio documenting the design, monitoring, detection, and investigation of security activity in a home lab.

## Lab Environment

- Windows 11 endpoint
- Wazuh SIEM
- Wazuh Windows agent
- Microsoft Sysmon
- Kali Linux
- Oracle VirtualBox
- Windows Event Logs
- Windows Defender Firewall
- PowerShell
- Nmap
- Wireshark

## Labs

### [Lab 01 – Environment Setup](./Lab01-Environment-Setup)
Built the SOC lab foundation, deployed the Wazuh environment, connected the Windows endpoint, and verified agent communication.

### [Lab 02 – First Detection & Investigation](./Lab02-First-Detection-Investigation)
Integrated Sysmon with Wazuh and investigated endpoint telemetry, including process activity and Wazuh rule/MITRE ATT&CK context.

### [Lab 03 – Network Scan Detection](./Lab03-Network-Scan-Detection)
Simulated authorized reconnaissance from Kali Linux with Nmap and investigated blocked network traffic using Windows Firewall and Windows Security logs.

### [Lab 04 – Failed Login Detection](./Lab04-Failed-Login-Detection)
Generated intentional failed Windows authentication attempts and investigated Event ID 4625 in Wazuh, including source address, logon type, failure status, rule ID, and severity.

## Skills Demonstrated

- SIEM monitoring and threat hunting
- Alert triage and event investigation
- Windows Event Log analysis
- Sysmon telemetry analysis
- Authentication investigation
- Network reconnaissance detection
- Windows Firewall analysis
- PowerShell and command-line investigation
- MITRE ATT&CK interpretation
- Incident documentation
- Evidence collection and screenshot documentation

## Investigation Workflow

For each lab, I practice the same analyst workflow:

1. Generate or observe activity in an authorized lab environment.
2. Identify the relevant Windows, Sysmon, firewall, or network telemetry.
3. Locate the event or alert in Wazuh.
4. Review the host, user, process, source IP, event ID, rule, severity, and surrounding activity.
5. Decide whether the activity is benign, suspicious, or malicious based on context.
6. Document the evidence and lessons learned.

## Repository Purpose

This repository is a learning portfolio. All simulated activity is performed only in systems I control for cybersecurity training and defensive security practice.

More labs will be added as I continue developing practical SOC analyst, detection, investigation, and incident response skills.
