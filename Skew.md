Type: #Atom 
References: [[Second Leg Down - WIP]] [[delta]] [[vega]]
[https://twitter.com/pat_hennessy/status/1583187292276940800?s=21](https://twitter.com/pat_hennessy/status/1583187292276940800?s=21)


Option skew is the difference in implied volatility for varying strikes of calls and puts for the same underlying. The x-axis are strikes (moneyness or delta), and the y-axis are implied volatilities. For most risk assets (e.g. equities), the skew is inverted--implied volatilities are higher for lower strikes than for higher strikes. This reflects the excess demand for puts over calls, which results from investors' desire to hedge naturally long positions. Treasuries may exhbit put skew if investors are worried about inflation or call skew if there's a flight to quality. Commodities like oil may show a more symmetrical smile due to demand for high strikes (e.g. consumers of oil) and for low strikes (e.g. producers of oil).

Equity indices have put skew even if the constituents have a call skew. Due to correlation, volatility of the index may be larger than the components. Hence, higher correlation leads to higher put skew, and the implied correlation can be determined from the correlation. 

There are different measures for skew. For example, risk reversal skew tracks the difference in IV between an OTM put and an OTM call (frequently 25D for each). This is related to the risk reversal option structure, that is, a short put plus a long call. If the RR put skew is steep (and you’re bullish) you might short the put (which has high IV and may be overpriced) and buy the call. 

During risk-off periods, there is typically more demand for puts and hence the skew further inverts (or steepens). A trade which benefits from demand for tail hedges exceeding lower strikes is long-skew. 


**RV trades**
_Deeply OTM Options (10 delta for example)_
It often makes sense to buy deeply OTM options even though they’re likely to expire worthless. If the underlying moves 30pct towards the strike, what seemed unlikely will seem possible and there will be a rush to buy them, causing them to outperform higher delta nearer struck options. You could combine that with selling the further ITM options which may be overpriced. The spread trade lets you neutralize the volatility. 

*Bullish / short skew*  
When put skew is steep you may put on a 1:2 ratio spread. This is a long ATM (50 delta) put and 2 short 25 delta puts. This will be delta neutral and take advantage of the expensive OTM puts. This is a bullish trade as the short puts will appreciate if the market drops sharply. This trade initially has positive time decay (that is you’re long theta) until just before expiry. If nothing happens you also benefit from a flattening of the skew. However you are exposed to large downside shocks. The trade has large negative Vega and is exposed to a sharp sell off with rising vol (and further skew steepening). A ladder is similar to a ratio by the two short legs are set at different strikes. **The large Vega means the trade may be a good short if you want to hedge against extreme downside shocks.**

*Bearish / short skew* 
A fly structure combines a ratio with a further OTM long put to cap the downside. This structure gets cheaper as vol increases and as skew steepens. Hence, this structure makes sense after vol is already elevated. The trade is net negative vega initally since the small vega on the OTM put doesn't compensate for the two short puts. It gets cheaper with higher skew as the OTM put's cost doesn't offset the other strikes. The vega of the OTM strikes rapidly declines as time goes on. So assuming no change in underlying, the vega increases over time (due to the two short puts) making the structure more defensive. This continues until right before expiry. 

The catch to the fly is that initially it isn't much of a hedge (due to negative vega). It makes sense if you don't know when the move will come but don't think it'll come right away. It's similar to an iron butterfly, except that the latter is long skew (by being long OTM options). The fly should be short skew, allowing you to take advantage of elevated skew post the first draw down. 

*Long Skew*
Selling 1:2 put ratios - ie selling 25 delta put and buying 2x 10 delta puts assumes that moderately OTM puts are relatively overpriced. That is, investors are overestimating risk of moderate loss. An increase in vol disproportionately benefits the further OTM long put as does a steepening of the skew. The payoff is negative if losses are moderate, but extreme downside is hedged.

Skew is currently historically flat. Forward prices are also at an unusually high premium since interest rates > Div yields. This is making collars much more attractive. You can sell a 4150 call, and buy a 3300 put and receive $6.. for oct 23. With a higher skew you’d normally have to pay for that collar or accept a lower put strike.





Sometimes you see call skew with treasury yields.

Even if you have positive average returns, large drawdowns can cause you to decay towards zero. For example +50pct followed by -45pxt will veer towards zero.

May do a short 25delta put vs 2.5 long OTM puts to stay delta neutral