Author:  Hari Krishnan
Type: #source #book
Topics: #volatility #trading #systematic
References: [[Monetary Tightening - 2022]]

Summary:


Atoms:
**skew and RV trades**
Deeply [[OTM]] Options (10 [[delta]] for example)
It often makes sense to buy deeply OTM options even though they’re likely to expire worthless. If the underlying moves 30pct towards the strike, what seemed unlikely will seem possible and there will be a rush to buy them, causing them to outperform higher delta nearer struck options. You could combine that with selling the further ITM options which may be overpriced. The spread trade lets you neutralize the volatility. 


Risky assets like equity indices or risk on currencies tend to have put skew - that is, more demand for OTM puts. Treasuries can exhibit put skew (at times with inflation) and call skew during risk on when there’s flight to quality. Risk reversal skew tracks the difference in IV between an OTM put and an OTM call. This is related to the risk reversal option structure, that is, a short put plus a long call. If the RR put skew is steep (and you’re bullish) you might short the put (which has high IV and may be overpriced) and buy the call. 

Equity indices have put skew even if the constituents have a call skew. Due to correlation, volatility of the index may be larger than the components. Hence, higher correlation leads to higher put skew, and the implied correlation can be determined from the correlation. 


Bullish / short skew - 
When put skew is steep you may put on a 1:2 ratio spread. This is a long ATM (50 delta) put and 2 short 25 delta puts. This will be delta neutral and take advantage of the expensive OTM puts. This is a bullish trade as the short puts will appreciate if the market drops sharply. This trade initially has positive time decay (that is you’re long theta) until just before expiry. If nothing happens you also benefit from a flattening of the skew. However you are exposed to large downside shocks. The trade has large negative Vega and is exposed to a sharp sell off with rising vol (and further skew steepening). A ladder is similar to a ratio by the two short legs are set at different strikes. **The large Vega means the trade may be a good short if you want to hedge against extreme downside shocks.**

Bearish / short skew - 
A [[fly]] structure combines a ratio with a further OTM long put to cap the downside. This structure gets cheaper as vol increases and as skew steepens. Hence, this structure makes sense after vol is already elevated. The trade is net negative [[vega]] initally since the small vega on the OTM put doesn't compensate for the two short puts. It gets cheaper with higher skew as the OTM put's cost doesn't offset the other strikes. The vega of the OTM strikes rapidly declines as time goes on. So assuming no change in underlying, the vega increases over time (due to the two short puts) making the structure more defensive. This continues until right before expiry. 

The catch to the fly is that initially it isn't much of a hedge (due to negative vega). It makes sense if you don't know when the move will come but don't think it'll come right away. It's similar to an iron butterfly, except that the latter is long skew (by being long OTM options). The fly should be short skew, allowing you to take advantage of elevated skew post the first draw down. 

Selling 1:2 put ratios - ie selling 25 delta put and buying 2x 10 delta puts assumes that moderately OTM puts are relatively overpriced. That is, investors are overestimating risk of moderate loss. An increase in vol disproportionately benefits the further OTM long put as does a steepening of the skew. The payoff is negative if losses are moderate, but extreme downside is hedged.

Skew is currently historically flat. Forward prices are also at an unusually high premium since interest rates > Div yields. This is making collars much more attractive. You can sell a 4150 call, and buy a 3300 put and receive $6.. for oct 23. With a higher skew you’d normally have to pay for that collar or accept a lower put strike.

Source - 

