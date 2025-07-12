# 🥗 Project 6: Automated Diet Planner via Telegram

## 📌 Project Description

The **Gym Diet Automation Workflow** is a fully automated AI-powered system built using **n8n**, **OpenAI GPT-4o**, **Google Sheets**, and **Telegram Bot Integration**. It streamlines the process of generating personalized diet plans based on user input, and delivers a downloadable **PDF chart** directly to the user — without manual effort.

Designed for **fitness trainers, online coaches, nutritionists**, and **gym clients**, the system transforms raw user data into professional, goal-specific diet charts tailored for fat loss, muscle gain, or maintenance — with support for both **veg** and **non-veg** preferences.

---

## ⚙️ Working Mechanism

### 1. 🧾 User Data Collection via Form
- Users fill out an **n8n-powered form** capturing:
  - Name
  - Gender
  - Height & Weight
  - Fitness Goal (e.g., Fat Loss, Muscle Gain, Maintenance)
  - Diet Preference (Vegetarian/Non-Vegetarian)
- Data is logged to **Google Sheets** for record-keeping.

### 2. ✅ Filtering & Entry Validation
- n8n filters incoming form entries to:
  - Ensure completeness
  - Remove invalid records
- A **loop node** processes each valid user one-by-one.

### 3. 🧠 AI-Based Diet Plan Generation
- **Agent 1**: Generates diet structure (meal types: breakfast, lunch, snacks, dinner).
- **Agent 2**: Adds specific meals, quantities, and timings based on user metrics.
- **Agent 3**: Refines and formats the full diet plan into a well-organized chart.

### 4. 📄 PDF Generation
- A **custom PDF generation sub-workflow** takes the AI output and creates a user-friendly document including:
  - User’s Name
  - Meal-by-meal breakdown
  - Macronutrient info (optional)
  - Diet customization based on the user’s goal
- PDF is hosted or stored publicly with a sharable link.

### 5. 📬 Delivery to User
- Final PDF is automatically delivered via:
  - 📩 **Email** (Gmail API / SMTP)
  - 💬 **Telegram message** (Bot API)
- Users receive their personalized diet instantly.

---

## 🧠 Scope & Utility

| Aspect         | Description                                                             |
|----------------|-------------------------------------------------------------------------|
| Automation     | End-to-end automation of data intake, plan generation, and delivery.    |
| Personalization| AI-driven plans tailored to individual health goals and preferences.    |
| Scalability    | Handles multiple users simultaneously; adaptable to fitness platforms.  |
| Use Cases      | Gym member onboarding, fitness coaching, challenge tracking, app add-on.|

---

## 🛠️ Tools & Technologies Used

- **n8n** – Core workflow engine (form handling, filtering, logic, file delivery)
- **Google Sheets API** – Submission logging and data tracking
- **OpenAI GPT-4o** – Multi-agent system for generating and formatting meal plans
- **Custom PDF Generator** – Converts structured output into a downloadable file
- **Telegram Bot / Gmail API** – Final delivery channel to users

---

## 📁 Sample Output

- 📎 **PDF Diet Plan**:
  - Includes user's name, goals, and a complete daily diet chart
  - Optionally includes macronutrient breakdown
  - Professionally formatted for readability
- 🔗 **Delivery Channel**:
  - Public PDF link via Telegram or Email

---
