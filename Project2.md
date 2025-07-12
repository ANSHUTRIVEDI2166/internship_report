# 🏗️ Batch Tender Scraper with GUI Interface

A fully automated Python-based system designed to scrape real-time procurement data from multiple state eProcurement portals. With a simple GUI built using Tkinter and orchestration via Windows batch files, this tool allows users to enter a keyword and instantly gather tender data — including downloadable ZIP files — from multiple states simultaneously.

---

## 📌 Project Overview

This project automates the tedious task of monitoring tenders across different state procurement portals. With built-in support for Rajasthan, Maharashtra, Tamil Nadu, West Bengal, and Andaman, the scraper handles everything from keyword input to ZIP file downloads and saves data in both JSON and Excel formats.

---

## ⚙️ Working Mechanism

### 🪟 1. Batch File: Launch Ports
- Opens five separate instances of Google Chrome.
- Each instance is assigned to a specific state portal.

### 🖥️ 2. Batch File: Run GUI
- A Tkinter-based GUI is launched.
- User enters a **search keyword** (e.g., *road*, *building*, *IT*).
- Submitting the keyword triggers the scraping process.

### 🕷️ 3. Batch File: Trigger Scraper
- Executes the main Python script to:
  - Enter the keyword in each portal’s search bar.
  - Navigate and scrape all matching tenders.
  - Extract tender ID, title, department, due date, etc.
  - Click and download ZIP files.
  - Return to listings to continue the loop.

### 💾 4. Data Storage
- All tender data is saved in:
  - **JSON** for programmatic/API use.
  - **Excel (.xlsx)** for human-readable reports.

### 📁 5. Output Handling
- Each state’s results are stored separately.
- Filenames are dynamically generated based on keyword and timestamp.

---

## 📈 Scope & Utility

| Feature      | Description                                                             |
|--------------|-------------------------------------------------------------------------|
| **Automation** | Full end-to-end flow, no manual data collection required.               |
| **Scalability**| Can be extended to central or national portals.                        |
| **Reliability**| Batch-based separation improves debugging and modular execution.       |
| **Use Cases** | Procurement monitoring, vendor scouting, regional trend analysis.       |

---

## 🛠️ Tools & Technologies Used

- **Python** – Web scraping logic, ZIP handling, and file I/O.
- **Tkinter** – GUI for user input and interaction.
- **Batch Files (.bat)** – Controls task execution flow and multi-instance browser handling.
- **Google Chrome** – Launched in parallel sessions for simultaneous scraping.
- **JSON & Excel Libraries** – For structured and human-readable data storage.

---
