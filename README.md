# 🛡️ Phishing Email Analysis – Cybersecurity Internship Task 2

This repository contains a thorough analysis of a **realistic phishing email**, completed as part of a cybersecurity internship module focused on threat detection, email spoofing, and header analysis.

---

## 🎯 Objective

To identify and document the traits of a phishing email using both **email content analysis** and **technical header inspection**. This task enhances awareness of common phishing techniques, spoofed domains, and authentication failures (SPF, DKIM, DMARC).

---

## 🗂️ Repository Contents

| File Name           | Description                                      |
|---------------------|--------------------------------------------------|
| `email_raw.txt`     | Raw phishing email content for analysis.         |
| `email_header.txt`  | Simulated email header used for technical review.|
| `report.md`         | Complete breakdown of phishing indicators found. |
| `header analyzer.png` | Screenshot of email header analysis result from Google's Message Header Analyzer. |

---

## 🧪 Key Security Concepts Covered

- **Phishing Awareness** – Recognizing deceptive tactics in fake emails.
- **Social Engineering Detection** – Identifying language used to induce fear or urgency.
- **Email Spoofing** – Analyzing forged sender information.
- **Header Analysis** – Reviewing SPF, DKIM, DMARC results using industry-standard tools.

---

## 🔧 Tools & Resources Used

| Tool | Purpose |
|------|---------|
| [Google Header Analyzer](https://toolbox.googleapps.com/apps/messageheader) | Decodes and validates technical email headers. |
| Gmail / Email Client | Used to extract email headers and raw message format. |
| Markdown & GitHub | For structured documentation and project presentation. |

---

## 📊 Summary of Findings (Based on Header Analysis Screenshot)

| Attribute | Result | Reason |
|----------|--------|--------|
| **SPF**   | ❌ Fail | IP address used to send email not authorized by domain `icici-alerts.com`. |
| **DKIM**  | ❌ Fail | Email failed digital signature verification (domain: unknown). |
| **DMARC** | ❌ Fail | Policy enforcement failed due to spoofed domain. |
| **Delivery Delay** | ⏱ 4 hours | Indicates email may have been throttled or rerouted through suspicious hosts. |
| **Sender IP** | Unknown | No valid domain authority — likely an anonymous host or spam server. |

---

## 🔍 Outcome

Through this task, I demonstrated:

- The ability to **recognize phishing red flags** in both language and technical metadata.
- Practical usage of **email header analysis tools** to detect forged sender info and authentication failures.
- The creation of a **professional security report** summarizing technical and social cues of phishing attempts.



