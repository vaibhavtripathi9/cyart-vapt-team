🔐 Capstone Project - Full VAPT Cycle

🎯 Objective

The objective of this project is to perform a complete Vulnerability Assessment and Penetration Testing (VAPT) cycle on a vulnerable environment. The goal is to identify security weaknesses, exploit vulnerabilities, and provide remediation strategies to improve system security.

---

🧪 Methodology

1. Reconnaissance

In this phase, the target system was identified and basic information was gathered. Network discovery techniques were used to determine the active host and its IP address within the local network environment.

---

2. Scanning

Network scanning was performed using Nmap to identify open ports and running services. This helped in understanding the attack surface of the target system.

Command Used:

nmap -sV 192.168.154.129

Findings:

- Port 21: FTP (VSFTPD 2.3.4)
- Port 22: SSH
- Port 80: HTTP

---

3. Vulnerability Assessment

Vulnerabilities were identified based on the services detected. The FTP service was found to be running a vulnerable version, and the web application (DVWA) exposed multiple vulnerabilities such as SQL Injection and Cross-Site Scripting (XSS).

---

4. Exploitation

Exploitation was performed using Metasploit Framework and manual testing.

- VSFTPD backdoor vulnerability was exploited to gain system access.
- SQL Injection was performed on DVWA to extract database information.
- Burp Suite was used to intercept and manipulate HTTP requests.

---

5. Post-Exploitation

After gaining access, further enumeration was conducted to assess the level of compromise.

Commands Used:

whoami
id
uname -a
cat /etc/passwd

The results confirmed root-level access, indicating full system compromise.

---

6. Network Analysis

Network traffic was captured using Wireshark to analyze HTTP requests and responses. Sensitive data such as session cookies and parameters were observed in unencrypted traffic.

---

7. Privilege Escalation

Privilege escalation techniques were applied to verify access level. The system already provided root-level access, confirming complete control over the target system.

---

⚠️ Key Findings

ID| Vulnerability| Severity| Description
F001| VSFTPD Backdoor| Critical| Allows remote command execution
F002| SQL Injection| Critical| Database access without authentication
F003| XSS (Reflected/Stored)| Medium| Client-side script execution
F004| Weak Session Handling| Medium| Session hijacking risk

---

🛠️ Remediation

- Update outdated services such as VSFTPD
- Implement input validation and prepared statements
- Enable HTTPS for secure communication
- Improve session management (secure cookies)
- Apply least privilege principle
- Regularly perform security testing

---

📊 Conclusion

This project demonstrated a complete VAPT lifecycle, starting from reconnaissance to exploitation and reporting. Multiple critical vulnerabilities were successfully exploited, leading to full system compromise. The assessment highlights the importance of secure coding practices, system updates, and regular security audits.

---

📸 Screenshots

All screenshots related to:

- Nmap Scan
- Exploitation (Metasploit)
- Burp Suite Testing
- Wireshark Analysis
- Privilege Escalation

are available in the Screenshots folder.

---

📁 Project Structure

Week 4/
│
├── Documentation/
├── Screenshots/
├── Notes/
└── README.md

---

👨‍💻 Author

Vaibhav Tripathi
VAPT Intern
