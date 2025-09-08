# Suspicious User-Agent Incident Response

## Summary
Web requests containing known malicious strings. Scanners, bots, or scripted exploitation attempts.

## Detection
- Source: Web access logs, WAF logs  
- Indicator: User-Agent in known bad list (AbuseIPDB, VT, GreyNoise)  
- Tools: Custom regex matching, enrichment feeds

## Response Steps
1. Review requests tied to suspicious user-agent.  
2. Check IP addresses against threat intel feeds.  
3. Block recurring User-Agent/IP's combinations >> WAF, (check) reverse proxy.  
4. Inspect for exploitation attempts (e.g., probing paths, uploads).  
5. Monitor for new variations of User-Agent strings.  

## Artifacts
- WAF/Server logs showing malicious User-Agents  
- Enrichment results from VT/AbuseIPDB  

## Notes
- Related MITRE ATT&CK: [T1595 - Active Scanning]  
- Detection tuning: Avoid false positives from legitimate crawlers (Googlebot, Bingbot).  
