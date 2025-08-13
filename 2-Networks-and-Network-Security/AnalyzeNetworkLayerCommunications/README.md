# Analyze Network Layer Communications

This project simulates the role of a cybersecurity analyst investigating a network access issue for a client website. The investigation involves analyzing DNS and ICMP traffic to determine the cause of a reported connectivity problem.

---

## Scenario
You are a cybersecurity analyst at a company providing IT services for clients. Several customers reported that they were unable to access the client’s website, **www.yummyrecipesforme.com**, receiving the error:

> "Destination port unreachable"

After verifying the issue, you used a network analyzer tool (`tcpdump`) to capture and analyze traffic during an attempted webpage load.

---

## Investigation Summary
- **Initial observation:** Customers and internal tests confirmed the "destination port unreachable" error.  
- **DNS resolution attempt:** Browser sent a query to a DNS server via **UDP** to port 53, as part of the DNS protocol.  
- **Analysis result:** ICMP packets were returned with the error message **"udp port 53 unreachable"**.  
- **Impact:** Port 53, which is essential for DNS resolution, was unreachable, preventing the domain name from resolving to an IP address.  
- **Most likely cause:** The DNS server was unresponsive, potentially due to a **Denial of Service (DoS) attack**.

---

## Findings from Network Traffic Analysis

**Part 1 – Summary of the Problem**  
The `tcpdump` analysis revealed that UDP packets to the DNS server (port 53) resulted in ICMP messages indicating **port 53 unreachable**. Without DNS resolution, the browser could not obtain the IP address for the website, causing access failures.

**Part 2 – Analysis and Possible Cause**  
- Customer reports were first logged at **1:24 p.m.**.  
- IT team reproduced the issue and captured traffic using `tcpdump`.  
- ICMP response anomalies suggested possible packet manipulation or spoofing.  
- The behavior is consistent with a **DoS attack targeting the DNS server**, though further server log analysis would be required to confirm.

---

## Deliverables
- **Network Traffic Log (tcpdump output)**  
  ![TCPDump Log](./tcpdump_log.png)

- **Cybersecurity Incident Report – Network Traffic Analysis**  
  📄 [Download PDF](./Cybersecurity_incident_report_network_traffic_analysis.pdf)

---

## Skills Demonstrated
- Network protocol analysis (DNS, UDP, ICMP)
- Use of `tcpdump` for packet capture and inspection
- Incident verification and hypothesis development
- Technical reporting and documentation

---

## Tools Used
- **tcpdump** – Network packet analyzer
- **ICMP** – Diagnostic protocol for network communication issues
- **DNS Protocol** – Understanding of UDP port 53 resolution process
