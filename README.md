# Dexscreen-data-fetcher

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
