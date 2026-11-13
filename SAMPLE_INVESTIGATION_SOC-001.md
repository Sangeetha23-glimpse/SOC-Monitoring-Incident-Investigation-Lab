# Sample Investigation — SOC-001

**Type:** Sysmon network-connection review  
**SIEM:** Splunk Cloud  
**Event:** Sysmon Event ID 3 — Network connection  
**Endpoint:** Windows 11 lab endpoint

## Objective
Review selected network events and examine process, destination, port, protocol, hostname, and connection-initiated fields.

## Observed evidence
The reviewed results included:
- Process images associated with Google Chrome and Google Updater.
- Destination IP `142.251.222.174`.
- Destination hostname ending in `1e100.net`.
- Destination port `443`.
- Protocol `tcp`.
- `Initiated=true`.

A separate search also showed Microsoft Edge traffic to `40.104.107.178` on port `443`.

## Assessment
The hostname suffix `1e100.net` is associated with Google infrastructure. The Chrome/Google Updater process context is consistent with ordinary application HTTPS activity. The available evidence does not establish malicious activity.

## Outcome
**Disposition:** No confirmed malicious activity in the reviewed sample.  
**Follow-up:** Investigate future events showing unusual process paths, unexpected destinations, suspicious command lines, or corroborating indicators.

## ATT&CK note
No ATT&CK technique is assigned to this benign observation. A network connection alone is not evidence of adversary behaviour.
