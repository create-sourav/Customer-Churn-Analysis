# 📊 Telecom Customer Churn Analysis – A Business Intelligence Case Study

## 🔍 Project Objective

This project aims to uncover key factors contributing to customer churn in the telecom industry and quantify the associated revenue impact. Through interactive data visualizations, we seek to identify patterns of behavior among customers likely to churn and propose actionable insights to improve retention.

---

## 📁 Dataset Overview

- **Source**: [Kaggle – Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Total Records**: 7,043 Customers
- **Key Features**:  
  Demographics (Gender, Senior Citizen, Tenure),  
  Services (Internet, OnlineSecurity, etc.),  
  Charges (Monthly, Total),  
  Customer Status (Churned or Retained)

---

## 🛠️ Tools Used

- **Power BI** – for data transformation and building an interactive dashboard  
- **DAX** – for creating measures like churn rate and revenue loss  
- **Excel** – for initial data cleaning and pre-processing  
- **GitHub** – for version control and public portfolio showcase

---

## 📌 Dashboard Preview

[![Dashboard Screenshot](Dashboard%20Screenshot.png)](Dashboard%20Screenshot.png)

---

## 📈 Key Insights

### 🧾 Overall Metrics
- 💸 **Total Revenue Lost**: ₹139.13K  
- 🙍 **Total Customers Churned**: 1,869

These numbers reflect a major financial loss due to customer churn.

---

### 📉 Churn Rate by Tenure
- Customers with **0–20 months tenure** exhibit the **highest churn rate**, peaking above 60%.
- Churn **declines with increased tenure**, indicating improved retention over time.

---

### 🔄 Service-Level Churn Drivers
- **Month-to-Month + Fiber Optic + No Security/Backup/Protection** = Highest churn risk.
- Lack of **value-added services** leads to higher churn probability.

---

### 🧾 Billing & Contract Influence
- **Paperless billing** users on **month-to-month contracts** churn more — likely due to low switching cost.
- **1–2 year contracts** show significantly lower churn rates.

---

### 🧑‍🤝‍🧑 Segmentation Analysis
- **Gender** has negligible impact.
- More actionable segmentation based on:
  - Senior Citizen status
  - Internet Service Type
  - Multiple Lines
  - Tenure groups (e.g., 0–12, 13–24, 25+ months)

---

## 🧮 DAX Measures

```DAX
Churn Rate (%) = 
DIVIDE(
    CALCULATE(COUNTROWS(ChurnData), ChurnData[Churn] = "Yes"),
    COUNTROWS(ChurnData)
)

Total Revenue Lost = 
CALCULATE(SUM(ChurnData[MonthlyCharges]), ChurnData[Churn] = "Yes")

Total Churned Customers = 
CALCULATE(COUNTROWS(ChurnData), ChurnData[Churn] = "Yes")

Avg Monthly Charges (Churned) = 
CALCULATE(AVERAGE(ChurnData[MonthlyCharges]), ChurnData[Churn] = "Yes")

Avg Monthly Charges (Retained) = 
CALCULATE(AVERAGE(ChurnData[MonthlyCharges]), ChurnData[Churn] = "No")


---

## ✅ Key Insights
- 🔴 Churn rate highest among month-to-month contracts with fiber optic internet
- 🧓 Senior citizens without device protection churn more frequently
- 💡 Offering online security and paperless billing reduces churn in long-term contracts

---

## 🧠 Skills Demonstrated
- Data cleaning & transformation in Power BI
- DAX Measures (Churn Rate, Revenue Loss)
- Visual storytelling with charts & slicers

---

## 📁 Files Included
| File Name | Description |
|-----------|-------------|
| `customer_churn.pbix` | Final Power BI dashboard file |
| `WA_Fn-UseC_-Telco-Customer-Churn.csv` | Raw data from Kaggle |
| `Project_Summary.docx` | Word document summary of project |
| `dashboard.png` | Screenshot of the dashboard |

---

## 🚀 How to Use
1. Download the `.pbix` file
2. Open it with Power BI Desktop
3. Explore insights with interactive filters

---

## 📬 Contact
**Created by:** Sourav Mondal 
📫 [LinkedIn] https://www.linkedin.com/in/sourav-mondal-7991b5373/?trk=opento_sprofile_goalscard | ✉️ [souravmondal5f@gmail.com]
