# SOC Analyst Maps & Playbooks (LabCommand.com)

This repository documents the core detection and response maps I use to defend and monitor **LabCommand.com** — a live web infrastructure where I run threat hunting, detection engineering, and SOC workflows.

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



### Vulnerability Map 🧭
Track exposed services, software versions, and known CVEs.
```
| Asset | IP Address | Service | Port | Version | CVE(s) | Risk Level | Scan Tool | Date Found |
|-------|------------|---------|------|---------|--------|------------|-----------|------------|
```

---

### 🌐 Network Topology Map
Document your lab or live environment connectivity.
```
| Node | IP | OS | Role | Connected To | Interface | Notes |
|------|----|----|------|--------------|-----------|-------|
```

---

### 🧱 Firewall / ACL Map
Log ingress/egress rules, blocklists, and allowed paths.
```
| Source IP | Destination IP | Port | Protocol | Direction | Action | Notes |
|-----------|----------------|------|----------|-----------|--------|-------|
```

---

### 📊 Logging Coverage Map
Track what logs you collect, how often, and where visibility is missing.
```
| Log Source | System | Format | Collection Tool | Frequency | Retention | Gaps |
|------------|--------|--------|------------------|-----------|-----------|------|
```

---

### 🕵️ Detection Map
Log detection logic, trigger conditions, and tuning notes.
```
| Detection Name | Source Log | Trigger Condition | Action Taken | False Positive Rate | ATT&CK Mapping | Notes |
|----------------|------------|-------------------|---------------|----------------------|-----------------|-------|
```

---

### 👤 Threat Actor Map
Track malicious IPs/domains, behaviors, and TTPs.
```
| IP / Domain | Type | Behavior Observed | Source | Blocked? | Notes |
|-------------|------|-------------------|--------|----------|-------|
```

---

### 💥 Incident Response Playbook
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

### 🧩 Asset Inventory Map
Track every system in your environment and link it to detections and logs.
```
| Hostname | IP Address | MAC Address | OS | Role | Logging Enabled? | Last Seen | Notes |
|----------|------------|-------------|----|------|------------------|------------|-------|
```

---

🔧 Built and maintained by: [LabCommand.com](https://labcommand.com)  
🧠 Designed for self-hosted SOC workflows, threat hunting, and detection lab operations.
