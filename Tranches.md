Type: #Atom 
References: 
#convexity 

Theta
- 1 year theta = 1yr carry + 1yr rolldown 
- higher risk tranches have more theta (why?)
- delta hedged long risk equity tranche typically has positive theta (negative for senior tranches)
	- so positive theta and positive convexity? only true assuming no defaults
	- compensation for bearing JTD risk?
	
JTD
- delta hedged equity tranche have positive convexity and theta but negative JTD
- delta hedged senior tranches have negative convexity and negative theta but positive JTD 
	- make more on the short index leg than lose on the long senior tranche leg (delta doesn't capture big moves)
- JTD on equity tranche will be less than weight of one credit x loss rate x tranche width

 Dispersion
 - higher dispersion leads to wider equity tranches and tighter senior tranches as means worse credits widen and best credits tighten 
 - one step closer oto JTD

Correlation
- spread of index only reflects spreads (risk) of constituents, not the correlation
- spread of tranches does depend on correlation of default risk
- all things equal, low correlation makes equity tranches riskier
	- more likely to have an outlier default and impact the equity tranche (for a given average expected loss)
	- equity tranche holders only care about the first loss
		- in a highly correlated scenario, there are fewer scenarios (out of the total possible scenarios) under which the credits default (more credits will default, but that doesn't matter to the equity tranche)
		- for the same reason, it makes the senior tranche riskier
		- e.g. there are ten possible scenarios, and one default in each scenario
			- you are guaranteed to have a first loss
		- 10 defaults in one scenario, and 0 in the rest 
			- 90% chance of no hits to the equity tranche so less risk for the equity tranche 
- high correlation makes senior tranches more risky because if one credit defaults, likely to have more defaults, and hence likelier to hit the senior tranche 

Convexity
- short risk senior tranches are positively convex (i.e. owning protection on senior tranche)
	- at inception, the spread on senior tranche is compensating for risk of rising spreads not JTD (as equity tranche has to absorb those first)
	- as spreads widen though, an increasing amount of expected losses are expected to be borne by senior tranche (as equity tranche will be exhausted)
	- hence the tranche becomes riskier to the downside as spreads widen 

Trades
- senior tranche may give best market to market on spread widening per unit of premium due to convexity (vs equity tranche or index)