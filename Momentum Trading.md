Type: #Atom 
Sources:
References: [[Stationarity]]

-   securities may exhibit momentum after a new piece of information comes out - i.e. the slow diffusion of new information
-   need to look for evidence of regime change
    -   from mean-reverting to momentum for example
-   time series momentum means past returns are positively correlated w/ future returns
-   Use Hurst exponent and Variance ratio to rule out null hypothesis of random walk
    -   Hurst 0.5 = random walk
    -   > 0.5 = trending market        
    -   <0.5 = mean reverting
-   indicators:
    -   moving averages (e.g. when 50 crosses 200)
    -   Exponential MA
    -   MACD
    -   RSI
-   potential strategies
    -   MACD or MA crosses
        -   close out trade when momentum falls - use low period RSI
            -   e.g. close out trade if 2 day RSI falls < 90 ([](https://medium.com/raposa-technologies/build-a-bot-to-beat-the-bear-market-8a3d715c775c)[https://medium.com/raposa-technologies/build-a-bot-to-beat-the-bear-market-8a3d715c775c](https://medium.com/raposa-technologies/build-a-bot-to-beat-the-bear-market-8a3d715c775c))
-   curve smoothing
    -   moving averages
    -   kernel regression