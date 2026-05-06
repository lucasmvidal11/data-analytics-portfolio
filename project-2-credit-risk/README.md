## Project 2 — Credit Risk Analysis

### Objective
Analyze a real bank loan dataset (150,000 clients) to identify the key 
factors that predict credit default and build a predictive model.

### Dataset
Give Me Some Credit — Kaggle Competition (2011)  
150,000 real borrower records with 10 financial variables

### Methodology
- **Dataset:** Give Me Some Credit (Kaggle, 2011 competition) — 
  150,000 real US borrower records
- **Model:** Random Forest Classifier selected for its robustness 
  with imbalanced datasets and interpretability via feature importance
- **Class imbalance:** Default rate of 6.7% — model trained with 
  standard split (80/20 train/test)
- **Note:** Dataset reflects pre-2011 US credit market conditions. 
  Findings are directionally valid but should not be applied to 
  current lending decisions without retraining.

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
![Default Distribution](default_distribution.png)
![Risk Factors](risk_factors.png)
![Feature Importance](feature_importance.png)
