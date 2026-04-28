# The Retention Architect: Churn Prediction Model (HackNU 2026)

## 📌 Project Overview
This project was developed for the **HackNU 2026** hackathon to solve the problem of user churn classification. The primary goal is to build an intelligent system that not only predicts the probability of a user leaving but also distinguishes between two types of churn:
1.  **Voluntary Churn:** When a user actively decides to cancel their subscription.
2.  **Involuntary Churn:** Caused by technical issues, payment failures, or expired cards.

## 🛠 Tech Stack
* **Language:** Python 3.12
* **Libraries:**
    * `Pandas`, `NumPy`: Data manipulation and feature engineering.
    * `XGBoost`: Gradient boosting algorithm for multi-class classification.
    * `Scikit-learn`: Data splitting and evaluation metrics.
    * `SHAP`: Model interpretability (Explainable AI).
    * `Joblib`: Model serialization.

## 📊 Data Pipeline & Features
The model integrates data from multiple sources to create a comprehensive user profile:
* **Activity Logs:** Processing large-scale generation logs in chunks to extract activity frequency and content safety (NSFW) ratios.
* **Payment History:** Analyzing transaction attempts to identify payment friction (Involuntary risk).
* **User Surveys (Quizzes):** Leveraging user intent and frustration levels reported in onboarding quizzes.
* **Geographical Data:** Assessing risk factors based on user location and regional payment success rates.

## 🤖 Model Performance
We utilized an **XGBoost Classifier** optimized for multi-class tasks. 

**Key Achievements:**
* **Explainability:** Integrated SHAP values to provide "Product Managers" with specific reasons for each user's churn risk.
* **Categorization:** High recall for identifying potential churners, allowing for proactive retention strategies.
