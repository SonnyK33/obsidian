Type: #Atom 

References: [[Options - Outline]]
[https://twitter.com/bennpeifert/status/1572019785797603328?s=51&t=BWxHJcs4NTmr41flqp71Lg](https://twitter.com/bennpeifert/status/1572019785797603328?s=51&t=BWxHJcs4NTmr41flqp71Lg)

Theta shouldn't be viewed as carry but as compensation for taking non-symmetrical risks.
For example for every unit of time, you get theta, but lose with changes in the underlying and in volatility. In big moves of the underlying, you lose a lot from gamma (0.5 x gamma^2). If the option is far from ATM, and ivol moves a lot, you lose a lot from volga (0.5 x vega ^2) as well.  
You also have vanna exposure (which is another way of looking at skew or the relationship between spot and vol).
e.g. if you sell a put and the underlying falls, ivol may also rise. You'll lose again from this interaction - i.e. vanna. 

if you only consider sigma, t, and x (underlying); V = V(sigma, t, x)
dV(sigma, t, x) = dV/dt x dt + dV/disgma x dsigma + dV/dx x dx
                          + 0.5 x d^2/dsigma^2 x dsigma^2
                          + 0.5 x d^2/dx^2 x dx^2
                          + d^2/dsigma dx x disgma dx
if dt=1 then higher order terms can be ignored and are captured in theta anyways
dV = theta + vega * dsigma + delta x dx + 0.5x volga x dsigma^2 + 0.5 x gamma x dx^2
+ +vanna x disgma dx

If you're short an option, as these variables move, you can lock in the losses by dynamic hedging. If you don't hedge, those losses are accumulating and you're making continuous double or nothing bets (martingales) that the moves will reverse. 

When selling an option (i.e. earning the VRP), need to decide if gamma,  volga, and vanna are overpriced. If they are, then the theta should exceed the losses from those exposures.

[[To Read - Outline]]
- vol roll down - ivol on OTM options will rapidly increase as you get close to maturity (even with no changes to underlying)
- means that a short option won't decay as quickly as you think (or as fast as theta implies)
- what risk measure captures this?