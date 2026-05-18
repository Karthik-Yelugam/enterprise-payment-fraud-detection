# 🛡️ Enterprise Payment Fraud Detection: Behavioral Anomaly Extraction 💸
**Author:** Karthik Yelugam | Data Analyst

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Data_Analysis-0052CC?style=for-the-badge&logo=google-analytics&logoColor=white)

## 🚀 Project Overview
Finding financial fraud is like finding a needle in a haystack. In this project, I analyzed a massive **6.3 Million row (500MB)** enterprise transaction dataset to uncover exactly how thieves operate. By engineering new behavioral metrics, I discovered the specific pathways fraudsters use and created actionable rules to stop them before money leaves the bank.

---

## 🗄️ The "Sample & Ignore" Data Strategy
* **The Problem:** The raw enterprise dataset is massive—**6.3 Million rows (500MB)**. This breaks GitHub's 100MB file limit and makes local analysis incredibly slow.
* **The Solution:** We extracted a **5% Stratified Sample**. This perfectly preserves the real-world class imbalance (99.9% Safe vs. 0.1% Fraud) while keeping the repository lightweight. The heavy 500MB file is safely ignored via `.gitignore`.

---

## 💡 Key Business Insights (The "Aha!" Moments)
1. **📍 Isolated Pathways:** Fraud doesn't happen everywhere. **100%** of successful attacks are isolated to just two methods: `TRANSFER` and `CASH_OUT`.
2. **💰 The Money Gap:** Thieves want maximum payout. Fraudulent transfers are massively larger than everyday, legitimate customer transactions.
3. **🎯 The "Smoking Gun" (Account Drain):** By engineering a new metric (`balance_drained_pct`), we proved that fraudsters systematically attempt to drain exactly **100%** of a victim's account in a single rapid strike. Normal users almost always leave funds behind.

---

## 🛡️ Actionable Next Steps
* **The "Fast Lane":** Allow regular `PAYMENT` and `DEBIT` transactions to process instantly with low friction.
* **The "Heavy Guard":** Trigger an immediate security hold or MFA challenge if a user attempts a `TRANSFER` of >95% of their total balance.
* **Upgrade to AI:** Deploy real-time Machine Learning models strictly on the `TRANSFER` and `CASH_OUT` pipelines to catch complex patterns in milliseconds.

---

## 🛠️ How to Run This Project
The lightweight, ready-to-use dataset is located in `data/processed/`. You do not need to download the massive raw file.

```bash
# 1. Clone the repository
git clone [https://github.com/Karthik-Yelugam/enterprise-payment-fraud-detection.git](https://github.com/Karthik-Yelugam/enterprise-payment-fraud-detection.git)

# 2. Launch the Jupyter Notebook environment
jupyter notebook notebooks/exploratory_data_analysis.ipynb
```

---

## 📂 Repository Structure

```bash
enterprise-payment-fraud-detection/
│
├── .gitignore
├── README.md
│
├── data/
│   ├── raw/
│   │   └── enterprise_transactions_raw.csv    <-- (Ignored via .gitignore)
│   └── processed/
│       └── transactions_5pct_sample.csv       <-- (Tracked & ready to use)
│
├── docs/
│   ├── final_analytical_report.pdf            <-- (Business Whitepaper)
│   └── executive_presentation.pdf             <-- (Slide Deck)
│
└── notebooks/
    └── exploratory_data_analysis.ipynb     <-- (Documented Code)
```

---

## 🤝 Connect With Me

**Karthik Yelugam** | Data Analyst

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/karthik-yelugam/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Karthik-Yelugam)

*Thank you for reviewing this project. If you are a recruiter or data team lead, I welcome the opportunity to discuss how these methodologies can be applied to your organization's data challenges.*
