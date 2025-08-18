# Networks and Network Security

This section of the portfolio focuses on **network security analysis, incident response, and preventive hardening**.  
The projects simulate real-world scenarios where different types of network-based attacks or vulnerabilities were investigated, documented, and mitigated.  
Each folder contains supporting logs (e.g., `tcpdump`, `Wireshark`) and written analysis reports in PDF format.

---

## 📂 Projects

### 1. [Analyze Network Layer Communications](./AnalyzeNetworkLayerCommunications)
- **Scenario:** Customers reported they could not access `yummyrecipesforme.com`, receiving a *“destination port unreachable”* error.  
- **Focus:** DNS queries via UDP and ICMP error analysis.  
- **Deliverables:**  
  - `tcpdump_log.png`  
  - **Cybersecurity Incident Report – Network Traffic Analysis** (PDF)

---

### 2. [Brute Force Website Compromise](./BruteForce_Website_Compromise)
- **Scenario:** A disgruntled ex-employee brute-forced the admin credentials of `yummyrecipesforme.com`, injected JavaScript to prompt malware downloads, and redirected users to a fake domain.  
- **Focus:** Brute force attack exploitation, HTTP protocol analysis, and malware redirection.  
- **Deliverables:**  
  - `tcpdump_traffic_log.pdf`  
  - **Security Incident Report** (PDF)

---

### 3. [DDoS Incident Response Using NIST CSF](./DDoS_Incident_Response_NIST_CSF)
- **Scenario:** A DDoS ICMP flood attack disrupted a multimedia company’s internal network for two hours due to an unconfigured firewall.  
- **Focus:** Applying the **NIST Cybersecurity Framework (CSF)** to identify, protect, detect, respond, and recover.  
- **Deliverables:**  
  - **Incident Report Analysis – NIST CSF** (PDF)

---

### 4. [Network Hardening Risk Assessment](./Network_Hardening_Risk_Assessment)
- **Scenario:** A social media company experienced a data breach exposing customer PII. Investigation revealed weak password practices, default credentials, lack of MFA, and firewall misconfigurations.  
- **Focus:** Preventive risk assessment and network hardening strategies.  
- **Deliverables:**  
  - **Security Risk Assessment Report** (PDF)

---

### 5. [SYN Flood Attack Analysis](./SYN_flood_attak_analysis)
- **Scenario:** A travel agency’s web server was overwhelmed by a SYN flood DoS attack, preventing employees and customers from accessing services.  
- **Focus:** TCP three-way handshake exploitation and SYN flood attack mitigation.  
- **Deliverables:**  
  - `Wireshark_TCP_HTTP_log.pdf`  
  - `Wireshark_TCP_HTTP_log-Color_coded_TCP_log.pdf`  
  - **SYN Flood Attack Analysis Report** (PDF)

---

## 🛠 Skills Demonstrated
- Network traffic analysis (`tcpdump`, `Wireshark`)  
- Brute force attack investigation  
- SYN flood and ICMP flood (DDoS) detection & mitigation  
- Application of the **NIST Cybersecurity Framework (CSF)**  
- Security risk assessment & hardening strategies  
- Writing professional incident reports  

---

## 🔑 Tools & Methods
- **tcpdump** – CLI-based network traffic capture  
- **Wireshark** – Packet-level analysis and visualization  
- **NIST CSF** – Framework for cybersecurity strategy  
- **Firewall Rules & IDS/IPS** – Attack prevention & mitigation  
- **Password Policies & MFA** – Hardening against brute force attacks  
