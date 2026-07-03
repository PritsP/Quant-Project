# Volatility Surface Construction & Arbitrage Detection

## Project Overview
Building an implied volatility surface from real SPY/SPX options data, 
testing it for static arbitrage violations, and simulating delta-hedging 
P&L to connect the surface to practical market-making mechanics.

## Data Sources
- CBOE end-of-day options chains (cboe.com/delayed_quotes)
- Underlying price history via yfinance
- Risk-free rate from FRED (3-month Treasury yield)

## Project Structure
- `/data` — raw and cleaned options data
- `/src` — core Python modules (BSM pricing, IV solver, surface construction)
- `/notebooks` — analysis and visualization notebooks
- `/tests` — sanity checks on pricing functions

## Status
Week 1 complete: BSM implementation + implied vol solver


Week 2 in progress: Volatility Surface Construction — Spline Interpolation and SVI Parameterization
