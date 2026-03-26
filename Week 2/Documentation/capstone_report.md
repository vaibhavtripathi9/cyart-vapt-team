# Capstone Project - Full VAPT Cycle

## Objective
To perform a complete Vulnerability Assessment and Penetration Testing (VAPT) cycle on a vulnerable system and analyze its security weaknesses.

## Methodology

### 1. Reconnaissance
Identified target system and gathered basic information.

### 2. Scanning
Used Nmap to identify open ports and services.

### 3. Vulnerability Scanning
Used Nikto to detect web vulnerabilities.

### 4. Exploitation
Used Metasploit to exploit Samba vulnerability.

### 5. Post-Exploitation
Collected system information and verified root access.

## Execution

### Target System
Metasploitable2

### Attacker System
Kali Linux

### Findings

- Open ports: 21 (FTP), 22 (SSH), 80 (HTTP)
- Vulnerable service: Samba
- Exploit used: usermap_script

### Result
Successfully gained root access using Metasploit.

## Vulnerability Detection Log

| Timestamp | Target IP | Vulnerability | Phase |
|----------|----------|--------------|------|
| Day 2 | 192.168.154.129 | Open Ports | Scanning |
| Day 2 | 192.168.154.129 | Apache Issue | Scanning |
| Day 2 | 192.168.154.129 | Samba Exploit | Exploitation |

## Remediation

- Update Samba service
- Disable unused ports
- Apply security patches
- Use firewall protection
- Regular vulnerability scanning


## Detailed Report

A complete VAPT assessment was performed on the Metasploitable2 system using Kali Linux. 
The process began with reconnaissance to identify the target system, followed by network scanning using Nmap to detect open ports and services.

Vulnerability scanning was conducted using Nikto, which revealed web server misconfigurations and outdated services. 
The exploitation phase involved using the Metasploit Framework, where the Samba usermap script vulnerability was successfully exploited.

A command shell session was obtained, allowing full interaction with the system. 
Post-exploitation activities included gathering system information and verifying root access.

The assessment demonstrated that the system is highly vulnerable and can be easily compromised if not properly secured.
Appropriate remediation measures such as patching, service hardening, and firewall implementation are recommended.


## Non-Technical Summary

The system tested contains multiple security weaknesses that allow unauthorized access. 
By using security testing tools, it was possible to gain full control of the system.

This highlights the importance of keeping systems updated and properly secured. 
Organizations should regularly test their systems and fix vulnerabilities to prevent attacks.

