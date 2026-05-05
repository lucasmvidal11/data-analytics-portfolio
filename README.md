#  Financial Data Analytics Portfolio
**Lucas Mesa Vidal** | Business Administration Student | HKA Karlsruhe

---

## Project 1 — US Banking Sector Stock Analysis

### Objective
Analyze and compare the stock performance of the four largest US banks 
over the last 2 years to identify trends, returns and volatility patterns.

### Companies Analyzed
| Ticker | Company |
|--------|---------|
| JPM | JPMorgan Chase |
| GS | Goldman Sachs |
| BAC | Bank of America |
| MS | Morgan Stanley |

### Key Findings
- **Highest return:** Goldman Sachs (~115%) — best performer over the period
- **Lowest return:** Bank of America (~47%) — significantly behind peers
- **Most volatile:** Morgan Stanley — peaked at 4.0% in April 2025
- **Most stable:** JPMorgan Chase — consistently lowest volatility
- **Notable event:** All 4 banks showed a sharp volatility spike in 
  April 2025, likely driven by macro uncertainty (tariff announcements)
- **Overall trend:** Entire sector delivered strong positive returns, 
  with Goldman Sachs and Morgan Stanley leading at ~115% and ~111%

### Tools Used
Python · Pandas · Matplotlib · yfinance · Google Colab

### Visualizations
![Stock Prices](stock_prices.png)
![Comparative Return](comparative_return.png)
![Volatility](volatility.png)

---

## Project 2 — Credit Risk Analysis

### Objective
Analyze a real bank loan dataset (150,000 clients) to identify the key 
factors that predict credit default and build a predictive model.

### Dataset
Give Me Some Credit — Kaggle  
150,000 real borrower records with 10 financial variables

### Key Findings
- **Default rate in the dataset:** 6.7%
- **Most predictive factor:** Revolving Utilization of Unsecured Lines (0.224)
- **2nd most predictive:** Debt Ratio (0.201)
- **Key insight:** Clients who defaulted had on average 2.1x more 90-day 
  late payments than non-defaulting clients
- **Age pattern:** Default risk is more concentrated between ages 30-55

### Tools Used
Python · Pandas · Scikit-learn · Matplotlib · Seaborn · Google Colab

### Visualizations
![Default Distribution](project-2-credit-risk/default_distribution.png)
![Risk Factors](project-2-credit-risk/risk_factors.png)
![Feature Importance](project-2-credit-risk/feature_importance.png)
