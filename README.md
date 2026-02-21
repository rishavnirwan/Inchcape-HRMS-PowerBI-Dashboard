# 📊 Inchcape HRMS Analytics Dashboard – Power BI Project

---

## 📌 Project Overview

This project is developed based on real-world HR business requirements.  
The dashboard provides strategic and analytical insights into:

- ✅ New Hires Analysis  
- ✅ Bad Hires Analysis  
- ✅ Active Employees Tracking  
- ✅ Separations & Attrition Analysis  
- ✅ KPI & Scorecard Reporting  

---

## 🎯 Business Objective

The HR department required a **single consolidated dashboard** to:

- Monitor recruitment trends
- Track employee attrition
- Analyze VP-level performance
- Perform region-wise workforce analysis
- Measure Year-over-Year hiring growth

---

## 🏗️ Data Model Architecture

Implemented **Star Schema Model**

**Fact Table**
- Employee

**Dimension Tables**
- Date
- BU
- Gender
- Ethnicity
- AgeGroup
- PayType
- Separation

Custom relationships and calculated columns were created using DAX.

---

## 🧠 Key DAX Calculations

```DAX
New Hires = SUM(Employee[isNewHire])

New Hires SPLY = 
CALCULATE([New Hires], SAMEPERIODLASTYEAR('Date'[Date]))

New Hires YoY % Change = 
DIVIDE([New Hires] - [New Hires SPLY], [New Hires SPLY])
```

Additional Measures Created:

- Bad Hires %
- Actives
- Separations
- Turnover %
- Average Tenure
- YoY Variance KPIs

---

## 📈 Dashboard Pages

### 1️⃣ VP Analysis Page
- VP-wise Hiring Performance
- Gender Distribution
- Region Analysis
- KPI Scorecard

### 2️⃣ New Hires Insights
- Year, Quarter, Month Trend
- YoY Growth %
- Age Group Comparison
- Full-time vs Part-time Trend

### 3️⃣ Bad Hires Analysis
- Bad Hire %
- Region Ranking
- Age Group Impact
- YoY Trend

### 4️⃣ Actives & Separations
- Attrition Rate
- Turnover %
- Separation Reasons
- VP & Region Comparison

---

## 🛠️ Tools Used

- Power BI Desktop
- Power Query
- DAX
- Data Modeling
- Excel

---

## 📊 Dashboard Preview

![VP Analysis](Screenshots/VP_Analysis.png)

![New Hires](Screenshots/New_Hires.png)

![Bad Hires](Screenshots/Bad_Hires.png)

![Actives & Separations](Screenshots/Actives_Separations.png)

---

## 🚀 Key Business Insights

- Improved hiring trend visibility
- Identified high attrition regions
- Tracked bad hire percentage
- Enhanced VP performance transparency
- Provided dynamic KPI monitoring

---


