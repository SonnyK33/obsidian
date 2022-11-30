Type: #Atom 
Source: podcast
Guest: Ernie Chan
References: [[Algorthmic Trading]] [[Momentum Trading]] 
Tags: #ML 

Chan uses meta labeling w ML. Has a certain strategy - long/short SP when trending intraday. Uses ML to predict when his given strategy will be profitable. Ie instead of predicting the market (bc signal to noise is low) he uses it to predict when his specific strategy will work. Ie under what vol (and other variables) does it tend to work. So uses it to reject trades when not likely to work.

Cites the work of Marco Prado (may have been in book I returned)

I could use this with CRAM model -
- pair trading between HY and IG CDX
	- rejection algo would have input variables - rates, curve, S&P performance
- buying/selling widest/tightest credits in rating-sector group
	- rejection algo variables - S&P performance, VIX, rates
could combine with hurst exponent to forecast whether in trending or mean-reverting regime