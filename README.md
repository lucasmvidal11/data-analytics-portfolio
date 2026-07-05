# Data Analytics Portfolio — Lucas Mesa Vidal

**Finance & Data Analytics | BWL Double-Degree (HKA & UNL)**  
A portfolio of 5 financial analysis projects combining corporate finance,
data analytics, and emerging market expertise — built to demonstrate
analytical thinking for roles in Finance, Controlling, M&A, and Risk.

---

## Projects

### 🏢 Project 1 — Gerresheimer AG: M&A Due Diligence
**[View Project](./project-1-gerresheimer-due-diligence)**

A full due diligence framework for a potential acquisition of Gerresheimer AG,
a leading German pharma packaging company undergoing strategic transformation.

- Comparable company analysis (EV/Revenue, EV/EBITDA) vs 3 peers
- DCF valuation: base case EUR 58.7/share (bull EUR 95.0, bear EUR 28.9)
- Risk assessment framework (16 factors, 4 dimensions)
- **Recommendation: BUY — +117% upside on revenue multiples**

`Python` `yfinance` `DCF` `Comparable Company Analysis` `Plotly`

---

### 📊 Project 2 — DAX 40: Financial Performance & Sector Analysis
**[View Project](./project-2-dax40-analysis)**

Benchmarking analysis of 20 DAX companies across 8 sectors, measuring
COVID recovery speed, KPI performance, and structural sector trends.

- Sector KPI scorecard: gross margin, ROE, EV/EBITDA, revenue growth
- COVID impact analysis: drop, recovery, and total return 2019–2023
- Normalized sector scoring matrix (0–100 across 4 dimensions)
- **Finding: Technology dominates; Automotive faces structural decline**

`Python` `yfinance` `FP&A` `Benchmarking` `Sector Analysis` `Plotly`

---

### 🏦 Project 3 — PYME Credit Scoring: Argentina Hyperinflation Context
**[View Project](./project-3-pyme-credit-scoring)**

Two Random Forest models — baseline vs inflation-adjusted — testing whether
standard credit risk models are transferable to hyperinflationary economies.

- Dataset: 32,581 loans enriched with BCRA/INDEC macro data (2015–2024)
- Baseline AUC: 0.9121 | Inflation-Adjusted AUC: 0.8968
- **Finding: Models trained on stable economies are NOT transferable to Argentina**
- Practical thresholds for German banks with EM exposure

`Python` `Scikit-learn` `Random Forest` `Credit Risk` `Feature Engineering`

---

### 💻 Project 4 — SAP SE: Investment & Latam Market Analysis
**[View Project](./project-4-sap-latam-analysis)**

Valuation analysis of SAP vs peers combined with a risk-adjusted market
opportunity framework for Latin America.

- SAP trades at 5.02x EV/Revenue vs peer median 8.09x — **+61% implied upside**
- Cloud revenue grew from 25% to 44% of total (2019–2023), CAGR ~18.5%
- Latam ERP market CAGR 9.3% — Brazil priority, Argentina high-risk
- Risk-adjusted opportunity matrix using country risk index (Project 5)

`Python` `yfinance` `M&A` `Comparable Company Analysis` `Latam` `Plotly`

---

### 🌎 Project 5 — Argentina vs Germany: Investment Risk Analysis
**[View Project](./project-5-argentina-germany-risk)**

A composite Investment Risk Index (0–100) built from 5 macroeconomic
indicators across 4 countries, with 3 forward scenarios for Argentina
through 2027.

- Argentina risk index peaked at ~75 in 2023 — 3x Germany's average (24)
- Scenario analysis under Milei reforms: optimistic (13), base (30), pessimistic (75)
- Strategic recommendation matrix for German companies entering Argentina
- Data: World Bank API + IMF World Economic Outlook

`Python` `World Bank API` `IMF API` `Scenario Analysis` `Risk Modeling` `Plotly`

---

## Portfolio Narrative

These 5 projects form a connected analytical system:

- **Project 5** builds the country risk framework used in Projects 3 and 4
- **Project 4** uses the risk index to assess SAP's Latam opportunity
- **Project 1** references the Latam risk context for Gerresheimer's exposure
- **Project 2** provides the DAX sector context in which Projects 1 and 4 operate
- **Project 3** applies the Argentina macro data to credit risk modeling

The common thread: **a European financial analysis perspective enriched
by deep Latin American market knowledge.**

---

## Tech Stack

| Tool | Usage |
|---|---|
| Python (Pandas, NumPy) | Data processing and modeling |
| Plotly | Interactive visualizations |
| Scikit-learn | Machine learning models |
| yfinance | Stock prices and financial metrics |
| World Bank API | Macroeconomic indicators |
| IMF API | Inflation and fiscal data |
| SAP Analytics Cloud | Business intelligence (certified) |
| Power BI | Dashboard reporting (certified) |

---

## About Me

**Lucas Mesa Vidal**  
24 years old | Argentine | Based in Karlsruhe, Germany

Double Degree BSc International Management  
Hochschule Karlsruhe (HKA) & Universidad Nacional del Litoral (UNL)  
Specialization: Finance & Data Analytics

**Languages:** Deutsch B2 · English C2 · Español (native) · Português B1

**Seeking:** Pflichtpraktikum in Finance, Controlling, or M&A 

[LinkedIn](https://linkedin.com/in/lucasmesavidal) · [Email](mailto:lucasmvidal11@gmail.com)
