# 🧾 Smart Quotation Generator with n8n

An AI-powered Telegram bot that automates the generation of dynamic product quotations in real-time using **n8n**, **OpenAI**, and **Google Sheets**. The system handles both text and voice messages, and delivers personalized PDF quotations without manual effort.

---

## 📌 Project Overview

This project eliminates manual steps in generating quotations by enabling users to interact with a Telegram bot using natural language (text or voice). The system understands the request, fetches real-time pricing data from Google Sheets, generates a customized PDF, and sends it back to the user instantly via Telegram.

---

## ⚙️ Working Mechanism

### 🔁 Workflow 1: Telegram Interaction & Quotation Trigger

1. **Telegram Trigger**
   - Listens for user messages (text or voice).
   - Starts the quotation workflow.

2. **Branching Logic**
   - If **text**: Directly routes to AI agent for processing.
   - If **voice**: Follows the voice transcription path.

---

### 🎤 Voice Message Handling

1. **Telegram File Fetch**
   - Downloads the user’s voice message.

2. **OpenAI Whisper / Audio Transcription**
   - Converts voice message to text.

3. **Send to AI Agent**
   - Transcribed text sent for further processing.

---

### 💬 Text Message Handling

1. **Edit Fields**
   - Cleans/prepares the text input.

2. **Send to AI Agent**
   - Text forwarded for analysis and response generation.

---

### 🧠 AI Agent Functionality

- Uses **OpenAI GPT-4o** to:
  - Understand user intent.
  - Generate dynamic responses.
  - Trigger external workflows.

- Integrates with:
  - **Google Sheets API** – For real-time product and pricing data.
  - **Simple Memory** – Maintains session context.
  - **Call Workflow Node** – Triggers PDF generation (Workflow 2).

- Final response (or PDF download link) is sent to the user via Telegram.

---

## 📄 Workflow 2: PDF Generation

- Generates a professional, formatted PDF quotation.
- Uses dynamic data (products, quantities, prices) from the request.
- Uploads and shares the link directly with the user.

---

## 🧠 Scope & Utility

| Feature        | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| **Automation** | No manual quotation preparation required.                                   |
| **Scalability**| Can be extended to WhatsApp, web chat, or email.                            |
| **Customization** | Product lists, templates, and pricing are fully dynamic via Google Sheets. |
| **Use Cases**  | Quotation generation, pricing requests, and sales team automation.          |

---

## 🛠️ Tools & Technologies Used

- **n8n** – Open-source workflow automation platform.
- **Telegram Bot API** – For real-time messaging with users.
- **OpenAI GPT-4o** – For natural language understanding and tool orchestration.
- **OpenAI Whisper** – For voice-to-text transcription.
- **Google Sheets API** – To manage and retrieve dynamic product/pricing data.
- **Custom PDF Generator (Workflow 2)** – For creating downloadable quotation files.

