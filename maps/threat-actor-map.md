# 🕵️ Threat Actor Map

Track malicious IPs/domains, behavior, and blocking actions.

| IP / Domain       | Type         | Behavior Observed     | Source               | Blocked? | Notes                |
|-------------------|--------------|------------------------|----------------------|----------|----------------------|
| 45.142.166.55     | IPv4         | XML-RPC POST Flood     | web access logs      | ✅ Yes   | Detected on 2025-08-20 |
| logicwebb.com     | Domain       | Contact form spam      | WAF logs             | ❌ No    | Needs investigation  |
| 185.220.101.33    | Tor Exit Node| Repeated login fails   | auth.log via Wazuh   | ✅ Yes   | Matches known Tor IOC |
| semrush.com       | Domain         | High-volume crawling    | web access logs      | ❌ No    | Benign SEO bot, allowlisted. |
| protonmail.com    | Email Domain   | Suspicious form sender  | contact form logs    | ⚠️ Review | Pattern of abuse, needs manual check. |
