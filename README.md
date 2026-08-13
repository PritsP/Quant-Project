# Project 1: Volatility Surface Construction, Arbitrage Detection, and Delta Hedging Simulation

## Project Overview
In this project, I built a version of the core tools that options traders use every day with real SPY options data. Starting from scratch, I first implemented the Black-Scholes pricing model and an implied volatility solver to extract the market’s expectation of future volatility from the observed option prices. From there, I constructed a map of the implied volatility across every strike price and expiry date. This revealed two clear market structures, being the put skew and the term structure. I then tested the volatility surface for arbitrage violations across three different independent checks: a put-call parity, butterfly spreads, and calendar spreads. My findings were that every violation that I found was explained away by dividend modeling assumptions or transaction costs rather than actual market inefficiency. Finally, I simulated dynamic delta hedging on a real option using historical price data. This demonstrated the gamma-theta tradeoff in practice and shows how hedging frequency directly impacts both profit and loss stability and transactions costs. For this project, I had Claude create a week by week plan and provide me with relevant readings. I also used Claude as an assistant to ask questions that I had throughout the week while working on the project. 

## Data Sources
- CBOE end-of-day options chains (cboe.com/delayed_quotes)
- Underlying price history via yfinance
- Risk-free rate from FRED (3-month Treasury yield)

## Project Structure
- `/data` — raw and cleaned options data
- `/src` — core Python modules (BSM pricing, IV solver, surface construction)
- `/notebooks` — analysis and visualization notebooks
- `/tests` — sanity checks on pricing functions

## Readings
- Hull "Options, Futures and Other Derivatives" Chapter 15 (Black-Scholes-Merton) and Chapter 19 (Greeks)
- Black & Scholes (1973) original paper
- Gatheral (2004) "A Parsimonious Arbitrage-Free Implied Volatility Parameterization" sections 1-3
- Derman & Kani (1994) "Riding on a Smile"
- Breeden & Litzenberger (1978) "Prices of State-Contingent Claims Implicit in Option Prices" skimmed
- Carr & Madan (2001) "Towards a Theory of Volatility Trading" sections 1-2
- Hull Chapter 19 "The Greek Letters" gamma and theta sections
- Wilmott "Paul Wilmott on Quantitative Finance" Chapter 7
- Carr & Wu (2004) "Variance Risk Premia"
- Natenberg "Option Volatility and Pricing" Chapters 1-4

## Status
Complete
