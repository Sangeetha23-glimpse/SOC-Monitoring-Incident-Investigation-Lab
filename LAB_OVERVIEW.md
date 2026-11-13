# Lab Overview

## Objective
Collect Windows endpoint telemetry and make it searchable in Splunk Cloud.

## Components
| Component | Purpose |
|---|---|
| Windows 11 | Endpoint |
| Sysmon | Process and network event logging |
| Splunk Universal Forwarder | Event collection and forwarding |
| Splunk Cloud | Search, analysis, dashboard |

## Data sources
- `Microsoft-Windows-Sysmon/Operational`
- Windows Security event logs

## Dashboard
The saved dashboard contains panels for process activity, successful Windows logons, PowerShell process activity, and Sysmon network connections.

This is a single-endpoint learning lab, not an enterprise SOC deployment. It does not claim production incident-response experience or confirmed threat discovery.
