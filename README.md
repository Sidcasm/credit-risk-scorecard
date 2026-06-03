# 🏦 AI-Powered Credit Risk Scorecard

A machine learning model that predicts loan default probability using real-world 
borrower data — built to simulate the credit decisioning workflow used by banks 
and financial institutions.

---

## 📌 Project Overview

Credit risk modelling is one of the most critical applications of AI in banking. 
This project builds an end-to-end ML pipeline on 150,000 real borrower records 
to predict the probability of default — and segments borrowers into actionable 
risk tiers for credit decisioning.

**Key Result: ROC-AUC of 0.84** — a strong benchmark for credit risk models 
in production banking environments.

---

## 🔍 Dataset

- **Source:** [Give Me Some Credit — Kaggle](https://www.kaggle.com/c/GiveMeSomeCredit)
- **Size:** 150,000 borrower records
- **Target Variable:** `SeriousDlqin2yrs` (1 = defaulted within 2 years)
- **Default Rate:** 6.68% (imbalanced dataset)

---

## ⚙️ Methodology

| Step | Details |
|---|---|
| Data Cleaning | Median imputation for missing income; capped outliers at 99th percentile |
| Imbalance Handling | `class_weight='balanced'` in Random Forest + threshold tuning |
| Model | Random Forest Classifier (100 trees) |
| Threshold Tuning | Lowered decision threshold from 0.5 → 0.3 to improve default recall |
| Evaluation | ROC-AUC, Precision, Recall, Confusion Matrix |

---

## 📊 Results

| Metric | Value |
|---|---|
| ROC-AUC Score | **0.84** |
| Default Recall (tuned) | 36% (vs 15% baseline) |
| Defaulters Caught | 729 out of 2,005 |
| Risk Tiers | Low / Medium / High / Very High |

---

## 🔑 Key Findings — Top Default Drivers

1. **Revolving Credit Utilization** — strongest predictor (0.27 importance)
2. **Debt Ratio** — monthly debt vs income (0.14)
3. **Age** — younger borrowers default more (0.12)
4. **Monthly Income** — lower income = higher risk (0.11)
5. **Times 90 Days Late** — past behaviour predicts future default (0.08)

---

## 📈 Power BI Dashboard

Built an interactive dashboard with:
- KPI cards — Total Borrowers, Default Rate, Avg Default Probability
- Donut chart — Borrower Risk Distribution across 4 tiers
- Bar chart — Default Rate by Risk Tier (with % labels)
- Risk Tier Slicer — for interactive filtering
📎 [View Dashboard PDF](Credit_Risk_Dashboard.pdf)

---

## 🛠️ Tech Stack

- **Python** — Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Jupyter Notebook**
- **Power BI Desktop**

---

## 👤 Author

**Siddhartha Yadav, CFA®**  
Finance Director | Credit Risk | CFA Charterholder  
siddhartha.3112@gmail.com
