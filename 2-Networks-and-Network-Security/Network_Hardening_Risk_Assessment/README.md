# Network Hardening – Security Risk Assessment

This project analyzes a data breach at a social media organization and provides a security risk assessment with recommendations to prevent similar incidents in the future. The focus is on identifying vulnerabilities, applying network hardening methods, and improving overall organizational security posture.

---

## Scenario
You are a security analyst working for a social media organization that recently experienced a **major data breach**, exposing customer personal information such as names and addresses.  

During your inspection, you discovered four major vulnerabilities:
1. Employees share passwords.  
2. The database admin password is still set to its **default value**.  
3. Firewalls have **no filtering rules** in place for incoming or outgoing traffic.  
4. **Multifactor authentication (MFA)** is not implemented.  

If these issues remain unaddressed, the organization risks further breaches and attacks.

Your task is to write a **security risk assessment report** recommending hardening methods to mitigate these risks.

---

## Key Recommendations
The following hardening tools and methods were selected for implementation:

1. **Multifactor Authentication (MFA)**  
   - Adds a second layer of verification beyond passwords (e.g., app code, hardware key, fingerprint).  
   - Protects against stolen, guessed, or shared credentials.  
   - Requires one-time setup but ongoing enforcement.  

2. **Password Policies**  
   - Enforces strong, unique, non-default credentials.  
   - Prevents weak or shared passwords from exposing systems.  
   - Must be reviewed and updated regularly in line with industry standards.  

3. **Firewall Maintenance**  
   - Ensures traffic filtering rules block unnecessary or malicious traffic.  
   - Reduces the attack surface by controlling inbound and outbound connections.  
   - Requires ongoing review of rules, log analysis, updates, and patching.  

---

## Provided Resources
- **Security Risk Assessment Report** – 📄 [View PDF](./Social_Media_Organization_Network_Hardening_assessment_report.pdf)  
  Includes detailed recommendations on MFA, password policies, and firewall maintenance.

---

## Skills Demonstrated
- Risk assessment and documentation  
- Application of network hardening strategies  
- Security controls selection and justification  
- Prevention-focused security planning  

---

## Tools & Methods Referenced
- **Multifactor Authentication (MFA)**  
- **Password Policy Enforcement**  
- **Firewall Configuration & Maintenance**
