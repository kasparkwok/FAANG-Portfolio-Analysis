# FAANG Portfolio Analysis- Abstract
Using FAANG stocks as an example to have a quick walk-through on stock price return and risk calculation. Followed by portfolio creation using the equally weighted methodology. It concludes by comparing the performance of the portfolio to S\&P500.


# Table of Content

### [1. Introduction to Stock Price Performance Analysis](#1-introduction-to-stock-price-performance-analysis)

1a. How does a stock perform over the a certain period of time?

1b. Advance Visualisation of the Stock Performance 

- Moving Averages 
- Candlesticks 

### [2. Diversification](#2-diversification)

2a. Why is diviersification important?

2b. What does a fund manager (portfolio manager) do?

### [3. Hypothesis](#3-hypothesis)

Null Hypothesis: Do technology stocks (FAANG) outperform than S&P 500 in the last two years?

### [4. Conclusion](#4-findings)


# 1. Introduction to Stock Price Performance Analysis

In order to perform individual stock price analysis, one can extract the relevant price information from [here](https://www.alphavantage.co/documentation/)

Additional documentation for the usage of pandas_datareader [click here](https://buildmedia.readthedocs.org/media/pdf/pandas-datareader/latest/pandas-datareader.pdf)

As the goal of this analysis is to perform a null hypothesis in FAANG stocks, a list of the relevant company names and their corresponding ticker symbols are created.

For more information in FAANG please click [here](https://www.investopedia.com/terms/f/faang-stocks.asp).

### Moving Averages

Moving averages acts as an indicator in technical analysis that helps smooth out price action by filtering out the “noise” from random short-term price fluctuations.

For instance, a 10 day moving average (10-Day SMA) calculate the mean of the 


There are other types of moving averages that gained populance in technical analysis. In general, there are 4 main types of MAs:

- Simple Moving Average (SMA)
- Exponential Moving Average (EMA)
- Weighted Moving Average (WMA)
- Moving Average Convergence Divergence (MACD)

For more information please read [here](https://www.investopedia.com/terms/m/movingaverage.asp)

[MACD](https://www.investopedia.com/terms/m/macd.asp) is particularly used by traders to spot trading opportunities.

### Candlestick graph

Candlesticks show that emotion by visually representing the size of price moves with different colors. Traders use the candlesticks to make trading decisions based on regularly occurring patterns that help forecast the short-term direction of the price.

For more information, please check [here](https://www.investopedia.com/trading/candlestick-charting-what-is-it/)

In order to create an interactive graph with the embedment of both candlesticks and moving averages in the original graph, __plotly express__ is used.

## Conclusion:
### Trading Strategy with the use of MAs
As a general simplistic trading rule of thumb, it is considered by traders to be a good opportunity to __short sell__ the underlying when the market is bearish (downtrend graph) and when the shorter MA (20 days MA in the above graph) crosses below the longer MA (50 days in the above graph). (E.g. early August 2018) 

In contrast, a great to __buy__ the underlying is when the market is bullish (uptrend graph) and when the shorter MA (20 days MA in the above graph) crosses above the longer MA (50 days in the above graph).

# 2. Diversification

## Why is diversification important?

### Caveat of the MA trading strategy
It is very noticeable that the share price dropped significantly (over 20%) in late July [background news](https://www.marketwatch.com/story/facebook-stock-crushed-after-revenue-user-growth-miss-2018-07-25)

If an investor would have simply followed the MA trading strategy and invested in early May, he/she would have incurred a huge loss in late July. While there are a lot of other ways to prevent this including setting a __target profit__ and placing a __stop loss order__, investors could potentially still lose significant portion of their investments if these are not executed properly.

Therefore, a __diversifcation strategy__ in stock investment is generally encouraged and used by all portfolio managers.

### [VaR (Value at Risk)](https://www.investopedia.com/terms/v/var.asp)

#### While calculating the expected return of a stock, one should always also consider the inherent risk from the stock.

#### Questions like: _What is the most I can - with a 95% or 99% level of confidence - expect to lose in dollars over the next month?_ are hence constantly raised by portfolio manager or their investors

In order to answer this question, several approach can be used.
1. Historical Method
2. Variance-Covariance Method
3. Monte Carlo Simulation

### Conclusion

By simply diversifying the investment, there is no significant gain in average daily return. However, the main advantage of diversifying the investment is to mitigate [Idiosyncratic Risk](https://www.investopedia.com/terms/i/idiosyncraticrisk.asp) from indiviudal stock investment.

However, there are numerous ways to optimise the portfolio and one of the first elementary steps to create one's optimised portfolio is to create an equal investment portfolio.  

## 3. Hypothesis 

### Null hypothesis: FAANG did not outperform S&P 500 in the last two years.


$$ H_0: mean_{FAANG} = mean_{S\&P500}$$
$$ H_1: mean_{FAANG} \neq mean_{S\&P500}$$

## 4. Findings

### Daily Return

According to the above statistical analysis, it is found that while FAANG did have a higher daily return in comparison to S&P500 from the last two years. There is __not enough statistical evidence to reject the null hypothesis__. 

### VaR

As seen from the above graph, the maximum potential loss with a 95% confidence interval of FAANG is significantly higher than that of S&P500.

### Conclusion

While there is __not enough statistical evidence to reject the null hypothesis__, it is seen that 
- FAANG stocks generate a higher return than S&P500
- FAANG stocks have a higher variance than S&P500
- The reason behind the higher variance could potentially be contributed to the fact that S&P 500 has a more diversified portfolio to mitigate the idiosyncratic risk from individual stocks.

Based on the above findings, it is therefore __inconclusive__ whether FAANG outperformed S&P 500 for the last two months.
Moreover, more resources should be allocated to pursuit of the optimisation of a portfolio. 
