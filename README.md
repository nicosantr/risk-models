# Risk Models

A few financial risk models I built in Excel while teaching myself VaR, Monte Carlo simulation, and climate risk modeling.

## What's here

**Gulf Coast Flood EAL Model** (`EAL_model_Louisiana.xlsx`)

This is the main one. It estimates the Expected Annual Loss from flooding for natural gas power plants on the Louisiana Gulf Coast. I used real data from FEMA's National Risk Index and the EIA-860 power plant database, and applied USACE depth-damage curves to estimate financial impact at the asset level.

The model runs 10,000 Monte Carlo simulations calibrated to climate-adjusted EAL, and includes a resilience ROI tab that compares mitigation cost against avoided losses. There's also an RCP 4.5 vs RCP 8.5 scenario toggle so you can see how EAL shifts under different climate pathways.

I built this because I live in New Orleans and wanted to understand the financial side of flood risk — not just that it exists, but what it actually costs.

**Equity VaR Models** (`PLTR_VaR_MonteCarlo.xlsx`, `ORCL_VaR_MonteCarlo.xlsx`)

Monte Carlo Value-at-Risk simulations on Palantir and Oracle. 10,000 simulations each using log-normal returns. Outputs include VaR at 95%, CVaR (expected shortfall), and a loss distribution. These were the first models I built while learning the methodology — the EAL model applies the same Monte Carlo framework to physical climate risk instead of equity returns.

## Data sources

- FEMA National Risk Index (county-level hazard EAL data)
- EIA-860 Schedule 2 and Schedule 3 (power plant locations and generator capacity)
- USACE depth-damage functions for commercial/industrial structures
- Yahoo Finance (historical equity prices for VaR models)

## About me

I'm Nicolas Rodriguez — incoming master's student at Tulane's Freeman School of Business in the Master of Management in Energy program. Background in finance, energy markets, and commodities. Based in New Orleans.

nicosantr@gmail.com
