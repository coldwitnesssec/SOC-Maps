# Playbook: Phishing Email Triage

## Detection
- Indicators: suspicious sender, mismatched domains, attachment anomalies
- Logs: email gateway, O365 message trace, spam filter

## Analysis
- Extract email headers
- Sandbox attachments or URLs
- Check IOCs (hash, URL, sender) against VT/AbuseIPDB

## Response
- Quarantine email and similar messages
- Alert affected user(s)+ > amount
- Block sender/domain/IP

## Escalation
- Escalate to Tier 2 if confirmed credential harvesting or malware delivery
- Escalate to IR team if multiple users impacted

## References
- MITRE ATT&CK: [Phishing (T1566)](https://attack.mitre.org/techniques/T1566/)
