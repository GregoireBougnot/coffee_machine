# Coffee Machine Sales Analysis  
A complete data analysis project including SQL data cleaning, Power BI dashboards, and business insights based on real coffee machine transactions.

---

## 📌 Project Overview  
This project analyzes transaction data from a coffee machine to uncover revenue trends, customer behavior, and product performance.  
The goal is to demonstrate end-to-end data analytics skills, from raw data cleaning to visual storytelling.

---

## 🛠️ Tools & Technologies  
- **SQL (MySQL)** – Data cleaning, transformations, feature creation  
- **Power BI** – Dashboard creation and visual analysis  
- **Excel / CSV** – Dataset preparation  
- **GitHub** – Documentation and version control

---

## 📂 Project Structure  
│
├─ Machine_a_cafe.pbix # Final Power BI dashboard
├─ index_1_sample.csv # Cleaned dataset (sample)
├─ README.md # Documentation
└─ images/ # Dashboard screenshots
├─ KPI.png
├─ Product Analysis.png

## 🪛 MYSQL Formulas
✔ Standardize coffee names
UPDATE index_1
SET coffee_name = LOWER(TRIM(coffee_name));

✔ Remove empty or invalid rows
DELETE FROM index_1
WHERE coffee_name = '' OR money = '';

✔ Convert money to decimal
ALTER TABLE index_1
MODIFY COLUMN money DECIMAL(10,2);

✔ Delete uneccessary spaces TRIM()
UPDATE index_1
SET coffee_name = TRIM(coffee_name);

✔  Replace synthax errors
UPDATE index_1
SET coffee_name = REPLACE(coffee_name, 'expresso', 'espresso');

## 📈 Predictive Analysis 

I created a simple Linear Regression model to estimate daily coffee machine sales for 2024. The model helps visualize general sales trends and gives a sense of how daily demand could evolve. This exercise allowed me to practice preparing data, applying a basic machine learning model, and visualizing predictions, while keeping the focus on real business insights like understanding popular products and overall demand patterns.



## 📊 Key Insights

The analysis highlights several opportunities from a business perspective. Card payments largely outperform cash, confirming that the machine benefits from offering seamless digital payment options. Revenue is mostly driven by a small number of popular products, with lattes and hot chocolate generating a significant share of total sales. This concentration suggests that focusing on these high-performing items through stock prioritization, pricing strategies, or promotional offers could further increase profitability. Additionally, the consistent volume of transactions indicates stable customer demand, making this machine a reliable revenue source with room for optimization based on top-selling products.
