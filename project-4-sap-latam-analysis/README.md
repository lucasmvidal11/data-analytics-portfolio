# SAP SE — Investment & Market Analysis

**Is SAP undervalued given its strategic shift to cloud?  
And where should SAP prioritize growth in Latin America?**  
This project answers both questions using financial data, comparable company analysis, 
and a risk-adjusted market opportunity framework.

---

## Key Findings

- SAP trades at **5.02x EV/Revenue** vs peer median of **8.09x** — implying **+61% upside** 
  if valued in line with Oracle, Salesforce, and Microsoft
- On **EV/EBITDA**, SAP is fairly valued (16.2x vs 16.0x peer median) — the discount is 
  purely a revenue multiple story
- SAP's cloud revenue grew from **25% to 44% of total revenue** between 2019 and 2023, 
  at ~18.5% CAGR — the transition is real and accelerating
- In Latam, **Brazil is the clear priority** ($0.55bn risk-adjusted addressable market), 
  followed by Mexico ($0.33bn); Argentina remains high-risk ($0.04bn) but improves 
  significantly under optimistic macro scenarios

---

## Methodology

### Comparable Company Analysis (Comps)
Standard M&A valuation methodology using EV/Revenue and EV/EBITDA multiples across 
4 peers: SAP, Oracle, Salesforce, Microsoft. Data sourced via yfinance API (current).

### Latam Opportunity Framework
Market sizing combines:
- ERP market projections by country (Statista, IDC estimates)
- SAP regional market share estimates (Gartner)
- Risk index from the companion project 
  [Argentina vs Germany Risk Analysis](../project-5-argentina-germany-risk)

Risk-adjusted opportunity = Addressable market × (1 − Risk Index / 100)

### Data Sources
| Dataset | Source |
|---|---|
| Stock prices & financial metrics | yfinance API |
| SAP revenue breakdown | SAP Annual Reports 2019–2023 |
| ERP market size Latam | Statista / IDC |
| SAP regional market share | Gartner |
| Country risk index | Companion project (World Bank + IMF) |

---

## Project Structure
```
sap-latam-analysis/
├── data/
│   ├── prices.csv                  # Daily stock prices 2019–2024
│   ├── financials.csv              # Current valuation multiples
│   ├── sap_revenue.csv             # SAP revenue breakdown 2019–2023
│   ├── comparable_analysis.csv     # Full comps table
│   ├── erp_market.csv              # Latam ERP market size projections
│   ├── sap_regional.csv            # SAP market share by region
│   └── latam_opportunity.csv       # Risk-adjusted opportunity matrix
├── notebooks/
│   ├── 01_data_fetch.ipynb         # Stock prices + financial metrics via yfinance
│   ├── 02_market_analysis.ipynb    # Cloud transition + stock performance
│   ├── 03_valuation.ipynb          # Comparable company analysis + implied valuation
│   ├── 04_latam_opportunity.ipynb  # Latam market sizing + risk adjustment
│   └── 05_recommendation.ipynb    # Investment thesis + final dashboard
└── outputs/
```

## Investment Thesis

SAP is currently **discounted on revenue multiples** relative to peers, reflecting 
market skepticism about the pace of its cloud transition. However, with cloud revenue 
compounding at ~18.5% annually and Latin America representing an underpenetrated 
high-growth region (ERP market CAGR 9.3%), SAP offers a compelling risk-adjusted 
opportunity. Brazil and Mexico provide near-term addressable markets with manageable 
risk profiles, while Argentina represents a high-volatility, high-upside option 
contingent on macroeconomic stabilization under the Milei reform agenda.

---

## Tech Stack

- **Python** — Pandas, Plotly, yfinance
- **Data Sources** — yfinance API, SAP Annual Reports, Statista, IDC, Gartner
- **Visualization** — Interactive Plotly dashboards

---

## Related Project

This analysis uses the country risk index developed in:  
[Argentina vs Germany — Investment Risk Analysis](../project-5-argentina-germany-risk)

---

## Author

**Lucas Mesa Vidal**  
Double Degree BSc International Management — Hochschule Karlsruhe & Universidad Nacional del Litoral  
Specialization: Finance & Data Analytics  
[LinkedIn](https://linkedin.com/in/lucasmesavidal) · [Portfolio](https://lucasmvidal11.github.io/data-analytics-portfolio)
