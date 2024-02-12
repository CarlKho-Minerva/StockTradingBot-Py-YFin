# StockTradingBot-Py-YFin

This trading bot uses a dual moving average crossover strategy to trade a list of assets. It fetches minute-level historical data for each asset, calculates fast and slow simple moving averages (SMA) of the closing prices, and makes trading decisions based on the relationship between the two SMAs.

## Features

- Trades exactly once per minute when a new bar opens
- Can trade multiple assets at once (both stocks and cryptocurrencies)
- Fetches live and up-to-date data from Yahoo Finance
- Keeps track of each asset’s holdings
- Keeps a trading log with the time, asset, quantity, and price of each trade
- It is generic enough to be used with any broker
- Uses the opening price of the next period as the fill price for its trades to avoid lookahead bias and make the backtesting process more realistic.

## Strategy

The bot uses a dual moving average crossover strategy. It calculates a fast SMA and a slow SMA for each asset. When the fast SMA crosses above the slow SMA, the bot buys the asset. When the fast SMA crosses below the slow SMA, the bot sells the asset.

## Trading Assets

The bot trades the following assets:

- Amazon (AMZN)
- Google (GOOG)
- Netflix (NFLX)
- Microsoft (MSFT)
- Tesla (TSLA)
- Bitcoin (BTC-USD)
- Ethereum (ETH-USD)

## Dependencies

The bot uses the following Python libraries:

- yfinance for fetching historical data
- pandas for data manipulation
- ta for technical analysis

## Disclaimer

This bot is for educational purposes only. It should not be used for real trading without further testing and refinement. The performance of the bot in backtesting does not guarantee its performance in live trading. Always use proper risk management when trading.
