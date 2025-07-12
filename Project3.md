# 🩺 Gynecological Health Data Tracker

A lightweight AI-powered health assistant for gynecologists and patients, designed to run entirely through Telegram using **n8n**, **Google Sheets**, and **GPT-4o-mini**. Patients can send messages or upload medical PDFs, which are intelligently processed, stored, and referenced in future interactions to support continuous, context-aware care.

---

## 📌 Project Overview

This system enables real-time health tracking, PDF analysis, and medical history retention via conversational interaction. All interactions are stored and linked to each patient’s Telegram Chat ID, ensuring seamless follow-up and improved doctor-patient engagement — without any paper-based recordkeeping.

---

## ⚙️ Working Mechanism

### 🔁 Telegram Message or File Upload
- **Trigger:** Listens for new messages or PDF files.
- **Switch Logic:** Distinguishes between text and PDF uploads.

### 📄 PDF File Processing
- **PDF-to-Text Conversion:** Extracts readable data from uploaded medical reports.
- **AI Extraction (GPT-4o-mini):** Identifies and extracts key data (e.g., symptoms, conditions, dates).

### 📝 Text Input Processing
- Directly cleaned and structured via the AI pipeline.

### 🧠 AI Agent with Medical Memory
- Combines new inputs with historical data.
- Provides context-rich, empathetic responses using stored user memory.

### 📊 Google Sheets as Database
- Checks if user already exists.
- Aggregates all historical inputs tied to that Chat ID.
- Updates or appends new medical entries.

### 🧩 Memory Layer
- Uses Simple Memory and Aggregation to maintain ongoing context.
- Enables accurate and personalized follow-up conversations.

### 📤 Telegram Response
- Sends a smart, health-aware reply back to the user via Telegram Bot API.

---

## 📈 Scope & Utility

| Feature       | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| **Automation**| Eliminates paper-based records and manual data entry for doctors and patients. |
| **Scalability**| Easily extendable to other medical specialties (e.g., dermatology, psychology). |
| **Accessibility**| Works directly over Telegram — no app downloads or logins required.           |
| **Use Cases** | Long-term symptom tracking, patient onboarding, PDF-based report analysis.    |

---

## 🛠️ Tools & Technologies Used

- **n8n** – Orchestrates the logic, data flow, and automation.
- **Telegram Bot API** – Manages communication and file upload.
- **OpenAI GPT-4o-mini** – Extracts medical intelligence and generates smart replies.
- **Google Sheets API** – Acts as the structured backend for patient records.
- **PDF-to-Text Converter** – Processes medical PDFs for AI analysis.
- **Simple Memory & Aggregator** – Maintains historical data for each user session.

---

