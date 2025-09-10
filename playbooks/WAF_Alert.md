# Incident Report

## Incident Type
**WAF Alert – Python Module Error**

---

### Trigger
WAF logs show `ModuleNotFoundError` from application

### Triage
- Confirm alert source and frequency  
- Correlate with deployment timeline

### Containment
- None required (informational only)

### Mitigation
- Notify application owner or deployment team if recurring

### Recovery
- Monitor for related anomalies (failed requests, downtime)

### Documentation
- Record in Detection Map and IR tracker  
- Tag: `App Misconfig`




## WAF Alert – Python Module Error

- **Trigger:** `ModuleNotFoundError` in WAF logs  
- **Triage:** Validate source, frequency, and timeline  
- **Containment:** N/A (informational)  
- **Mitigation:** Notify app/deployment team if persistent  
- **Recovery:** Watch for anomalies (failed requests, downtime)  
- **Documentation:** Detection Map + IR tracker → tag `App Misconfig`
