## Project 2 — Credit Risk Analysis

### Objective
Analyze a real bank loan dataset (150,000 clients) to identify the key 
factors that predict credit default and build a predictive model.

### Dataset
Give Me Some Credit — Kaggle Competition (2011)  
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
