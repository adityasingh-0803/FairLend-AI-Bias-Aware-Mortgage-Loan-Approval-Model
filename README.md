# 🧠 FairLend AI – Bias-Aware Mortgage Loan Approval Model

Welcome to the official repository for **FairLend AI**, submitted to the [AI Bias Bounty Hackathon 2025](https://devpost.com/).  
This project detects and mitigates bias in mortgage loan approval decisions using machine learning and fairness auditing tools.

---

## 📁 Repository Structure
```bash
ai-bias-bounty-2025/
├── loan_model.ipynb
├── loan_access_dataset_with_labels.csv   
├── submission.csv
├── ai_risk_report.docx
├── shap_summary.png
├── bias_visualization.png
├── shap_force_plot.png
├── confusion_matrix.png
├── README.md

```

---

## 📌 Problem Statement

Build an accurate and fair ML model for mortgage loan approvals using the `loan_access_dataset.csv`, and detect systemic biases related to sensitive features like **Race**, **Gender**, and **Zip Code Group**.

---

## 🤖 Model Summary

- **Model**: Logistic Regression  
- **Preprocessing**:
  - Label encoding for categorical variables
  - Synthetic label `LoanApproved` created using domain logic  
- **Validation Performance**:
  - Accuracy: 84.7%  
  - Precision: 0.81  
  - Recall: 0.85  
  - F1 Score: 0.83

---

## ⚖️ Bias Detection & Fairness Audit

Tools and metrics used:
- 📊 Approval Rate Analysis by group
- 📉 Disparate Impact Ratio (DI)
- 🧮 Equal Opportunity Difference (EOD)
- 🧠 SHAP for interpretability (global + local)

### Key Findings:
| Group            | Bias Type         | Metric             |
|------------------|-------------------|--------------------|
| Native American  | Approval Disparity| DI Ratio = 0.414   |
| Race Groups      | TPR Gap           | EOD = 0.433        |
| Zip_Code_Group   | Feature Bias      | SHAP Top Feature   |
| Gender           | Approval Rate Gap | Minor but consistent |

---

## 🛠️ How to Run the Notebook

1. Clone the repo  
```bash
git clone https://github.com/hack-the-fest/ai-bias-bounty-2025.git
cd ai-bias-bounty-2025
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Open and run:
```bash
loan_model.ipynb
```


📄 Files Submitted
```bash
loan_model.ipynb: Full modeling + audits

submission.csv: Predictions on official test set

ai_risk_report.docx: Technical risk report

bias_visualization.png: Group approval rate

shap_summary.png, shap_force_plot.png: SHAP visualizations

confusion_matrix.png: Performance matrix
```
🙌 Acknowledgments
```bash
Hosted by Hack the Fest

Dataset inspired by U.S. mortgage lending patterns

Libraries used: pandas, scikit-learn, matplotlib, shap, seaborn

```




