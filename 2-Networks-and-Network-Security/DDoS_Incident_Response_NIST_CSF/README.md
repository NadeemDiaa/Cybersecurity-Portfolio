# DDoS Attack – Incident Report Analysis Using NIST Cybersecurity Framework

This project documents a Distributed Denial-of-Service (DDoS) attack on a multimedia company’s internal network. Using the **NIST Cybersecurity Framework (CSF)**, the analysis outlines the incident response and provides recommendations for strengthening defenses against future attacks.

---

## Scenario
You are a cybersecurity analyst for a multimedia company that provides web design, graphic design, and social media marketing services.  

The organization experienced a **DDoS attack** that:  
- Flooded the internal network with **ICMP packets**  
- Overwhelmed resources and blocked legitimate traffic  
- Caused a **two-hour service outage** that halted business operations  

### Incident Response
The Incident Management Team responded by:  
- Blocking all incoming ICMP packets  
- Taking **non-critical services** offline to conserve resources  
- Restoring **critical network services** after containment  

### Root Cause
The investigation revealed the vulnerability was due to an **unconfigured firewall**, which allowed the malicious ICMP flood to enter the network.

---

## NIST CSF Analysis
The incident was reviewed using the five NIST CSF functions:

1. **Identify**  
   - Vulnerability: unconfigured firewall exposed the network to ICMP flooding  
   - Impact: two-hour outage affecting design workflows, social media campaigns, and client communications  

2. **Protect**  
   - Firewall rules updated to limit ICMP traffic  
   - Network monitoring software deployed to flag abnormal traffic  
   - IDS/IPS systems configured to block suspicious ICMP packets  

3. **Detect**  
   - Implemented **source IP verification** to detect spoofed ICMP packets  
   - Monitoring tools integrated to improve detection speed  

4. **Respond**  
   - Blocked ICMP packets immediately  
   - Shut down non-critical services to preserve resources  
   - Restored critical operations and deployed new protective measures  

5. **Recover**  
   - Restored services using verified backups and hardened firewall configurations  
   - Validated network stability before re-enabling non-essential services  
   - Notified clients of delays via backup channels (email/SMS)  
   - Conducted root-cause analysis and implemented **quarterly DDoS simulation drills** to improve resilience  

---

## Provided Resources
- **Incident Report Analysis (NIST CSF)** – 📄 [View PDF](./Incident_report_analysis_NIST_CSF.pdf)  
  Contains detailed summary, NIST CSF analysis, and recovery reflections.

---

## Skills Demonstrated
- Application of the **NIST Cybersecurity Framework**  
- DDoS detection and mitigation strategies  
- Firewall configuration and traffic filtering  
- Incident response and recovery planning  

---

## Tools & Methods Referenced
- **Firewall Rules** – ICMP rate limiting and anti-spoofing checks  
- **IDS/IPS** – Intrusion detection and prevention for malicious ICMP traffic  
- **Network Monitoring Software** – Abnormal traffic detection  
- **Backups & Recovery Protocols** – Ensuring business continuity
