# 🛡️ IT Compliance Audit Lab Repository

This repository contains a virtual lab setup and tools used for auditing IT compliance based on industry-standard frameworks like HIPAA, NIST 800-53, ISO 27001, and SOX.

## 📁 Repository Structure

```
compliance-audit-lab/
├── audit_files/
│   └── custom_compliance_sample.audit
├── documentation/
│   ├── HIPAA-Checklist.md
│   ├── NIST800-53-Controls.md
│   ├── SOX-Simulation-Guide.md
│   └── Compliance-Audit-Report-Template.md
├── wazuh/
│   └── setup-guide.md
├── nessus/
│   └── custom-scan-guide.md
├── screenshots/
│   └── sample-findings.png
└── README.md
```

---

## ✅ Getting Started

### Tools You’ll Need:
- VirtualBox or VMware
- Nessus Essentials (Free)
- Wazuh All-in-One OVA
- Kali Linux ISO / Windows 10 ISO / Ubuntu ISO

---

## 🔍 Features
- 🧪 Custom compliance scan using Nessus audit files
- 📊 SIEM monitoring using Wazuh
- 📋 Documentation templates for real-world compliance reporting
- 🧾 SOX Section 404 controls simulation

---

## 📄 Sample Audit File
Found under `/audit_files/custom_compliance_sample.audit`, this file checks for:
- Windows Firewall enabled
- Password minimum length
- Audit log retention settings

---

## 🔐 Compliance Standards Covered
- HIPAA Technical Safeguards
- NIST 800-53 (Security and Privacy Controls)
- CIS Benchmarks (customizable)
- SOX (Sarbanes-Oxley Section 404)

---

## 📘 SOX Section 404 Simulation (Guide: `documentation/SOX-Simulation-Guide.md`)

### 🎯 Objectives:
Simulate IT General Controls (ITGC) for:
- Access control
- Change management
- Audit logging
- Data integrity

### 🧪 Implementation Summary:
1. **Access Control**
   - Create multiple user accounts (admin, finance_user, temp_user)
   - Enforce password complexity, RBAC, and monitor logins using Wazuh
2. **Change Management**
   - Simulate file/config changes, detect via Wazuh File Integrity Monitoring
3. **Audit Logging**
   - Enable system audit logs, ship logs with Wazuh agents, ensure retention
4. **Vulnerability Scanning**
   - Run Nessus scans, simulate remediation steps and SOX-aligned reporting
5. **Documentation**
   - Write policies, audit logs, remediation plans, and maintain evidence

### 📄 Files to Include:
- `SOX_Access_Control_Policy.md`
- `Change_Management_Log.md`
- `System_Audit_Log_Summary.md`
- `SOX_Risk_Matrix.xlsx`
- `SOX_Findings_Report.md`

---

## 📚 License
MIT License

---

## 🙋‍♂️ Contributing
Pull requests are welcome. Please submit ideas for new audit files, tools, or lab enhancements.

---

## 🔗 References
- [Wazuh Documentation](https://documentation.wazuh.com/)
- [Tenable Nessus](https://www.tenable.com/products/nessus)
- [HIPAA Security Rule](https://www.hhs.gov/hipaa/for-professionals/security/index.html)
- [NIST 800-53 Controls](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
- [SOX Overview](https://www.sec.gov/spotlight/sarbanes-oxley.htm)

---

> This repo serves as a practical compliance auditing portfolio project for aspiring GRC and cybersecurity professionals.