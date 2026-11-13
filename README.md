# SOC Monitoring & Incident Investigation Lab

**Environment:** Windows 11, Sysmon, Splunk Universal Forwarder, Splunk Cloud.

A single-endpoint learning lab demonstrating Windows telemetry collection, SPL searches, dashboard monitoring, and a sample network-connection review.

## Dashboard panels demonstrated
- Top Process Activity
- Successful Windows Logons
- PowerShell Process Activity
- Sysmon Network Connections

The dashboard is saved in the author's Splunk Cloud account. Access may require an authenticated account with permission to that deployment; it is not claimed to be public.

## Repository
- `spl/` — SPL searches
- `documentation/` — lab overview, validation notes, sample investigation
- `evidence/` — add redacted screenshots from your own lab

## Limitations
Failed-logon monitoring (Event ID 4625), real-time alerting, public dashboard sharing, and confirmed malicious detections were not demonstrated as completed features. A public IP or HTTPS connection alone does not indicate malicious activity.

Do not upload Splunk credentials, tokens, private keys, `passwords.conf`, or sensitive account details.
