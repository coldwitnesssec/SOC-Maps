# Brute Force Login Incident Response

## Summary
Excessive failed login attempts against `/wp-login.php` (authentication endpoints). Precursor of/for account takeover and/or credential stuffing. 
### [RCN-TTCK]

## Detection
- Source: `auth.log`, WAF/Server logs  
- Indicator: ≥5 failed logins within 2 minutes from same IP  
- Tools: Wazuh rules, regex parsing, Suricata alerting

## Response Steps
1. Confirm failed login patterns in logs.  
2. Identify targeted account(s) >> lockout and/or compromised.  
3. Block source IP(s) or rate limited.
4. Notify, enforce, & reset (if needed).  
5. Enable/Verify MFA.
6. Continue monitoring.
7. Note findings.

## Artifacts
- `../logs/sanitize/vt-output_2025-09-07.md` (enriched IOC IPs)  
- Auth/WAF logs with failed login attempts  

## Notes
- Related MITRE ATT&CK: [T1110 - Brute Force]  
- Often overlaps with XML-RPC flooding.  
