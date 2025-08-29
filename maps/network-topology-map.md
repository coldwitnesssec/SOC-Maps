### 🌐 Network Topology Map

| Node           | IP          | OS          | Role          | Connected To     | Interface | Notes                  |
|----------------|-------------|-------------|---------------|------------------|-----------|------------------------|
| analyst-vm     | 192.0.2.100 | Kali Linux  | SOC Analyst   | switch-01        | eth0      | Used for log parsing   |
| webserver-01   | 192.0.2.10  | Ubuntu      | Web Server    | switch-01        | ens33     | Public-facing HTTP     |
| switch-01      | N/A         | N/A         | Virtual Switch| analyst-vm, webserver-01 | br0   | Hyper-V bridge         |
| IDS-VM         | 192.0.2.50  | Debian      | Planned IDS   | switch-01        | eth1      | Will run Suricata      |
