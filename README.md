## Weighted strategy

[![tradingview](https://img.shields.io/badge/Post-TradingView-%23e32b3e)](https://www.tradingview.com/script/OF3TzrNS-Acrypto-Weighted-Strategy/)
![last modified](https://img.shields.io/github/last-commit/AlbertoCuadra/algo_trading_weighted_strategy)
[![license](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-%23299489)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![referral](https://img.shields.io/badge/Referral-TradingView-%23f08f07)](https://www.tradingview.com/gopro/?share_your_love=accry)

---
**Note**

This project is on hold until further news. The idea is to take it up again when I defend my PhD in June 2023.

Best,

Alberto

---


I have been developing a fully customizable Algorithmic Trading Weighted Strategy in Pine Script for the last year in my spare time. The algorithm is based on a set of well-documented strategies, each with its own weight (weighted strategy). Currently a set of 5 strategies have been implemented:

* `MACD`
* `Stochastic RSI`
* `RSI`
* `Supertrend`
* `MA crossover`

Moreover, the algo includes stop losses criteria and a taking profit strategy. The algo must be optimized for the desired asset to achieves its full potential. The 4H dataframe gives good results. The algo has been tested for several asset (same dataframe, different optimization values).

To set an order, first, the algorithm calculates the weight_strategy, which represents a value from 0 to 5 of the number of strategies that are satisfied (in case the weight of each strategy is the same, i.e., same relevance over the rest). To open a position, the value of weight_strategy must be greater than the value of weight_signal, by default 2. Modify the indicator parameters for the desired asset and data frame. Set stop-loss and take profit criteria.

## Pro and Premium version (in Development)
There are two additional new versions of the algorithm under development:
* Pro:
  + complete alert system ✅ 🐛
  + access to a telegram channel with instant signals of BTC/USDT ✅ 🐛
  + new entry strategy based on limit orders instead of market orders as in the basic plan 👨‍🏭
  + more control of the stop-loss and take profits orders 👨‍🏭
* Premium:
  + all of pro version
  + kernel based on more sophisticated indicators 👨‍🏭
  + compatible with 3Commas
  + access to the premium telegram channel with instant signals of BTC/USDT and few altcoins ✅ 🐛
  + the premium telegram channel allows auto-trading with the use of a secure third-platform API ✅ 🐛
  + access to more reliable signals based on an in-house optimization algorithm 👨‍🏭

## Features:

* The algorithm allows to trade with long, short or both positions.
* `Backtest the algorithm` over a defined interval (data stamp), e.g., from 01/01/2021 to 01/01/2022.
* Set stoploss (SL) orders based on a percentage of the previous candle source, e.g., close or hl2 (high + low)/2. The position will only be closed if after the candle closes, it still meets the stop condition.
* Set SL to previous TP targets.
* Set SL to the average position (after TP).
* Stop position in case the algo `detects a potential Top/Bottom`.
  + It can close a specific percentage of the remaining open long position.
  + It can close a specific percentage of the remaining open short position.
* It can `moves the stoploss` every time the algo takes profit (TP)
* `Take profit` based on a percentage of the open position. It is possible to define different values for short positions. Define the percentage of TP to close from the open position.
* Choose the maximum number of Take Profits (TP)
* `Define delays` to evaluate the strategies of more previous candles:
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
* `Buy/sell labels for possible reentries`.
* Monthly table performance.
* Configurable alarm system.

---
⚠️ **NOTE**
- Backtest the algorithm with different data stamps to avoid overfitting results.
- The given default setup correspond with a successful example to use with H4 $BTC/$USDT on @binance with +1700% in one year with a max drawdown of 8% approx.
  With the monthly performance, we can see that the algo has performed very well over the past two years, capturing the trend very accurately. However, from 2017 to 2019, the    algorithm can't even make a profit! This is a disclaimer, use at your own risk.
---

## Plots

* The color-trend represents when at least one of the strategies is satisfied, long in teal and short in gray and there is not a draw, same number of strategies satisfies for long and short.
* The `+` represent the next Take Profit (TP) target in teal and the Stop-Loss (SL) in gray.
* Plot labels for every time each strategy satisfies to open a long/short position
* Spot potential local Tops (T) and Bottoms (B) based on a combination of RSI, Stoch RSI, MACD, volume, and the weighted-strategy.

## Examples

* H4 BTC/USDT Binance (default) - 01/01/2021 - 19/02/2022
<p align="left">
    <img src="https://github.com/AlbertoCuadra/algo_trading/blob/main/Examples/example_BTC_USDT_Binance_4H.svg" width="1400">
</p>
<p align="left">
    <img src="https://github.com/AlbertoCuadra/algo_trading/blob/main/Examples/example_BTC_USDT_Binance_4H_results.svg" width="1400">
</p>

## How to use it
Search for `Acrypto - Weighted strategy` in the indicator tab using `TradingView` and add it to your layout. Modify the indicator parameters for the desired asset and data frame.

If you consider paying for a subscription on TradingView (which is not required for this script), I would be very grateful if you could use my referral link :)

`Referral link:` https://www.tradingview.com/gopro/?share_your_love=accry

`Original post:` https://www.tradingview.com/script/OF3TzrNS-Acrypto-Weighted-Strategy/

## Acknowledgements
The monthly table performance was developed by @QuantNomad. I have only changed some colors and also adapted the calculations to the last previous candle. The purpose of this change is to make this script compatible with this weighted strategy. Thanks again to @QuantNomad for this amazing script!

## Questions?
For discussions, questions, or just to share some settings, please leave a comment here in the [discussion channel](https://github.com/AlbertoCuadra/algo_trading_weighted_strategy/discussions).


## Developer

* **[Alberto Cuadra-Lara](https://acuadralara.com/)** 


Support this project by giving me an extra dose of caffeine :coffee: 

<a href="https://www.buymeacoffee.com/acuadra" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-green.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
