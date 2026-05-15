# A-Multi-Stage-Cyber-Attack-Simulation-Framework-for-Enterprise-Web-Applications

# Enterprise Breach Simulation, Detection & Security Hardening

## Project Overview

This project demonstrates a simulated enterprise cyber attack scenario in a controlled laboratory environment. The objective is to analyze how modern containerized and vulnerable web applications can be attacked, detected, investigated, and hardened using cybersecurity techniques aligned with industry frameworks such as MITRE ATT&CK and the Cyber Kill Chain.

The project simulates:

* Reconnaissance
* Web exploitation
* SQL Injection
* Cross-Site Scripting (XSS)
* Detection and monitoring
* Incident response
* Security hardening

---

# Technologies Used

| Technology         | Purpose                    |
| ------------------ | -------------------------- |
| Ubuntu Linux       | Victim environment         |
| Kali Linux         | Attacker machine           |
| XVWA / DVWA        | Vulnerable web application |
| Python HTTP Server | Lightweight web hosting    |
| Docker (attempted) | Containerized deployment   |
| Nmap               | Reconnaissance scanning    |
| Wazuh SIEM         | Monitoring and detection   |
| MITRE ATT&CK       | Attack mapping             |

---

# Architecture

```text
[Kali Linux]
      ↓
Reconnaissance & Attacks
      ↓
[Vulnerable Web Application]
(XVWA / DVWA)
      ↓
[Monitoring & Detection]
(Wazuh SIEM)
```

---

# Objectives

* Simulate realistic enterprise cyber attacks
* Analyze attacker behavior
* Detect malicious activities
* Perform forensic investigation
* Apply incident response procedures
* Harden infrastructure against future attacks

---

# Attack Simulation

## 1. Reconnaissance (Nmap Scan)

The attacker performs network scanning to identify exposed services.

### Command

```bash
nmap TARGET-IP
```

### MITRE ATT&CK

| Technique                 | ID    |
| ------------------------- | ----- |
| Network Service Discovery | T1046 |

---

## 2. SQL Injection

A SQL Injection attack is attempted against the vulnerable web application login/input fields.

### Payload

```sql
' OR 1=1 --
```

### MITRE ATT&CK

| Technique                         | ID    |
| --------------------------------- | ----- |
| Exploit Public-Facing Application | T1190 |

---

## 3. Cross-Site Scripting (XSS)

Reflected XSS attack performed through vulnerable input fields.

### Payload

```html
<script>alert('XSS')</script>
```

### MITRE ATT&CK

| Technique                         | ID    |
| --------------------------------- | ----- |
| Command and Scripting Interpreter | T1059 |

---

# Detection & Monitoring

The simulated enterprise environment integrates monitoring and logging mechanisms to detect suspicious activities such as:

* Port scanning
* SQL Injection attempts
* Unauthorized requests
* Web exploitation activities

---

# Incident Response

The following response actions were analyzed:

* Identification of malicious activity
* Containment of compromised services
* Blocking suspicious IP addresses
* Monitoring attacker behavior
* Security analysis and reporting

---

# Security Hardening Recommendations

## Docker & Container Security

* Avoid privileged containers
* Use least privilege principle
* Enable container logging
* Restrict exposed ports

## Network Security

* Implement firewall rules
* Apply network segmentation
* Enable Zero Trust principles

## Monitoring

* Continuous SIEM monitoring
* Centralized logging
* Alert correlation

## Web Security

* Input validation
* Prepared SQL statements
* Secure authentication
* Web Application Firewall (WAF)

---

# Screenshots Included

* Environment setup
* Vulnerable web application
* Nmap scan
* SQL Injection
* XSS attack
* Logs and detection
* Architecture diagram

---

# Challenges Faced

During deployment, Docker containerization encountered storage limitations within the Ubuntu live laboratory environment. Alternative lightweight vulnerable web applications and simulation methodologies were utilized to continue the enterprise breach simulation and analysis workflow.

---

# Learning Outcomes

This project helped in understanding:

* Enterprise attack lifecycle
* Web application exploitation
* MITRE ATT&CK framework
* Incident response procedures
* Security hardening techniques
* SOC and SIEM operations

---

# Conclusion

This project successfully demonstrated the design and analysis of a realistic enterprise breach simulation environment. Multiple attack vectors were explored, mapped to MITRE ATT&CK techniques, and analyzed from detection, forensic, and defensive perspectives. The project highlights the importance of proactive monitoring, secure architecture, and incident response in modern enterprise infrastructures.

---

# Author

**Minakshi Sinha**

Cybersecurity Project – Enterprise Breach Simulation, Detection & Security Hardening
