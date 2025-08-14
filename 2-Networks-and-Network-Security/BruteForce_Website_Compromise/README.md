# Website Compromise via Brute Force Attack – Incident Analysis

This project documents a cybersecurity incident involving a brute force attack against **yummyrecipesforme.com**, resulting in a malicious code injection and redirection to a malware-infected site. The analysis focuses on identifying the network protocols involved, documenting the incident timeline, and recommending security measures to prevent similar attacks.

---

## Scenario
You are a cybersecurity analyst for **yummyrecipesforme.com**, a website selling recipes and cookbooks.  
A disgruntled former employee used a **brute force attack** to guess the default administrator password for the web host. Once inside the admin panel, they injected **JavaScript** into the website’s source code to prompt visitors to download and run a malicious executable file.  

When customers ran the file, their browsers were redirected to **greatrecipesforme.com**, which hosted malware. The attacker then changed the admin password, preventing the website owner from regaining access.

Customer complaints to the helpdesk reported:
- Being prompted to download a file claiming to update their browser
- Redirection to a fake website after running the file
- Slow system performance afterward

---

## Investigation
To analyze the incident:
1. A **sandbox environment** was set up to safely reproduce the attack.
2. The **tcpdump** network protocol analyzer was run while visiting `yummyrecipesforme.com`.
3. The malicious behavior was confirmed — prompt to download and run an executable file followed by browser redirection to `greatrecipesforme.com`.

---

## Key Findings
- **Primary network protocol involved:**  
  Hypertext Transfer Protocol (**HTTP**), operating at the application layer.
  
- **Incident sequence from tcpdump log:**
  1. DNS resolution request sent for `yummyrecipesforme.com` → returned IP `203.0.113.22`.
  2. HTTP GET request made to `yummyrecipesforme.com`.
  3. Malicious file downloaded from `yummyrecipesforme.com`.
  4. DNS resolution request sent for `greatrecipesforme.com` → returned IP `192.0.2.17`.
  5. HTTP connection established with `greatrecipesforme.com` (malware site).

- **Cause:**  
  The admin password was never changed from its **default setting**, allowing a brute force attack to succeed without detection or prevention.

---

## Remediation Recommendations
To prevent future brute-force attacks:
- Enforce **two-factor authentication (2FA)** for all administrative accounts.
- Eliminate default credentials and require **strong initial passwords** (minimum 12 characters, mixed case, numbers, special characters).
- Implement **rate limiting** (lock accounts after 5 failed login attempts).
- Restrict admin access via **IP allowlisting**.

---

## Provided Resources
The following file was provided for analysis:
- **tcpdump Traffic Log** – 📄 [View PDF](./tcpdump_traffic_log.pdf)

---

## Deliverables
- **Security Incident Report** – 📄 [View PDF](./yummyrecipesforme_Security_incident_report.pdf)  
  Includes network protocol identification, incident documentation, and remediation recommendations.

---

## Skills Demonstrated
- Web application security analysis
- Brute force attack detection
- Network traffic investigation with `tcpdump`
- Security reporting and remediation planning

---

## Tools Used
- **tcpdump** – Network protocol analysis
- **Sandbox Environment** – Safe malware execution testing
- **DNS & HTTP Protocol Analysis** – Understanding of malicious redirection flow
