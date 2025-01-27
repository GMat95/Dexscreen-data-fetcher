# Dexscreen-data-fetcher
# Meme Coin Alert Bot (Week 1)

A Python bot that fetches token data from DexScreener, filters tokens based on customizable criteria, and sends alerts to Telegram. Designed for tracking new and trending meme coins on Solana.

---

## Features
- **Real-Time Data Fetching**: Pulls token data from DexScreener API every 5 minutes.
- **Custom Filters**: Filters tokens by liquidity, volume, and age.
- **Telegram Alerts**: Sends formatted alerts with key metrics (price, liquidity, volume) and DexScreener links.
- **Duplicate Prevention**: Logs processed tokens to avoid duplicate alerts.

---

## How It Works
1. **Data Fetching**:  
   - The bot fetches token data from DexScreener’s public API.  
   - Filters are applied to narrow down tokens (e.g., liquidity > $10k, volume > $50k).  

2. **Token Filtering**:  
   - Tokens are checked against criteria (e.g., age < 24 hours).  
   - Duplicates are skipped using a local SQLite database.  

3. **Telegram Alerts**:  
   - Sends formatted messages to Telegram with token details.  
   - Includes links to DexScreener for quick analysis.  

4. **Logging**:  
   - Logs all processed tokens to avoid duplicate alerts.  

---

## Setup Instructions

### 1. Install Dependencies
bash
pip install requests python-dotenv pyyaml

Simplified Workflow:

- Fetch Data: Query DexScreener API with filters (e.g., liquidity, volume).

- Filter Tokens: Remove duplicates and apply criteria.

- Send Alerts: Post formatted messages to Telegram.

- Log Results: Store results in SQLite to avoid duplicate alerts.

Component Breakdown
Data Fetcher	Fetches token data from DexScreener API.
Token Filter	Applies criteria (e.g., liquidity, volume) to filter tokens.
Alert System	Sends alerts to Telegram with token details.
Database	Logs processed tokens to avoid duplicate alerts.
Main Script	Coordinates all components and runs the bot periodically.

📂 Project Structure
Copy

meme-alert-bot/  
├── core/  
│   ├── fetcher.py         # DexScreener API calls  
│   ├── filters.py         # Apply criteria to tokens  
│   ├── alerts.py          # Telegram alert logic  
│   └── database.py        # SQLite logging  
├── config/  
│   ├── filters.yml        # Criteria (e.g., min liquidity)  
│   ├── keys.yml           # Telegram API token  
│   └── settings.yml       # Refresh interval, etc.  
├── scripts/  
│   └── run_bot.py         # Main script  
└── README.md  
