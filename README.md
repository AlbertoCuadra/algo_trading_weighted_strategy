# Acrypto - Weighted strategy 

I have been developing a fully customizable algo over the last year. The algorithm is based on a set of different strategies, each with its own weight (weighted strategy). Currently it has implemented a set of 5 strategies:

* MACD
* Stochastic RSI
* RSI
* Supertrend
* MA crossover

Moreover, the algo includes STOP losses criteria and a taking profit strategy. The algo must be optimized for the desired asset to achieves its full potential. The 1H and 4H dataframe give good results. The algo has been tested for several asset (same dataframe, different optimization values).



The algorithm is based on a combination of well-documented indicators. First, the algorithm calculated the weight_strategy, which represents a value from 0 to 5 of the number of strategies that are fulfilled (in case the weight of each strategy is the same). To open a position, the value of weight_strategy must be greater than the value of weight_signal, by default 2. Modify the indicator parameters for the desired asset and data frame. Set stop-loss and take profit criteria.

# Features:

* The algorithm allows to trade with long, short or both positions.
* Backtest the algorithm over a defined interval (data stamp), e.g., from 01/01/2021
* Set stoploss (SL) orders based on a percentage of the previous candle source, e.g., close or hl2 (high + low)/2. Only close the position after the candle is close!
* Stop position in case the algo detects a potential Top/Bottom.
  + It can close a specific percentage of the remaining open long position.
  + It can close a specific percentage of the remaining open short position.
* It can moves the stoploss every time the algo takes profit (TP)
* Take profit based on a percentage of the open position. It is possible to define different values for short positions. Define the percentage of TP to close from the open position.
* Choose the maximum number of Take Profits (TP)
* Define delays to evaluate the strategies of more previous candles:
  + Candle Delay is for MACD strategy
  + Candle Delay Stoch RSI is for the Stochastic RSI strategy.
  + Candle Delay RSI is for the RSI strategy.
  + Candle Delay Exit is the number of candles the algorithm waits to open a new position.
* Choose if you want to use the weighted strategy or just some of them.
* Choose the weight (relevance) of each strategy.
* Customize the well-documented MACD strategy.
* Customize the well-documented Stochastic RSI strategy.
* Customize the well-documented RSI strategy.
* Customize the well-documented Supertrend strategy.
* Customize the well documented MA cross strategy.
* Buy/sell labels for possible reentries.
* Monthly table performance. All the credits to @QuantNomad. I have only changed some colors and also adapted the calculations to the last previous candle. The purpose of this change is to make this script compatible with this weighted strategy. Thanks again to @QuantNomad for this amazing script!

---
⚠️ **NOTE**
- Backtest the algorithm with different data stamps to avoid overfitting results.
- The given default setup correspond with a successful example to use with $BTC/$USDT on @binance with +1400% in one year with a max drawdown of 9% approx.
  With the monthly performance, we can see that the algo has performed very well over the past two years, capturing the trend very accurately. However, from 2017 to 2019, the    algorithm can't even make a profit! This is a disclaimer, use at your own risk.
---

# Plots
* The color-trend represents when at least one of the strategies is satisfied, long in teal and short in gray and there is not a draw, same number of strategies satisfies for long and short.
* The + represent the next Take Profit (TP) target in teal and the Stop-Loss (SL) in gray.
* Plot labels for every time each strategy satisfies to open a long/short position
* Detect potential TOP and BOTTOMS based on a combination of RSI, Stoch RSI, MACD, volume, and the weighted-strategy.

# Examples



Enjoy!

Best,
Alberto
