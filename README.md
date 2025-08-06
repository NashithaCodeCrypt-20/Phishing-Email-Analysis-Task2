# 🎯 Phishing Email Analysis – Cyber Security Internship Task 2

## ✅ Objective

To identify and document phishing indicators in a suspicious email sample using manual analysis and online tools. The aim is to improve awareness of email-based threats and phishing detection techniques.

---

## 📧 Sample Phishing Email

```
From: Amazon Support <support@amz-check.com>
Subject: Important: Your Account Has Been Suspended

Hello,

We have noticed unusual activity in your Amazon account. For your protection, we have temporarily suspended your account.

Please verify your identity by clicking the link below:

https://amazon-login-secure-check.com

Failure to respond within 24 hours will result in permanent account suspension.

Regards,  
Amazon Security Team
```

---

## 🚨 Identified Phishing Indicators

| Indicator | Observation | Status |
|----------|-------------|--------|
| **Fake Sender Address** | support@amz-check.com instead of official @amazon.com | ❌ |
| **Urgent Language** | "Your account has been suspended", "24 hours" | ⚠️ |
| **Suspicious Link** | Hover link points to a non-Amazon domain | ❌ |
| **Generic Greeting** | No use of recipient's real name | ⚠️ |
| **Spoofed Domain** | Looks similar to "amazon.com" but isn't | ❌ |
| **Poor Authentication** | SPF, DKIM, DMARC all failed | ❌ |

---

## 🛠 Tools Used

- ✅ [Google Admin Toolbox – Message Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/)
- ✅ [VirusTotal](https://www.virustotal.com) (for checking links)
- ✅ Manual inspection (hover technique, language analysis)

---

## 🔎 Email Header Analysis (via Google Admin Toolbox)

| Field | Result |
|-------|--------|
| **SPF** | ❌ `fail with IP Unknown` |
| **DKIM** | ❌ `none` |
| **DMARC** | ❌ `fail` |
| **From IP** | Unknown/private IP: `192.168.1.22` |
| **Delay** | 1 sec |
| **Authentication** | All failed — high risk |

📸 **Screenshot Evidence:**
- See `Messageheader.png`
- See `Message header analysis.png`

---

## 📝 Conclusion

This email is a **confirmed phishing attempt**. It uses:
- **Email spoofing** (fake sender domain)
- **Social engineering** (fear/urgency)
- **Invalid authentication headers**
- **Suspicious links** that could lead to credential theft

⚠️ It should **not** be trusted or interacted with. Always verify sender domains and email headers for authenticity.

---

## 📂 Repo Structure

```
Phishing-Email-Analysis-Task2/
├── README.md
├── phishing_sample.txt
├── email_header_sample.txt
├── Messageheader.png
├── Message header analysis.png
└── Phishing_Email_Header_Analysis_Report.pdf
```

---

## 👨‍💻 Author

- **Intern:** Your Name  
- **Date:** August 2025  
- **Task Link:** [Submission Form](https://forms.gle/8Gm83s53KbyXs3Ne9)