[https://twitter.com/pat_hennessy/status/1583187292276940800?s=21](https://twitter.com/pat_hennessy/status/1583187292276940800?s=21)


Sometimes you see call skew with treasury yields.

Even if you have positive average returns, large drawdowns can cause you to decay towards zero. For example +50pct followed by -45pxt will veer towards zero.

May do a short 25delta put vs 2.5 long OTM puts to stay delta neutral

**term structure**

People tend to overpay for medium term puts and there’s likely value in short term (weekly or less) or long term puts. Some statistical studies show that returns have very fat tails for short term horizons (4 or less days), and hence there’s value in buying weekly OTM puts. Since volatility begets more volatility, you can wait for the first move before buying a weekly put. Though time decay is severe, you’re already paying less as most of the heavily decaying days have already occurred.

Vol podcast with Cem

Looks for RV In skew for different term structures 

On risk adjusted basis, skew is highest for 30day period bc that’s a popular timeframe to buy protection 

Looks for RV against that time frame 

When vol is low like in 2017, looks for dispersion trades bc correlation is low 

Index is pinned so constituents needs to move

You can hedge exposure to moves against you with weekly puts after the weekend. They cost more than monthly puts if you continuously roll them (indicating that they offer value and more frequently go ITM).

Long-dated options can also provide value. They have the highest Vega/theta ratio but are not gamma plays the way short-dated options are. Longer-dated options also have much higher rho. Given the effects on forward prices, a cut in dividend helps long-dates call prices. Higher dividends, or lower (r-d) causes the forward curve to move into backwardation, lowering forwards, and benefiting long-dated puts(check this?). After a risk event, long-term vol may still be cheap, especially in other asset classes (when you expect all asset classes to eventually correlate). Short term vol will be high, but Vega on short-term options is low so options may still

Be cheap. So you want to buy long term options before a risk event happens and short term options after a risk event, as a last resort. Weekly options benefit from contagion effects that occur in the short term. They have lots of gamma and are less affected by vol and so they offer value after a move. Long-dated options reprice on sentiment.

Structured products eg those offering yield to retail customers in Japan may rely on long term option writing and hence create opportunities for cheap long term options.

You buy long term options when investors are overly optimistic so you can benefit when sentiment changes. You should check this now. Should also check for the forward to spot premium as this will prob come down.


**IV vs RV**

Realized vol vs [[Implied vol]]
Delta hedging a short option is guaranteed to make profits When realized volatility is below implied. However, infrequent big moves can make it hard to get filled and blow up the hedge. It’s often better to hedge an option with another option to truncate the blow up risk. Having a trade with bounded downside is easier to maintain and often easier to extract alpha from.



**VIX**

The vix is calculated by a weighted average of all outstanding OTM options. Vix spot would be an ideal hedge but it can’t be bought. Vix futures aren’t a long term strategy as the curve is mostly in contango.

Short Vix futures + over buying ATM calls at 1.5x ratio to start delta neutral. If vol falls, you benefit from short position and net negative delta. If vol rises, delta rises and you get convex payouts.

From podcast with Ben (acid capitalist)

  

There’s an intrinsic level that Vix futures can go vs spot SPX vol. beyond that level you’re being paid to take a convex bet

ATM option is best guess for short term RV

Variance swap should be that plus a premium bc has a squared exposure to that so you’re short concvexiry wrt to vol you lose a lot of vol goes up

You lose way more if you’re short a variance swap so you have to be paid for that

So if atm vol is 20, variance swap could be 23

Vix future is a forward on variance swap calc

The way it’s trading, the Vix was implying it would trade at a discount to atm vol 

Can’t trade there bc you could  be getting free convexiry vs vol

From mutiny podcast -22 w Kris

Generates yield w capped short Vega trades -

Selling call spreads on VIX or put spreads on equities in order to fund long gamma trades - long 5 delta puts or calls

Trend following systems can diversify across timeframes. For example multiple moving average crossover systems have little correlation with each other (eg signal from crossing 5d moving avg vs crossing 50d).

VIX trades

When Vix in contango - short/short

Short front month Vix for roll yield and short SandP

Opposite when inverted

Risk is sudden Vix spike, though you normally have a warning due to vol clustering 

Sometimes you benefit when vix goes up and stocks go up or the opposite 

  

Calendar spread - long front month to be long vol but financed w short future month (which gives roll yield) 

Doing this intraday is more capital efficient as most margin requirements are overnight



**post-sell off trades**
Short-time frame Options
Weekly options may be useful for hedging as you’re not overpaying for volatility (after a move already occurred). 

Strategies post a market drop -

- trading reversals ie buying bad closes. Assumes you can buy at the close. Takes advantage of fact that some levered traders may have to sell on a down day, exaggerating the move into a close 

- risk reversal hedged with short futures. Eg short 25d puts + long 25d calls + short futures. Works in a moderate sell off or in a big reversal. Takes advantage of the high skew post sell off and bets that this will decrease. Short downside gamma and long gamma to the upside.

- sell put spreads. Sell 40d put and buy 25d put. Works if market reverses or doesn’t fall too much. Could do this w 4 wk expiry and put on whenever market has a negative weekly return. Signal tends to be on 50pct of the time.

It may be best to only do this when implied vol is high which correlates w higher equity risk premise and higher premiums collected 

- buy VIX puts. Assuming the term structure is in contango, benefits from roll down as forward prices roll down towards the strike. The roll down and mean reversion of vol (after a sell off) tend to compensate for theta. Can also get windfall gains if you called the bottom of the market. Strategy has positive gamma, positive expected value, and bounded risk. Could combine this with far OTM call spreads. This bets that vol won’t stay at an elevated level. It either falls or spikes again. Buying puts may have less expected returns now as skew has steepened (check this).
- sell VIX call spreads. Bets that vol won’t continue rising and exploits fact that level of Vix and implied vol of Vix are highly correlated. Ie when VIX comes down so does IV. Market only accounts for mean reversion once VIX gets high. Assuming markets stabilize, You benefit from negative delta and negative Vega - short Vega on lower strike short call dominates. Market doesn’t have to recover just stop falling. This is a variation on the put/put spread buying strategy. It doesn’t gain from roll down but does from falling IV. Declining vol works against the long put spread esp if curve has inverted. 

  

Trading vol after a big move makes sense since it’s the easiest of the moments to forecast.

This is because it itself exhibits less variance than mean, skew, or kurtosis. Vol is heavily mean reverting and a stationary process (I think?). High levels on the VIX are correlated with subsequent negative returns and shorting the Vix when above 30 tends to work .

  

- can take advantage of this with calendar spreads. When the curve inverts, buy the second month and short the near month. Roll yield is negative since it’s backwardated - you’re betting this is temporary. You’re betting on mean reverting spot volatility and hedging with the future month. This is still exposed to sharp sell offs as near term contract will move a lot more 

  

All of the above are variations on buying dip in risky assets, selling vol, and selling skew. They must be sized appropriately and only work if you didn’t lose too much in the first draw down

Tracking price action and volatility (eg an indicator based on when price and vol exceed 2 standard deviations) is a good indicator of unsustainable price action 


**Other Long-Vol trades**

Trend Following
Trend following slightly diversifies as isn’t correlated w volatility.

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