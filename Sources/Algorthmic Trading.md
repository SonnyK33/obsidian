Type: #source 
Title: Algorithmic Trading
Author: Ernest Chan
References: [[Stationarity]] [[Cointegration]] [[Momentum Trading]]

Chapter 2: Basics of Mean Reversion

**Linear Mean Reversion Trading Strategy**
- use OLS to find regression coeffiecient ($\lambda$) between $\Delta$y and y<sub>t</sub>
- find half-life of reversion from lambda 
- buy (sell) units inversely proportional to the assets's deviation from the mean (use z-score to normalize)
	- if z-score = 2 (i.e you're 2 means above standard deviation), should be short 2 units
- while variance is supposed to be zero, this model assumes variance is simply growing less fast than brownian motion 
- mean should also be fixed, but in practice this may change with changes in corporate policies 
- this can be extended to a portfolio with more than 2 assets - the unit (whose moving average and standard deviation is calculated and turned into a z-score) is the portfolio with appropriate hedge weights
- ETFs often provide good instruments for trading stationary portfolios
- mean reversion often benefits from fundamental rationale (e.g. GDX and Gold px cointegrate) versus many momentum strategies 
- ratios may also work if a pair isn't trully cointegrated 