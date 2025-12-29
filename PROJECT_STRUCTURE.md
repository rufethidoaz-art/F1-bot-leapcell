# Project Structure

## Clean Vercel Version

This is the optimized structure for Vercel deployment, removing all unnecessary files and hosting-specific configurations.

### Root Directory

```
F1-bot-vercel/
├── README.md                 # Main documentation
├── VERCEL_DEPLOYMENT.md      # Vercel-specific deployment guide
├── PROJECT_STRUCTURE.md      # This file
├── .gitignore               # Git ignore rules
├── app.py                   # Main Flask application
├── f1_bot.py                # Core bot logic
├── optimized_scraper.py     # Live timing scraper
├── requirements.txt         # Python dependencies
├── streams.txt             # Default stream links
├── user_streams.json       # User stream data
└── static/                 # Static assets (if needed)
```

### Removed Files

The following files have been removed from the original repository to create a clean Vercel version:

#### Test Files
- `test_bot.py`
- `test_httpx_bs4.py`
- `test_mechanicalsoup.py`
- `test_playwright.py`
- `test_pyppeteer.py`
- `test_selenium.py`

#### Hosting-Specific Files
- `render.yaml` - Render.com configuration
- `Procfile` - Heroku configuration
- `Dockerfile` - Docker configuration
- `replit.nix` - Replit configuration
- `.replit` - Replit configuration
- `leapcell.yaml` - Leapcell configuration

#### Test Directories
- `f1_bot_flyio_test/` - Fly.io test configuration
- `f1_bot_koyeb_test/` - Koyeb test configuration
- `f1_bot_leapcell_test/` - Leapcell test configuration
- `f1_bot_railway_test/` - Railway test configuration

#### Documentation Files
- `DEPLOYMENT_GUIDE.md` - General deployment guide (replaced with Vercel-specific)
- `RUN_INSTRUCTIONS.md` - Run instructions (not needed for Vercel)
- `SETUP_COMPLETE.md` - Setup completion (not needed for Vercel)

#### Alternative Bot Files
- `f1_bot_simple.py` - Alternative simple version
- `main.py` - Alternative main file
- `final_working_scraper.py` - Alternative scraper

### Key Files

#### `app.py`
Main Flask application that serves as the entry point for Vercel deployment.

#### `f1_bot.py`
Core bot logic containing all Telegram bot functionality, API integrations, and command handlers.

#### `optimized_scraper.py`
Optimized web scraper for live timing data from Formula Timer.

#### `requirements.txt`
Minimal dependencies optimized for Vercel deployment.

### Benefits of Clean Structure

1. **Smaller Deployment Size**: Removed unnecessary files reduce deployment time
2. **Clear Purpose**: Focused on Vercel deployment only
3. **Easier Maintenance**: Less confusion about which files to modify
4. **Better Performance**: Fewer files to process during deployment
5. **Cleaner Git History**: Focused repository history

### Development Workflow

1. Make changes to core files (`f1_bot.py`, `optimized_scraper.py`)
2. Update `requirements.txt` if new dependencies are needed
3. Test locally with `python app.py`
4. Deploy to Vercel via GitHub integration
5. Monitor deployment and bot functionality