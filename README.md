# 💼 Internship Automation Projects – AI, RPA, and Web Automation

This repository showcases a series of automation-focused projects developed during my internship, utilizing technologies like **n8n**, **OpenAI GPT-4o**, **Selenium**, **Python**, **Google APIs**, and **Telegram Bots**. Each solution is built with a goal of reducing manual effort, improving data workflows, and providing real-world business value.

---

## 🔹 PROJECT 1: College Event Manager Agent

### 📌 Description
An AI-powered event management system built using **n8n** and **OpenAI**, designed to automate college event planning. It generates event schedules, reminders, participant credentials, and handles real-time Q&A via a chatbot.

### ⚙️ Features
- Form-based event creation.
- GPT-4o-generated schedule & reminders.
- Automated emails with personalized participant cards.
- Live Q&A chatbot using OpenAI.
- Admin and Participant panels.

### 🔧 Tools Used
- n8n
- OpenAI GPT-4o
- Google Calendar API
- Email & Credential Generator

---

## 🔹 PROJECT 2: E-Commerce Assistant for WhatsApp/Telegram

### 📌 Description
A conversational chatbot for WhatsApp/Telegram that helps users browse items, check prices, and place orders. It uses **Google Sheets** as a dynamic product database and provides real-time responses based on queries.

### ⚙️ Features
- Natural-language product inquiries.
- Price matching with fuzzy logic.
- Order form generation and logging.
- Works on WhatsApp or Telegram.

### 🔧 Tools Used
- n8n
- Google Sheets API
- Dialogflow (optional)
- Telegram API / WhatsApp Cloud API

---

## 🔹 PROJECT 3: ReWear – Image-Based Product Classifier

### 📌 Description
An AI-powered feature for a clothing resale platform that uses **image classification** to categorize clothing uploads automatically, saving seller time and improving catalog quality.

### ⚙️ Features
- Accepts user-uploaded product images.
- AI model predicts item category, type, gender (e.g., "Men’s Formal Shirt").
- Tags stored with product metadata.

### 🔧 Tools Used
- Python
- TensorFlow / PyTorch
- Flask API / FastAPI
- Frontend integration with web platform

---

## 🔹 PROJECT 4: IREPS Railway Tender Automation

### 📌 Description
A **Python Selenium + BeautifulSoup** scraper that extracts structured tender data from the Indian Railways eProcurement site (IREPS), including attached documents and metadata.

### ⚙️ Workflow Highlights
- Connects to pre-logged-in Chrome via remote debugging.
- Parses tender rows and details.
- Extracts downloadable PDFs and flags failures.
- Stores output in JSON for easy integration.

### 🔧 Tools Used
- Python
- Selenium
- BeautifulSoup
- Regex
- JSON
- Chrome (remote debugging)

---

## 🔹 PROJECT 5: Lead Generation via Email Automation

### 📌 Description
A **fully automated email outreach system** built with **n8n**, **OpenAI**, and **Gmail API**. It generates personalized emails using AI and logs results to Google Sheets.

### ⚙️ Workflow
1. Upload Google Sheet with leads (company, email, etc.).
2. Validate entries via filters.
3. GPT-4o agents generate, refine, and finalize email content.
4. Gmail API sends personalized emails.
5. All activity is logged (status, timestamp, etc.).

### 🔧 Tools Used
- n8n
- OpenAI GPT-4o
- Google Sheets API
- Gmail API
- OAuth2

---

## 🔹 PROJECT 6: Automated Diet Planner via Telegram

### 📌 Description
An intelligent gym and diet automation system that collects fitness data via form, generates a **custom diet plan using OpenAI**, and delivers a **PDF chart** via Telegram or email.

### ⚙️ Workflow
1. User fills fitness form (goal, gender, height, etc.).
2. n8n logs and validates data.
3. OpenAI generates structured diet plan.
4. Plan is formatted into a downloadable PDF.
5. Delivered via Telegram Bot or Email.

### 🔧 Tools Used
- n8n
- Google Sheets API
- OpenAI GPT-4o
- PDF Generator Node
- Telegram Bot / Gmail API

---

## 📊 Summary

| Project | Area | Key Tech | Output |
|--------|------|----------|--------|
| 1 | Event Automation | n8n, GPT-4o | Event Pages, Schedules |
| 2 | Chatbot + E-Com | Telegram, Sheets | Orders via Chat |
| 3 | AI Tagging | ML, Python | Product Category |
| 4 | Web Scraping | Selenium, BS4 | JSON Tender Data |
| 5 | Lead Gen | GPT-4o, Gmail | Personalized Emails |
| 6 | Health & Fitness | AI + PDF | Telegram Diet Charts |

---

## 🛠️ Tech Stack Overview

- **Automation**: n8n, Wait Nodes, Subflows
- **AI Intelligence**: OpenAI GPT-4o
- **Web Scraping**: Selenium, BeautifulSoup
- **Data Storage**: Google Sheets API, JSON
- **Delivery**: Gmail API, Telegram Bot, PDF Generator

---
