# IOC Summary: Contact Form Abuse (Sept 2025)

Repeated hits to `/about/contact/` endpoint using spoofed User-Agents (Opera, Vivaldi, YaBrowser).  
Behavior consistent with automated spam bots rotating IPs and UAs.

---

## High Confidence IOCs
(Flagged by AbuseIPDB + VirusTotal, observed in logs)

- **156.248.87.78**  
  - Source: Firewall + Server logs  
  - Behavior: Repeated POSTs to `/about/contact/`  
  - UA: Opera / Vivaldi variants  
  - Abuse Score ≥25, Reports ≥100  

- **156.233.91.84**  
  - Source: Firewall + Server logs  
  - Behavior: Contact form spam, rotating UAs  
  - Abuse Score ≥25, Reports ≥160  

- **190.185.109.130**  
  - Source: Firewall + Server logs  
  - Behavior: Contact form spam, multiple UA strings  
  - Reports ≥120  

- **45.202.78.111**  
  - Source: Firewall + Server logs  
  - Behavior: Repeated contact form hits  
  - UAs: YaBrowser/Yowser spoofed  

---

## Medium Confidence IOCs
(Observed in logs, lower volume but still abusive patterns)

- **156.249.60.5**  
  - Source: Firewall logs  
  - Behavior: Contact form spam  

- **156.228.99.252**  
  - Source: Firewall logs  
  - Behavior: Contact form hits, repeated  

- **154.213.204.19**  
  - Source: Firewall logs  
  - Behavior: Suspicious contact form activity  
  - Abuse Score ~22  

---

## Notes
- All IOCs were tied to **form abuse campaigns** (spam runs against `/about/contact/`).  
- User Agent rotation = bot behavior >> not legitimate browsers.  
- Recommend:  
  - Add to **deny/block lists** in Firewall.  
  - Enable **reCAPTCHA/honeypot** on all forms.  
  - Log to central SIEM for correlation.  

---

## Additional IOCs (Seen in Webserver/Firewall, Not in Form Submissions)

These IPs did not appear in the **contact form abuse logs**, but were observed in **webserver and firewall activity**.  
They are tied to the same provider blocks (3xK Tech GmbH and others) as confirmed abusive neighbors and carry significant AbuseIPDB/VT flags.  
They should be tracked and considered for block/alerting.

- **156.253.164.131**  
  - Block: 156.253.164.0/24  
  - Abuse Score: 26 (≥25) | Reports: 38  
  - VT: 2 malicious detections  
  - Verdict: Suspicious  

- **156.253.164.165**  
  - Block: 156.253.164.0/24  
  - Abuse Score: 17 | Reports: 34  
  - VT: 0 malicious, 1 suspicious  
  - Verdict: Suspicious  

- **156.233.88.232**  
  - Block: 156.233.88.0/24  
  - Abuse Score: 24 | Reports: 11  
  - VT: 1 malicious, 2 suspicious  
  - Verdict: Suspicious  

- **156.233.88.167**  
  - Block: 156.233.88.0/24  
  - Abuse Score: 16 | Reports: 17  
  - VT: 1 malicious  
  - Verdict: Suspicious  

- **156.233.72.6**  
  - Block: 156.233.0.0/16  
  - Abuse Score: 21 | Reports: 14  
  - VT: 1 malicious  
  - Verdict: Suspicious  

- **156.228.97.100**  
  - Block: 156.228.0.0/16  
  - Abuse Score: 37 (≥25) | Reports: 138  
  - VT: 1 malicious  
  - Verdict: Suspicious  

- **156.228.76.136**  
  - Block: 156.228.0.0/16  
  - Abuse Score: 31 (≥25) | Reports: 143  
  - VT: 2 malicious  
  - Verdict: Suspicious  

- **156.242.47.139**  
  - Block: 156.242.0.0/16  
  - Abuse Score: 25 (≥25) | Reports: 31  
  - VT: 2 malicious  
  - Verdict: Suspicious  

- **45.202.76.55**  
  - Block: 45.202.0.0/16  
  - Abuse Score: 21 | Reports: 17  
  - VT: 0 malicious, 1 suspicious  
  - Verdict: Suspicious  

- **154.94.13.83**  
  - Block: 154.94.0.0/16  
  - Abuse Score: 40 (≥25) | Reports: 29  
  - VT: 1 malicious  
  - Verdict: Suspicious  

- **173.239.254.37**  
  - Provider: LogicWeb Inc.  
  - Abuse Score: 64 (≥25) | Reports: 123  
  - VT: 2 malicious, VT reputation −1  
  - Verdict: Suspicious (high confidence)  

- **185.251.19.104**  
  - Provider: T.K Bytech LTD  
  - Abuse Score: 21 | Reports: 49  
  - VT: 0 malicious  
  - Verdict: Suspicious  

- **98.159.233.65**  
  - Provider: VPN Consumer Network  
  - Abuse Score: 26 (≥25) | Reports: 27  
  - VT: 2 malicious  
  - Verdict: Suspicious  

