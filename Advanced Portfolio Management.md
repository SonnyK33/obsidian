Author: Giuseppe Paleologo
References: [[Laws of Trading]]

This book is about turning investment ideas into trades. This is how the author describes portfolio management and risk management. There’s some parallels with [[Laws of Trading]]. Decompose your risks and understand the ones you are taking. Hedge the rest. You need to understand the limits of your knowledge. The goal is to forecast pervasive returns not company specific ones. You want to find many sources of returns that have a common explanatory factor. You need to understand these factors and hence the environment you’re operating in. That’ll help separate the issuer from the environment and isolate the risks you want to take.   

After you do your fundamental work, use forecasted returns to size positions. When looking at the overall portfolio, what risks are you taking? What factor risks and what idiosyncratic risks? Strive to decrease and balance factor risks. When measuring performance, separate selection (your best), from timing (your worst), and sizing. If you want to be long/short a certain factor, that's fine, but be aware of it, and ensure it's the most liquid way of doing it. 


**Tour of risk** 

*Single factor model* 

This separates returns into alpha and beta x market returns. Alpha is the job of the fundamental analyst, beta and epsilon (error term) that of the quant, and m is job of macro analyst. There are various sources of alpha, and these are your day job. Besides the obvious (modeling FCF, etc), there’s liquidity and crowding (how consensus is your trade and what’ll be the reaction If the mood shifts?). In [[The Laws of Trading]], these would be the costs associated with your edge. 

Decompose portfolio into idiosyncratic and market returns. Regress positions against the market (HYG for HY bonds) to get the betas and idiosyncratic returns. Get volatilities for bonds and the idiosyncratic factors. You can then derive expected losses on portfolio and attribute them to market and idiosyncratic factors. Multi factor model takes this one step further and attributes risk to other non-market factors. Forecast different market returns and use that to forecast returns attributable to market.   

**Potential factors**

Econ environment, industries (e.g. GICS).

Beta/volatility/profitability - high beta/vol tends to be negative factor. That is, exposure to these stocks is expected to lead to losses. It could be because high vol stocks are in demand by investors and are overpriced. Optionality is expensive. Managers may like them because of potential idiosyncratic returns, but you must be aware of the costs incurred. The opposite is true for the profitability factor. 

Trading environment, Short interest, and Active manager holdings to get long/crowded bias are other factors.

Momentum has a pattern. Performance in the last month mean reverts (even more for last week). For one month to a year, there’s continuation. Beyond a year, it reverts again. This may be explained by multiple loops at work [[Laws of Trading]]. The market-maker is always selling volatility, and at some point, expects the trade to mean revert. 

When a momentum factor underperforms, it tends to be on the short side. Maybe because the equities are now cheap options and highly sensitive to any positive news.

Long successful positions will eventually have a positive momentum loading so they’re unavoidable. Need to balance the upside of these positions with the risks of the factor. The cost of momentum factor is risk of sudden drawdowns (mostly from short side).

Valuation factors 

Value vs growth can be measured w different ratios p/b, p/s, etc. the difference between value and growth is a key driver of returns. Value is similar to short duration investments where the return is realized quickly. Growth stocks are high duration and derive most value in the future. It’s been shown that the yield curve shape is correlated with value stock returns. High value (ie distressed) tends to outperform. This could be because growth is overestimated for momentum stocks. Or it could be to compensate for the risk you’re taking as value tends to be riskier and more susceptible to earning shocks.  

Value factor could be represented by yield or spread for bonds. 


**Portfolio construction - heuristics for alpha sizing** 

The sharpe ratio is ubiquitous and something you must measure. Tells you if you can apply leverage to magnify returns and how efficient you are with your capital (eg risk) budget. 
Portfolio construction takes expectations about returns, objectives, and risk tolerance and spits out a portfolio. It must be systematic and rules based.  

*Estimating expected returns*

Must express as idiosyncratic returns in expectation over common investment horizon for all positions. Views should be based on idiosyncratic returns; is a given trade an industry, style (eg value) or country bet? 

When you have an estimated return, think about it relative to the sector. You want to neutralize factors with different positions. Alpha is what’s left. Expectation means weighted average of all scenarios. Scale positions to one time horizon.

*Sizing* 

A simple rule where positions are held proportional to their expected returns is simple and may be better than various mean variance or risk parity rule. Scale the GMV so that dollar idio volatility matches a target. This vol targeting leads to better risk adjusted returns. Portfolios with many positions (more than 50 stocks) shouldn’t have large factor exposures as you unlikely have edge in factors. They’re unavoidable but you should at least be aware. Factors models also let you separate risk into idio and systematic.

*Portfolio risk decomposition* 

Break portfolio into idio and factor risk. Further decompose factor risk into style and industry factors. For each factor you should see how much variance it adds to the portfolio, dollar exposure, volatility dollars, and marginal contribution to factor risk. And for each position, see the margin factor risk it adds, and decide whether to add or reduce. You can then manage this factor risk and change as needed. You should know these for your portfolio. 
For new positions should be able to plug them into model and get these stats. That’ll tell whether to add or reduce.   

*Tactical portfolio construction*

Get your fundamental theses. Convert into positions by weighting by expected return. Perform the above decomposition, and examine factor and idio split. If idio risk is too low, determine which factor risk is too high. You should have single factor exposures. Find trades inline with convictions that reduce factor risk. These should be in line with objectives for reducing or increasing gross market value. Tactical adjustments are necessary as the market moves. You typically want to minimize trading costs subject to max factor risk and a min GMV.  

*How much factor risk should you take?*

Most managers have no skill in factors. If you assume all PnL comes from idio factors, you want to keep idio variance as a pct of total as high as possible. Above 75pct you have diminishing returns though dude to trading costs and limited accuracy of models. Rule of thumb is lowering share by 5pct cuts returns by 2.5pct. Your sharpe ratio decreases with factor risk. The higher your sharpe, the less market exposure you want - see book for calculation. The more stocks you can own the easier it is to be market neutral. I’m not sure the same can be said for bonds. That is, it could be tougher to run market neutral. 
Factor exposure should be minimized but it’s hard to keep it at zero. Keep exposures within a range and Be mindful of where they could go. Ie how much could energy widen?  

*Understand your performance* 

Idio performance can be broken into sizing, selection, and timing. Assess skill in sizing by comparing your portfolio sharpe to that of an equally weighted portfolio. Do this for whole portfolio as well as for short and long books separately. Timing skill can be measured similarly by comparing performance against a portfolio which has consistent positions across dates. So idio skill is broken part by looking at simpler and simpler portfolios. Selection skill is the residual. Typically fundamental investors are best at selection, bad at timing, and mediocre at sizing. Diversification should be a skill multiplier. If hit rate is above 50, a larger breadth will increase information ratio. In reality though as breadth increases, hit rate often falls. 

Have a strategy for trading events, particularly earnings for your stuff.

All funds have a stop loss whether it’s explicit or not. Better make it transparent. It offsets the PM’s call option by encouraging a decrease in volatility. The downside is a loss in efficiency as you lose out on the recovery. This hurts lower sharpe ratio trades/PM more. A stop loss strategy should this be set based on that trade off. How high is your sharpe and what kind of efficiency are you okay losing?