### 💥 Incident Response Playbook

Standardized response flow for common incidents.

---

## Incident Type: [e.g., Web Shell Upload Attempt]

**Trigger:**  
Suspicious file upload to `/wp-content/uploads/` flagged by WAF or log anomaly.

**Triage:**  
Check logs, verify uploader IP, confirm file presence and hash.

**Containment:**  
Block offending IP at firewall, disable PHP in upload dir.

**Mitigation:**  
Delete file, scan for persistence, patch vulnerable plugin.

**Recovery:**  
Restart affected services, validate normal operation, reset creds if needed.

**Documentation:**  
Log timeline of events, include hashes, commands used, and lessons learned.
