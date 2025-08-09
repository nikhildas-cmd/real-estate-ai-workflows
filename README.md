# 🏠 Daily Real Estate Lead Scraper & Dispatcher (n8n Workflow)

## 📌 Overview
This **n8n automation** scrapes property listing data daily, filters for **only new leads**, and sends them to real estate agents or admins via **Telegram** and **Gmail**.

It is designed for the Indian real estate market but can be adapted for any region or property source.

---

## ⚙️ Workflow Steps
1. **Daily Trigger**  
   - Runs at a scheduled time (default: every day at 9:00 AM IST).

2. **Scrape Leads (HTTP Request)**  
   - Fetches property data from an API endpoint (`https://dummyjson.com/products` used as an example — replace with your actual data source).

3. **Filter New Leads**  
   - Compares the listing date with the last 24 hours to include only **fresh leads**.

4. **Send to Telegram**  
   - Sends a property alert message to your configured Telegram chat.

5. **Send to Gmail**  
   - Emails lead details to a chosen recipient.

---

## 🛠️ Setup Instructions
1. **Import the Workflow in n8n**
   - Download `daily_lead_scraper_dispatcher.json`.
   - In n8n, click **Import** and select the JSON file.

2. **Replace Placeholders**
   - `REPLACE_WITH_YOUR_TELEGRAM_CHAT_ID` → Your Telegram chat ID.
   - `REPLACE_WITH_TELEGRAM_CREDENTIAL_ID` → Your Telegram credentials in n8n.
   - `REPLACE_WITH_EMAIL` → Email address where leads should be sent.
   - `REPLACE_WITH_GMAIL_CREDENTIAL_ID` → Your Gmail OAuth2 credential in n8n.

3. **Update the Data Source**
   - Change the HTTP Request node’s URL from the dummy API to your real property source (API or web scraper).

4. **Activate the Workflow**
   - Turn on the workflow in n8n to start receiving daily lead notifications.

---

## 🔒 Security Notes
- Do **not** commit your actual credential IDs or personal email addresses to GitHub.
- This repo contains a **sanitized** version safe for public sharing.

---

## 📈 Example Use Cases
- Real estate agencies receiving fresh daily listings.
- Broker networks distributing leads instantly.
- Internal property monitoring for investor opportunities.

---

## 📬 Contact
For customization or integration with RERA compliance checks, AI price predictions, and buyer-property matching, reach out via LinkedIn or email.
