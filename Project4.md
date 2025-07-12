# 🚄 Project 4: IREPS Railway Tender Automation

## 📌 Project Description

This project automates the extraction of tender data from the **Indian Railways E-Procurement System (IREPS)** using **Python**, **Selenium**, and **BeautifulSoup**. The script dynamically interacts with the portal to extract structured tender information, attached documents, and corrigenda. Output is stored in **JSON format**, making it easy to integrate with analytics tools or dashboards.

⚠️ **CAPTCHA and login are bypassed** by connecting to a pre-authenticated Chrome browser via **remote debugging**, eliminating the need to solve them programmatically.

---

## ⚙️ Working Mechanism

### 1. 🔐 Remote Browser Connection
- Chrome is manually launched with `--remote-debugging-port=9222`.
- Script connects using `Options().debugger_address`.
- This avoids handling login/CAPTCHA each time.

### 2. 📋 Tender Row Parsing
- Navigates to the tender listing page.
- Parses all `<tr>` rows with height `"20"` using **BeautifulSoup**.
- Extracted fields:
  - Tender ID
  - Department Name
  - Description
  - Status
  - Published Date
  - Due Date

### 3. 🔗 Navigation to Tender Detail Pages
- Parses `onclick` JavaScript from rows (e.g., `postRequestNewWindow()`).
- Constructs real detail URLs.
- Uses **Selenium** with **explicit waits** to ensure content loads fully.

### 4. 🧾 Detailed Metadata Extraction
- Extracts data from the `advSearch` table:
  - Tender No.
  - Department/Railway
  - Closing Date/Time
  - Tender Title
  - Tender Type
  - Tender Status
- Uses helper functions for resilience to missing/dynamic elements.

### 5. 📎 Attached Document Extraction
- Locates table with `id="attach_docs"`.
- Extracts:
  - Document Name
  - Description
  - Dynamic PDF URLs
- Appends data to the `Documents Attached` field in the JSON.

### 6. 📥 Main Tender PDF Extraction
- Scans `<script>` tags for `downloadtenderDoc` functions.
- Uses **regex** to extract the actual PDF download URLs.

### 7. 🚨 Error Handling & Logging
- If required fields are missing, the tender is flagged.
- Flagged tender IDs are stored in `failed_tenders.json`.

### 8. ✅ Output & Completion
- Successfully parsed tenders saved in `tenders_ireps_full_pages.json`.
- Summary message shows counts for:
  - Total Processed
  - Successfully Saved
  - Failed Tenders

---

## 🧠 Scope & Utility

| Aspect       | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| Automation   | Fully automates multi-page scraping and detail parsing from a secured portal. |
| Robustness   | Handles layout changes and missing fields gracefully.                        |
| Integration  | JSON format is easily ingestible by analytics pipelines or alert systems.    |
| Use Cases    | Vendor tracking, procurement monitoring, railway market research.            |

---

## 🛠️ Tools & Technologies Used

- **Python** – Main scripting language
- **Selenium** – Browser automation & dynamic navigation
- **BeautifulSoup** – HTML parsing and data extraction
- **Chrome (Remote Debugging)** – To bypass CAPTCHA and manual login
- **Regex** – To parse embedded JavaScript URLs
- **JSON** – Output format for structured tender metadata

---

## 📁 Output Samples

- `tenders_ireps_full_pages.json`: Successfully scraped tenders
- `failed_tenders.json`: Tenders missing critical data

---
