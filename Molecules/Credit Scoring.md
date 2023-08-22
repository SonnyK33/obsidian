Type: #molecule 

One way of ranking credits across ratings, sectors, and geographies, would be look (downside - upside) divided by the spread. Good shorts would have a highly positive numerator and a small denominator. Good longs would be the opposite. This roughly translates into the Merton model, as the spread is the premium for the put, and the downside - upside is a risk neutral approximation of "upside", from the perspective of a protection buyer (short the credit). If you're short, you want to maximize the potential downside (less the upside which reflects the possibility of being wrong), for every bp of spread that you're paying as carry. 

Related to the upside/downside calculation above, we should score credits by the amount of fixed cost leverage embedded in the capital structure. 

FC / EBITDA (or FCF) will give you the "beta" to a given % change to revenue
e.g. if FC/EBITDA = 30%, every 1% move in revenue will result in a 1% x (1 + 30%) = 1.3% change in EBITDA

if we have upside and downside cases for revenue (if sensitizing quantities, keep gross margin constant; if sensitizing price, variable costs are also fixed), we can translate that into FCF, EV, and even spreads.

% Rev change -> (via above calculation) % FCF change -> % EV change (regardless of EV multiple) --> spread change (depending on the delta of the put i.e. the bond)

The last step will be an approximation. Roughly speaking, a highly distressed credit will have a delta of -1, and so a change in EV should directly map to a change in spreads. You'll need to convert the delta so it can use % changes rather than absolute changes. If the credit is IG, the delta will be near zero, and so this analysis will have limited impact. Other variables include the maturity of the bond. If the put is OTM (i.e. performing), a longer duration bond will have a higher delta. Vice versa for an ITM put (i.e. stressed). 

Using these two together can tell you by how much fixed cost leverage should affect spreads. If FC/FCF doubles, all else equal, the spread should also double, assuming the delta is near -1 (which will be true for stressed credits). If delta is 0.5, it should result in a 50% increase in spreads. I may not be accounting for % change properly with respect to the delta. 