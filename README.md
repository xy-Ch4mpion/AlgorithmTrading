# AlgorithmTrading

## Introduction
An ATM option strategy.

### Summary 
An automatic trading program using dalayed synthetic future strategy. The strategy uses the ATM call options and ATM put options to synthesize the futures and mistmatches the time when synthesizing the future in order to gain the profit from the opposite movement of the market. For example, when we are longing calls and the market goes down, we can short the put at a higher price.

### Features
Automatic trading.
Can customize the trading frequency.
Trading time from 9:45 to 11:30 and from 13:00 to 14:45.
Closing all position from 14:50 to 14:55.

## Requirements
Using DolphinDB API to achieve everyday data.

## Usage
Inputs:

underlying - The underlying asset. (50ETF, 300ETF)

x - Each time long/short volume.

m - The amount option price changes.

start - The data you want to trade.

money - The initial capital you have.

ATM.trade() - Execute one-day trading.

one_day_test(date) - Backtesting for one day.

backtest(underlying, start, end, x, m, init_money) - Backtesting for a time window from start to end.

## Changelog
V0.0 Script
<br>V0.1 The initial version.
<br>V0.2

  V0.2.1

  Solve the time problem when it comes to the festival. Set the initial capital and the commission for each trade. Make the program can automatically identify the next month    contract. Fix some bugs in V0.1.

   V0.2.2
   
   Track every option in one day trading and modify the data structure to improve the efficiency. Output the position each time traded. Add more information into the trading records. Correct the strike price of trading calls and puts.
