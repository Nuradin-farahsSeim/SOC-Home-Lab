# Lab 03 – Network Scan Detection and Firewall Investigation

## Objective

Simulate authorized network reconnaissance from Kali Linux against the Windows endpoint and investigate how Windows Defender Firewall and Windows Security logging recorded the activity.

## Environment

- Windows 11 endpoint
- Kali Linux
- Wazuh SIEM
- Wazuh Windows agent
- Windows Defender Firewall
- Nmap
- PowerShell
- Oracle VirtualBox

## Activity Generated

A TCP connection scan was launched from Kali Linux against the Windows endpoint:

```bash
nmap -Pn -sT --top-ports 20 <WINDOWS-IP>
```

### Command Breakdown

- `-Pn` — skips host discovery and treats the target as online.
- `-sT` — performs a TCP connect scan.
- `--top-ports 20` — scans 20 commonly used TCP ports.

## Investigation

The scan showed the target system was reachable while the tested ports were filtered. Windows Defender Firewall logs recorded dropped TCP traffic from the Kali system to the Windows endpoint.

Windows Security auditing also generated Event ID **5152**, which means:

> The Windows Filtering Platform blocked a packet.

## Key Event IDs

- **5152** — blocked packet
- **5156** — allowed connection
- **5157** — blocked connection

## SOC Analysis

The activity was expected because it was generated intentionally inside an authorized home lab. In a production environment, repeated connection attempts across many ports from an unfamiliar source could indicate reconnaissance or service discovery and should be correlated with additional network and endpoint evidence.

## Classification

**Benign / Authorized Security Testing**

## Evidence

See the [Screenshots](./Screenshots) folder for endpoint, Kali, Wazuh, and network evidence.

## Skills Practiced

- Nmap reconnaissance
- Firewall log analysis
- Windows Filtering Platform events
- Source/destination IP analysis
- Network event triage
- SOC investigation documentation
