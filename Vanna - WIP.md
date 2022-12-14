Type: #molecule 
References: [[Pinning - Trades]]
Flirting w models podcast; Cem Karsan ; S4E1
[[charm]] [[Dispersion]][[Credit Correlation]] [[Tranches -WIP]]

[[To Write - Outline]]
- atom
- calls and puts have positive and negative vanna respectively
	- higher vol increases the odds of expiring in the money
		- makes call delta more positive
		- makes put delta more negative 
- understand what causes negative and positive vanna
- how changes with vol and dealer positioning 

[[To Read - Outline]]
- how are 0DTE calls impacting these vanna flows?


Gamma, charm, and vanna - are all about reflexivity in the market. They reflect how dealers will have to hedge their positions.

If dealers are long delta, they will be getting longer as you get closer to expiry.

If long vol or skew will be a dampening effect. See [[Pinning - Trades]] and [[Delta_Hedging]].
If you're long gamma (or vol), you'll be hedging against the direction of the market.

Vanna and charm more important for day to day effects of dealer positioning, while Gamma most important for tail events but those are rare. 

They can explain many trading cliches:
- never short a dull market
	- dealers are short puts and long calls (bc everyone is long market and hedging) - “short the carry trade” -and as time passes, they have to buy stock
	- they hedge short puts and long calls with short positions in stock
	- if nothing happens to stock prices, the deltas converge to zero, allowing them to reduce their hedges and buy back stock
	- Vol term structure is normally upward sloping and so there’s natural vanna. That is, as vol slides down the term structure, delta decreases (for OTM options).
		- as they hedged with short positions, they have to buy back stock
		- "Dealers have to buy back vol"

- If vol is pinned at the index level (in 2017 this was due to one fund - catalyst - having a big position at a certain strike), there will be more dispersion at the underlying level since individual equities aren’t pinned
- Positive vanna flows in index bc dealers are short puts (so long vanna)
	- i.e. delta gets on the puts get closer to -1 as vol increases for OTM options
	- hedge ratio increases as vol increases
	- they're short stock as a hedge
	- they have to sell more stock 

- Opposite for underlying if there's call skew 
	- dealers are short calls (short vanna) and long stock as a hedge 
	- delta on the calls increases and get closer to 1 and so hedge ratio increases
	- if momentum slows there’s negative vanna -> don't understand this
	- as stock prices decrease, delta decreases as well
	- they'll sell some stock as don't need to be as long 