# GoldBench UAE

A live precious-metals dashboard for the UAE: gold, silver and platinum rates in AED, plus jewellery pricing calculators and a historical gold price calculator.

🔗 **Live site:** https://goldbenchuae.vercel.app

> **For educational and research purposes only.** See the [Disclaimer](#disclaimer).

## Features
- **Live rates**: gold, silver and platinum spot prices (USD/oz) converted to AED per gram, by karat
- **Rate Calculator**: gold value, making charges and VAT for any weight and karat
- **Weight Converter**: grams, ounces, tola and more
- **History Calc**: price lookup for any past date with a multi-row quote table (gold value, making charges, VAT, grand total)
  - Today: live spot price
  - Past dates: daily close, falling back to monthly averages back to 1833
- Dark and light themes, mobile-friendly layout

## Data sources
- Live spot: Swissquote (primary), gold-api.com (fallback)
- Historical: Alpha Vantage `GOLD_SILVER_HISTORY` plus embedded monthly and daily data
- Charts: TradingView; economic calendar: Tradays (MQL5)
- AED peg: 1 USD = 3.6725 AED

## Calculation
```
price per gram = USD/oz × 3.6725 ÷ 31.1035 × (karat ÷ 24)
total          = (gold value + making charges) + 5% VAT
```

## Tech
A single static `index.html` with no build step, hosted on Vercel. Pushes to `main` deploy automatically.

## Updating
1. Edit or replace `index.html` in this repository.
2. Commit to `main`. Vercel redeploys within about a minute.
3. Hard refresh the site (Ctrl+Shift+R) to see the change.

## Security
See [SECURITY.md](SECURITY.md) for how to report a vulnerability.

## Disclaimer
GoldBench UAE is built **purely for educational and research purposes**. Rates and calculations are indicative only and are not financial, investment or trading advice. Do not use them as the basis for buying, selling or pricing real transactions. Always confirm against an official trading, refinery or exchange rate. The author accepts no liability for decisions made using this tool.

## Credits
Idea and coded by **Subash M**. © 2025–2026 Subash M. All rights reserved.
