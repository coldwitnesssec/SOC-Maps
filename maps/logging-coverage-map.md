### 📊 Logging Coverage Map

| Log Source           | System        | Format   | Collection Tool   | Frequency | Retention | Gaps                    |
|----------------------|---------------|----------|--------------------|-----------|-----------|-------------------------|
| Apache Access Logs   | Web Server    | .log     | Local tail         | Daily     | 30d       | None                    |
| Auth Logs            | Linux Server  | .log     | Local              | Daily     | 90d       | No SIEM yet             |
| PHP Error Logs       | Web Server    | .log     | None               | Manual    | Unknown   | Visibility gap          |
| MalCare Logs         | WordPress     | .csv     | Manual Download    | Weekly    | 1 file    | Needs automation        |
| WP Access Logs       | WordPress     | .csv     | Manual Download    | Weekly    | 1 file    | No correlation engine   |
| Future IDS Alerts    | Planned IDS   | .log     | TBD (Snort?)       | TBD       | TBD       | Not yet configured      |
