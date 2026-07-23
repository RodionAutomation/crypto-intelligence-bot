# 🤖 Crypto Intelligence Bot

A production-ready cryptocurrency Telegram bot built entirely in **n8n**.

This project demonstrates how to build a scalable Telegram bot using low-code automation while following production-oriented workflow design, centralized error handling, retry strategies, and modular architecture.

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
- Latest BTC / ETH / SOL overview
- Daily market summary

### 👤 User Management
- Automatic user registration
- Automatic cleanup of blocked Telegram users
- User existence validation

### ⚙ Reliability
- Retry strategy for external services
- Centralized Error Trigger workflow
- Graceful error handling
- Automatic recovery where possible

---

# 🏗 Workflow Architecture

The project is split into multiple workflows for easier maintenance.

| Workflow | Purpose |
|-----------|---------|
| Main Workflow | Handles all Telegram commands and user interaction |
| Alert Checker | Monitors active alerts and triggers notifications |
| Morning Digest | Sends scheduled morning market digest |
| Evening Digest | Sends scheduled evening market digest |
| Error Handler | Centralized workflow error processing |

---

# 🛠 Technologies

### Core Platform
- n8n
- JavaScript

### APIs
- Telegram Bot API
- CoinGecko API

### Storage
- Google Sheets

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
- Conditional branching

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
├── assets/
│   └── bot-logo.png
│
├── README.md
├── LICENSE
└── .gitignore
```

---

# 📸 Workflow Architecture

![Workflow Architecture](docs/architecture.png)

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

---

# 🔒 Security

Before publishing, all sensitive information has been removed and replaced with placeholders, including:

- API Keys
- Telegram Tokens
- Spreadsheet IDs
- Webhook IDs
- OAuth Credentials
- User-specific identifiers

---

# 🚀 Future Improvements

- Portfolio tracking
- Watchlist
- Fear & Greed Index
- Economic Calendar
- AI Market Analysis
- AI News Digest
- Multi-language support

---

# 📄 License

MIT License
