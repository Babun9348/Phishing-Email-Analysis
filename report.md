# 📧 Phishing Email Analysis Report

## 📝 Task Overview

This report is part of **Task 2** of the Cybersecurity Internship, focused on identifying and analyzing a phishing email. The analysis includes both **content-based inspection** and **technical header review** using online tools.

---

## 📨 Email Overview

- **From**: ICICI Bank <no-reply@icici-alerts.com>
- **To**: jyotiprakash.mishra@email.com
- **Subject**: [IMPORTANT] Your ICICI Bank Account is Temporarily Locked
- **Received At**: Mon, 24 Jun 2024, 10:14 PM (Delivered after 4 hours)

---

## ⚠️ Phishing Indicators (Content Analysis)

| Indicator | Description |
|----------|-------------|
| **Spoofed Sender** | Email came from `icici-alerts.com`, which is not the official ICICI domain (`icicibank.com`). |
| **Urgent Language** | Phrases like "Your account is temporarily locked" and "Failure to respond within 12 hours will result in permanent lockout" are used to induce panic. |
| **Suspicious Link** | `https://icici-verify.com/security/reauthenticate` is a fake ICICI portal intended for phishing credentials. |
| **Generic Greeting** | Although my name is used, no account details are provided — a common phishing tactic. |
| **No Reply Warning** | Ends with “Do not reply,” which avoids interaction and verification. |

---

## 🧪 Technical Header Analysis

Header details were analyzed using the [Google Message Header Analyzer](https://toolbox.googleapps.com/apps/messageheader).  
Key findings:

| Attribute | Status | Explanation |
|----------|--------|-------------|
| **SPF**   | ❌ Fail | Sending IP is not authorized by the domain `icici-alerts.com`. |
| **DKIM**  | ❌ Fail | Digital signature from the domain could not be validated. |
| **DMARC** | ❌ Fail | Domain policy explicitly rejects unauthorized sources. |
| **Sender Host** | unknown-host.com | No official mail server detected. |
| **Delivery Delay** | 4 Hours | May indicate manipulation or use of unauthorized relays. |

📸 **Screenshot of header analysis included:**  
![Header Analyzer Results](./header_analyzer.png)

---

## ✅ Conclusion

This email is confirmed to be a **phishing attempt** due to:
- Spoofed email domain
- Failed authentication (SPF, DKIM, DMARC)
- Use of urgent psychological tactics
- Malicious link targeting ICICI customers

---

## 🛡 Recommended Action

- **Do not click** any links.
- **Report the email** to ICICI’s official security team (phishing@icicibank.com).
- **Block the sender** in your email client.
- Mark it as **“Phishing” or “Spam”** for automatic filtering.

---

## 📁 Supporting Files

- `email_raw.txt` – Raw phishing email content
- `email_header.txt` – Full technical header of the email
- `header_analyzer.png` – Screenshot of header analyzer tool
