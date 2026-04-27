Credit Risk Modelling & Credit Scoring
Kenya Fintech Simulation
🔷 Overview

This project simulates how fintech lenders in Kenya assess borrower risk using limited but high-frequency data such as income, loan size, and mobile money activity.

The goal is to:

Predict the likelihood of loan default
Convert predictions into a usable credit score (300–850)
Demonstrate how machine learning supports lending decisions in fintech environments
🔷 Problem Statement

In many fintech lending environments, especially in emerging markets, traditional credit history is often unavailable.

As a result, lenders rely on:

Behavioral data (e.g., mobile money usage)
Income patterns
Loan history

This project builds a model to estimate default risk and translate it into an actionable credit score.

🔷 Dataset

A synthetic dataset was created to simulate a Kenyan fintech environment, including:

age → Borrower age
monthly_income → Estimated monthly earnings
loan_amount → Requested loan amount
mobile_txn_count → Mobile money transaction frequency (proxy for financial activity)
loan_history → Number of past loans
default → Target variable (1 = default, 0 = non-default)
🔷 Methodology
1. Data Simulation
Generated realistic borrower profiles using statistical distributions
Introduced relationships between income, loan size, and behavioral variables
2. Exploratory Data Analysis (EDA)
Examined feature distributions
Checked class balance
Analyzed correlations between variables
3. Feature Engineering
Derived risk-related features such as:
Loan-to-income ratio
Behavioral proxies for financial stability
4. Model Development

A Decision Tree Classifier was used because:

It captures non-linear relationships
It is interpretable
It is commonly used in risk-based decision systems
5. Model Evaluation

The model was evaluated using:

Precision & Recall
F1 Score
ROC-AUC

These metrics help balance:

Detecting defaulters (risk control)
Avoiding false rejections (customer retention)
🔷 Credit Scoring System

Predicted probabilities were converted into a credit score using:

Credit Score = 300 + (1 - Probability of Default) × 550
Interpretation:
300 → High risk
850 → Low risk

This allows the model to be used in real decision-making scenarios.

🔷 Key Insights
Higher loan-to-income ratio increases default risk
Higher mobile transaction activity indicates financial stability
Borrowers with prior loan history tend to be lower risk
🔷 Model Deployment

The model was deployed using Gradio, enabling:

Real-time predictions
Interactive user input
Credit score generation

Users can input borrower details and receive:

Default probability
Credit score
🔷 Business Application

This system can support:

Loan approval decisions
Risk-based pricing (interest rates)
Customer segmentation
Fraud and risk flagging
🔷 Tech Stack
Python (Pandas, NumPy)
Scikit-learn
Matplotlib / Seaborn
Gradio
🔷 Project Structure
credit-risk-modelling/
│
├── notebooks/
│   └── credit_risk_model.ipynb
├── data/
├── README.md
└── requirements.txt
🔷 Future Improvements
Use real-world datasets (e.g., lending data)
Implement advanced models (XGBoost, LightGBM)
Handle class imbalance more robustly
Deploy as a web application (API-based)
🔷 Author

Clyde Wawire
Data Analyst | Operational & Business Analytics

🔷 Final Note

This project reflects my interest in applying data to:

Real-world decision-making
Financial risk assessment
Scalable analytics systems
