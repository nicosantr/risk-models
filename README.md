# Financial Risk Models

Risk models I built in Excel covering climate-financial risk, Monte Carlo simulation, and Value-at-Risk.

## Climate Risk

**Gulf Coast Flood EAL Model** — `climate-risk/EAL_model_LouisianaV3.xlsx`

Expected Annual Loss model for Louisiana natural gas power plants exposed to flood hazard. Built with real data from FEMA's National Risk Index (filtered to 64 Louisiana parishes), EIA-860 power plant database (55 LA gas plants with MW capacity), and USACE depth-damage curves for industrial structures.

What it does:
- Calculates asset-level EAL from flood hazard using return period probabilities and depth-damage functions
- Runs 10,000 Monte Carlo simulations calibrated to climate-adjusted EAL
- Compares results under RCP 4.5 and RCP 8.5 climate scenarios
- Includes a Resilience ROI tab comparing mitigation cost against avoided losses
- Validates output against FEMA NRI parish-level flood EAL benchmarks

I built this in New Orleans, where the financial cost of mispriced flood risk is not theoretical.

FYI — the original file was 27MB because it had the full national FEMA and EIA datasets loaded in. I used Claude to strip it down to just the Louisiana data and the model tabs, which brought it to 0.1MB. The model itself and all the formulas are my work.

## Equity Risk

**Palantir VaR** — `equity-risk/PLTR-ORCL-VaR.xlsx`

Monte Carlo Value-at-Risk models using 10,000 simulations on log-normal returns. Outputs include 95% VaR, CVaR (expected shortfall), and loss distribution histograms. Built these first to learn the simulation methodology, then applied the same framework to physical climate risk in the EAL model.

## Data Sources

- FEMA National Risk Index — hazards.fema.gov/nri
- EIA-860 Plant and Generator Data — eia.gov/electricity/data/eia860
- USACE Depth-Damage Functions (via FEMA HAZUS Technical Manual)
- Yahoo Finance (historical equity prices)

## Tools

Excel (primary), Claude (for data cleaning and learning), working toward Python

## About

Nicolas Rodriguez
Master of Management in Energy — Tulane University (Fall 2026)
nicosantr@gmail.com
