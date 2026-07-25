# 🤖 Crypto Intelligence Bot

A cryptocurrency Telegram bot built with n8n automation workflows.

This project demonstrates how to build a modular Telegram bot using n8n, JavaScript and external APIs while following clean workflow architecture, retry strategies and centralized error handling.

The bot allows users to monitor cryptocurrency prices, create personalized alerts, receive scheduled market digests, and manage their alerts directly inside Telegram.

---

# ✨ Features

### 📈 Real-time Cryptocurrency Prices
- Check live prices for BTC, ETH and SOL
- 24-hour price change
- Clean formatted Telegram responses

### 🔔 Price Alert System
- Create custom price alerts
- Multiple comparison operators (`>`, `<`, `>=`, `<=`)
- Duplicate alert protection
- Maximum alert limit per user
- Automatic alert deletion after triggering

### 📋 Alert Management
- View active alerts
- Delete alerts using inline Telegram buttons
- Callback Query handling

### 🌅 Market Digest
- Morning market digest
- Evening market digest
- Latest BTC, ETH and SOL market overview
- Daily market summary

### 👤 User Management
- Automatic user registration
- Automatic removal of users who blocked the bot
- User existence validation

### ⚙ Reliability
- Retry strategy for external services
- Centralized Error Trigger workflow
- Graceful error handling
- Automatic recovery where possible

---

# 🏗 Workflow Architecture

The project is split into multiple workflows for easier maintenance.

| Workflow | Responsibility |
|-----------|---------|
| Main Workflow | Handles all Telegram commands and user interaction |
| Alert Checker | Monitors active alerts and triggers notifications |
| Morning Digest | Sends scheduled morning market digest |
| Evening Digest | Sends scheduled evening market digest |
| Error Handler | Centralized workflow error processing |

---

# 🛠 Technologies

- n8n
- JavaScript
- Telegram Bot API
- CoinGecko API
- Google Sheets(used as a lightweight database for this demo project)

### n8n Nodes
- HTTP Request
- Google Sheets
- Telegram
- Code (JavaScript)
- Switch
- IF
- Merge
- Schedule Trigger
- Telegram Trigger
- Error Trigger

### Concepts Used
- Modular workflow architecture
- Callback Queries
- Inline Keyboards
- Retry on Fail
- Error Output
- Data validation
- Duplicate detection
- Dynamic message generation
- Scheduled automation
- Workflow branching

---

# 📂 Project Structure

```
Crypto-Intelligence-Bot/
│
├── workflows/
│   ├── main-workflow.json
│   ├── alert-checker.json
│   ├── morning-digest.json
│   ├── evening-digest.json
│   └── error-handler.json
│
├── docs/
│   └── architecture.png
│
├── images/
│   └── bot-logo.png
│   └── workflow-overview.png
│
├── README.md
├── LICENSE
└── .gitignore
```

---

# 📸 Workflow Architecture

![Workflow Architecture](docs/main-workflow.png)

---

# 🛡 Error Handling

The project uses a dedicated Error Trigger workflow that:

- captures workflow failures
- sends administrator notifications
- handles blocked Telegram users
- removes inactive users from the database
- prevents workflow interruption where possible

---

# 🔄 Reliability Features

- Retry on external API requests
- Retry on Telegram operations
- Retry on Google Sheets operations
- Continue using Error Output where appropriate
- Validation before every critical operation
- User-friendly error messages
- Automatic cleanup of invalid Telegram users
---

# 🚀 Future Improvements

- AI News Digest
- Portfolio tracking
- Watchlist
- Fear & Greed Index
- Economic Calendar
- AI Market Analysis
- Multi-language support

---

# 📄 License

MIT License
