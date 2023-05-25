Type: #molecule 
References: [[Volatility Machine]]
[[Credit as Option Trades]]
[[Edge]]
This is an explanation of how the Merton model can be used to understand management's incentives and, in turn, for trade construction. 

Management is incentivized with equity and thus thinks like a shareholder. It will want to invest in the business when gains accrue to shareholders, and not creditors. That's when the equity delta exceeds the credit delta. When Assets = Debt, equity is worthless. At this point, both options are ATM with a delta of 0.5. Increases in asset value will accrue 50/50 to equity holders and creditors. As the asset value increases, the equity call goes further ITM and the delta tends towards 1. Management should increasingly want to invest in the business. 

You want to be long the credit (short the put), when you expect the put to decrease in value. This can occur if the asset value is expected to increase or volatility will decrease. At a certain point, the short put becomes a synthetic call (because you also are long a put struck at the next junior layer of debt, and the long put + short ITM put is a synthetic version of a long call position). At this point, your incentives are aligned with management (and equity holders), and you both benefit from more volatility. That's when you want to be long. Otherwise, you may want to be short credit (long the put), as management may want to increase volatility to enhance the call option value. This will be whenever higher vol will increase the option value by more than it will decrease the underlying value. This will be true when intrinsic value is low.
