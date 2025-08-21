## Detection Table

| Detection Type         | Trigger Logic                   | Source File/Tool     | True/False Positive Rate | Last Tested |
|------------------------|----------------------------------|-----------------------|---------------------------|-------------|
| Brute Force Login      | 5+ failed logins in 2 mins       | auth.log + Wazuh      | Low False Positives       | 2025-08-21  |
| WebShell Upload Attempt| Suspicious POST w/ PHP extension | nginx access log      | Medium Noise              | 2025-08-18  |
| Port Scan Detection    | >10 ports hit in <5 seconds      | Suricata              | High False Positives      | 2025-08-17  |
| XML-RPC Flooding       | 230 POSTs in 60s to xmlrpc.php   | Web access logs       | Low FP, High TP           | 2025-08-20  |
| Suspicious User-Agent  | Known bot UAs seen               | Web access logs       | Low FP                    | 2025-08-20  |

### Notes:
- **XML-RPC Flooding**: Confirmed abuse from multiple IPs. Used custom Python script for detection.
- **Brute Force Login**: POSTs to `/wp-login.php` within 2 min window. Regex on status codes.
- **Suspicious User-Agent**: Matched against AbuseIPDB & VirusTotal.
