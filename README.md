# Dexscreen-data-fetcher
Dexscreen data fetcher
edits

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
