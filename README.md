# 🤖 StudentSpot Automation — Multi-Bot News Delivery System

---

## 📌 What is this project?

This project is a fully automated news delivery system built using **n8n** — a no-code automation platform.

It automatically:
- Fetches fresh news from 80+ websites
- Summarizes them using AI (Groq API - LLaMA 3.3 70B)
- Delivers them to Telegram bots
- Runs fully automatically (no manual work)

---

## 🎯 Why was this built?

Students struggle to track updates across multiple domains like:
Tech, AI, Finance, Sports, Crypto, Startups, etc.

This system solves that by delivering:
- 📌 Daily summarized news
- 📌 Simple English explanations
- 📌 Domain-specific updates
- 📌 Directly to Telegram

---

## 🤖 The 10 Bots

| Bot | Domain | Schedule Timing |
|-----|--------|--------|
| 🇮🇳 IndiaNewsDaily | India News | 8AM & 6PM |
| 🌍 GlobalNewsDaily | Global News | 9AM & 7PM |
| 🌐 TechWorldDaily | Tech & Startups | 10AM & 8PM |
| 📈 StockFinanceNews | Stock Market & Finance | 8:30AM & 3:30PM |
| 🤖 AI Daily Updates | Artificial Intelligence | 11AM & 9:30PM |
| 🚀 StartupPulse | Startups & VC | 12PM & 8:30PM |
| 🪙 CryptoWorldDaily | Cryptocurrency | 1PM & 10PM |
| ⚡ ElectroTechDaily | Electronics & Gadgets | 2PM & 10:30PM |
| 🏆 DailySportsUpdate | Sports | 5PM & 9PM |
| 💰 MoneyMentor | Personal Finance | 4PM |

---

## ⚙️ How does the workflow work?

### 1️⃣ Schedule Trigger
Each bot runs at a fixed time using n8n schedule triggers.



### 2️⃣ RSS Read Nodes
Each bot fetches articles from 80+ news websites using RSS feeds.



### 3️⃣ Filter Node
Filters only **recent articles** (removes old/outdated news).



### 4️⃣ Merge Node
Combines multiple RSS feeds into a single stream per domain.



### 5️⃣ Loop Over Items
Processes each article one by one for better handling.



### 6️⃣ Wait Node
Adds delay between messages to avoid API rate limits.



### 7️⃣ HTTP Request Node (Groq AI)
Each article is processed using:
**Groq API — LLaMA 3.3 70B**

AI performs:
- Removes irrelevant content
- Classifies category
- Creates structured summary
- Generates Telegram-ready format



### 8️⃣ Telegram Node
Final output is sent to:
- Telegram bots
- Groups or personal chats

---

## 📡 Key Features

- ✅ Fully Automated (24/7 running)
- 🤖 AI-powered summarization
- 📰 Domain-specific bots
- 🚫 No duplicate news
- ⏱️ Smart scheduled delivery
- 📊 Fresh news only
- 🔁 Highly scalable system

---

## 💡 Tech Stack

| Technology | Purpose |
|------------|--------|
| n8n | Workflow automation |
| Groq API (LLaMA 3.3 70B) | AI summarization |
| Telegram Bot API | Message delivery |
| @BotFather | Bot creation |
| RSS Feeds | News data source |
| Oracle Cloud (planned) | Free hosting (24/7) |

---

## 🗂️ Workflow Files

| File | Bot |
|------|-----|
| india-news.json | 🇮🇳 India News |
| global-news.json | 🌍 Global News |
| techworld.json | 🌐 TechWorld Daily |
| stock-finance.json | 📈 Stock Finance |
| ai-updates.json | 🤖 AI Updates |
| startup-pulse.json | 🚀 Startup Pulse |
| crypto.json | 🪙 Crypto News |
| electronics.json | ⚡ Electronics |
| sports.json | 🏆 Sports |
| money-mentor.json | 💰 Money Mentor |

---

## 🚀 How to use these workflows?

1. Download the JSON workflow file
2. Open your n8n instance
3. Click **"+" → Import Workflow**
4. Upload JSON file
5. Configure the following:

   - Telegram Bot Token (from @BotFather)
   - Chat ID (your group or personal chat)
   - Groq API Key

6. Save and activate workflow

---

## ⚠️ Setup Requirements

Each user must create their own:

- Telegram Bot
- Chat ID
- Groq API Key

---

## ☁️ Upcoming — Oracle Cloud Hosting

Planning migration to Oracle Cloud Free Tier:

- ✅ Free forever VM
- ✅ 24/7 uptime
- ✅ No laptop dependency
- ✅ Scalable automation system

---

## 🙏 Credits

Built by **Munnuri Vaishnavi**  
Part of the **StudentSpot Automation Team**

Under guidance of **Rajkamal Panthagani**  
Founder of *The StudentSpot 🎓*

---

> Stay curious. Keep building. 🚀
