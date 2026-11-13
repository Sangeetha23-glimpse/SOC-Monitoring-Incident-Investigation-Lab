# 🛡️ SOC Monitoring & Incident Investigation Lab

**A hands-on Security Operations Centre (SOC) project using Splunk Cloud, Sysmon, Windows 11 and Splunk Universal Forwarder.**

[![Platform](https://img.shields.io/badge/Platform-Windows%2011-blue)](https://www.microsoft.com/windows)
[![SIEM](https://img.shields.io/badge/SIEM-Splunk%20Cloud-green)](https://www.splunk.com/)
[![Monitoring](https://img.shields.io/badge/Monitoring-Sysmon-orange)](https://learn.microsoft.com/sysinternals/downloads/sysmon)
[![Focus](https://img.shields.io/badge/Focus-SOC%20L1-red)](https://attack.mitre.org/)

## 📌 Project Overview

This project demonstrates the setup of a basic SOC monitoring environment to collect, monitor and investigate Windows endpoint security events using Splunk Cloud.

The lab uses Sysmon to generate detailed endpoint telemetry and Splunk Universal Forwarder to collect and forward event logs to Splunk Cloud, where SPL searches and dashboards are used to monitor system activity and investigate network connections.

The objective is to gain practical exposure to SIEM monitoring, endpoint visibility, log analysis and basic SOC investigation workflows.

## 🖥️ Dashboard Preview

**SOC Monitoring Dashboard**

[View SOC Lab Demonstration Dashboard](./evidence/SOC%20L1%20Lab%20%E2%80%93%20Demonstration%20Dashboard%20(synthetic%20sample%20data).html)

*Note: Upload the HTML demonstration dashboard into the `evidence` folder using the filename shown above for this link to work.*

The Splunk dashboard includes:

1. **Top Process Activity** – Monitors process execution activity.
2. **Successful Windows Logons** – Displays successful logon activity.
3. **PowerShell Process Activity** – Provides visibility into PowerShell process activity.
4. **Sysmon Network Connections** – Displays process names, destination IP addresses, ports and user information.

## 🏗️ Lab Architecture

```text
Windows 11 Endpoint
        |
        v
      Sysmon
        |
        v
Windows Event Logs
        |
        v
Splunk Universal Forwarder
        |
        v
    Splunk Cloud
        |
        v
 SPL Searches & Dashboard
        |
        v
 SOC Monitoring and Investigation
```

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Windows 11 | Endpoint environment |
| Sysmon | Endpoint activity monitoring |
| Splunk Universal Forwarder | Log collection and forwarding |
| Splunk Cloud | SIEM and log analysis |
| SPL | Search and investigation |
| PowerShell | Windows administration and event verification |
| MITRE ATT&CK | Security investigation reference |

## 🔍 Monitoring & Investigation Activities

### 1. Endpoint Process Monitoring
- Monitored process execution activity using Sysmon.
- Reviewed process names and execution paths.
- Created SPL searches to summarise process activity.

### 2. Windows Logon Monitoring
- Reviewed successful Windows logon events.
- Used Windows Security Event ID 4624.
- Displayed logon activity in the Splunk dashboard.

### 3. PowerShell Activity Monitoring
- Monitored PowerShell-related process activity.
- Used SPL searches to identify PowerShell process events.

### 4. Network Connection Investigation
- Analysed Sysmon Event ID 3.
- Extracted process image, destination IP, destination port, hostname and protocol.
- Reviewed outbound connections associated with browser and system processes.
- Documented a sample investigation based on observed network events.

## 📝 Sample SOC Investigation

**Case ID:** SOC-001  
**Investigation:** Network Connection Analysis  
**Event Source:** Sysmon Event ID 3

During the investigation, network connections associated with Google Chrome and Google Updater were reviewed.

The investigation examined:
- Process image
- Destination IP address
- Destination hostname
- Destination port
- Network protocol
- Connection initiation status

**Observation:** The reviewed connection to a hostname ending in `1e100.net` was consistent with Google infrastructure and application HTTPS activity.

**Conclusion:** No confirmed malicious activity was identified in the reviewed sample.

See [`SAMPLE_INVESTIGATION_SOC-001.md`](./documentation/SAMPLE_INVESTIGATION_SOC-001.md) for the investigation notes.

## 📂 Repository Structure

```text
SOC-Monitoring-Incident-Investigation-Lab/
│
├── README.md
│
├── spl/
│   ├── 01_sysmon_network_connections.spl
│   ├── 02_external_network_connections.spl
│   ├── 03_investigate_selected_destinations.spl
│   ├── 04_process_activity.spl
│   ├── 05_successful_windows_logons.spl
│   └── 06_powershell_process_activity.spl
│
├── documentation/
│   ├── LAB_OVERVIEW.md
│   ├── SAMPLE_INVESTIGATION_SOC-001.md
│   └── VALIDATION_NOTES.md
│
└── evidence/
    └── README.md
```

## 🎯 Skills Demonstrated

- SIEM monitoring using Splunk Cloud
- SPL search queries and event analysis
- Windows Security Event Log monitoring
- Sysmon endpoint telemetry
- Process activity monitoring
- Network connection investigation
- Basic SOC investigation documentation
- MITRE ATT&CK fundamentals

## ⚠️ Project Scope & Limitations

- This is a single-endpoint learning lab, not a production SOC environment.
- The sample investigation did not identify a confirmed security threat.
- Failed logon monitoring (Event ID 4625) and real-time alerting are not included as completed features.
- The Splunk Cloud dashboard is saved in the author's account and may require authentication and appropriate permissions.
- No credentials, passwords or authentication tokens are included in this repository.

## 🚀 Learning Outcome

This project provided practical exposure to configuring endpoint telemetry collection, forwarding Windows event logs to a SIEM platform, creating SPL searches, building monitoring dashboards and documenting a basic network investigation.

**Project Focus:** SOC Analyst L1 | Security Monitoring | SIEM | Endpoint Investigation
