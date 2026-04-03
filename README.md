
---

# 📊 Internet Banking Usage Analysis - Bank-wise Transaction & User Trends (2022–2025)

---

## 📌 Project Overview

This project presents a comprehensive analysis of **internet banking usage in India**, focusing on transaction volume, transaction value, and user engagement across **163 banks** over a **46-month period (March 2022 – December 2025)**.

The objective is to uncover patterns in **digital adoption**, identify **market leaders**, evaluate **efficiency metrics**, and generate **data-driven business insights**.

---

## 🎯 Project Objectives

* Analyze transaction **volume and value trends**
* Compare performance across **bank categories**
* Measure **user engagement (Tx/User)**
* Identify **top and bottom-performing banks**
* Study **monthly and yearly trends**
* Detect **outliers and anomalies**
* Understand **relationship between users and transactions**

---

## 📂 Dataset Description

| Feature       | Description                 |
| ------------- | --------------------------- |
| Dataset Name  | Internet Banking Statistics |
| Source        | RBI / India Data Portal     |
| Time Period   | Mar 2022 – Dec 2025         |
| Total Records | 4,815                       |
| Total Columns | 6                           |
| Unique Banks  | 163                         |

### 📊 Key Variables:

* `bank_name` → Name of the bank
* `no_of_transactions` → Total transactions
* `amt_of_transactions` → Transaction value
* `active_users` → Number of users
* `month` → Time reference

---

# 🧭 STAGE 1: Data Understanding & Initial Cleaning

## 🔍 Dataset Structure Analysis

* Used `.shape` → Identified **4,815 rows & 6 columns**
* Used `.info()` → Verified data types (int, float, object)
* Used `.describe()` → Observed statistical distribution

### 📌 Key Observation:

* Average transactions per record ≈ **3.58 million**
* Large variation indicates **market inequality**

---

## 🧹 Missing Value Analysis

* Checked using `.isnull().sum()`

### ✅ Result:

* **No missing values found**

👉 Insight: Dataset is **complete and reliable**

---

## 🔁 Duplicate Check

* Checked using `.duplicated().sum()`

### ✅ Result:

* **No duplicate records**

👉 Insight: No redundancy → clean dataset

---

# 🧭 STAGE 2: Data Preparation & Feature Engineering

## 🔄 Data Transformation

* Converted `month` → **datetime format**
* Enabled **time-based analysis**

---

## 🧠 Feature Engineering

Created new meaningful metrics:

### 1. 📊 Transactions per User

```
tx_per_user = no_of_transactions / active_users
```

👉 Measures **user engagement**

---

### 2. 💰 Average Transaction Value

```
avg_tx_value = amt_of_transactions / no_of_transactions
```

👉 Measures **transaction size behavior**

---

### 3. 📅 Time Features Extracted

* `year`
* `month_name`

👉 Helps in **trend analysis & seasonality detection**

---

## 📌 Outcome of Stage 2

* Dataset transformed into **analysis-ready format**
* New KPIs introduced for deeper insights

---

# 🧭 STAGE 3: EDA, Statistical Analysis & Visualization

---

## 🔍 1. Exploratory Data Analysis (EDA)

### 🏆 Market Leadership

* **Top Volume Bank:** State Bank of India (SBI)
* **Top Value Banks:** HDFC Bank, ICICI Bank
* **High Engagement:** Payments banks

👉 Insight: Large banks dominate, but **smaller banks show higher engagement efficiency**

---

### 📅 Seasonal Trends

* Peak months:

  * **March (Financial Year-End)**
  * **December (Festive Season)**

👉 Insight: Banking usage is **seasonally influenced**

---

### 📈 Growth Trend

* Continuous growth from **2022 → 2025**

👉 Insight: Strong **digital adoption trend**

---

## 📊 2. Statistical Analysis

### 📉 Distribution Analysis

* Mean > Median → **Right-skewed distribution**

👉 Interpretation:

* Few banks dominate majority transactions

---

### 🔗 Correlation Analysis

