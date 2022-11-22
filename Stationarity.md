Type: #Atom 
References: [[Time Series]] [[Algorthmic Trading]] [[Momentum Trading]]


 - mean-reversion implies that the change in price series of the next element is proportional to the difference between the current element and the mean
 - mathematical description of stationarity is that the variance of the log of prices increases slower than geometric  random walk, that is, it's sublinear
	 - sublinear function is $\tau$<sup>2H</sup>  where tau is the time between two measurements and H(urst exponent)<0.5 if it's stationary 
	 - H can help determine the extent of mean reversion or trending
	 - H=0.5: random walk
	 - H<0.5: stationary (the lower, the more stationary)
	 - H>0.5: trending (the higher, the more trending)
-   models covered require weak stationarity
    
    -   mean of time series is constant (i.e. mean reverting)
	    - mu(t) = mu; i.e. it doesn't vary with time and hence we can use the sample mean to estimate the population mean 
    -   autocorrelation only depends on time difference b/w points
    -   finite and constant variance
-   in non-stationary TS, auto-correlations will slowly die off
- if we have a stationary TS in the mean and in the variance, can discuss second order stationarity - TS is second order stationary if correlation between sequential observations is only a function of the lag

- strict stationarity requires that distribution of a time series is contant for different time periods 
	- i.e. mean and variance are constant 

-   in stationary, auto-correlations will all be close to zero
    
-   can also run [[Augmented Dickey-Fuller]] test to check; where null hypothesis is non-stationarity
	- ADF tests if the next value depends on the current value (specifically the null hypothesis is that coefficient between the next value and the current difference from the mean is zero )
	- can also interpret the ADF test statistic ($\lambda$ ) as the speed of mean reversion and still use a strategy if we can't reject the null hypothesis 
	- if the linear model is transformed by ignoring drift and the lags, you get the Ornstein-Uhlenbeck formula for a mean-reverting process
	- solving this equation shows that  y decays exponentially to the value of -$\mu$ $\lambda$  and the half life is equal to -log(2)/$\lambda$ 
	- if lambda is positive, the process isn't mean reverting; if it's zero, the mean reversion will be very slow
	- the half life can help determine the right lookback window for a mean reversion strategy 
	- lambda can be calculated by regressing $\Delta$ y<sub>t</sub> on y<sub>t-1</sub> 
	
    
-   can transform a non-stationary TS to stationary by differencing
    
-   can detrend by removing deterministic relationship with time
    
    -   can regress time series on time, and then use the residuals
    - 