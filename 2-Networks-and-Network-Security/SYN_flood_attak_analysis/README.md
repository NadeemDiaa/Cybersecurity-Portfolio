# SYN Flood Attack – Network Traffic Analysis

This project simulates the investigation of a SYN flood attack on a travel agency’s website. As a security analyst, you identify the cause of a website outage, analyze captured network traffic, and prepare findings for management.

---

## Scenario
You work as a security analyst for a travel agency that promotes vacation packages on its website. Employees regularly access the company’s sales page to help customers find deals.

One afternoon, your monitoring system sends an alert indicating a web server issue. Attempting to access the site results in a **connection timeout** error. Using a packet sniffer, you detect a high volume of **TCP SYN requests** from an unfamiliar IP address, overwhelming the server’s capacity to respond.  

To mitigate the issue, you:
- Temporarily take the server offline to allow recovery
- Block the malicious IP address in the firewall
- Prepare an incident analysis for your manager detailing the type of attack and its impact

---

## Attack Identification

**Section 1 – Type of Attack**  
The evidence indicates the web server was subjected to a **SYN flood attack**, a type of **Denial-of-Service (DoS)** attack.  
- Connection timeouts began after a sudden surge of TCP SYN requests from a single unknown IP address.
- Packet capture logs confirm the abnormal traffic pattern.

---

## Attack Impact

**Section 2 – How the Attack Caused the Website to Malfunction**  
The attack exploited the TCP **three-way handshake** process:  
1. **SYN** – The client sends a SYN packet to initiate a connection.  
2. **SYN-ACK** – The server acknowledges and reserves resources for the connection.  
3. **ACK** – The client completes the handshake, establishing the session.  

In a SYN flood:
- The attacker sends a massive number of SYN packets without completing the handshake.
- The server reserves resources for each pending connection, quickly exhausting available ports.
- Legitimate connection attempts fail, resulting in website downtime for both customers and employees.

Captured logs show:
- **Green:** Normal TCP handshakes  
- **Red:** Attack activity (large volume of SYN requests)  
- **Yellow:** Legitimate TCP connections failing due to resource exhaustion caused by the attack

---

## Provided Resources
The following files were provided for the activity and used for analysis:
- **Wireshark TCP/HTTP Log (Raw)** – 📄 [Download PDF](./Wireshark_TCP_HTTP_log.pdf)  
- **Wireshark TCP/HTTP Log – Color Coded** – 📄 [Download PDF](./Wireshark_TCP_HTTP_log-Color_coded_TCP_log.pdf)  

---

## Deliverables
- **Attack Analysis Report** – Includes identification of the SYN flood attack, explanation of TCP handshake exploitation, and analysis of attack impact on server availability.

---

## Skills Demonstrated
- Network protocol analysis (TCP handshake)
- DoS attack identification
- Traffic pattern recognition using Wireshark
- Incident documentation and communication

---

## Tools Used
- **Wireshark** – Packet capture and analysis
- **TCP Protocol Analysis** – Understanding of the three-way handshake
- **Firewall Configuration** – IP blocking to mitigate immediate threats
