
[[Gamma]]
- If delta hedged, long gamma means you will gain whether the underlying increases or decreases, everything else equal
- theta represents the cost of this optionality 

Second Leg Down [[Hari Krishnan]]

Deeply [[OTM]] Options (10 [[delta]] for example)
It often makes sense to buy deeply OTM options even though they’re likely to expire worthless. If the underlying moves 30pct towards the strike, what seemed unlikely will seem possible and there will be a rush to buy them, causing them to outperform higher delta nearer struck options. You could combine that with selling the further ITM options which may be overpriced. The spread trade lets you neutralize the volatility. 

Short-time frame Options
Weekly options may be useful for hedging as you’re not overpaying for volatility (after a move already occurred). 

Trend Following
Trend following slightly diversifies as isn’t correlated w volatility.

Realized vol vs [[Implied vol]]
Delta hedging a short option is guaranteed to make profits When realized volatility is below implied. However, infrequent big moves can make it hard to get filled and blow up the hedge. It’s often better to hedge an option with another option to truncate the blow up risk. Having a trade with bounded downside is easier to maintain and often easier to extract alpha from.

  

[[Vol surface]]

Short term market shocks may cause term structure of vol to invert, though this is normally temporary and the curve is generally upward sloping. Short term vol tends to have much higher beta then long term. For example if we regress different expiry ATM implied vol to 3m ATM vol and graph the betas against the time to maturity, it’s downward sloping and convex.

That is 1 week ATM vol is high and it rapidly comes down as maturity increases. For longer dated options, skew is much flatter— that is OTM implied vol isn’t much higher than ATM.

The focus of vol surface modeling should be to determine what strikes/maturities will move the most with a change in the underlying. Figure out which parts are most in need of hedging and/or will give the most bang for your buck.

[[Option skew]]
Risky assets like equity indices or risk on currencies tend to have put skew - that is, more demand for OTM puts. Treasuries can exhibit put skew (at times with inflation) and call skew during risk on when there’s flight to quality. Risk reversal skew tracks the difference in IV between an OTM put and an OTM call. This is related to the risk reversal option structure, that is, a short put plus a long call. If the RR put skew is steep (and you’re bullish) you might short the put (which has high IV and may be overpriced) and buy the call. 

Equity indices have put skew even if the constituents have a call skew. Due to correlation, volatility of the index may be larger than the components. Hence, higher correlation leads to higher put skew, and the implied correlation can be determined from the correlation. 

**Short Vol Trades**
Batman - combines a call ratio spread with a put ratio spread, or can be thought of as a long straddle with a short strangle. This does okay with moderate moves in either direction, but fails in either extreme. 

Calendar spreads - long gamma/short vega. Long near term put vs short long-term put.  Exposed to the risk that the vol term structure steepens without the underling moving.  


**Skew trades:**
Bullish / short skew - 
When put skew is steep you may put on a 1:2 ratio spread. This is a long ATM (50 delta) put and 2 short 25 delta puts. This will be delta neutral and take advantage of the expensive OTM puts. This is a bullish trade as the short puts will appreciate if the market drops sharply. This trade initially has positive time decay (that is you’re long theta) until just before expiry. If nothing happens you also benefit from a flattening of the skew. However you are exposed to large downside shocks. The trade has large negative Vega and is exposed to a sharp sell off with rising vol (and further skew steepening). A ladder is similar to a ratio by the two short legs are set at different strikes. **The large Vega means the trade may be a good short if you want to hedge against extreme downside shocks.**

Bearish / short skew - 
A [[fly]] structure combines a ratio with a further OTM long put to cap the downside. This structure gets cheaper as vol increases and as skew steepens. Hence, this structure makes sense after vol is already elevated. The trade is net negative [[vega]] initally since the small vega on the OTM put doesn't compensate for the two short puts. It gets cheaper with higher skew as the OTM put's cost doesn't offset the other strikes. The vega of the OTM strikes rapidly declines as time goes on. So assuming no change in underlying, the vega increases over time (due to the two short puts) making the structure more defensive. This continues until right before expiry. 

The catch to the fly is that initially it isn't much of a hedge (due to negative vega). It makes sense if you don't know when the move will come but don't think it'll come right away. It's similar to an iron butterfly, except that the latter is long skew (by being long OTM options). The fly should be short skew, allowing you to take advantage of elevated skew post the first draw down. 