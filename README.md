# DAX 40 — Financial Performance & Sector Analysis (2019–2023)

**Which DAX 40 sectors recovered fastest post-COVID?  
And which are structurally underperforming?**  
A financial benchmarking analysis of 20 DAX companies across 8 sectors,
combining stock performance, KPI analysis, and sector scoring.

---

## Key Findings

- **Technology** dominates across all metrics — highest gross margins (59.1%),
  highest revenue growth, and near-top ROE (15.4%)
- **Sartorius** delivered the highest total return (+197.5%) — driven by
  COVID-era biotech and lab equipment demand
- **Bayer** was the worst performer (-35.3%) — structural headwinds from
  glyphosate litigation and patent cliff
- **Automotive** faces a structural margin squeeze — lowest gross margins
  (14.2%) and lowest ROE (5.2%) amid EV transition capex pressure
- **COVID recovery was inversely correlated with initial drop** — companies
  that fell hardest (Mercedes -38%, Infineon -30%) recovered fastest

---

## Sector Scorecard

| Sector | Gross Margin | Profit Margin | ROE | Revenue Growth |
|---|---|---|---|---|
| Technology | 59.1% | 13.4% | 15.4% | +3.2% |
| Consumer | 53.3% | 8.3% | 14.6% | +0.2% |
| Chemicals | 47.4% | 3.4% | 2.0% | -2.7% |
| Healthcare | 35.4% | 5.5% | 7.0% | +1.9% |
| Industrials | 31.8% | 7.9% | 12.9% | -3.3% |
| Financials | 20.1% | 14.7% | 15.7% | +1.3% |
| Logistics | 17.5% | 4.2% | 15.6% | -1.9% |
| Automotive | 14.2% | 3.7% | 5.2% | -5.2% |

---

## Methodology

- **Universe:** 20 DAX companies across 8 sectors
- **Period:** January 2019 – December 2023
- **Stock performance:** Indexed to Base 100 (Jan 2019)
- **COVID analysis:** Pre-COVID (Jan 2020) → Trough (Mar 2020) → Recovery (Dec 2021)
- **KPI benchmarking:** Gross margin, profit margin, ROE, EV/EBITDA, revenue growth
- **Sector scoring:** Normalized 0–100 score across 4 KPI dimensions
- **Data source:** yfinance API (current financials + historical prices)

---

## Project Structure
dax40-financial-analysis/
├── data/
│   ├── dax_prices.csv              # Daily stock prices 2019–2024
│   ├── dax_financials.csv          # Current financial metrics
│   ├── dax_financials_clean.csv    # Cleaned and formatted metrics
│   ├── covid_recovery.csv          # COVID drop, recovery, total return
│   └── sector_kpis.csv             # Aggregated KPIs by sector
├── notebooks/
│   ├── 01_data_fetch.ipynb         # Data collection via yfinance
│   ├── 02_sector_analysis.ipynb    # Benchmarking + KPI dashboard
│   └── 03_insights_recommendation.ipynb  # Executive summary + visuals
└── outputs/

## Tech Stack

- **Python** — Pandas, NumPy, Plotly
- **Data Source** — yfinance API
- **Visualization** — Interactive Plotly charts + heatmaps

---

## Related Projects

This analysis complements:
- [Gerresheimer AG — M&A Due Diligence](../project-1-gerresheimer-due-diligence)
  *(Gerresheimer is a DAX-listed pharma packaging company)*
- [SAP SE — Investment & Latam Analysis](../project-4-sap-latam-analysis)
  *(SAP is the top Technology sector performer in this analysis)*

---

## Author

**Lucas Mesa Vidal**  
Double Degree BSc International Management — Hochschule Karlsruhe & Universidad Nacional del Litoral  
Specialization: Finance & Data Analytics  
[LinkedIn](https://linkedin.com/in/lucasmesavidal) · [Portfolio](https://lucasmvidal11.github.io/data-analytics-portfolio)