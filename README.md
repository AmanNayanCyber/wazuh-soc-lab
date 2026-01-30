# Wazuh SOC Detection Lab

## Overview

This project demonstrates a hands-on Security Operations Center (SOC) lab built using Wazuh. The goal was to simulate real-world attacker techniques and validate that security monitoring and detection mechanisms successfully identify malicious or suspicious activity.

The lab focuses on endpoint detection, log analysis and SIEM operations, with detections mapped to the MITRE ATT&CK framework.

---

## Lab Architecture

**Wazuh Server**
- Ubuntu Linux (SIEM + Dashboard)

**Monitored Endpoint**
- Kali Linux (Wazuh Agent installed)

The server collects logs, analyzes events and generates alerts based on security rules and file integrity monitoring.

---

## ⚔️ Attack Simulations Performed

The following attacker behaviors were simulated in a controlled lab environment:

| Technique | Description | Detection Source |
|----------|-------------|------------------|
| SSH Brute Force | Multiple failed login attempts | Auth logs |
| Privilege Escalation | User switching to root via sudo | System logs |
| New User Creation | Creation of a new privileged user | Account monitoring |
| SSH Key Persistence | Unauthorized key added to authorized_keys | File Integrity Monitoring |
| Cron Job Persistence | Malicious scheduled task created | File Integrity Monitoring |
| Defense Evasion | Wazuh agent service stopped | Agent monitoring |

---

## 🚨 Detection Techniques Used

- Log source onboarding (SSH, auth logs)
- File Integrity Monitoring (FIM)
- Rule validation and alert analysis
- Security event investigation via dashboard

---

## 🗺 MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|-------|-----------|----|
| Credential Access | Brute Force | T1110 |
| Privilege Escalation | Abuse of sudo | T1548 |
| Persistence | Scheduled Task | T1053 |
| Persistence | Account Manipulation (SSH Key) | T1098 |
| Defense Evasion | Impair Defenses | T1562 |

---

## 🧠 Skills Demonstrated

SIEM deployment and configuration  
Endpoint log collection and analysis  
Security detection validation  
Threat behavior mapping  
SOC investigation workflow  

---

## ⚠️ Disclaimer

This lab was conducted in a private, isolated environment for educational purposes only. No unauthorized systems were targeted.
