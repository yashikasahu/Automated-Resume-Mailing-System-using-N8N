# 📬 Automated Resume Mailing System using N8N

A smart automation workflow that sends **personalized job application emails** (with attachments) to multiple companies **daily** — fully powered by **n8n, Google Sheets, and Gmail API**.

---

## ✨ Features

* 📄 **Fetches contact data** from Google Sheets
* 🔍 **Checks if an email has already been sent** (avoiding duplicates)
* ✅ **Verifies email deliverability** using Hunter.io
* 📧 **Sends personalized emails** to valid addresses
* 📊 **Updates Google Sheets** with:

  * Sent date
  * Status ("Mailed")
* 📨 **Supports multiple email slots per company** (up to 4 in current workflow)
* ⚡ **Fully automatic** — no manual effort required

---

## 🛠 Tools & Services Used

* **n8n (Cloud)** – Workflow automation platform
* **Google Sheets** – Data storage and tracking
* **Gmail API** – Sending emails
* **Hunter.io** – Email deliverability check
* **Google Gemini API** – Extracts company names
* **Google Drive** – Attaches resume
* **Scheduler** – Automates daily runs

---

## 📸 Screenshots

### 🛠 Workflow in n8n

<img width="911" height="321" alt="Screenshot 2025-08-08 160226" src="https://github.com/user-attachments/assets/7b4382a2-35c3-4829-aaf4-75b278687f1d" />

### 📧 Sample Email Output

![Email Sample](https://github.com/user-attachments/assets/ee626f2d-be17-45c7-a018-75bb1ccb2926)

> **Note:** Emails are blurred for privacy reasons.

---

## 📂 Workflow Structure

1. **Schedule Trigger** – Runs automation on a set schedule
2. **Get Rows from Google Sheets** – Fetches contact list
3. **Check Mailed or Not** – Skips contacts already emailed
4. **Insert to Items & Update Row in Sheet** – Keeps sheet updated
5. **Attach Resume** – Fetches file from Google Drive
6. **Email Verification & Sending** – Multiple parallel branches for different email fields (Email 1 to Email 4)
7. **Status Update** – Marks as "Mailed" once sent

---

## 🚀 Setup Instructions

1. **Clone this repository**

   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   ```
2. **Import the n8n workflow**

   * Open n8n
   * Go to **Import Workflow**
   * Upload the provided `.json` file
     
3. **Configure environment variables**

   * Gmail API or SMTP credentials
   * Google Sheets API credentials
   * Hunter.io API key
     
4. **Deploy & Run**

---

## 📜 License

MIT – Feel free to use and modify!

---
