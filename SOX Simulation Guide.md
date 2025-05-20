# 🧾 SOX Section 404 Compliance Simulation Guide

This guide outlines how to simulate key SOX (Sarbanes-Oxley Act) Section 404 IT General Controls (ITGC) in a virtual lab using open-source and free tools.

## 🎯 Objective
To implement and monitor simulated controls that support internal controls over financial reporting (ICFR), including:
- Access Control
- Change Management
- Audit Logging
- Data Integrity

---

## 🧱 Lab Architecture

| VM Name           | Purpose                                 |
|------------------|------------------------------------------|
| Wazuh Manager     | Centralized log monitoring & SIEM       |
| Ubuntu Server     | Simulated finance system (web/server)   |
| Windows 10 VM     | Workstation with users and logs         |
| Nessus Essentials | Vulnerability & misconfiguration scanner|

---

## 🔐 1. Access Control Simulation

- Create 3 users: `admin`, `finance_user`, `temp_user`
- Set password policies (e.g., min 12 characters, expiration)
- Use Wazuh to:
  - Detect login attempts (Event ID 4624, 4625)
  - Alert on privilege escalation or failed logins

## 🔁 2. Change Management Control

- Simulate changes to critical files:
  - Ubuntu: `/etc/passwd`, `/etc/ssh/sshd_config`
  - Windows: Registry changes
- Use Wazuh File Integrity Monitoring (FIM) to detect unauthorized changes
- Log and document the change in `Change_Management_Log.md`

## 🧾 3. Audit Logging & Retention

- Enable system and security logs on:
  - Windows Event Viewer (Security, System)
  - Ubuntu (`syslog`, `auth.log`, `auditd`)
- Configure Wazuh agents to forward logs to manager
- Verify:
  - Logs are complete and timestamped
  - Retention policy is enforced (e.g., 90 days minimum)

## 🛡️ 4. Vulnerability & Misconfiguration Scanning

- Run scans using Nessus Essentials
  - Look for weak passwords, missing patches, exposed shares
- Export scan report and interpret compliance impact
- Document findings in `SOX_Findings_Report.md`

## 📝 5. Documentation for SOX Auditing

Maintain the following:
- `SOX_Access_Control_Policy.md`
- `Change_Management_Log.md`
- `System_Audit_Log_Summary.md`
- `SOX_Risk_Matrix.xlsx`
- `SOX_Findings_Report.md`

---

## ✅ Outcome
This simulation replicates SOX Section 404 compliance processes in a virtual lab and helps demonstrate your understanding of:
- Technical enforcement of IT controls
- Monitoring and logging for auditability
- Documentation practices for regulatory readiness

---


