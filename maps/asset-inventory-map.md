### 🧩 Asset Inventory Map

Track every system in your environment and link it to detections and logs.

| Hostname       | IP Address    | MAC Address       | OS            | Role         | Logging Enabled? | Last Seen        | Notes                       |
|----------------|---------------|-------------------|---------------|--------------|------------------|------------------|-----------------------------|
| webserver-01   | 192.0.2.10    | 00:0c:29:aa:bb:cc  | Ubuntu 22.04  | Web Server   | Yes              | 2025-08-28 12:00 | Collects NGINX + PHP logs  |
| kali-vm        | 192.0.2.50    | 00:0c:29:dd:ee:ff  | Kali Linux    | Analyst VM   | Partial          | 2025-08-27 18:44 | Manual log review only     |
| win10-siem     | 192.0.2.20    | 00:0c:29:11:22:33  | Windows 10    | Log Parser   | Yes              | 2025-08-28 15:12 | Wazuh agent active         |
