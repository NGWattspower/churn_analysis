# Customer Churn Analysis – EDA  

This project is part of a Data Analytics.  The goal is to perform **Exploratory Data Analysis (EDA)** on a bank customer churn dataset to uncover insights about customer behavior and the factors driving churn.  

---

## Project Overview  

- **Objective:** Identify key drivers of customer churn and provide actionable insights.  
- **Dataset:** `churn_modelling.csv` (10,000 rows, 14 columns).  
- **Target Variable:** `Exited`  
  - `1` = customer churned  
  - `0` = customer retained  

---

## 📂 Repository Structure  
customer_churn_analysis/
│
├── data/
│ └── churn_modelling.csv # raw dataset
│
├── notebooks/
│ └── churn_eda.ipynb # Jupyter notebook with full analysis
│
├── reports/
│ └── Churn_EDA_Presentation.pdf # final presentation
│
├── images/ # optional, saved plots
│
├── README.md # project overview
│
└── requirements.txt # optional, dependencies

---

## Data Cleaning  

- Dropped identifier columns: `RowNumber`, `CustomerId`, `Surname`.  
- Confirmed no missing values.  
- Dataset reduced to 11 predictive features + target.  

---

## Exploratory Analysis  

**Categorical Insights:**  
- Geography: German customers churn the most.  
- Membership: Inactive members churn more.  
- Number of Products: 2 products = lowest churn; 3–4 products = highest churn.  
- Gender & Credit Card: Weak predictors.  

**Numerical Insights:**  
- Age: Older customers churn more often.  
- Balance: Higher balances linked to churn, zero balances often retained.  
- Tenure & Salary: Weak predictors.  

---

## Key Drivers of Churn  

- Geography (Germany)  
- Membership Activity (inactive)  
- Number of Products (non-linear effect, 2 = safe zone)  
- Age (older customers at higher risk)  
- Balance (high balances linked with churn)  

---

## Recommendations  

- Target retention strategies for German customers, inactive members, and older high-balance clients.  
- Encourage customers to adopt **2 products** as it strongly reduces churn.  
- Investigate dissatisfaction among customers with 3+ products.  
- Focus onboarding and engagement in the first year to reduce early churn.  

---

## How to Run  

1. Clone this repo:  
   ```bash
   git clone https://github.com/YOUR-USERNAME/customer_churn_analysis.git

   cd customer_churn_analysis

   jupyter notebook notebooks/churn_eda.ipynb

Python 3.8+

pandas

matplotlib

seaborn

jupyter

Install with:

pip install -r requirements.txt



