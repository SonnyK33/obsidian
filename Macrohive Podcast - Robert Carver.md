Type: #source 
Referenes: [[Algorthmic Trading]]

[[To Read - Outline]]
Systematic Trading 

He starts with using same trading rules for all assets; this allows him to expand trading universe quickly. The second step is to underweight rules that lead to more frequent trading for those securities that have high transaction costs (eg Eurobonds are expensive, S&P is cheap). Lowering transaction costs (that is by less frequent trading) may be the best way to generate sustainable returns. However, if you don't trade enough, holding costs can start to weigh on returns. 

Avoid in sample bias - for example, using 20 yrs of history to get a model and then backtesting on previous periods within that 20 years. You wouldn’t of had 20 yrs of forward looking data. Should just one year at a time and then an expanding window 

It may make sense to use a blend of models even if one looks a little better, as the difference may not be statistically significant.
  
**Momentum strategies**

Prefers moving averages to looking at 1yr or 3m returns because the latter is very sensitive to starting and ending points. Moving averages, especially exponentially moving averages smooths returns and has fewer trades and hence improves costs. He likes momentum because it works - people don’t sell winners or buy cheap assets. Momentum tends to have a positive skew - small losses and big winners. You don’t need stop losses with momentum since you exit when the market moves. He tracks momentum on different periods simultaneously - 1m, 3m 12m, but would overweight shorter windows for S&P and longer ones for Eurodollars because they’re more expensive to trade. 

  
Combines momentum with carry strategies which should be uncorrelated. He will have multiple carry trades on - sizing inversely proportional to risk (std dev of returns). He doesn't use prevoius max drawdown as only risk measure as may just have not seen how bad it can get yet.

  
**Mean Reversion**
Tends to work for multi year periods or a few days. It may work to buy things that just had a negative skew over last few months and sell the positive skew. Positive skew means it made a lot/lost a little (eg. energy in 2022). Measures skew as third moment and uses direction for trade signal. 

Vol is used to size trades not determine whether to buy or sell. Skew trade may work better for non-equities eg vix which is mean reverting by definition. Doesn’t try to compete w quant firms in the very short horizons. Longer horizon trading based more on human psychology which hasn’t changed. Not into fancy ML instead focuses on strategies that have worked for centuries. Focus on limiting trading costs and not over fitting, should be able to harvest risk premia. Focus on dollars of pnl not percentages . Recommends book by Robert bass on systematic trading.

