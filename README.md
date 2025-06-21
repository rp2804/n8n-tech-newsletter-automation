# 📰 n8n Tech Newsletter Automation

An automated daily newsletter workflow built using [n8n](https://n8n.io), [NewsAPI](https://newsapi.org), and Gmail SMTP.  
This project fetches the top 50 tech headlines, picks 10 at random, formats them into a clean HTML newsletter, and sends personalized emails to a list of recipients — automatically.

---

## 🚀 Features

- 📡 Pulls live tech news using NewsAPI (Top 50 headlines)
- 🧠 Randomly selects 10 articles on every run
- 💌 Sends formatted HTML email using Gmail SMTP
- 📅 Runs daily using Schedule Trigger
- 📋 Reads recipient list from Excel file (can be replaced with Google Sheets)
- ✨ Built in n8n — no code required!

---

## 🧩 Workflow Overview
```plaintext

[Schedule Trigger]
        ↓
[HTTP Request → NewsAPI]
        ↓
[Code Node → Format HTML + Randomize]
        ↓
[Send Email → Personalized HTML Email]
        ↺
