Type: #Atom 
References: [[Algorthmic Trading]]

- calculating hedge ratios easy when a pair is perfectly cointegrated
- when the hedge ratio moves dynamically, need a different approach
	- EMA over-weights more recent observations
- using Kalman filters avoids needing to pick a weighting scheme
- assumes a linear relationship between target variable at time t and its previous observation as well as with another observed variable at time t
- allows you to dynamically calculate the mean and variance of the target variable (i.e. the hedge ratio in this case)

**Need to find a better explanation of this**