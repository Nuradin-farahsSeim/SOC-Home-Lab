# Lab 02 – Sysmon Integration and First Detection Investigation

## Objective

Improve Windows endpoint visibility by installing Microsoft Sysmon, forwarding Sysmon telemetry to Wazuh, and investigating a detected endpoint event.

## Environment

- Windows 11 endpoint
- Wazuh SIEM
- Wazuh Windows agent
- Microsoft Sysmon
- PowerShell
- Windows Event Viewer
- Oracle VirtualBox

## Why Sysmon?

Sysmon provides detailed endpoint telemetry that can help analysts investigate process execution, file creation, network connections, registry activity, DNS activity, hashes, and other security-relevant behavior.

## Tasks Completed

1. Downloaded Sysmon from Microsoft Sysinternals.
2. Installed Sysmon using a configuration file.
3. Verified the `Sysmon64` service was running.
4. Added the Sysmon Operational channel to the Wazuh agent configuration.
5. Restarted the Wazuh agent.
6. Confirmed Sysmon telemetry appeared in Wazuh Threat Hunting.
7. Opened a detected event and reviewed the surrounding documents and Wazuh rule details.

## Wazuh Collection Configuration

```xml
<localfile>
  <location>Microsoft-Windows-Sysmon/Operational</location>
  <log_format>eventchannel</log_format>
</localfile>
```

## Investigation Example

One investigated Wazuh event matched:

- **Rule ID:** 92205
- **Rule level:** 9
- **MITRE ATT&CK mapping:** T1105 – Ingress Tool Transfer

The MITRE mapping was treated as context rather than proof that malicious activity occurred. The analyst still needs to review the process, command line, user, host, file path, source, and surrounding events.

## Analyst Workflow Practiced

1. Identify what happened.
2. Review when and where it occurred.
3. Identify the user, process, or file involved.
4. Review the Wazuh rule and severity.
5. Review MITRE ATT&CK context.
6. Inspect surrounding events.
7. Classify the activity based on evidence.

## Evidence

See the [Screenshots](./Screenshots) folder for Sysmon installation, Wazuh configuration, alert investigation, timeline, and rule details.

## Skills Practiced

- Sysmon deployment
- Endpoint telemetry collection
- Wazuh Threat Hunting
- Process and file-event investigation
- MITRE ATT&CK interpretation
- Alert triage
- Timeline analysis
