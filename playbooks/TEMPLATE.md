# Playbook: [Name of Playbook]

## Detection
- Indicators: [list observable signs,> suspicious process, email domain, network traffic]
- Logs: [which logs show it,> Windows Security log, O365, firewall]
- Tools: [which tools generate alerts,>  Splunk, Elastic, EDR]

## Analysis
- Manual Checks:
  - [first check]
  - [extraction/inspection steps]
- Automated Checks:
  - [sandboxing, VirusTotal, AbuseIPDB, YARA rules]

## Response
- Containment:
  - [isolate host, block sender/IP, quarantine email]
- Eradication:
  - [kill process, delete malicious file, disable account]
- Recovery:
  - [reset password, patch, restore backups]

## Escalation
- Criteria for Tier 2 / Incident Response:
  - [malicious/high value accounts affected]
- Criteria for Legal/Compliance:
  - [when PII/data exfiltration suspected]

## References
- MITRE ATT&CK: [T####](https://attack.mitre.org/techniques/T####)
- Vendor docs or best practices: [link here .PDF > ect.]
