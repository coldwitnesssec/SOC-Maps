| Source IP       | Destination IP  | Port | Protocol | Direction | Action | Notes                        |
|-----------------|-----------------|------|----------|-----------|--------|------------------------------|
| 99.175.87.246   | 192.0.2.10      | 80   | TCP      | Ingress   | Block  | Repeated /wp-login attempts  |
| ANY             | 192.0.2.10      | 22   | TCP      | Ingress   | Allow  | SSH access for internal use |
| 192.0.2.10      | 0.0.0.0/0       | 443  | TCP      | Egress    | Allow  | Web traffic out              |
| 203.0.113.45    | 192.0.2.10      | 80   | TCP      | Ingress   | Block  | Malicious scanner (Shodan)  |
| 10.0.0.0/8      | 192.0.2.10      | *    | ANY      | Ingress   | Allow  | Internal trusted subnet     |
