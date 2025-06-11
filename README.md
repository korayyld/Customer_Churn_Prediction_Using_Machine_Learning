
# Customer Churn Prediction Using Machine Learning

This project aims to predict customer churn using machine learning techniques on the "Telco Customer Churn" dataset. By analyzing customer behavior, demographics, and transaction history, we build predictive models to identify at-risk customers and enable proactive retention strategies.

## 🧠 Project Team
- Selahattin Koray Yıldız
- Emrullah Ayaz

## 🧩 Problem Statement
Customer churn refers to when customers stop doing business with a company. Retaining existing customers is more cost-effective than acquiring new ones, making churn prediction vital for business success.

## 📊 Dataset Overview
- Dataset: [Telco Customer Churn](https://www.kaggle.com/datasets/yeanzc/telco-customer-churn-ibm-dataset)
- Rows: 7,043
- Columns: 33
- Types: Categorical, Numerical, Geographical, Textual
- Target: `Churn` (binary: Yes/No)

## 🛠 Data Preprocessing
- Handling missing values (e.g. median imputation for skewed numerical features)
- Dropped high-risk leakage columns (e.g., `Churn Reason`)
- One-Hot Encoding for categorical features
- StandardScaler for numerical features
- Stratified train-test split (80/20)

## 🤖 Models Evaluated
- Logistic Regression
- Random Forest
- XGBoost
- Gradient Boosting ✅ **(Best)**
- SVM
- KNN

### ✅ Best Model: Gradient Boosting
- Accuracy: 92.69%
- Precision: 84%
- Recall: 88%
- F1 Score: 86%
- Fine-tuned with `GridSearchCV` (5-fold Stratified CV)

## 🔍 Explainable AI (XAI)
To improve trust and transparency:
- **SHAP** for global & local feature importance
- **LIME** for individual customer-level explanations
- Features like `Contract`, `Tenure`, and `Monthly Charges` were most influential

## 🧠 Key Insights
- Long-term contracts and tenure reduce churn
- Fiber optic users churn more
- High monthly charges increase churn for some groups

## 📎 References
- IBM Telco Dataset (Kaggle)
- Lundberg & Lee (2017). SHAP
- Molnar (2022). Interpretable ML Book
- Multiple ML survey papers on churn prediction (see reports)

## 📁 Project Structure
```
├── data/
│   └── Telco_customer_churn.xlsx
├── notebooks/
│   ├── cmpe442-report2-codes.ipynb
│   ├── cmpe442-report3-4-codes.ipynb

```

## 📌 Conclusion
Gradient Boosting + Explainability tools provided high accuracy and actionable insights for telecom customer churn prediction. These models can be directly used for personalized marketing and customer retention strategies.
