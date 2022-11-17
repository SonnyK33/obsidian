Type: #Atom 
References: [[Algorthmic Trading]] [[Stationarity]] [[Augmented Dickey-Fuller]]

If a group of price series are not stationary, but a linear combination of them are, then the group is cointegrated. Pairs trading is based on this, but it can be extended to 3 or more assets as well. 

We can use OLS to first find the hedge ratios between two series (can test different combinations of dependent and independent variables) and then use the ADF test on the combination to test that the combination is stationary (and hence the pair are cointegrated)

The Johansen test can be used to find all of the cointegrating relationships between a group of assets (even 2 assets could have 2 possible hedge ratios depending on which is the dependent variable). 
