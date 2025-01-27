# Dexscreen-data-fetcher

Simplified Workflow:

    Fetch Data: Query DexScreener API with filters (e.g., liquidity, volume).

    Filter Tokens: Remove duplicates and apply criteria.

    Send Alerts: Post formatted messages to Telegram.

    Log Results: Store results in SQLite to avoid duplicate alerts.
    

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
