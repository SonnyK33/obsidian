Type: #molecule 
References: [[Edge]]

If you view long credit trades as short puts struck against at the amount of debt through the tranche, you can make various analogies between credit and option risk metrics.

**Theta/Short Duration Yield**
For a very short term option theta is very high, and it decays rapidity into maturity. Similarly a short term bond has very high yield to maturity if trading below par

**Bond Duration vs Option Vega**
At first glance, delta and gamma are similar to duration and convexity. However, while long maturity bonds have more convexity,  long term options have less gamma. That’s because in the Merton model, the underlying isn’t interest rates but the issuer's asset value. If you think of spread as a measure of volatility of the underlying asset, the analogy works. Longer dated options have more Vega. For a bond, higher vol equates to higher yield and will lower the bond price by more than a short dated bond. So bond duration is captured by vega not delta. Convexity would be captured by Volga (the second partial with respect to volatility) 

Check if Volga higher for longer dates options ?
Maybe duration should be thought of like delta. But a given deterioration of business will raise yields more than an improvement will lower yields. So in that way owning the bond (short the put) is negative convexity/gamma.



I convert credit trades to option trades to better understand the risk I'm taking. In the below examples, "carry" should refer to current yield and not YTM. YTM is annualzing carry and gives too much credit for short-term returns. All trades can be broken into:
1) A long risk position is a short put where you're getting paid carry to take JTD (asymmetric) risk. 
2) A short risk position is a long put where you're paying carry for the possibility of JTD (asymmetric returns). 
3)  A steepener (short back-end versus long front-end). JTD will likely be negative (front-end will be trading at a higher cash price then back-end) but is defined. In a non-distressed credit, the yield curve will be upward sloping, so a steepener will be negative carry.  This is like a calender spread where you're short a near-term put and long a long-term put. That would be negative gamma and long vega. When does this make sense?

	In a distressed credit, the yield curve will be inverted. A steepener is betting on normalization. Carry will depend on the relative cash prices. It makes sense to be negative gamma here (because the credit is already inverted and so the gains from gamma have already been realized) and long vega
6) Flattener
7) Compression
8) Decompression
9) RV across different credits 