# NIFTY 50 Dip-Buy Strategy

Interactive GitHub Pages web application for backtesting the NIFTY 50 dip-buying strategy.

## Strategy

- Investment per purchase: ₹30,000 by default
- Normal trigger: NIFTY 50 daily close falls at least 1% from the previous trading day's close
- Cooldown: 7 trading days after every purchase
- New-low override: during cooldown, buy if the current close is at least 1% below the most recent purchase price
- Every purchase resets the cooldown and reference price
- Maximum one purchase per trading day
- Total corpus is a hard limit
- No partial final purchase
- XIRR uses actual purchase dates and the index-linked value on the selected end date

## Data

The app automatically loads the configured historical NIFTY CSV from GitHub. You can also upload your own CSV with `Date` and `Close` columns.

## GitHub Pages

In the repository, open **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/(root)`, then save. The site will be available at the GitHub Pages URL shown by GitHub.

## Limitations

This is an index-level backtest. It does not model ETF/fund tracking error, dividends, brokerage, taxes, slippage, or execution-price differences.
