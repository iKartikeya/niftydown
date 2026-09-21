# NIFTY 50 Dip-Buy Backtester

A client-side GitHub Pages website for testing the NIFTY 50 dip-buying strategy.

## Strategy

- Investment per trigger: ₹30,000
- Daily fall trigger: 1%
- Cooldown: 7 trading days
- New-low override: 1% below the most recent purchase price
- Every purchase resets the cooldown and reference price
- Total corpus is a hard limit
- No partial final purchase
- XIRR is calculated from actual purchase dates and the portfolio value on the selected end date

## Data

Upload a CSV containing at least:

`Date, Close`

The website processes the file locally in the browser. It does not upload the CSV anywhere.

## GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html` and this `README.md`.
3. Go to **Settings → Pages**.
4. Select **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`.
6. Save. GitHub will provide the Pages URL.

## Important

This is an index-level backtest. It does not model ETF/fund tracking error, dividends, brokerage, taxes, slippage, or execution differences.
