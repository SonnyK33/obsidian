Author:  Hari Krishnan
Type: #source #book
Topics: #volatility #trading #systematic
References: [[Monetary Tightening - 2022]]
[[VIX]] [[Skew]] [[Delta_Hedging]] [[Variance Risk Premium]] [[Vol Surface]] [[Futures Curves]]

Summary:
Second Leg Down gives a playbook of hedging options to implement when there has already been a large draw-down, the VIX is high, and implied vol on options is high, and skew is typically elevated. Most of the trades take advantage of high skew post sell-off. One of the author's key premises is that trading vol after a big move makes sense since it’s the easiest of the moments to forecast. This is because it itself exhibits less variance than mean, skew, or kurtosis. Vol is heavily mean reverting and a stationary process (I think?). High levels on the VIX are correlated with subsequent negative returns and shorting the Vix when above 30 tends to work. Most of the described trades are variations on buying dip in risky assets, selling vol, and selling skew. They must be sized appropriately and only work if you didn’t lose too much in the first draw down. It also discusses trade-offs between gamma and vega. Pre-crash, you want vega, as it becomes too expensive after an event. This translates to wanting long-term options pre-crash and short-term post. 




**Post-sell off trades**

- Weekly options may be useful for hedging as you’re not overpaying for volatility (after a move already occurred). 

- trading reversals ie buying bad closes. Assumes you can buy at the close. Takes advantage of fact that some levered traders may have to sell on a down day, exaggerating the move into a close 

- risk reversal hedged with short futures. Eg short 25d puts + long 25d calls + short futures. Works in a moderate sell off or in a big reversal. Takes advantage of the high skew post sell off and bets that this will decrease. Short downside gamma and long gamma to the upside.

- buy put spreads. Sell 40d put and buy 25d put. Works if market reverses or doesn’t fall too much. Could do this w 4 wk expiry and put on whenever market has a negative weekly return. Signal tends to be on 50pct of the time. It may be best to only do this when implied vol is high which correlates w higher equity risk premise and higher premiums collected 

- buy VIX puts. Assuming the term structure is in contango, benefits from roll down as forward prices roll down towards the strike. The roll down and mean reversion of vol (after a sell off) tend to compensate for theta. Can also get windfall gains if you called the bottom of the market. Strategy has positive gamma, positive expected value, and bounded risk. Could combine this with far OTM call spreads. This bets that vol won’t stay at an elevated level. It either falls or spikes again. Buying puts may have less expected returns now as skew has steepened (check this).


- sell VIX call spreads. Bets that vol won’t continue rising and exploits fact that level of Vix and implied vol of Vix are highly correlated. Ie when VIX comes down so does IV. Market only accounts for mean reversion once VIX gets high. Assuming markets stabilize, You benefit from negative delta and negative Vega - short Vega on lower strike short call dominates. Market doesn’t have to recover just stop falling. This is a variation on the put/put spread buying strategy. It doesn’t gain from roll down but does from falling IV. Declining vol works against the long put spread esp if curve has inverted. 

- When the curve inverts, buy the second month and short the near month. Roll yield is negative since it’s backwardated - you’re betting this is temporary. You’re betting on mean reverting spot volatility and hedging with the future month. This is still exposed to sharp sell offs as near term contract will move a lot more 

- Calendar spreads - long Near term vs short long term ATM puts are positive gamma and negative Vega. You generally want Vega protection pre draw down and gamma post as it’s too late to get the Vega at that point. This trade looks good If the vol doesn’t shift up. But it’s exposed to the risk that the underlying doesn’t move initially but plummets afterwards and long-term vol increases - a steepening of the vol term structure.
	- it makes sense after skew has steepened

  
**Before the sell-off**
While the book is focused on post-sell off trades, it gives a few clues on how to detect draw downs and buy hedges before you need them. Tracking price action and volatility (eg an indicator based on when price and vol exceed 2 standard deviations) is a good indicator of unsustainable price action. 



**Other Long-Vol trades**

Trend Following
Trend following slightly diversifies as isn’t correlated with volatility.Trend following systems can diversify across timeframes. For example multiple moving average crossover systems have little correlation with each other (eg signal from crossing 5d moving avg vs crossing 50d). This was counter-intuitive to me; I though trend following was a short-vol strategy. I think trend following mimics some long-vol strategies because it takes advantage of vol's mean reverting characteristic. The mean reversion in vol causes trends in the underlying asset.



**Short Vol Trades**
Mainly for contrast, a few long-vol strategies are described. 

Batman - combines a call ratio spread with a put ratio spread, or can be thought of as a long straddle with a short strangle. This does okay with moderate moves in either direction, but fails in either extreme. 






