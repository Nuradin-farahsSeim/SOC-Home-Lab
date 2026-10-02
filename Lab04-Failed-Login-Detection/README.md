# Lab 04 – Failed Login Detection and Investigation with Wazuh

## Objective
Practice investigating failed Windows authentication events with Wazuh and Windows Security logs.

## Environment
- Windows 11 endpoint
- Wazuh SIEM
- Wazuh Windows agent
- PowerShell
- Windows Security Event Logs

## Key Event
**Event ID 4625** indicates that an account failed to log on.

## Investigation Findings
- Endpoint: Windows-Host
- Event ID: 4625
- Logon Type: 2
- Source address: 127.0.0.1
- Status: 0xC000006D
- Substatus: 0xC000006A
- Wazuh Rule ID: 60122
- Wazuh Rule Level: 5
- Rule description: Logon Failure - Unknown user or bad password

## Analysis
Logon Type 2 represents an interactive local logon. The loopback source address supports that the activity originated from the same endpoint. The status and substatus values indicate a failed authentication caused by an incorrect password.

A single failed login can be normal. Repeated failures can be more significant when combined with unusual source addresses, multiple accounts, rapid repetition, account lockout, or other suspicious activity.

## Classification
**Benign / Authorized Security Testing**

## Skills Practiced
- Windows authentication analysis
- Event ID 4625 investigation
- Wazuh alert triage
- Logon type interpretation
- Event correlation
- Incident documentation
