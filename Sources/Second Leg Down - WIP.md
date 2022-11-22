Author:  Hari Krishnan
Type: #source #book
Topics: #volatility #trading #systematic
References: [[Monetary Tightening - 2022]]
[[VIX]] [[Skew]] [[Delta_Hedging]] [[Variance Risk Premium]] 

Summary:
Second Leg Down gives a playbook of hedging options to implement when there has already been a large draw-down, the VIX is high, and implied vol on options is high, and skew is typically elevated. Most of the trades take advantage of high skew post sell-off. One of the author's key premises is that trading vol after a big move makes sense since it’s the easiest of the moments to forecast. This is because it itself exhibits less variance than mean, skew, or kurtosis. Vol is heavily mean reverting and a stationary process (I think?). High levels on the VIX are correlated with subsequent negative returns and shorting the Vix when above 30 tends to work.



**Post-sell off trades**

- Weekly options may be useful for hedging as you’re not overpaying for volatility (after a move already occurred). 

- trading reversals ie buying bad closes. Assumes you can buy at the close. Takes advantage of fact that some levered traders may have to sell on a down day, exaggerating the move into a close 

- risk reversal hedged with short futures. Eg short 25d puts + long 25d calls + short futures. Works in a moderate sell off or in a big reversal. Takes advantage of the high skew post sell off and bets that this will decrease. Short downside gamma and long gamma to the upside.

- buy put spreads. Sell 40d put and buy 25d put. Works if market reverses or doesn’t fall too much. Could do this w 4 wk expiry and put on whenever market has a negative weekly return. Signal tends to be on 50pct of the time. It may be best to only do this when implied vol is high which correlates w higher equity risk premise and higher premiums collected 

- buy VIX puts. Assuming the term structure is in contango, benefits from roll down as forward prices roll down towards the strike. The roll down and mean reversion of vol (after a sell off) tend to compensate for theta. Can also get windfall gains if you called the bottom of the market. Strategy has positive gamma, positive expected value, and bounded risk. Could combine this with far OTM call spreads. This bets that vol won’t stay at an elevated level. It either falls or spikes again. Buying puts may have less expected returns now as skew has steepened (check this).

[describe strikes below:]
- sell VIX call spreads. Bets that vol won’t continue rising and exploits fact that level of Vix and implied vol of Vix are highly correlated. Ie when VIX comes down so does IV. Market only accounts for mean reversion once VIX gets high. Assuming markets stabilize, You benefit from negative delta and negative Vega - short Vega on lower strike short call dominates. Market doesn’t have to recover just stop falling. This is a variation on the put/put spread buying strategy. It doesn’t gain from roll down but does from falling IV. Declining vol works against the long put spread esp if curve has inverted. 

  





  

- can take advantage of this with calendar spreads. When the curve inverts, buy the second month and short the near month. Roll yield is negative since it’s backwardated - you’re betting this is temporary. You’re betting on mean reverting spot volatility and hedging with the future month. This is still exposed to sharp sell offs as near term contract will move a lot more 

  

All of the above are variations on buying dip in risky assets, selling vol, and selling skew. They must be sized appropriately and only work if you didn’t lose too much in the first draw down

Tracking price action and volatility (eg an indicator based on when price and vol exceed 2 standard deviations) is a good indicator of unsustainable price action 


**Other Long-Vol trades**

Trend Following
Trend following slightly diversifies as isn’t correlated w volatility.


Trend following systems can diversify across timeframes. For example multiple moving average crossover systems have little correlation with each other (eg signal from crossing 5d moving avg vs crossing 50d).
**vol surface**


Short term market shocks may cause term structure of vol to invert, though this is normally temporary and the curve is generally upward sloping. Short term vol tends to have much higher beta then long term. For example if we regress different expiry ATM implied vol to 3m ATM vol and graph the betas against the time to maturity, it’s downward sloping and convex.

That is 1 week ATM vol is high and it rapidly comes down as maturity increases. For longer dated options, skew is much flatter— that is OTM implied vol isn’t much higher than ATM.

The focus of vol surface modeling should be to determine what strikes/maturities will move the most with a change in the underlying. Figure out which parts are most in need of hedging and/or will give the most bang for your buck.


  

**Short Vol Trades**
Batman - combines a call ratio spread with a put ratio spread, or can be thought of as a long straddle with a short strangle. This does okay with moderate moves in either direction, but fails in either extreme. 

Calendar spreads - long Near term vs short long term ATM puts are positive gamma and negative Vega. You generally want Vega protection pre draw down and gamma post as it’s too late to get the Vega at that point.

This trade looks good If the vol doesn’t shift up. 

But it’s exposed to the risk that the underlying doesn’t move initially but plummets afterwards and long-term vol increases - a steepening of the vol term structure.

**futures curve**

Roll yield is the positive or negative carry generated by maintaining a futures position by continuously rolling to the next month. If the curve is in contango the roll yield is negative - this reflects the cost of carry - and is true for most commodities. If the yield curve is steep, the bond futures curve will be in contango which generates positive returns as bond prices rise w lower yields. You can generate positive carry when the curve is in backwardation by rolling down the curve and buying the cheaper next month contract.

Equity index forward curves are now in contango as forwards are at a premium since interest rates > dividends by a large margin. This makes it attractive to continually short the front month contract. This also means calls are overpriced relative to puts.




**Central Banks**
Central banks - by keeping rates low - can cause excess credit to Build and create bubbles (obvs)

They increase credit by:

Directly lending (primary - lending 1-28 days and secondary - for troubled banks thru discount window 

Open market purchase of treasuries 

Repos - collateraized loans made to primary dealers - collateral something like treasuries 

Central banks raising rates at a time of high leverage frequently leads to sell offs (duh)


**Dispersion**
When vol is low like in 2017, looks for dispersion trades bc correlation is low 

Index is pinned so constituents needs to move
