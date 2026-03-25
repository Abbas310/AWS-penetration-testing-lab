# Penetration Testing Lab – DVWA on AWS

## Overview
This project demonstrates a full penetration testing workflow on a vulnerable web application (DVWA) deployed on an AWS EC2 instance. The objective was to identify and exploit vulnerabilities, gain system access, and analyze the target environment.

---

## Lab Setup
- Target: DVWA (Damn Vulnerable Web Application)
- Hosting: AWS EC2 (Ubuntu)
- Attacker machine: Kali Linux
- Tools: Nmap, Netcat, Burp Suite (optional), Linux CLI

---

## Methodology

### 1. Vulnerability Identification
- Identified command injection vulnerability in DVWA
- Input fields allowed execution of system commands

### 2. Exploitation
- Injected commands into the vulnerable input field
- Executed system commands such as:
  - `whoami`
  - `uname -a`

### 3. Reverse Shell Access
- Established a reverse shell using Netcat
- Gained remote access to the target system

### 4. Post-Exploitation
- Enumerated system information:
  - OS version
  - user privileges (`www-data`)
- Verified system-level access

---

## Key Findings
- Web application vulnerable to command injection
- Lack of input sanitization
- Successful remote command execution
- Reverse shell allowed full interaction with the system

---

## Security Implications
- Improper input validation can lead to full system compromise
- Publicly exposed services increase attack surface
- Weak configurations can allow privilege escalation

---

## Mitigation Strategies
- Input validation and sanitization
- Use of prepared statements / secure coding practices
- Restrict execution privileges
- Network-level protections (firewalls, segmentation)
- Monitoring and logging of suspicious activity

---

## Screenshots
(Insert your screenshots here)

---

## Conclusion
This lab demonstrates how a simple web vulnerability can escalate into full system compromise, highlighting the importance of secure coding and system hardening.
