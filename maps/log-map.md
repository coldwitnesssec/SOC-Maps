# Log Map

## Overview
This map documents the key log sources I currently monitor across my lab infrastructure, including my public web server and Linux VMs. Logs are collected locally for now, but a centralized SIEM setup is planned.

## Log Sources
- Web server logs (e.g., Apache access logs)
- Auth logs (`/var/log/auth.log`)
- Syslog from Linux servers (`/var/log/syslog`)
- Application logs (WordPress, PHP errors)
- IDS alerts (planned Snort/Suricata)

## Log Storage & Collection
- [x] Local
- [ ] Centralized via rsyslog or Wazuh or Filebeat
- [ ] SIEM (Splunk/ELK/etc.)

## Examples
Paste in sanitized log examples here to show structure:
```plaintext
192.168.0.5 - - [20/Aug/2025:12:00:00 -0500] "GET /index.php HTTP/1.1" 200
