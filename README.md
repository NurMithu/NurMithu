<div align="center">

# Nur-A-Alam

**Data Scientist — Machine Learning & Business Analytics**

Postgraduate Diploma in Data Science candidate, building production-style analytics solutions for retail, financial services, and customer analytics use cases. Available for remote and freelance engagements.

[Email](mailto:zarictg@gamil.com) · [LinkedIn](#) · [Portfolio](#)

</div>

---

## Overview

I design and deploy end-to-end data science solutions — from data ingestion and cleaning through model development to a working, interactive tool a business can use directly. Each project below follows a consistent standard: a real, publicly verifiable dataset; multiple modeling approaches compared on evidence rather than assumption; results translated into plain-language business recommendations; and a live, deployed demo rather than a static notebook alone.

---

## Selected Projects

### Customer Churn & Lifetime Value Analysis
*Churn prediction and CLV modeling for a subscription retail business*

A fifteen-module analysis covering data quality assessment, statistical testing, feature engineering, and two production-candidate models, concluding with prioritized business recommendations.

- **Approach:** Logistic Regression (churn), Multiple Linear Regression (lifetime value)
- **Result:** ROC AUC of 0.789 on churn prediction, with the decision threshold explicitly tuned for early-warning retention outreach rather than left at a default
- **Stack:** pandas, scikit-learn, statsmodels
- **Repository:** [Zephyr_Retail_Churn_CLV_Analysis](https://github.com/NurMithu/Zephyr_Retail_Churn_CLV_Analysis)

### Retail Sales Forecasting & Promotion Impact
*Daily sales forecasting across 1,115+ retail stores*

Three modeling approaches — linear regression, Random Forest, and XGBoost — evaluated against a time-based holdout, with the best-performing model selected on evidence rather than assumed in advance.

- **Result:** XGBoost reduces forecast error (RMSPE) by approximately 40% relative to a linear baseline (R² = 0.926); promotional activity is associated with a measured 39% average sales lift
- **Stack:** XGBoost, Random Forest, pandas, Streamlit
- **Repository:** [sales-forecasting-rossmann](https://github.com/NurMithu/sales-forecasting-rossmann) · **[Live demo](https://sales-forecasting-rossmann-2vkhappr8sgdidmbvkorvl.streamlit.app/)**

### Credit Card Fraud Detection
*Imbalanced classification and unsupervised anomaly detection*

Addresses the core technical challenge of fraud detection directly — a fraud rate under 1% renders standard accuracy metrics meaningless. Five approaches are compared, including a from-scratch autoencoder trained without any labeled fraud examples.

- **Result:** Random Forest achieves 85% precision at 85% recall at a business-calibrated decision threshold; the unsupervised autoencoder independently catches 81% of fraud cases with no labeled training data
- **Stack:** XGBoost, SMOTE, scikit-learn, Streamlit
- **Repository:** [fraud-detection](https://github.com/NurMithu/fraud-detection) · **[Live demo](https://fraud-detection-ywooiuryujcxw7q2ss5hsy.streamlit.app/)**

### Customer Sentiment Analysis
*Sentiment classification and brand benchmarking on customer feedback*

Compares a zero-training rule-based baseline against four trained models, then applies the result to brand benchmarking and root-cause complaint analysis.

- **Result:** The trained model outperforms the rule-based baseline by approximately 39% (Macro F1 0.714 vs. 0.513) and identifies the leading driver of negative sentiment
- **Stack:** NLTK, TF-IDF, Logistic Regression, Streamlit
- **Repository:** [sentiment-analysis](https://github.com/NurMithu/sentiment-analysis) · **[Live demo](https://sentiment-analysis-ytcvdn7yhftrexed7yoczj.streamlit.app/)**

---

## Technical Skills

**Languages & Data:** Python, SQL, pandas, NumPy

**Machine Learning:** scikit-learn, XGBoost, imbalanced-learn, statistical modeling and hypothesis testing

**Deep Learning:** Artificial Neural Networks, Convolutional Neural Networks, Autoencoders, Recurrent Neural Networks / LSTM

**Deployment & Visualization:** Streamlit, Plotly, Power BI, Jupyter

---

## Approach

Each project in this profile is built to a consistent standard:

- Real, publicly sourced datasets rather than synthetic data
- Multiple modeling approaches evaluated against each other, with the selection justified by results
- Documented limitations and known failure modes, not just headline metrics
- A deployed, interactive interface in addition to the underlying analysis

---

## Contact

Open to remote data science, analytics, and machine learning engagements.

**Email:** zarictg@gmail.com