| Variables                    | Correlation |
| ---------------------------- | ----------- |
| Active Users vs Transactions | **0.85**    |
| Transactions vs Amount       | **0.83**    |
| Avg Value vs Others          | ~0          |

👉 Insight:

* Growth depends heavily on **user base**
* Transaction size is **independent**

---

### 🚨 Outlier Detection (IQR Method)

* **49 anomalies detected**

👉 Interpretation:

* Likely **corporate/high-value transactions**
* Or **reporting irregularities**

---

## 📊 3. Visualization Insights

### 📌 Key Charts & Meaning

* **Histogram (Transactions)**
  → Shows unequal distribution (few dominant banks)

* **Box Plot (Year vs Amount)**
  → Identifies extreme high-value transactions

* **Line Chart (Monthly Trend)**
  → Shows steady upward growth

* **Bar Chart (Top Banks)**
  → SBI dominates clearly

* **Scatter Plot (Users vs Transactions)**
  → Strong linear relationship

* **Heatmap (Correlation)**
  → Highlights relationships between variables

---

# 🧭 STAGE 4: Insights, Interpretation & Business Understanding

---

## 📌 Key Insights

### 1. 📈 Growth of Digital Banking

* Continuous increase in transactions and users
  👉 Internet banking is becoming dominant

---

### 2. 🏦 Market Concentration

* Few banks dominate majority share

👉 Highly **centralized market**

---

### 3. 👥 User Engagement

* Average: **5–20 transactions/user/month**

👉 Engagement varies across banks

---

### 4. 🔗 Users vs Transactions

* Strong positive relationship

👉 More users → More transactions

---

### 5. 📅 Time-Based Patterns

* Growth + seasonality

👉 Influenced by:

* Festivals
* Financial deadlines

---

### 6. ⚡ Efficiency Insights

* Some banks:

  * High volume, low value
  * Low volume, high value

---

### 7. 🚨 Outliers

* Represent large corporate transactions

---

### 8. ✅ Data Quality

* Clean dataset
* Reliable for analysis

---

# 🧭 STAGE 5: Advanced Analytics

---

## 🔎 Descriptive Analysis

* Total Records: **4,815**
* Banks: **163**
* Avg Tx/User: **~12.5**
* Outliers: **49**

---

## 🔍 Diagnostic Analysis (Why?)

* SBI dominance → Large network + rural reach
* High correlation → User growth drives volume
* Low avg value correlation → Behavior consistent across banks

---

## 🔮 Predictive Analysis (Future)

* Expected growth: **15–20% in 2026**
* Expansion in:

  * Rural banks
  * Co-operative banks

---

## 🧠 Prescriptive Analysis (Actions)

### For Banks:

* Improve **engagement strategies**
* Focus on **retention**
* Strengthen **high-value transaction systems**

### For Government:

* Support **digital banking infrastructure**
* Reduce **digital divide**

---

# 📊 Final Business Recommendations

* ✔ Invest in **user acquisition + engagement**
* ✔ Enhance **digital platforms**
* ✔ Monitor anomalies regularly
* ✔ Improve rural banking digitization
* ✔ Use data analytics for decision-making

---

# 🏁 Final Conclusion

India’s digital banking ecosystem is rapidly evolving. The analysis confirms:

* Strong **growth trajectory**
* High **market concentration**
* Increasing **user engagement importance**

👉 Future success depends on:

* **User experience**
* **Digital accessibility**
* **Engagement strategies**

---

## 👨‍💻 Author

👤 **M. Punitha**

💼 *Aspiring Data Analyst*

📧 **Email:**   *[punithagvgvc@gmail.com](mailto:punithagvgvc@gmail.com)*

🔗 **LinkedIn:** [www.linkedin.com/in/punitha-muthusamy-6b46b2244](http://www.linkedin.com/in/punitha-muthusamy-6b46b2244)

🐙 **GitHub:** github.com/punithamuthusamy-ux

---

⭐ *If you found this useful, don't forget to star the repository!* 

```
