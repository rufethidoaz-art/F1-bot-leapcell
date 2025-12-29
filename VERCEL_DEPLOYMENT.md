# Vercel Deployment Guide

This guide explains how to deploy the F1 Telegram Bot to Vercel.

## Prerequisites

- GitHub account
- Telegram bot token from [@BotFather](https://t.me/BotFather)
- Vercel account

## Environment Variables

Set these environment variables in your Vercel project:

| Variable | Value | Description |
|----------|-------|-------------|
| `TELEGRAM_BOT_TOKEN` | `your_bot_token_here` | Your Telegram bot token |
| `PYTHON_VERSION` | `3.11.0` | Python version |
| `PLAYWRIGHT_BROWSERS_PATH` | `0` | Playwright browsers path |

## Build Configuration

- **Framework Preset**: None
- **Build Command**: `pip install -r requirements.txt && playwright install chromium`
- **Output Directory**: Leave empty
- **Install Command**: `pip install -r requirements.txt`

## Runtime Configuration

The bot runs as a Flask application on Vercel. The main entry point is `app.py`.

## Monitoring

- Check Vercel dashboard for deployment logs
- Monitor bot performance through Telegram
- Use Vercel's built-in monitoring tools

## Troubleshooting

### Build Failures
- Ensure all dependencies are in `requirements.txt`
- Check Python version compatibility
- Verify Playwright installation

### Runtime Issues
- Check environment variables are set correctly
- Verify bot token is valid
- Check Vercel logs for error details

### Live Timing Issues
- Live timing only works during active F1 sessions
- Playwright dependencies must be installed
- Check session status with `/live` command