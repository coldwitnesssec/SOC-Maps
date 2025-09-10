# SOC Analyst Maps & Playbooks

This repository documents the core detection and response maps I use to defend and monitor **Websites** — infrastructures where I run threat hunting, detection engineering, and SOC workflows.

---

## 📂 Contents

- [🧭 Vulnerability Map](#vulnerability-map)
- [🌐 Network Topology Map](#network-topology-map)
- [🔥 Firewall / ACL Map](#firewall--acl-map)
- [🧠 Detection Map](#detection-map)
- [👾 Threat Actor Map](#threat-actor-map)
- [🌸 Incident Response Playbook](#incident-response-playbook)
- [🖥 Asset Inventory Map](#asset-inventory-map)
- [🧪 Logging Coverage Map](#logging-coverage-map)
- [🪵 Log Map](#log-map)



### Vulnerability Map
Track exposed services, software versions, and known CVEs.
```
| Asset | IP Address | Service | Port | Version | CVE(s) | Risk Level | Scan Tool | Date Found |
|-------|------------|---------|------|---------|--------|------------|-----------|------------|
```

---

### Network Topology Map
Document your lab or live environment connectivity.
```
| Node | IP | OS | Role | Connected To | Interface | Notes |
|------|----|----|------|--------------|-----------|-------|
```

---

### Firewall / ACL Map
Log ingress/egress rules, blocklists, and allowed paths.
```
| Source IP | Destination IP | Port | Protocol | Direction | Action | Notes |
|-----------|----------------|------|----------|-----------|--------|-------|
```

---

### Logging Coverage Map
Track what logs you collect, how often, and where visibility is missing.
```
| Log Source | System | Format | Collection Tool | Frequency | Retention | Gaps |
|------------|--------|--------|------------------|-----------|-----------|------|
```

---

### Detection Map
Log detection logic, trigger conditions, and tuning notes.
```
| Detection Name | Source Log | Trigger Condition | Action Taken | False Positive Rate | ATT&CK Mapping | Notes |
|----------------|------------|-------------------|---------------|----------------------|-----------------|-------|
```

---

### Threat Actor Map
Track malicious IPs/domains, behaviors, and TTPs.
```
| IP / Domain | Type | Behavior Observed | Source | Blocked? | Notes |
|-------------|------|-------------------|--------|----------|-------|
```

---

### Incident Response Playbook
Standardized response flow for common incidents.
```
## Incident Type: [e.g., Web Shell Upload Attempt]
**Trigger:**  
**Triage:**  
**Containment:**  
**Mitigation:**  
**Recovery:**  
**Documentation:**  
```

---

### Asset Inventory Map
Track every system in your environment and link it to detections and logs.
```
| Hostname | IP Address | MAC Address | OS | Role | Logging Enabled? | Last Seen | Notes |
|----------|------------|-------------|----|------|------------------|------------|-------|
```

---

### Log Map

Document your key log sources, collection methods, and sample entries across your lab infrastructure.

#### Log Sources

- **Web server logs** (e.g., Apache access logs)
- **Auth logs** (`/var/log/auth.log`)
- **Syslog** from Linux servers (`/var/log/syslog`)
- **Application logs** (WordPress, PHP errors, etc.)
- **IDS alerts** (planned Suricata/Snort setup)

#### Log Collection

- Local collection (log files stored on host)
- Centralized via rsyslog, Filebeat, or Wazuh (in progress)
- Future SIEM integration (e.g., Splunk, ELK, Graylog)

#### Examples

Paste sanitized log lines here to show structure and support detection tuning.

```log
192.168.0.5 - - [09/Aug/2025:12:09:00 -0500] "GET /index.php HTTP/1.1" 200
Aug 09 12:09:01 kali sshd[2301]: Failed password for invalid user admin from 10.10.10.10 port 445 ssh2


🔧 Built and maintained by: [LabCommand.com](https://labcommand.com)  
🧠 Designed for self-hosted SOC workflows, threat hunting, and detection lab operations.
