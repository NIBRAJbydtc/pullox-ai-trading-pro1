PULLOX AI TRADING PRO — Android source + GitHub Cloud Build workflow
This ZIP is NOT a compiled APK. It includes a GitHub Actions workflow to build the APK in the cloud from a browser/phone.

PHONE-ONLY BUILD STEPS:
1. Download and extract this ZIP using your Android Files app.
2. Open https://github.com in Chrome and sign in/create a GitHub account.
3. Create a NEW PUBLIC repository, e.g. pullox-ai-trading-pro. Do not add README/license/gitignore during creation.
4. In the repository choose Add file > Upload files.
5. Upload ALL extracted project contents preserving folders, including the hidden .github/workflows/build-apk.yml file. Important: Android file pickers sometimes hide .github; if you cannot select hidden folders, create the workflow on GitHub manually:
   - Add file > Create new file
   - filename: .github/workflows/build-apk.yml
   - paste the workflow content from this ZIP's .github/workflows/build-apk.yml
   - Commit changes.
6. Commit uploaded files to main.
7. Open the repository's Actions tab. Select "Build PULLOX Android APK", tap Run workflow if shown, then open the latest run.
8. Wait until green success. Open Artifacts and download PULLOX-AI-TRADING-PRO-debug-apk.zip.
9. Extract it on the phone. Install app-debug.apk. Android may ask permission to install unknown apps.

If build fails, open the failed workflow run and copy the red error lines; do not upload account passwords or keys.

Security:
- Public repository source code is visible to everyone. This project contains no broker passwords/API keys. Never add Exness login details, API secrets, or private credentials.
- The workflow runs only the code you upload; inspect code before using. APK is a debug build, suitable for personal testing, not Play Store release.

FEATURES / LIMITS:
- BTCUSDT public Binance candles; proxy, not Exness BTCUSDc quote.
- Gold XAUUSD=X Yahoo public chart endpoint; indicative only and may be blocked/unavailable.
- 1m, 2m (aggregated), 5m, 15m, 1h, 4h timeframe choices.
- Candlestick chart, EMA 9/21, RSI 14, MACD, ATR, volume.
- Approximate support/resistance, engulfing/pin bar, BOS, liquidity sweep, FVG proxy.
- Rule-based BUY/SELL/WAIT confluence; not AI prediction, no profit guarantee.
- No Exness login, API connection, auto-execution, or order placement. User manually checks and places trades in Exness.
- No live economic news/calendar feed.
- 20% risk on $10 means $2 risk in one trade. Five consecutive full losses reduce $10 to about $3.28 before fees/slippage. Prefer 1–2% and demo testing.
