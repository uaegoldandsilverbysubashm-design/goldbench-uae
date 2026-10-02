# GoldBench UAE

A live precious-metals terminal for UAE jewellers: gold, silver and platinum rates in AED, plus calculators for pricing jewellery quickly and accurately.

🔗 **Live site:** https://goldbenchuae.vercel.app

## Features
- **Live rates** – gold, silver and platinum spot prices in USD/oz converted to AED per gram, by karat
- **Rate Calculator** – gold value, making charges and VAT for any weight and karat
- **Weight Converter** – grams, ounces, tola and more
- **History Calc** – price lookup for any past date, with a multi-row quote table (gold value, making charges, VAT, grand total)
  - Today: live spot price
  - Past dates: daily close, falling back to monthly averages back to 1833
- Dark and light themes, mobile-friendly layout

## Data sources
- Live spot: Swissquote (primary), gold-api.com (fallback)
- Historical: Alpha Vantage `GOLD_SILVER_HISTORY` plus embedded monthly and daily data
- AED peg: 1 USD = 3.6725 AED

## Calculation
`price per gram = USD/oz × 3.6725 ÷ 31.1035 × (karat ÷ 24)`
`total = (gold value + making charges) + 5% VAT`

## Tech
A single static `index.html` file with no build step, hosted on Vercel. Pushes to `main` deploy automatically.

## Disclaimer
Rates are indicative and for reference only. Always confirm against your trading or refinery rate before dealing.
