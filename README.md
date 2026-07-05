# PYME Credit Scoring — Argentina Hyperinflation Context

**Do standard credit risk models fail under hyperinflation?**  
This project builds and compares two Random Forest models — a standard baseline 
and an inflation-adjusted version — to test whether macroeconomic context variables 
improve credit scoring for SMEs in high-inflation environments like Argentina.

---

## Key Finding

They don't — and that's the point.

Adding inflation-adjustment features to a model trained on stable-economy data 
produces **no meaningful improvement** (AUC 0.9121 vs 0.8968). This confirms the 
central hypothesis: **credit risk models are not transferable across macroeconomic 
contexts**. A model trained on US or European borrower data will systematically 
underestimate default risk in Argentina — not because the math is wrong, but because 
the training data contains no inflation-driven defaults.

---

## Model Comparison

| Metric | Baseline RF | Inflation-Adjusted RF |
|---|---|---|
| AUC-ROC | 0.9121 | 0.8968 |
| Default Recall | 65.6% | 58.4% |
| Default Precision | 95.7% | 94.8% |
| Accuracy | 92.3% | 91.2% |

---

## Macroeconomic Context

Argentina's inflation trajectory makes it an extreme stress test for any credit model:

| Year | Inflation | BCRA Policy Rate |
|---|---|---|
| 2018 | 47.6% | 60.0% |
| 2019 | 53.8% | 63.0% |
| 2022 | 94.8% | 75.0% |
| 2023 | 211.4% | 133.0% |
| 2024 | 117.8% | 110.0% |

Average inflation 2018–2023: **87.5%**

---

## Methodology

### Dataset
- Base dataset: 32,581 loans with 12 features (Kaggle — Credit Risk Dataset)
- Macro enrichment: BCRA/INDEC inflation data + BCRA policy rates (2015–2024)
- Temporal simulation: 60% pre-crisis years (2015–2020), 40% crisis years (2021–2024)

### Inflation-Adjusted Features
| Feature | Formula | Rationale |
|---|---|---|
| real_income | nominal_income / cum_inflation_factor | Deflates income to 2015 pesos |
| real_interest_burden | loan_rate − inflation | Measures true cost of debt |
| inflation_stress | max(0, (inflation−50)/100) | Captures extreme inflation shock |
| real_debt_burden | loan_amount / real_income | Debt load in real terms |

### Models
Both models use Random Forest (100 trees, max_depth=8). The only difference 
is the feature set — baseline uses standard loan features, adjusted model 
adds the four inflation-derived variables above.

---

## Recommendations for German Banks

Based on the findings, a German bank or fintech expanding into Argentina should:

- **Never deploy a model trained on European/US data** in Argentina without 
  local retraining — the distributional shift is too large.
- **Add macro thresholds as hard rules** on top of any model score:
  - Inflation < 30%: standard model scores reliable
  - Inflation 30–80%: apply +10% risk premium to model output
  - Inflation > 80%: manual review required for all Grade D+ loans
- **Prioritize recall over precision** — missing a default in an emerging 
  market is costlier than a false alarm.
- **Recalibrate quarterly** when annual inflation exceeds 50%.

---

## Project Structure
pyme-credit-scoring-argentina/
├── data/
│   ├── credit_risk_raw.csv          # Original Kaggle dataset
│   ├── credit_risk_clean.csv        # Cleaned dataset
│   ├── argentina_macro.csv          # BCRA inflation + policy rates 2015–2024
│   ├── final_model_comparison.csv   # Model metrics comparison
├── notebooks/
│   ├── 01_data_fetch.ipynb          # Data loading + macro enrichment
│   ├── 02_eda.ipynb                 # Exploratory data analysis
│   ├── 03_baseline_model.ipynb      # Standard Random Forest (no macro context)
│   ├── 04_inflation_adjusted.ipynb  # Inflation-adjusted feature engineering + model
│   └── 05_comparison_recommendation.ipynb  # Model comparison + final recommendation
└── outputs/
├── rf_baseline.pkl              # Saved baseline model
└── rf_adjusted.pkl              # Saved adjusted model

## Tech Stack

- **Python** — Pandas, NumPy, Scikit-learn, Plotly
- **Data Sources** — Kaggle (loan dataset), BCRA/INDEC (inflation), BCRA (policy rates)
- **Models** — Random Forest Classifier

---

## Related Projects

This project is part of a connected portfolio on emerging market financial analysis:
- [Argentina vs Germany — Investment Risk Analysis](../project-5-argentina-germany-risk)
- [SAP SE — Investment & Latam Market Analysis](../project-4-sap-latam-analysis)

---

## Author

**Lucas Mesa Vidal**  
Double Degree BSc International Management — Hochschule Karlsruhe & Universidad Nacional del Litoral  
Specialization: Finance & Data Analytics  
[LinkedIn](https://linkedin.com/in/lucasmesavidal) · [Portfolio](https://lucasmvidal11.github.io/data-analytics-portfolio)