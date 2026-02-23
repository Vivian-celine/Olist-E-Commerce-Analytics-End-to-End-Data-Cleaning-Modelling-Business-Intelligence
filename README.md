##📦Olist E-Commerce Data Analysis

Full-Cycle Data Cleaning, Modelling & Business Intelligence Project

📌 Project Overview

This project performs a complete end-to-end analysis of the Brazilian Olist e-commerce dataset, from data cleaning in Python to dimensional modelling and dashboard development in Power BI.

The goal was not just to clean data — but to properly model interconnected tables, resolve orphan records, and build a robust analytical structure that supports reliable business insights.

---

##🎯 Project Objective

To evaluate overall business performance by analyzing:

📈 Revenue trends

🗺️ Geographic sales distribution

🛍️ Product performance

🚚 Delivery efficiency

⭐ Customer satisfaction

---

###🗂 Dataset Description

The dataset comes from the Olist Brazilian e-commerce marketplace.

Core Tables Used

Customers

Products

Orders

Order_items

Payments

Reviews

The dataset follows a Snowflake Schema structure, requiring proper relationship management.

---

##🧹 Data Cleaning Process (Python)
1️⃣ Initial Exploration

Used .info() to inspect structure and data types

Verified primary keys for duplicates

Converted object date columns to datetime

2️⃣ Business Logic Cleaning

Filtered orders to Delivered status only

Validated logical date flow:

Purchase Date → Approval Date → Delivery Date

Created delivery time difference columns

Removed unrealistic delivery times (> 90 days)

Removed products with zero numeric values

🧠 Data Modelling & Orphan Row Detection

Because this dataset is highly relational, improper modelling caused blanks in Power BI visuals.

🔎 Orphan Records Identified
Issue	Count
Orders without customer	0 ✅
Payments without order	3,295
Reviews without order	3,016
Order_items without product	1,612
Order_items without order	2,894
Orders without order_items	1,336

These orphan rows caused broken relationships and blank visuals.

After impact validation, they were removed to enforce referential integrity.

---

##🔄 Modelling Improvements

✔ Integrated customer_unique_id into Orders to create proper 1-to-many relationships
✔ Aggregated Reviews table for cleaner analytical use
✔ Merged review_id into Order_items for product-level satisfaction analysis
✔ Rebuilt model in Power BI using clean relationships

This eliminated blank visuals and ensured analytical accuracy.

---

## 📁 Repository Structure

```
Olist-Ecommerce-Analysis
│
├── image/
│   ├── sales_overview.png
│   └── customer_experience.png
│
├── notebook/
│   └── olist_data_cleaning.ipynb
│
├── README.md
│
└── project_files_link.md   (Contains Google Drive links)
```

##📊 Dashboard Overview

The final Power BI dashboard includes:

📊 12 analytical charts

📌 4 KPI indicators

👥 Customer segmentation:

One-time

Occasional

Regular

Loyal

Each visual was designed to tell a business story — not just display metrics.

---

### 🟢 Sales Overview

![Sales Overview](image/sales%20overview.png)

### ⭐ Customer Experience

![Customer Experience](image/customer%20experience.png)

---
##🔍 Key Insights
📈 Revenue Growth

Revenue grew steadily from 2016 to 2018, with 2017 showing the strongest expansion — indicating rapid scaling and increasing market penetration.

🗺️ Geographic Concentration

Sales are highly concentrated in São Paulo.
The top three states contribute a disproportionate share of revenue — presenting geographic concentration risk.

🛍️ Product Revenue Drivers

Revenue is concentrated in a small number of categories.
Top revenue drivers:

beleza_saude

cama_mesa_banho

🚚 Delivery & Satisfaction Relationship

There is a clear negative relationship between delivery time and review score.
Customer satisfaction drops significantly when delivery exceeds 21 days.

📍 Logistics Impact

States with longer average delivery times tend to show lower review scores — reinforcing how operational efficiency affects customer perception.

⭐ Customer Feedback Pattern

Most reviews are 5-star ratings, showing generally positive sentiment.
However, a small subset of product categories consistently underperform — signaling improvement opportunities.

💳 Payment Dependency Risk

~78% of revenue comes from credit card payments, indicating heavy reliance on a single payment method and potential financial channel risk.

---

##🛠 Tools Used

🐍 Python (Pandas, NumPy)

📊 Power BI

🧠 Data Modelling (Snowflake Schema)

📁 Git & GitHub

---


## 📂 Access to Full Project Files

Due to GitHub file size limitations, the full dataset and Power BI dashboard file are hosted externally.

- 📊 Power BI Dashboard (.pbix):  
  [Download Here](https://drive.google.com/file/d/1XoNaYl-T1ch3C_sdckcKOWoMn3EaEm4k/view?usp=sharing)

- 📁 Raw & Clean Dataset Files:  
  [Download Here](https://drive.google.com/drive/folders/1VtiQKW2sxBEVm4UvjFlTwfSYD9TqNveJ?usp=sharing)

---
