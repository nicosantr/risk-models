# Financial Risk Models

Risk models I built in Excel covering climate-financial risk, Monte Carlo simulation, and Value-at-Risk.

## Climate Risk

**Gulf Coast Flood EAL Model** — `climate-risk/EAL_model_Louisiana.xlsx`

Expected Annual Loss model for Louisiana natural gas power plants exposed to flood hazard. Built with real data from FEMA's National Risk Index (filtered to 64 Louisiana parishes), EIA-860 power plant database (55 LA gas plants with MW capacity), and USACE depth-damage curves for industrial structures.

What it does:
- Calculates asset-level EAL from flood hazard using return period probabilities and depth-damage functions
- Runs 10,000 Monte Carlo simulations calibrated to climate-adjusted EAL
- Compares results under RCP 4.5 and RCP 8.5 climate scenarios
- Includes a Resilience ROI tab comparing mitigation cost against avoided losses
- Validates output against FEMA NRI parish-level flood EAL benchmarks

I built this in New Orleans, where the financial cost of mispriced flood risk is not theoretical.

**Data Center Heat Stress OPEX Model** — `climate-risk/DataCenter_HeatStress_OPEX.xlsx`

Projects how rising temperatures increase cooling costs for data centers in Phoenix, Houston, and Atlanta over 20 years under RCP 4.5 and RCP 8.5. Uses EIA commercial electricity rates, Uptime Institute PUE benchmarks, and NOAA temperature projections.

What it does:
- Models year-by-year cooling OPEX with temperature-driven cost increases and rate escalation
- Compares three locations side by side under two climate scenarios
- Ranks locations by a "climate-only premium" that isolates the warming signal from rate inflation
- Includes a sensitivity table flexing the cost-per-degree assumption from 1% to 5%

The counterintuitive finding: Atlanta has the lowest baseline costs but the highest climate-driven cost growth, making it the most exposed location on a relative basis.

FYI — I used Claude to help with formula construction and data cleaning across these models. The methodology, assumptions, and structure are my work.

## Equity Risk

**Palantir & Oracle VaR** — `equity-risk/PLNTR-ORCL-VaR.xlsx`

Monte Carlo Value-at-Risk models using 10,000 simulations on log-normal returns. Outputs include 95% VaR, CVaR (expected shortfall), Student's t-VaR for fat-tail adjustment, historical simulation comparison, and a two-stock portfolio VaR with diversification benefit analysis. Built these first to learn the simulation methodology, then applied the same framework to physical climate risk in the models above.

## Data Sources

- FEMA National Risk Index — hazards.fema.gov/nri
- EIA-860 Plant and Generator Data — eia.gov/electricity/data/eia860
- EIA Electric Power Monthly (commercial rates) — eia.gov/electricity/monthly
- USACE Depth-Damage Functions (via FEMA HAZUS Technical Manual)
- Uptime Institute Global Data Center Survey 2025 (PUE benchmarks)
- NOAA Climate Explorer — crt-climate-explorer.nemac.org
- Yahoo Finance (historical equity prices)

## Tools

Excel (primary), Claude (formula construction and data cleaning), working toward Python

## About

Nicolas Rodriguez
Master of Management in Energy — Tulane University (Fall 2026)
nicosantr@gmail.com
