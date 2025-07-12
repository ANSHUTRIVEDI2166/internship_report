# 📧 Project 5: Lead Generation via Email Automation

## 📌 Project Description

This project implements a **fully automated, AI-powered email outreach system** using **n8n**, **OpenAI GPT-4o**, **Google Sheets**, and the **Gmail API**. The workflow streamlines lead generation by automatically fetching lead data, generating personalized emails, and sending them directly to prospects.

Designed for marketing and business development teams, the system reduces manual effort, ensures high-quality messaging, and scales outreach operations with professionalism and efficiency.

---

## ⚙️ Working Mechanism

### 1. 🧾 Lead Sheet Submission
- A user submits a **Google Sheets link** via an n8n web form.
- The sheet includes:
  - Company Name
  - Lead Email Address
  - (Optional) Contact Name, Role, Industry

### 2. ✅ Data Fetching & Validation
- n8n uses the **Google Sheets node** to retrieve all lead entries.
- A **filter node** ensures:
  - Proper formatting
  - Presence of all required fields
- If valid, the system loops through each lead.

### 3. 🧠 Personalized Email Generation with AI
- Within the loop, multiple **OpenAI Agent nodes** collaborate:
  - **Agent 1**: Creates raw email based on lead/company context
  - **Agent 2**: Refines tone, structure, and clarity
  - **Agent 3**: Finalizes formatting for professional delivery
- (Optional) Intermediate logging in Google Sheets for QA or reviews.

### 4. 📬 Email Sending & Logging
- Emails are sent via the **Gmail API** using **OAuth2** authentication.
- Each email is **uniquely tailored** per lead.
- A **log sheet** records:
  - Lead Email
  - Company
  - Send Status (Success/Failure)
  - Timestamp

### 5. 🕒 Flow Control & API Rate Management
- A **Wait/Delay node** is used after each email to:
  - Prevent hitting Gmail API rate limits
  - Ensure consistent delivery
  - Avoid blacklisting for mass outreach

---

## 🧠 Scope & Utility

| Aspect         | Description                                                             |
|----------------|-------------------------------------------------------------------------|
| Automation     | Eliminates manual email drafting and sending.                          |
| Personalization| GPT-4o generates messages tailored to each company or individual.       |
| Scalability    | Supports high-volume outreach with built-in rate control.               |
| Use Cases      | Marketing, sales, networking, event invitations, partnership outreach. |

---

## 🛠️ Tools & Technologies Used

- **n8n** – Workflow automation engine handling logic and flow control
- **Google Sheets API** – Imports lead data and logs email outcomes
- **OpenAI GPT-4o** – AI agents to generate, refine, and finalize email content
- **Gmail API (OAuth2)** – Sends personalized emails securely
- **Throttle/Wait Nodes** – Controls timing to maintain API health

---

## 📁 Output Samples

- **Sent Email Log (Google Sheet)**:
  - `Lead Email`, `Company`, `Send Status`, `Timestamp`
- **(Optional)** Draft Review Sheet:
  - Intermediate AI-generated email content for QA

---
