Type: #molecule 
References: [[2023 Trades]]
Questions to Ask:
- Where is the asymmetric risk and are you being compensated for it?
- if you take the risk and you're right, how much do you make? how much do you lose?
	- what does that imply about the odds being priced in?
	- are those odds consistent with other parts of the market?
	- e.g. short-vol has asymmetric risk, and so you're paid a VRP for taking it
		- VIX term structure is upward sloping because you need to be compensated for being short it
- compensation for the risk should be proportional to how asymmetric it is not the absolute upside/downside (which are prone to more forecast errors anyways)


- fundamentals - focus on the variance around estimates rather than their mean
	- hard to just do a better job at predicting a company's EBITDA esp given how much coverage liquid credits have
	- instead I try to determine how risky those estimates are
		- what is the range for sales, costs, etc
		- what is the range for EBITDA, a FCF and where should things trade in the extremes of that range
		- based on that, is there asymmetry?
	- it doesn't matter what next year's EBITDA is, that's unknowable - what matters is the degree to which it can be estimated and the range of possible outcomes
		- that's how you price risk and look for trading opportunities 
- by being a generalist, have a better sense of how to price risk
	- risk-free vs IG vs HY
	- DM vs EM 
	- high beta vs low beta credits

I convert credit trades to option trades to better understand the risk I'm taking. In the below examples, "carry" should refer to current yield and not YTM. YTM is annualzing carry and gives too much credit for short-term returns. All trades can be broken into:
1) A long risk position is a short put where you're getting paid carry to take JTD (asymmetric) risk. 
2) A short risk position is a long put where you're paying carry for the possibility of JTD (asymmetric returns). 
3)  A steepener (short back-end versus long front-end). JTD will likely be negative (front-end will be trading at a higher cash price then back-end) but is defined. In a non-distressed credit, the yield curve will be upward sloping, so a steepener will be negative carry.  This is like a calender spread where you're short a near-term put and long a long-term put. That would be negative gamma and long vega. When does this make sense?

	In a distressed credit, the yield curve will be inverted. A steepener is betting on normalization. Carry will depend on the relative cash prices. It makes sense to be negative gamma here (because the credit is already inverted and so the gains from gamma have already been realized) and long vega
6) Flattener
7) Compression
8) Decompression
9) RV across different credits 