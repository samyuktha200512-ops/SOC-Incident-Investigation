# 🛡️ SOC Incident Investigation using Linux Logs and Splunk

## 📌 Project Overview

This project demonstrates a Security Operations Center (SOC) investigation by analyzing Linux authentication and system logs to identify suspicious activities, classify security incidents, develop detection logic, and recommend appropriate response actions.

The investigation was validated using Splunk Enterprise, where the provided logs were imported and analyzed using Search Processing Language (SPL) queries.

---

## 🎯 Objectives

- Analyze Linux authentication and system logs.
- Identify normal and suspicious activities.
- Create detection logic for security monitoring.
- Classify incidents based on severity.
- Recommend appropriate incident response actions.
- Validate findings using Splunk Enterprise.

---

## 🛠️ Skills Demonstrated

- Security Log Analysis
- Linux Log Investigation
- Incident Detection
- Incident Classification
- Detection Rule Development
- Splunk SIEM
- Security Documentation
- Incident Response

---

## ⚙️ Tools Used

- Splunk Enterprise
- Linux Authentication Logs (`auth.log`)
- Linux System Logs (`syslog.log`)
- GitHub
- Google Docs

---

## 🔍 Investigation Workflow

The investigation followed a standard Security Operations Center (SOC) incident response process:

```text
Linux Logs
     │
     ▼
Log Analysis
     │
     ▼
Threat Detection
     │
     ▼
Incident Classification
     │
     ▼
Response Recommendation
     │
     ▼
Splunk Validation
     │
     ▼
Final Incident Response Report
```

This workflow demonstrates how security analysts transform raw log events into actionable security findings and documented incident reports.

---

## 🚨 Key Findings

The investigation identified both normal system activities and events that required further security analysis.

| Finding | Status | Severity |
|---------|--------|----------|
| Multiple Failed Login Attempts | ⚠️ Detected | Medium |
| Invalid User Login Attempts | ⚠️ Detected | Medium |
| Successful Login After Failed Attempts | 🚨 Detected | High |
| New User Account Creation | 🚨 Detected | High |
| Password Changes | ⚠️ Detected | Medium |
| User Session Activities | ✅ Observed | Low |
| CRON Scheduled Tasks | ✅ Normal | Low |
| Certbot Certificate Renewal | ✅ Normal | Low |
| Logrotate Execution | ✅ Normal | Low |

### Summary

- Normal scheduled system maintenance activities (CRON, Logrotate, Certbot) were successfully identified.
- Authentication logs contained multiple failed login attempts and invalid user authentication attempts.
- Successful authentication following repeated failures requires verification by the security team.
- User account creation and password modification events should always be validated to ensure they were authorized.
- Session creation and closure events indicate normal user activity unless correlated with suspicious authentication behavior.

---

## 📂 Repository Structure

```text
SOC-Incident-Investigation/
│
├── README.md
├── Report/
│   └── SOC_Incident_Response_Report.pdf
│
├── Logs/
│   ├── auth.log
│   └── syslog.log
│
├── Splunk/
│   ├── SPL_Queries.md
│   └── Screenshots/
│
├── Detection Logic/
│   └── Detection_Logic.md
│
└── Incident Classification/
    └── Incident_Classification.md
```

---

## 📸 Splunk Validation

The provided Linux logs were imported into Splunk Enterprise and analyzed using Search Processing Language (SPL).

The following activities were successfully validated:

- Failed login attempts
- Invalid user authentication
- Successful password authentication
- Public key authentication
- CRON scheduled jobs
- Logrotate execution
- Certbot certificate renewal
- User session creation and termination

The SPL queries used during the investigation are documented in:

```text
Splunk/SPL_Queries.md
```

---

## 📖 Learning Outcomes

Through this project, I gained practical experience in:

- Investigating Linux authentication logs
- Distinguishing normal and suspicious system activities
- Writing detection logic for SOC monitoring
- Classifying security incidents by severity
- Developing response recommendations
- Using Splunk Enterprise to validate security findings
- Creating professional incident response documentation

---

## 🚀 Future Improvements

Future enhancements for this project include:

- Creating custom Splunk dashboards
- Developing automated Splunk alerts
- Writing Sigma detection rules
- Mapping findings to the MITRE ATT&CK Framework
- Correlating authentication logs with additional system logs

---

## 👩‍💻 Author

**Samyuktha Saravanan**

Aspiring SOC Analyst

Cybersecurity Student

---

> **Disclaimer**
>
> This project was completed for educational purposes using provided sample logs. No production systems or real organizational data were analyzed.