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

✔  REPLACE synthax errors
UPDATE index_1
SET coffee_name = REPLACE(coffee_name, 'expresso', 'espresso');
