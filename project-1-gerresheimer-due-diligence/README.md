# Gerresheimer AG — M&A Due Diligence Analysis

**Should a strategic buyer acquire Gerresheimer AG?**  
A data-driven due diligence framework analyzing valuation, financial health,
risk profile, and Latam exposure of a leading German pharma packaging company
undergoing a strategic transformation.

---

## Recommendation: ✅ BUY — Strategic Acquisition Opportunity

Gerresheimer trades at a **significant discount to peers** (1.35x EV/Revenue
vs peer median 2.93x) while delivering consistent margin expansion and
above-market revenue growth. The ongoing "Formula G" transformation from
commodity packaging to high-margin drug delivery systems is the central
value driver.

---

## Valuation Summary

| Method | Implied EV | Upside vs Current |
|---|---|---|
| Current EV | EUR 3.12bn | — |
| EV/Revenue (peer median 2.93x) | EUR 6.80bn | +117.5% |
| EV/EBITDA (peer median 11.60x) | EUR 4.16bn | +33.0% |
| DCF Base Case | — | EUR 58.7/share |
| DCF Bull Case | — | EUR 95.0/share |
| DCF Bear Case | — | EUR 28.9/share |

---

## Key Findings

**Investment Highlights:**
- Revenue CAGR 9.9% (2019–2023) — consistent above-market growth
- EBITDA margin expansion: 20.7% → 25.3% in 4 years
- Pharma packaging: defensive, non-cyclical demand profile
- Drug delivery systems: higher margins + higher switching costs
- Deep valuation discount vs peers on revenue multiples

**Key Risks:**
- Leverage elevated: Net Debt/EBITDA 2.85x (threshold: 3.0x)
- Capex intensity 14.5% of revenue — heavy investment phase
- Formula G execution risk — transformation must deliver
- Latam exposure EUR 41mn risk-adjusted (manageable at 2.1%)

---

## Suggested Acquisition Parameters

| Parameter | Value |
|---|---|
| Entry EV range | EUR 3.5bn – 4.2bn (15–35% premium) |
| Max leverage post-acquisition | 3.5x Net Debt/EBITDA |
| Target synergies | EUR 80–120mn |
| Hold period | 5–7 years |
| Exit multiple | 10–12x EV/EBITDA |

---

## Methodology

### Comparable Company Analysis
EV/Revenue and EV/EBITDA multiples across 4 pharma packaging peers:
Gerresheimer, Schott Pharma, Stevanato, AptarGroup. Data via yfinance API.

### DCF Valuation
5-year explicit forecast + terminal value. Base case assumes 7% revenue
CAGR and 26% EBITDA margin target. WACC 8.5%, terminal growth 2.5%.

### Risk Framework
16 risk factors across 4 dimensions (Financial, Strategic, Market, Latam),
each scored 1–5. Overall risk score: 2.56/5.00 (Medium).

### Latam Risk Integration
Country risk indices from companion project
[Argentina vs Germany Risk Analysis](../project-5-argentina-germany-risk)
used to risk-adjust Gerresheimer's Latam revenue exposure.

---

## Project Structure
gerresheimer-due-diligence/
├── data/
│   ├── prices.csv                  # Stock prices 2019–2024
│   ├── financials.csv              # Current valuation multiples
│   ├── gxl_historical.csv          # Gerresheimer Annual Report data
│   ├── gxl_ratios.csv              # Computed financial ratios
│   ├── comparable_analysis.csv     # Full comps table
│   ├── dcf_results.csv             # DCF scenarios
│   ├── latam_risk_exposure.csv     # Risk-adjusted Latam exposure
│   ├── sensitivity_analysis.csv    # WACC/TG sensitivity matrix
│   └── investment_summary.csv      # Final recommendation metrics
├── notebooks/
│   ├── 01_target_screening.ipynb   # Company selection + data fetch
│   ├── 02_financial_analysis.ipynb # KPIs, ratios, red/green flags
│   ├── 03_valuation.ipynb          # Comps + DCF valuation
│   ├── 04_risk_assessment.ipynb    # Risk framework + Latam exposure
│   └── 05_investment_recommendation.ipynb  # Final recommendation
└── outputs/

## Tech Stack

- **Python** — Pandas, NumPy, Plotly, yfinance
- **Valuation** — Comparable Company Analysis + DCF
- **Data Sources** — yfinance API, Gerresheimer Annual Reports 2019–2023
- **Risk Framework** — Custom scoring model (16 factors, 4 dimensions)

---

## Related Projects

This analysis integrates risk data from:
- [Argentina vs Germany — Investment Risk Analysis](../project-5-argentina-germany-risk)
- [SAP SE — Investment & Latam Market Analysis](../project-4-sap-latam-analysis)

---

## Author

**Lucas Mesa Vidal**  
Double Degree BSc International Management — Hochschule Karlsruhe & Universidad Nacional del Litoral  
Specialization: Finance & Data Analytics  
[LinkedIn](https://linkedin.com/in/lucasmesavidal) · [Portfolio](https://lucasmvidal11.github.io/data-analytics-portfolio)
