# 🕵️‍♂️ E-Commerce Fraud Risk Analysis — Investigation Workflow Simulation

### 📊 Project Overview
This case study replicates the **analytical workflow of a fraud and claims-investigation specialist**, focusing on fraud detection, decision-making, and operational risk analytics within e-commerce return and reimbursement operations.

The goal is to demonstrate how large-scale fraud-risk teams identify suspicious claims, quantify exposure, and improve process efficiency using **data-driven analysis and statistical validation**.

---

## ⚙️ Tools & Libraries
**Python Stack:** pandas, numpy, matplotlib, seaborn, scipy, statsmodels  
**Statistical Tests:** Chi-Square, ANOVA/Welch’s, Correlation, Cramér’s V, Cohen’s d  
**Dataset:** Synthetic case-level data (~200 K rows) simulating return & reimbursement workflows  
**Environment:** Jupyter Notebook (Python ≥ 3.9)

---

## 🧮 Analytical Methodology
The analysis integrates:
- **Descriptive analytics** for claim trends and fraud patterns  
- **Inferential statistics** (chi-square, ANOVA, t-tests) to validate differences  
- **Correlation analysis** to explore numeric relationships  
- **Effect-size metrics** to assess real-world significance  

Insights are interpreted both statistically and operationally — balancing quantitative evidence with practical fraud-investigation logic.

---

## 🔍 Key Insights

### 🧩 Fraud Rate & Distribution
- Certain refund programs show higher fraud incidence (~27 %) compared with operational categories (~12 %).  
- Fraud is marginally higher on **mobile transactions** (~20 %) and **weekends** (~17 %).  
- **Region** and **account age** have negligible predictive influence.

---

### 🧭 Customer Behavior & Claim Frequency
- Fraud probability rises slightly with prior claim frequency (+18 %), but the effect size is weak (η² ≈ 0.01).  
- Account age and claim recency show **no strong correlation** with fraud.  
- Resolution times differ statistically between fraud/non-fraud claims but **not operationally** (Cohen’s d = 0.04).

---

### 💰 Transaction & Financial Metrics
- **Claim** and **refund amounts** are moderately correlated (r = 0.41).  
- Refund value does not differ significantly between fraudulent and legitimate claims.  
- Monetary size alone offers limited predictive value; behavioral variables perform better.

---

### 💳 Payment Method & Operational Attributes
- Fraud likelihood varies across payment methods: highest in **Gift Card** and **Cash-on-Delivery** (~24 %).  
- **Escalated claims** take significantly longer to close (median = 45 days) than approved/denied ones (~16 days).  
- **Chargeback frequency** alone is not a strong fraud predictor.

---

### ⚖️ Dispute & Chargeback Dynamics
- Fraud rate rises marginally when **disputes and chargebacks** co-occur (max ≈ 22 %).  
- Although statistically significant, effect sizes are small (Cramér’s V ≈ 0.015).  
- These indicators add incremental value when combined in a composite fraud-risk feature.

---

## 💡 Recommendations
- Combine **behavioral and categorical indicators** (claim reason, payment method, dispute count) into a **composite risk score**.  
- Prioritize **subjective claim reasons** (e.g., counterfeit, not received) for enhanced manual review.  
- Streamline **escalation workflows** to balance SLA performance and fraud-control accuracy.  
- Emphasize **behavioral patterns** over purely monetary or geographic factors in fraud-prevention models.

---

## 🖼️ Key Visuals

**Fraud Rate by Claim Type**  
![Fraud Rate by Claim Type](figs/fraud_rate_by_claim_type.png)

**Fraud Probability Distribution**  
![Fraud Probability Distribution](figs/fraud_probability_distribution.png)

**Fraud by Payment Method**  
![Fraud by Payment Method](figs/fraud_by_payment_method.png)

**Resolution Time by Claim Type**  
![Resolution Time by Claim Type](figs/resolution_time_boxplot.png)

**Combined Dispute–Chargeback Fraud Rate**  
![Dispute–Chargeback Relationship](figs/combined_dispute_chargeback_fraud.png)

**Fraud Trends 2023 – 2024**  
![Fraud Trend](figs/fraud_trends_2023_2024.png)

---

## 🏁 Final Summary
This project demonstrates how structured analytics can emulate the **decision logic used in large-scale fraud-risk operations**.  
Through hypothesis testing, behavioral segmentation, and statistical validation, the analysis converts case-level data into **evidence-backed insights** for fraud detection and process improvement.

> Case Data → Statistical Evidence → Insight Generation → Operational Action

---

## 🧾 License & Disclaimer
This project uses **synthetic, non-proprietary data** generated solely for educational and illustrative purposes.  
It is not affiliated with, endorsed by, or representative of any specific organization.

---

> 🧮 **Note:** The notebook was executed on the full dataset (~200 K records, ~45 MB) to show complete results and charts.  
> The `/data/sample_case_data.csv` file is a smaller synthetic subset (≈ 200 records) included for reproducibility.
