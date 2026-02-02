# Credit Risk Assessment & Loan Approval Framework (Lending Club)

## Business Problem
A digital lending platform aims to issue personal loans while minimizing credit defaults.  
The objective of this project is to **assess borrower credit risk**, predict **Probability of Default (PD)**, and design a **risk-based loan approval policy** similar to real-world fintech lending workflows.

---

## Analyst Role
Acted as a **Credit Risk Analyst**, responsible for:
- Data preparation and feature selection
- Probability of Default (PD) modeling
- Risk segmentation and policy design
- Portfolio-level risk interpretation

---

## Dataset
- Source: Lending Club historical consumer loan data  
- Size: ~38,000 completed loans  
- Target Variable:
  - `default = 1` → Charged Off  
  - `default = 0` → Fully Paid  

Only completed loans were used to avoid outcome leakage.

---

## Tools & Technologies
- Python (pandas, numpy)
- Scikit-learn (Logistic Regression)
- Google Colab
- GitHub

---

##  Data Preparation
- Filtered completed loans only (Fully Paid, Charged Off)
- Selected risk-relevant features (income, DTI, credit utilization, delinquencies)
- Treated missing values using credit-risk best practices
- Converted categorical variables using one-hot encoding
- Scaled numeric variables to address model convergence

---

## Credit Risk Modeling
- Built a **Logistic Regression** model to predict Probability of Default (PD)
- Evaluated using ROC-AUC

### Model Performance
- **Baseline Test AUC:** ~0.61  
- **Improved Test AUC (after scaling):** **~0.70**

The model demonstrated stable generalization with no overfitting.

---

##  Risk Bucketing
Predicted PDs were segmented into risk buckets:

| Risk Bucket | Default Rate |
|------------|-------------|
| Low Risk | ~3.5% |
| Medium Risk | ~7.3% |
| High Risk | ~14.4% |
| Very High Risk | ~29.1% |

Monotonic increase in default rates confirms strong risk separation.

---

##  Loan Approval Policy
A PD-driven approval framework was designed:

| Decision | Loans | Default Rate |
|--------|------|--------------|
| Approve | 1,155 | ~3.5% |
| Approve with Limits | 3,160 | ~7.3% |
| Reject | 7,259 | ~19.5% |

This policy balances **portfolio growth** with **risk containment**.

---

##  Key Insights
- Feature scaling significantly improved model performance
- PD-based segmentation enables transparent credit decisions
- Risk-based approval policies reduce portfolio default exposure

---

##  Outcome
This project replicates a **real-world fintech credit risk workflow**, covering:
Data → Model → Risk Segmentation → Decisioning

---

##  Author
**Shubhankari Rai**  


