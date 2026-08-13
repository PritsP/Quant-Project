# Project 1: Volatility Surface Construction, Arbitrage Detection, and Delta Hedging Simulation

## Project Overview
Project 1 builds the complete analytical toolkit of an options market maker using real SPY options data. Starting from scratch, I implemented the Black-Scholes pricing model and an implied volatility solver to extract the market's expectation of future volatility from observed option prices. From there I constructed a full volatility surface — a map of implied volatility across every strike price and expiry date — revealing two clear market structures: the put skew, where crash protection is consistently more expensive than upside speculation, and the term structure, where uncertainty grows with time. I then tested the surface for arbitrage violations across three independent checks — put-call parity, butterfly spreads, and calendar spreads — finding that every apparent violation was explained by dividend modeling assumptions or transaction costs rather than genuine market inefficiency. Finally I simulated dynamic delta hedging on a real option using historical price data, demonstrating the gamma-theta tradeoff in practice and showing that hedging frequency directly impacts both P&L stability and transaction costs.

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
