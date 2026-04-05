# Sector Sentiment Analyser

A single HTML file. Open in browser. Done.

---

## What it does

- Fetches live VIX from Yahoo Finance
- Pulls headlines from Yahoo Finance, MarketWatch, and WSJ RSS feeds
- Scores 8 market sectors (-5 to +5) using Llama 3.3 70B via Groq
- Shows trend, score bar, and one-line driver per sector

---

## Setup

**Step 1 — Get a free Groq API key**

Go to https://console.groq.com
Sign up → API Keys → Create key
Copy the key (starts with gsk_)

**Step 2 — Open the file**

Just open sector-sentiment.html in any browser.
No server. No install. No dependencies.

**Step 3 — Run**

Paste your Groq key into the input field
Press Enter or click Run analysis
Wait 10–15 seconds for results

---

## How scores work

| Score | Meaning |
|-------|---------|
| +3 to +5 | strongly bullish |
| +1 to +3 | mildly bullish |
| -1 to +1 | neutral |
| -3 to -1 | mildly bearish |
| -5 to -3 | strongly bearish |

VIX calibrates the scores:
- Below 15 → calm market
- 15 to 20 → low volatility
- 20 to 30 → elevated fear
- Above 30 → high fear / panic

---

## Sectors covered

Technology · Energy · Financials · Healthcare
Consumer · Industrials · Materials · Defence

---

## Data sources

| Data | Source | Cost |
|------|--------|------|
| VIX | Yahoo Finance | Free, no key |
| Headlines | Yahoo / MarketWatch / WSJ RSS | Free, no key |
| AI scoring | Groq (Llama 3.3 70B) | Free tier |

---

## Groq free tier limits

14,400 requests per day on llama-3.3-70b-versatile
More than enough for personal use

---

## Notes

- Your API key never leaves your browser tab
- Not financial advice
- RSS feeds may occasionally be slow or unavailable
- If scoring fails, check your Groq key is valid and has quota
