Type: #source
Title: Advanced Algorthmic Trading 
Author: MIchael Halls-Moore
References: [[Algorthmic Trading]]
[Time Series]

- for quantitative finance, assume time series are results of random variables
- sequence of random variables is known as a discrete-time stochastic process
- Time series include:
	- trends - a consistent directional movement in TS; may contain a deterministic and stochastic component
		- common in commodity prices
	- seasonal variaton 
		- also common in comodities
	- serial dependence - serial correlation 
		- observations close to one another are correlated 
		- #volatility clustering is common in financial markets 

	- use Time Series analysis to:
		- forecast values
		- simulate a series (and hence forecast number of trades, commission costs, infrastructure needs, etc)
		- infer relationships between different series 
		- can combine with #Bayesian tools and #ML to develop models  to forecast and detect regime change 

#autocorrelation (or serial correlation)
-  once a TS has been decomposed into trends and seasonal components, there is still the random or error term
- in financial TS, these error terms are frequently correlated with one another 
- autocorrelation of lag k of a second order stationary TS is the autocovariance normalized by the prodct of the spread (rho(k) = C/sigma^2) where C is the autocovariance 
	- by definition, the first lag should have a correlation of one 
	- most of the other lags should be close to zero (ACF diagram shows a blue shading in python to show the 5% confidence intervals)
	- may have a few lags outside of these boundaries due to unexpected seasonality effects 



- TS models may be superior to ML models where you have limited data and a lot of random noise
    
-   ML models are prone to overfitting whereas TS ones will properly take into account random noise
    
-   autocorrelation just measures correlation b/w two observations in the same time series at different times
    
-   partial autocorrelation compute correlation adjusting for previous periods (analogous to multivariate regression)
    
-   for instance, if you ran a PACF plot (showing partial correlations on the y-axis and lag on the x-axis) there would be high correlation for the first lag, and it would then drop to close to zero
    
    -   this is because almost all of the correlation is explained by the first lag, the future lags have limited correlation w/ the first observation when controlling for the first period’s correlation
    
    

TS Models
- goal is to fit a model to a time series until the remaining series lacks any serial correlation 
- if a model is able to adequately explain a model, than the residuals should be serially uncorrelated 
- can use discrete white noise -- specifically Gaussian discrete white noise (mean=0, mean =1, and corr = 0 for all lags after 0) as a model for residuals 
- #randomwalk - a TS where every element is equal to the previous element + white noise
	- by definition, the difference between 2 elements is white noise, so if we difference the whole series, the result should be white noise 

- more sophisiticated than random walk models are AR, MA, and ARMA models
	- they all assume constant vol however and so don't work well for financial TS which have vol clustering or conditional heteroskedasticity 
	- that will lead to need for ARCH and GARCH models 
- can categorize models using the Akaike Information Criterion #AIC which penalizes a model for more parameters but rewards it if likelihood increases 

[Autoregressive]AR(p) Models_

-   specifies X as a function of lagged TS values X(t-1), X(t-2)… X(t-p)
    -   X = mu + k1 * X(t-1) … +K(p) * x(t-p) + epsilon
-   can use OLS to get the coefficients
-   may be non-stationary as shocks from the past can influence X, hence may not be mean reverting
-   key parameter is p (the number of lags)
-  is an extension of random walk (which is just AR(1) with 1 for first coefficient)
- not necessarily stationary
	- can tell by setting characteristic equation (AR model in backward shift notation) to zero; all |roots| >1 for it to be stationary 
- tries to take into account market participant behaviors in the past and capture momentum and/or mean reversion
-

[Moving Average] MA(q) Models_

-   similar to AR models except express X as a linear combination of random shocks (white noise)
-   still has mu (intercept) term, but uses epsilons as coefficients for the random shock terms
-   is stationary by design since the shocks are random
-   key parameter is number of shocks to include
- MA model only takes into account q white noise terms, whereas AR models take all of the previous ones (though in decreasing amounts) into account 
- as in AR models, the mean is zero (just the mean of a bunch of random shocks)
- tries to take into account past reactions to shocks 

[Autoregressive Moving Average]  [ARMA] (p,q) Models

-   combines the previous two models
-   X = mu + k1 * X(t-1) + … + k(p) * X(t-p) + epsilon(t) + epsilon(t-1) * shock(1) +…eps(t-1)*shock(q)
-   need to choose p and q
- ARMA model is parsimonious and redundant meaning may require fewer parameters than either MA or AR models 

[Autoregressive Integrated] [ARIMA] [[ARIMA]] (p,d,q) Models_

-   ARMA model with differencing (d)
- can reduce a non-stationary series to stationary by successive differencing 
- *integrated* - a TS is integrated of order d, if d differencing turns it into white noise 
- if a TS when differenced d times is an ARMA(p,q) model than the original TS is an ARIMA(p,d,q) model
- may need repeated differencing if it's a non-linear trend 

Conditional [[heteroskedasticity]]
- when subsets of a TS have differing variance, the series is called heteroskedastic 
- conditional heteroskedasticity is when increases in variance are correlated with more increases in variance 
- e.g. when sell-offs cause investors to sell even more 
	- leads to heteroskedasticity which is conditional on periods of increased variance 

Autoregressive Conditional Heteroskedastic Models [[ARCH]]
- uses an AR process for variance 
- can determine if an ARCH model is appropriate by fitting an appropriate model and then squaring the residuals and applying an AR model to the residuals 


Generalised Autoregressive Conditional Heteroskedastic Models ([[GARCH]])
- the ARMA equivalent of ARCH models, i.e. uses moving average terms
- sum of the model parameters must sum to < 1
- plotting the correlogram of series (i.e of epsilon) will show autocorrelations quickly dissipating - i.e white noise
- plotting the squares of epsilon (which i believe represents the variance since epsilon = sigma * white_noise), shows lags which decay over time - representative of a conditionally heteroskedastic model 
- GARCH is used after first using an ARIMA model and then checking for conditional heteroskedasticity by checking the correlogram of the squared residuals 
- backtesting a GARCH + ARIMA model vs buy and hold shows strong returns during periods of high vol, e.g. GFC, and then lower returns when markets enters into a more stochastic phase 
	- very important to identify the regime 


_Decomposition Models_

-   breaks a TS (X) into trend, seasonal, and error components
-   common forms assume X = T + S + E or X = TSE
-   various ways to decompose - [Kalman filters], [STL], [exponential smoothing]

Model Fitting

[Box Jenkins] -

1.  step for stationarity
    
2.  transform to stationary TS
    
3.  check residuals after fitting best versions of models → should be white npise residuals if stationary
    

-   plot partial autocorrelations
-   may show some large values for distant lags, but first few terms should be low

4.  run [Ljung Box] test on residuals

-   want to fail to reject null hypothesis that residuals are white noise

[STL] Model

-   uses loess regression → applies more weight to data closer in time

Follow-ups

-   advanced TS - [ARCH] and [GARCH] model changing variance over time
-   vector auto-regression for multiple TS and dependencies b/w them
-   TS in NN for sequence data ([LSTM]s)
-   cointegration, granger causality, serial correlation, regression with TS
-   [bayesian] TS



Sources:
- R course on coursera
- Advanced Algorithmic Trading (Moore)