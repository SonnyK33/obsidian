Type: #source 
Tags: #convexity 
References: GS primer
[[Second Leg Down]]


Tranches are subsections of credit indices which allow you to take a view on the number of defaults in a set period, as well as correlations between single names. The lowest tranche - the equity - represents the first 15 defaults for the HY index. As defaults occur, the lowest tranches become impaired first. Taking a short risk position in one of the junior tranches allows you take a view that defaults will occur without picking the names. The equity tranche will underform (on a delta hedged basis) the rest of the tranches as dispersion increases, so tranches also allow you to take a view regarding correlation/dispersion. 


TODOs:
- link w/ delta
- atom giving gist of tranche
- molecule comparing to put spreads and capital structure trades
- link with trade framework - under what scenarios would certain trades work?
	- link w/ second leg down - what trade to do when vol already high and spreads are wide?
- compare implied correlation w/ implied correlations from equity index/single name volatilities

Indices
- indices give exposure to a portfolio of individual CDS contracts
- losses on the index = weight of the defaulted credits x LGD on those credits 
- IG and main indices have 125 members so each name = 0.8%
- HY CDX has 100 members

Tranches
- gives exposure to a sub-segment of the index
- for HY:
	- equity tranche (0-15%)
	- Junior Mezz (15%-25%)
	- Sr Mezz (25-35%)
	- Senior (35%-100%)
- currently the HY index has taken a roughly 10.5% hit and so the equity tranche has 4.5% left



Mark to Market
- tranche PnL through expiry will be determined by actual defaults and recovery rates
- MtM though is determined by spread changes on the index (which is a function of individual spreads and correlation) as well as defaults
	- MtM loss will be bigger on lower tranches (higher delta)

Tranche Cashflows
- when a credit defaults, its weight * LGD / tranche width = tranche loss
- e.g. if a HY credit defaults and recovers 20%, loss on equity tranche = 1% x 80% / 15% = 5.33% 
- tranche notional starts as the width between attachment and detachment points (100 for the index)
	- each default reduces notional by 1/number of members
	- coupons are paid on remaning notional 

Delta
- a measure of tranche's sensitivity to general moves in the index (i.e. all memebrs move by the same amount)
- if delta is 2.0 on a tranche, its MtM will be 2x that of the index
	- they are computed by moving the underlying spreads by a small amount  in each direction and calculating how the tranches and index move in response 
		- the ratio is equal to the delta 
	- e.g. if spreads widen 1bp, the losses on a 5yr tranche with 2x = 1bp x ~5 duration x 2 delta = 10bps loss 
- more senior tranches have lower deltas (<1 for senior tranche)
- for equity like tranches, the delta decreases at maturity increases; opposite for senior tranches
	- for the equity tranches, longer durations will have spreads so high that the delta will have to come down (relative to earlier maturities)
		- opposite for senior tranches 
- if delta hedged, you're hedged against general small moves in index; you're still exposed to:
	- large moves (convexity or gamma)
	- moves in individual names (dispersion or iGamma)
	- supply and demand for specific tranches (changes in implied correlation)
	- theta (negative carry of time just passing by)
	- jump to default
	


Theta
- 1 year theta = 1yr carry + 1yr rolldown 
- higher risk tranches have more theta (why?)
- delta hedged long risk equity tranche typically has positive theta (negative for senior tranches)
	- so positive theta and positive convexity? only true assuming no defaults
	- compensation for bearing JTD risk?
- carry is so high on the equity tranche it offsets the negative index carry even delta adjusted
	
JTD
- delta hedged equity tranche have positive convexity and theta but negative JTD
- delta hedged senior tranches have negative convexity and negative theta but positive JTD 
	- make more on the short index leg than lose on the long senior tranche leg (delta doesn't capture big moves)
- JTD on equity tranche will be less than weight of one credit x loss rate x tranche width (bc some priced in already?)

 Dispersion
 - higher dispersion leads to wider equity tranches and tighter senior tranches as means worse credits widen and best credits tighten 
 - one step closer to JTD

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

Implied Correlation
- correlation determines how expected loss is distributed through the tranches
	- expected loss = spread x duration 
	- e.g. 2yr expected loss = 2 x 330bps = ~6.6%


Convexity
- long risk in equity tranche (delta hedged) is positively convex because you'll make more on a tightening and lose less in a widening than the delta-adjusted position in the index
	- so long risk equity + short risk delta adjusted index will be positive MtM for large moves 
	- PnL looks like a straddle 
	- still have JtD risk
- long risk in senior tranches is negatively convex
	- as spreads widen, the equity tranche quickly exhausts (hence positively convex) but more risk shifts to more senior tranches 
- short risk senior tranches are positively convex (i.e. owning protection on senior tranche)
	- at inception, the spread on senior tranche is compensating for risk of rising spreads not JTD (as equity tranche has to absorb those first)
	- as spreads widen though, an increasing amount of expected losses are expected to be borne by senior tranche (as equity tranche will be exhausted)
	- hence the tranche becomes riskier to the downside as spreads widen 
- long/short convexity depends on where the expected losses on the index are
	- tranches, whose attachment point is above the current expected loss (spread x duration), will be positively convex (for owners/short risk)		
	- tranches below the attachment point will be positively convex for long risk (sellers)
- in general, if you're below the expected loss threshold you're equity-like, and if you're long-risk, you are:
	- positively convex to spread movements
	- long correlation / short dispersion
	- long theta
	- short JTD
- if you're above the threshold, you're senior like, with the opposite relationships to convexity and correlation 
- can calculate an implied correlation from tranche pricing - is an analogue to implied vol for options

Trades
- senior tranche may give best mark to market on spread widening per unit of premium due to convexity (vs equity tranche or index)
- Short HY 39 Jr Mezz vs Index
	- expect dispersion to increase
		- low correlation/high dispersion -> want to be short lower tranches 
	- higher dispersion w/o JTD would affect Jr mezz more than equity as cash prices are already low and so equity tranche somewhat saturated
		- long risk equity tranche is now positively convex (delta hedged) as is trading below expected expected losses
	- outright short is expensive (>900 on HY 33 - Dec'24)
		- but delta is >3x
			- subordination is not 15% given losses that've already been experienced (in 15-25 tranche, effective subordination is ~5%)
				- attachment point now at 5 more defaults x 100 expected losses
				- don't need the defaults, just the risk of one 
	- risk is dipersion narrows and weakest names bounce back
		- currently, the weakest names are being driven by idiosyncratic issues
			- 