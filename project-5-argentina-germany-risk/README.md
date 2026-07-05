# Argentina vs Germany — Investment Risk Analysis (2004–2023)

**Can a German company invest in Argentina today?**  
This project builds a quantitative framework to answer that question using 20 years of macroeconomic data.

---

## Project Overview

This analysis compares the investment risk profiles of Argentina, Germany, Brazil, and Mexico 
between 2004 and 2023. Brazil and Mexico serve as regional benchmarks, revealing that 
Argentina's risk profile is an outlier even within Latin America — not just against Germany. 
The project then projects three forward-looking scenarios for Argentina through 2027, 
based on the structural reforms introduced by the Milei administration.

The output is a composite **Investment Risk Index (0–100)** built from five macroeconomic 
indicators, plus a strategic recommendation matrix for German companies considering 
market entry in Argentina.

---

## Key Findings

- Argentina's risk index peaked at **~75 in 2023** — more than 3x Germany's average (24)
- Under the **base scenario**, Argentina's risk index falls to ~30 by 2027 (gradual stabilization)
- Under the **optimistic scenario**, Argentina converges with Germany's risk level by 2027
- Under the **pessimistic scenario**, risk remains above 75 through 2027
- **Commodity investments** (lithium, agriculture) are recommended even under the base scenario, 
  as their value is largely independent of domestic market conditions

---

## Methodology

### Risk Index Composition

| Indicator | Weight | Source | Logic |
|---|---|---|---|
| Inflation | 35% | IMF WEO + World Bank | Higher = more risk |
| Public Debt / GDP | 20% | IMF WEO | Higher = more risk |
| GDP Growth | 20% | World Bank | Lower = more risk |
| Unemployment | 15% | World Bank | Higher = more risk |
| FDI Inflow / GDP | 10% | World Bank | Lower = more risk |

All indicators are normalized to a 0–100 scale using min-max normalization 
across the full dataset (all countries, all years).

### Data Notes

- Argentina's inflation data (2005–2017) is sourced from the **IMF World Economic Outlook** 
  due to known reliability issues with INDEC official statistics during that period
- Public debt data sourced from IMF for all countries due to incomplete World Bank coverage
- Missing values (2005 extremes) filled using linear backfill

### Scenario Assumptions (2024–2027)

| Variable | Optimistic | Base | Pessimistic |
|---|---|---|---|
| Inflation | 50% → 8% | 120% → 25% | 200% → 120% |
| GDP Growth | 3% → 5.5% | -2% → 3.5% | -5% → 1% |
| Unemployment | 6.5% → 5% | 8% → 6.5% | 12% → 11% |
| Debt / GDP | 85% → 70% | 90% → 82% | 100% → 120% |
| FDI Inflow | 2.5% → 5.5% | 1.5% → 3% | 0.5% → 0.8% |

---

## Strategic Recommendation Matrix

| Strategy | Optimistic | Base | Pessimistic |
|---|---|---|---|
| Export (goods to AR) | ✅ Recommended | ⚠️ Possible | ❌ Not recommended |
| Direct Investment (production) | ✅ Recommended | ⏳ Wait | ❌ Not recommended |
| Joint Venture (local partner) | ✅ Recommended | ⚠️ Possible | ⏳ Wait |
| Commodity Investment (lithium, agri) | ✅ Highly recommended | ✅ Recommended | ⚠️ Possible |

---

## Project Structure
```
argentina-germany-risk-analysis/
├── data/
│   ├── world_bank_raw.csv      # Cleaned macroeconomic dataset (4 countries, 2004–2023)
│   ├── risk_index.csv          # Dataset with computed risk index per country/year
│   └── scenarios.csv           # Projected risk index under 3 scenarios (2024–2027)
├── notebooks/
│   ├── 01_data_fetch.ipynb     # Data collection: World Bank API + IMF API
│   ├── 02_risk_index.ipynb     # Risk index construction and visualization
│   └── 03_scenarios_recommendation.ipynb  # Scenario analysis + recommendation matrix
└── outputs/                    # Generated charts and reports
```

## Tech Stack

- **Python** — Pandas, NumPy, Plotly
- **Data Sources** — World Bank API, IMF World Economic Outlook API
- **Visualization** — Interactive Plotly charts, hosted on GitHub Pages

---

## Author

**Lucas Mesa Vidal**  
Double Degree BSc International Management — Hochschule Karlsruhe & Universidad Nacional del Litoral  
Specialization: Finance & Data Analytics  
[LinkedIn](https://linkedin.com/in/lucasmesavidal) · [Portfolio](https://lucasmvidal11.github.io/data-analytics-portfolio)
