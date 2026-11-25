
<div align="center">

# 🏥 Mediroza General Hospital — Penetration Testing

**Black-box security assessment, exposed data investigation, PDF security analysis, and vulnerability reporting**

</div>

<p align="center">
<img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
<img src="https://img.shields.io/badge/Platform-Kali%20Linux-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
<img src="https://img.shields.io/badge/Assessment-Black--Box-0070C0?style=flat-square&labelColor=000000" />
<img src="https://img.shields.io/badge/Focus-Web%20Security-404040?style=flat-square&labelColor=C00000" />
<img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=000000" />
<img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
</p>

---

## 📌 Project Overview

This project documents the Week 4 practical penetration-testing assessment completed as part of the **NetworkWalks Cybersecurity Internship**.

The exercise involved a black-box security assessment of the assigned hospital website, covering web request analysis, retrieval and password auditing of three PDF reports, investigation of exposed resources, and documentation of security findings.

The assessment identified several security weaknesses, including a publicly accessible database backup. Analysis confirmed the presence of employee salary information and shareholder details within the exposed backup.

The full assessment, evidence screenshots, findings, risk assessment, and remediation recommendations are documented in the PDF report included in this repository.

---

## 🎯 Objectives

- Perform reconnaissance against the assigned web application.
- Inspect and modify HTTP requests using Burp Suite Repeater.
- Retrieve the three PDF reports required by the exercise.
- Analyze and crack the password protection of the retrieved PDFs.
- Investigate publicly exposed directories and backup files.
- Identify the exposure of employee salary and shareholder information.
- Document findings, evidence, impact, and remediation recommendations.

---

## 🛠️ Lab Specifications & Tools

| Component / Tool | Purpose |
| :--- | :--- |
| **Kali Linux** | Primary security testing environment |
| **Burp Suite** | HTTP request inspection and Repeater testing |
| **Web Browser** | Website navigation and public resource inspection |
| **curl** | HTTP requests and response-header inspection |
| **PDF utilities** | PDF metadata and document analysis |
| **Hashcat / password-auditing utilities** | Offline password-recovery testing |
| **Linux command-line tools** | Evidence review and integrity verification |

---

## 🔍 Assessment Workflow

### **M1 — Initial Access**

- Inspected the assigned website and its authentication workflow.
- Captured and examined HTTP requests using Burp Suite.
- Used Repeater to inspect request behavior while testing the username parameter.
- Retrieved the three PDF reports required by the exercise.

### **M2 — PDF Encryption Analysis**

- Examined the retrieved PDF documents and their encryption properties.
- Extracted the information required for offline password auditing.
- Successfully recovered the passwords for all three PDFs.
- Opened the documents to verify successful password recovery.

### **M3 — Further Data Exposure**

- Reviewed the public `robots.txt` file and identified the `/old/` path.
- Investigated the directory and observed that directory listing was enabled.
- Identified the exposed `mediroza_db_backup_2019.sql` database backup.
- Confirmed that the backup URL was accessible without authentication.
- Analyzed the backup and identified employee salary and shareholder information.

### **M4 — Reporting**

- Consolidated the assessment results.
- Documented security findings and their impact.
- Assigned severity ratings.
- Prepared remediation recommendations and the final report.

---

## 🐞 Key Security Findings

| Finding | Severity |
| :--- | :--- |
| Publicly accessible database backup | **High** |
| Weak PDF password protection | **High** |
| Public directory listing | **High (contextual)** |
| SQL error information disclosure | **Medium** |
| Server technology disclosure | **Low** |

---

## 📄 Final Penetration Testing Report

The report includes the assessment methodology, milestone results, evidence screenshots, security findings, risk assessment, and remediation recommendations.

**[📥 MEDIROZA Penetration Testing Report (PDF)](./MEDIROZA_Penetration_Testing_Report)**

---

## 💡 What I Learned

1. **Web request analysis:** Inspecting and modifying HTTP requests using Burp Suite Repeater.
2. **PDF security:** Understanding how weak document passwords can be recovered through offline password auditing.
3. **Information disclosure:** Recognizing how exposed directories and backup files can disclose sensitive information.
4. **Evidence documentation:** Preserving and presenting evidence responsibly.
5. **Security reporting:** Communicating findings, risks, and remediation measures in a structured report.

---

## ⚠️ Responsible Disclosure & Scope

This was an authorized educational exercise. Testing was limited to the assigned target and the scope defined by the training instructions.

This repository contains the final report only. Sensitive patient information, raw database backups, credentials, and unredacted employee or shareholder information are not included.

---

## 👤 Author

**Malek Aroua**  
*Computer Networks Graduate | Cybersecurity Specialist*

---
