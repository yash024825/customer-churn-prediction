# Customer Churn Prediction & Retention Analysis
### Python · Scikit-learn · Pandas · Seaborn · Power BI

---

## 📌 Project Overview

An end-to-end machine learning and analytics project analyzing **7,032 telecom customer records** to identify churn drivers, predict at-risk customers, and build a retention-focused business dashboard. The project covers the full data science workflow — from exploratory data analysis and preprocessing, through ML model building and evaluation, to an interactive 5-panel Power BI dashboard delivering actionable retention insights.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data cleaning, EDA, feature engineering |
| Scikit-learn | ML models (Logistic Regression, Random Forest) |
| Imbalanced-learn (SMOTE) | Class balancing |
| Matplotlib / Seaborn | EDA visualizations, confusion matrix |
| Power BI | Interactive retention dashboard |
| Git / GitHub | Version control |

---

## 📂 Project Structure

```
customer-churn-prediction/
├── notebooks/
│   ├── churn_analysis.ipynb        ← Full Python analysis & ML notebook
│   ├── eda_charts.png              ← EDA: Churn by contract, service, tenure
│   ├── correlation_heatmap.png     ← Feature correlation heatmap
│   ├── feature_importance.png      ← Top 10 Random Forest feature importances
│   └── confusion_matrix.png        ← Model comparison confusion matrices
└── Churn_Prediction_Dashboard.pbix ← Power BI dashboard file
```

---

## 📊 Dataset

- **Source:** [Telco Customer Churn — IBM Watson Analytics](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 records, 21 features
- **After cleaning:** 7,032 records, 20 features
- **Target variable:** `Churn` (Yes / No)
- **Overall churn rate:** 26.5%

> Raw CSV file not uploaded due to licensing. Download directly from Kaggle link above.

---

## 🔍 Key Steps

### 1. Data Cleaning & Preprocessing
- Converted `TotalCharges` from object to numeric — identified and removed 11 corrupted rows
- Mapped `Churn` to binary (Yes=1, No=0)
- Label encoded 15 categorical features for model compatibility
- Applied **SMOTE** to balance class distribution from 5,163/1,869 to 4,130/4,130

### 2. Exploratory Data Analysis
- Analyzed churn rate across 6 key dimensions: contract type, internet service, tenure, monthly charges, senior citizen status, and payment method
- Built correlation heatmap across all 19 features
- Identified top 5 churn-correlated features

### 3. Model Building & Evaluation
- Trained and compared **Logistic Regression** and **Random Forest** classifiers
- Evaluated using Accuracy, F1 Score, and ROC-AUC metrics
- Generated feature importance scores to identify business-actionable churn drivers

### 4. Power BI Dashboard
Built a 5-panel interactive retention dashboard:
- KPI cards (Total Customers, Churn Rate, High Risk Count, Avg Churn Probability)
- Churn rate by Contract Type (Bar chart)
- Customer Risk Segments (Pie chart)
- Churn rate by Internet Service (Bar chart)
- Churn Probability by Tenure (Line chart)

---

## 📈 Key EDA Findings

| Segment | Churn Rate |
|---|---|
| Month-to-Month contract | 42.7% |
| One-Year contract | ~11% |
| Two-Year contract | 2.8% |
| Fiber Optic internet | 41.9% |
| DSL internet | ~19% |
| Senior Citizens | 41.7% |
| Non-Senior Citizens | 23.7% |

---

## 🤖 Model Performance

| Model | Accuracy | F1 Score | ROC-AUC |
|---|---|---|---|
| Logistic Regression | 73.8% | 0.589 | 0.809 |
| **Random Forest** | **76.3%** | **0.565** | **0.808** |

**Winner: Random Forest** — higher accuracy with comparable ROC-AUC score.

---

## 🏆 Top 5 Churn Predictors

| Rank | Feature | Importance Score |
|---|---|---|
| 1 | MonthlyCharges | 0.136 |
| 2 | TotalCharges | 0.136 |
| 3 | Contract | 0.136 |
| 4 | Tenure | 0.121 |
| 5 | OnlineSecurity | 0.087 |

---

## 📊 Risk Segmentation Results

| Risk Segment | Customers | % of Total |
|---|---|---|
| Low Risk | 3,777 | 53.7% |
| High Risk | 1,782 | 25.3% |
| Medium Risk | 459 | 7.6% |

---

## 💡 Business Recommendations

1. **Prioritize contract upgrades** — Month-to-Month customers churn at 42.7% vs 2.8% for Two-Year contracts. Offer discounted annual plan incentives to convert high-risk month-to-month customers.

2. **Investigate Fiber Optic pricing** — 41.9% churn rate is critically high and likely driven by pricing dissatisfaction. A competitive pricing review is recommended.

3. **Senior citizen retention program** — At 41.7% churn, senior customers need dedicated support, simplified plans, and proactive outreach.

4. **Target 1,782 high-risk customers immediately** — Use the churn probability scores from the Random Forest model to prioritize retention calls and loyalty offers.

5. **Focus on first 12 months** — Tenure analysis shows churn probability drops sharply after month 12. Early engagement programs within the first year are critical.

---

## 🚀 How to Run

1. Clone this repository
```bash
git clone https://github.com/yash024825/customer-churn-prediction.git
```

2. Install required libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn jupyter
```

3. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) and place CSV in a `data/` folder

4. Open `notebooks/churn_analysis.ipynb` in VS Code or Jupyter and run all cells

5. Open `Churn_Prediction_Dashboard.pbix` in Power BI Desktop

---

## 👤 Author

**Tatikonda Yeshwanth**
Data Analyst | Python · SQL · Power BI · Scikit-learn

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/tatikonda-yeshwanth-3868b0296/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/yash024825)
